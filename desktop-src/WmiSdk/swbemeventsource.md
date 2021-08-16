---
description: Das SWbemEventSource-Objekt ruft Ereignisse aus einer Ereignisabfrage in Verbindung mit SWbemServices.ExecNotificationQuery ab.
ms.assetid: 7efd5e6a-4311-4d20-8b05-e9208eec098a
ms.tgt_platform: multiple
title: SWbemEventSource-Objekt (Wbemdisp.h)
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
ms.openlocfilehash: e38dab258ebccacb24cf92b7445752102b297ab1207b99e40355c30fde99113d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992140"
---
# <a name="swbemeventsource-object"></a>SWbemEventSource-Objekt

Das **SWbemEventSource-Objekt** ruft Ereignisse aus einer Ereignisabfrage in Verbindung mit [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)ab. Sie erhalten ein **SWbemEventSource-Objekt,** wenn Sie **SWbemServices.ExecNotificationQuery** aufrufen, um eine Ereignisabfrage zu erstellen. Sie können dann die [**NextEvent-Methode**](swbemeventsource-nextevent.md) verwenden, um Ereignisse abzurufen, sobald sie eintreffen. Dieses Objekt kann nicht durch den [VBScript-CreateObject-Aufruf](/previous-versions//xzysf6hc(v=vs.85)) erstellt werden.

## <a name="members"></a>Member

Das **SWbemEventSource-Objekt** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **SWbemEventSource-Objekt** verfügt über diese Methoden.



| Methode                                          | BESCHREIBUNG                                                                                                                                  |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**NextEvent**](swbemeventsource-nextevent.md) | Wird verwendet, um ein Ereignis in Verbindung mit [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)abzurufen.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **SWbemEventSource-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                    | Zugriffstyp          | BESCHREIBUNG                                              |
|:------------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [**Sicherheit\_**](swbemeventsource-security-.md)<br/> | Schreibgeschützt<br/> | Wird zum Lesen oder Ändern der Sicherheitseinstellungen verwendet.<br/> |



 

## <a name="examples"></a>Beispiele

Dieses Skript verwendet die Methoden der **SWbemEventSource-Klasse** und der [**SWbemServices-Klasse**](swbemservices.md) in Verbindung mit einer WQL-Abfrage für Anwendungsereignisse. Weitere Informationen zu WMI-Ereignisbenachrichtigungen und -Abfragen finden Sie unter [Überwachen von Ereignissen,](monitoring-events.md) [Ausführen eines Skripts basierend auf einem Ereignis](running-a-script-based-on-an-event.md)und Empfangen von [asynchronen Ereignisbenachrichtigungen.](receiving-asynchronous-event-notifications.md)


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
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemEventSource<br/>                                                      |
| IID<br/>                      | IID \_ ISWbemEventSource<br/>                                                       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Skripterstellung für API-Objekte](scripting-api-objects.md)
</dt> </dl>

 

