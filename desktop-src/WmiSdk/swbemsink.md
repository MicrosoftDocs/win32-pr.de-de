---
description: Das slibemsink-Objekt wird von Client Anwendungen implementiert, um die Ergebnisse von asynchronen Vorgängen und Ereignis Benachrichtigungen zu empfangen.
ms.assetid: a90777ef-fa26-4bfb-b196-c083a0c92a29
ms.tgt_platform: multiple
title: Taubemsink-Objekt (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink
- ISWbemSinkEvents
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b8007b7387a09e31f49dbc833f657bc959ee11e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353204"
---
# <a name="swbemsink-object"></a>Swap-Objekt

Das **slibemsink** -Objekt wird von Client Anwendungen implementiert, um die Ergebnisse von asynchronen Vorgängen und Ereignis Benachrichtigungen zu empfangen. Um einen asynchronen-aufzurufen, müssen Sie eine Instanz eines " **taubemsink** "-Objekts erstellen und als *objwbemsink* -Parameter übergeben. Die Ereignisse in der Implementierung von " **taubemsink** " werden ausgelöst, wenn Status oder Ergebnisse zurückgegeben werden oder wenn der-Vorgang beendet ist. Der VBScript-Befehl zum Erstellen von **Objekten** erstellt dieses Objekt.

## <a name="members"></a>Member

Das **taubemsink** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Das **taubemsink** -Objekt verfügt über diese Methoden.



| Methode                             | BESCHREIBUNG                                                                        |
|:-----------------------------------|:-----------------------------------------------------------------------------------|
| [**Abbrechen**](swbemsink-cancel.md) | Bricht alle asynchronen Vorgänge ab, die dieser Senke zugeordnet sind.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Ein asynchroner Rückruf ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke. Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen. Um die Risiken auszuschließen, verwenden Sie entweder die semisynchrone Kommunikation oder die synchrone Kommunikation. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

### <a name="events"></a>Ereignisse

Sie können Unterroutinen implementieren, die aufgerufen werden, wenn Ereignisse ausgelöst werden. Wenn Sie z. b. jedes Objekt verarbeiten möchten, das von einem asynchronen Abfrage Vorgang zurückgegeben wird, z. b. [**SWbemServices.Execqueryasync**](swbemservices-execqueryasync.md), erstellen Sie eine Unterroutine mithilfe der Senke, die im asynchronen-Befehl angegeben wird, wie im folgenden Beispiel gezeigt.


```VB
Sub SinkName_OnObjectReady(objObject, objAsyncContext)
```



Verwenden Sie die folgende Tabelle als Referenz, um Ereignisse und triggerbeschreibungen zu identifizieren.



| Ereignis                                            | BESCHREIBUNG                                                             |
|--------------------------------------------------|-------------------------------------------------------------------------|
| [**OnCompleted**](swbemsink-oncompleted.md)     | Wird ausgelöst, wenn ein asynchroner Vorgang beendet ist.                   |
| [**Onobjectput**](swbemsink-onobjectput.md)     | Wird ausgelöst, wenn ein asynchroner Put-Vorgang beendet ist.               |
| [**Onobjectready**](swbemsink-onobjectready.md) | Wird ausgelöst, wenn ein von einem asynchronen-Befehl bereitgestelltes Objekt verfügbar ist. |
| [**OnProgress**](swbemsink-onprogress.md)       | Wird ausgelöst, um den Status eines asynchronen Vorgangs bereitzustellen.            |



 

**Asynchrones Abrufen von Ereignisprotokoll Statistiken**

WMI unterstützt sowohl asynchrone als auch semisynchrone Skripts. Beim Abrufen von Ereignissen aus den Ereignisprotokollen werden diese Daten von asynchronen Skripts häufig viel schneller abgerufen.

In einem asynchronen Skript wird eine Abfrage ausgegeben, und die Steuerung wird sofort an das Skript zurückgegeben. Die Abfrage wird weiterhin in einem separaten Thread verarbeitet, während das Skript sofort die zurückgegebenen Informationen verarbeitet. Asynchrone Skripts sind ereignisgesteuert: jedes Mal, wenn ein Ereignisdaten Satz abgerufen wird, wird das onobjectready-Ereignis ausgelöst. Wenn die Abfrage abgeschlossen ist, wird das onabgeschlossene-Ereignis ausgelöst, und das Skript kann basierend auf der Tatsache fortgesetzt werden, dass alle verfügbaren Datensätze zurückgegeben wurden.

In einem semisynchronen Skript wird im Gegensatz dazu eine Abfrage ausgegeben, und das Skript fügt dann eine große Menge an abgerufenen Informationen in die Warteschlange ein, bevor es darauf reagiert. Bei vielen-Objekten ist die semisynchrone Verarbeitung angemessen. Wenn Sie z. b. ein Festplattenlaufwerk nach seinen Eigenschaften Abfragen, kann es zwischen dem Zeitpunkt, zu dem die Abfrage ausgegeben wird, und dem Zeitpunkt, zu dem die Informationen zurückgegeben und verarbeitet werden, nur eine Sekunde geteilt werden. Der Grund dafür ist, dass die Menge der zurückgegebenen Informationen relativ klein ist.

Beim Abfragen eines Ereignis Protokolls kann jedoch das Intervall zwischen dem Zeitpunkt, zu dem die Abfrage ausgegeben wird, und dem Zeitpunkt, zu dem ein semisynchrones Skript die Rückgabe der Informationen abschließen kann, Stunden dauern. Darüber hinaus ist für das Skript möglicherweise nicht genügend Arbeitsspeicher verfügbar, und ein Fehler tritt auf, bevor er abgeschlossen wird.

Bei Ereignisprotokollen mit einer großen Anzahl von Datensätzen kann der Unterschied in der Verarbeitungszeit beträchtlich sein. Auf einem Windows 2000-basierten Testcomputer mit 2.000 Datensätzen im Ereignisprotokoll hat eine semisynchrone Abfrage, bei der alle Ereignisse abgerufen und in einem Befehlsfenster angezeigt wurden, 10 Minuten 45 Sekunden gedauert. Eine asynchrone Abfrage, die denselben Vorgang ausgeführt hat, hat eine Minute 54 Sekunden gedauert.

## <a name="examples"></a>Beispiele

Das folgende VBScript fragt die Ereignisprotokolle für alle Datensätze asynchron ab.


```VB
Const POPUP_DURATION = 10
Const OK_BUTTON = 0
Set objWSHShell = Wscript.CreateObject("Wscript.Shell")
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objSink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
objWMIService.InstancesOfAsync objSink, "Win32_NTLogEvent"
errReturn = objWshShell.Popup("Retrieving events", POPUP_DURATION, _
"Event Retrieval", OK_BUTTON)
Sub SINK_OnCompleted(iHResult, objErrorObject, objAsyncContext)
 WScript.Echo "Asynchronous operation is done."
End Sub
Sub SINK_OnObjectReady(objEvent, objAsyncContext)
 Wscript.Echo "Category: " & objEvent.Category
 Wscript.Echo "Computer Name: " & objEvent.ComputerName
 Wscript.Echo "Event Code: " & objEvent.EventCode
 Wscript.Echo "Message: " & objEvent.Message
 Wscript.Echo "Record Number: " & objEvent.RecordNumber
 Wscript.Echo "Source Name: " & objEvent.SourceName
 Wscript.Echo "Time Written: " & objEvent.TimeWritten
 Wscript.Echo "Event Type: " & objEvent.Type
 Wscript.Echo "User: " & objEvent.User
End Sub
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Wbemdisp. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Swap-senbemsink<br/> CLSID- \_ Austausch Vorgänge<br/>                           |
| IID<br/>                      | IID \_ iswbemsink<br/> IID \_ iswbemsinkevents<br/>                             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[API-Skript Objekte](scripting-api-objects.md)
</dt> </dl>

 

 




