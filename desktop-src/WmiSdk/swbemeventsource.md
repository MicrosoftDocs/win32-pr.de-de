---
description: Das Objekt "slibemeventsource" ruft Ereignisse aus einer Ereignis Abfrage in Verbindung mit SWbemServices.Execnotificationquery ab.
ms.assetid: 7efd5e6a-4311-4d20-8b05-e9208eec098a
ms.tgt_platform: multiple
title: Errbemeventsource-Objekt (wbemdisp. h)
ms.topic: reference
ms.date: 09/25/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemEventSource
- ISWbemEventSource
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8da55a7b6722c263fe9a3fb0af7a8db07d672e12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348886"
---
# <a name="swbemeventsource-object"></a>"Errbemeventsource"-Objekt

Das Objekt " **slibemeventsource** " ruft Ereignisse aus einer Ereignis Abfrage in Verbindung mit [**SWbemServices.Execnotificationquery**](swbemservices-execnotificationquery.md)ab. Sie erhalten ein " **slibemeventsource** "-Objekt, wenn Sie **SWbemServices.Execnotificationquery** aufrufen, um eine Ereignis Abfrage durchführen. Sie können dann die [**NextEvent**](swbemeventsource-nextevent.md) -Methode verwenden, um Ereignisse abzurufen, sobald sie eintreffen. Dieses Objekt kann nicht durch den VBScript-Befehl "up- [Object](/previous-versions//xzysf6hc(v=vs.85)) " erstellt werden.

## <a name="members"></a>Member

Das Objekt " **errbemeventsource** " verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das Objekt " **errbemeventsource** " verfügt über diese Methoden.



| Methode                                          | BESCHREIBUNG                                                                                                                                  |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**NextEvent**](swbemeventsource-nextevent.md) | Wird zum Abrufen eines Ereignisses in Verbindung mit [**SWbemServices.Execnotificationquery**](swbemservices-execnotificationquery.md)verwendet.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das Objekt " **errbemeventsource** " verfügt über diese Eigenschaften.



| Eigenschaft                                                    | Zugriffstyp          | BESCHREIBUNG                                              |
|:------------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [**Sicherheit\_**](swbemeventsource-security-.md)<br/> | Schreibgeschützt<br/> | Wird verwendet, um die Sicherheitseinstellungen zu lesen oder zu ändern.<br/> |



 

## <a name="examples"></a>Beispiele

Dieses Skript verwendet die Methoden der Klasse " **errbemeventsource** " und die Klasse " [**Swap Services**](swbemservices.md) " in Verbindung mit einer WQL-Abfrage für Anwendungs Ereignisse. Weitere Informationen zur WMI-Ereignis Benachrichtigung und zu Abfragen finden Sie unter über [Wachen von Ereignissen](monitoring-events.md), [Ausführen eines Skripts auf der Grundlage eines Ereignisses](running-a-script-based-on-an-event.md)und [empfangen von asynchronen Ereignis Benachrichtigungen](receiving-asynchronous-event-notifications.md).


```VB
' Connect to WMI, obtaining an SWbemServices object
set svc = _
CreateObject("Wbemscripting.SWbemLocator")._
   ConnectServer(,"root\cimv2")

' Obtain an SWbemEventSource object from the 
' SWbemServices.ExecNotificationQuery method to specify the 
' event source as "Application" events in a Win32_NTLogEvent
set evtsrc = svc.ExecNotificationQuery("SELECT * " _
   & "FROM __InstanceCreationEvent " _
   & "WHERE TargetInstance ISA 'Win32_NTLogEvent'" _
   & "AND TargetInstance.Logfile ='Application'")

' Wait for an event by executing the NextEvent method on the 
' SWbemEventSource object.
while (num < 5)
    set inst = evtsrc.NextEvent(-1)
    Wscript.echo inst.TargetInstance.Logfile
    num = num + 1
wend
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID-austauschen von " \_ errbemeventsource"<br/>                                                      |
| IID<br/>                      | IID \_ iswbemeventsource<br/>                                                       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[API-Skript Objekte](scripting-api-objects.md)
</dt> </dl>

 

