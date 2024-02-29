# Day-1 of building Own Home SOC Lab
In the day one, we will see the overview of how the data will flow, 
which types of actions will take place from which tool to which tool,
and what will be the responsibility of each tool.

For the designing the flow of data and understanding the workflow I am using draw.io tool (you can use can tool that fits you)

Let's first understand what we will include in our design and how will be our workflow:<br/>
1) We have a Client PC on which Windows is running(and on it Wazuh agent is installed), a PC on which SOC analyst is working, and we have all our three tools on cloud(for this instance say internet).<br/>
2) Events will transfer from Wazuh agent on client PC to internet or cloud through router and then to Wazuh manager.<br/>
3) Wazuh manager will then create alerts and transfer it to Shuffle.<br/>
4) Shuffle will enrich IOCs and pass this alerts to TheHive for creating case.<br/>
5) The Shuffle will then send email regarding alert to SOC analyst PC.<br/>
6) The SOC analyst after reading the email will repond accordingly and any reponsive action than need to be taken will pass to wazuh manager via Shuffle.<br/>
7) The Wazuh manager will then ask the Wazuh agen on clients PC to take particular reponsive action.<br/>

Here's the overflow of data or the  abstract design of how our SOC home lab will work:

<img width="390" alt="SOC_Automation_Lab_dataflow" src="https://github.com/Kathan0920/SOC_Automation_Lab/assets/118013800/81eefc11-da41-42ce-bb5d-8cb8d9d88d6f">
