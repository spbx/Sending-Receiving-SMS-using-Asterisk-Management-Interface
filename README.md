# Sending-Receiving-SMS-using-Asterisk-Management-Interface
-> Sending/Receiving SMS using Asterisk Management Interface
LibWAT Asterisk Management Interface

Sample scripts in PHP

 
Sending SMS
Action:WATSendSms
Span: <span number>
To-Number: <Destination/Called number>
Content: <message>


Full list of parameters
 
Receiving SMS

Event:WATIncomingSms
Span: <span number>
From-Number: <Origination/Calling number>
From-TON:<type of number>
From-NP:<numbering plan>
Timestamp: <timestamp in format yy/mm/dd hour:min:sec (zone:%d)>
Type: <PDU or TXT>
Message-Type-Indicator: SMS-DELIVER
Content: <message>


#See Full list of parameters#

Note:
ServiceCentre parameter is only available when SMS is received in PDU mode.
The zone in Timestamp is in relation to GMT, one unit is 15 mins, for example, zone=-12 means timezone is GMT-3.
When receiving multiple concated SMS's, the Sequence Number defines the message number and total number of message in group.

Network Status Change  

Event:WATNetStatus
Span: <span number>
Network-Status: <new status> 


Possible values for Network-Status:

    Not Registered
    Registered Home
    Not Registered, Searching
    Registration Denied
    Unknown
    Registered Roaming
    Invalid


