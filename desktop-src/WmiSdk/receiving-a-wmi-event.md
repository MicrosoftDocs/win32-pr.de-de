---
description: WMI enthält eine Ereignis Infrastruktur, die Benachrichtigungen zu Änderungen in WMI-Daten und-Diensten erzeugt. WMI-Ereignis Klassen stellen Benachrichtigungen bereit, wenn bestimmte Ereignisse auftreten.
ms.assetid: 347808a7-0f7b-4687-93f4-bea55c96795a
ms.tgt_platform: multiple
title: Empfangen eines WMI-Ereignisses
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 255f54f78bb64659d1cd07eddb72eae55b0263c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131016"
---
# <a name="receiving-a-wmi-event"></a>Empfangen eines WMI-Ereignisses

WMI enthält eine Ereignis Infrastruktur, die Benachrichtigungen zu Änderungen in WMI-Daten und-Diensten erzeugt. WMI- [*Ereignis Klassen*](gloss-e.md) stellen Benachrichtigungen bereit, wenn bestimmte Ereignisse auftreten.

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [Ereignis Abfragen](#event-queries)
-   [Beispiel](#example)
-   [Ereignisconsumer](#event-consumers)
-   [Bereitstellen von Ereignissen](#providing-events)
-   [Abonnement Kontingente](#subscription-quotas)
-   [Zugehörige Themen](#related-topics)

## <a name="event-queries"></a>Ereignis Abfragen

Sie können eine [semisynchrone](receiving-synchronous-and-semisynchronous-event-notifications.md) oder [**asynchrone**](receiving-asynchronous-event-notifications.md) Abfrage erstellen, um Änderungen an Ereignisprotokollen, Prozesserstellung, Dienststatus, Computer Verfügbarkeit oder freiem Speicherplatz auf dem Datenträger sowie andere Entitäten oder Ereignisse zu überwachen. Bei der Skripterstellung wird die [**SWbemServices.Execnotificationquery**](swbemservices-execnotificationquery.md) -Methode verwendet, um Ereignisse zu abonnieren. In C++ wird [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) verwendet. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

Eine Benachrichtigung über eine Änderung im standardmäßigen WMI-Datenmodell wird als System internes [*Ereignis*](gloss-i.md)bezeichnet. [**\_ \_ Instancecreationevent**](--instancecreationevent.md) oder [**\_ \_ namespacedeletionevent**](--namespacedeletionevent.md) sind Beispiele für systeminterne Ereignisse. Eine Benachrichtigung über eine Änderung, die ein Anbieter zum Definieren eines Anbieter Ereignisses vornimmt, wird als [*System externe-Ereignis*](gloss-e.md)bezeichnet. Beispielsweise definieren der [System Registrierungs Anbieter](/previous-versions/windows/desktop/regprov/system-registry-provider), der [Energie Verwaltungs Ereignis Anbieter](/windows/desktop/CIMWin32Prov/power-management-event-provider)und der [Win32-Anbieter](/windows/desktop/CIMWin32Prov/win32-provider) ihre eigenen Ereignisse. Weitere Informationen finden Sie unter [bestimmen des empfangenden Ereignis Typs](determining-the-type-of-event-to-receive.md).

## <a name="example"></a>Beispiel

Das folgende Skriptcode Beispiel ist eine Abfrage für das intrinsische [**\_ \_ instancecreationevent**](--instancecreationevent.md) der Ereignisklasse [**Win32 \_ ntlogevent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent). Sie können dieses Programm im Hintergrund ausführen, und wenn ein Ereignis vorliegt, wird eine Meldung angezeigt. Wenn Sie das Dialogfeld **warten auf Ereignisse** schließen, hält das Programm nicht mehr auf Ereignisse. Beachten Sie, dass **SeSecurityPrivilege** aktiviert werden muss.


```VB
Sub SINK_OnObjectReady(objObject, objAsyncContext)
    WScript.Echo (objObject.TargetInstance.Message)
End Sub

Set objWMIServices = GetObject( _
    "WinMgmts:{impersonationLevel=impersonate, (security)}") 

' Create the event sink object that receives the events
Set sink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
 
' Set up the event selection. SINK_OnObjectReady is called when
' a Win32_NTLogEvent event occurs
objWMIServices.ExecNotificationQueryAsync sink,"SELECT * FROM __InstanceCreationEvent " & "WHERE TargetInstance ISA 'Win32_NTLogEvent' "

WScript.Echo "Waiting for events"
```


```PowerShell

# Define event Query
$query = "SELECT * FROM __InstanceCreationEvent 
          WHERE TargetInstance ISA 'Win32_NTLogEvent' "

<# Register for event - also specify an action that
displays the log event when the event fires.#>

Register-WmiEvent -Source Demo1 -Query $query -Action {
                Write-Host "Log Event occured"
                $global:myevent = $event
                Write-Host "EVENT MESSAGE"
                Write-Host $event.SourceEventArgs.NewEvent.TargetInstance.Message}
<# So wait #>
"Waiting for events"
```





Das folgende VBScript-Codebeispiel zeigt das System externe-Ereignis [ \_ \_ RegistryValueChangeEvent](registering-for-system-registry-events.md) , das der Registrierungs Anbieter definiert. Das Skript erstellt einen temporären Consumer mithilfe des Aufrufes [**SWbemServices.Execnotificationqueryasync**](swbemservices-execnotificationqueryasync.md)und empfängt nur Ereignisse, wenn das Skript ausgeführt wird. Das folgende Skript wird unbegrenzt ausgeführt, bis der Computer neu gestartet, WMI beendet oder das Skript beendet wird. Um das Skript manuell anzuhalten, verwenden Sie den Task-Manager, um den Prozess zu unterbinden. Verwenden Sie zum programmgesteuerten beenden die Methode " [**Beenden**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) " in der Win32- \_ Prozess Klasse. Weitere Informationen finden Sie unter [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md)-Befehl.


```VB
strComputer = "."

Set objWMIServices=GetObject( _
    "winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\default")

set objSink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")


objWMIServices.ExecNotificationQueryAsync objSink, _
    "Select * from RegistryValueChangeEvent Where Hive = 'HKEY_LOCAL_MACHINE' and KeyPath = 'SYSTEM\\ControlSet001\\Control' and ValueName = 'CurrentUser'"

WScript.Echo "Waiting for events..."

While (True) 
     WScript.Sleep (1000)
Wend

 
WScript.Echo "Listening for Registry Change Events..." & vbCrLf 

While(True) 
    WScript.Sleep 1000 
Wend 

Sub SINK_OnObjectReady(wmiObject, wmiAsyncContext) 
    WScript.Echo "Received Registry Value Change Event" & vbCrLf & wmiObject.GetObjectText_() 
End Sub
```



## <a name="event-consumers"></a>Ereignisconsumer

Beim Ausführen eines Skripts oder einer Anwendung können Ereignisse mithilfe der folgenden Verbraucher überwacht oder genutzt werden:

-   Temporäre Ereignisconsumer

    Ein [*temporärer Consumer*](gloss-t.md) ist eine WMI-Client Anwendung, die ein WMI-Ereignis empfängt. WMI enthält eine eindeutige Schnittstelle, die verwendet, um die Ereignisse anzugeben, die von WMI an eine Client Anwendung gesendet werden sollen. Ein temporärer Ereignisconsumer gilt als temporär, da er nur funktioniert, wenn er von einem Benutzer explizit geladen wird. Weitere Informationen finden Sie unter [empfangen von Ereignissen für die Dauer Ihrer Anwendung](receiving-events-for-the-duration-of-your-application.md).

-   Permanente Ereignisconsumer

    Ein [*dauerhafter Consumer*](gloss-p.md) ist ein COM-Objekt, das jederzeit ein WMI-Ereignis empfangen kann. Ein dauerhafter Ereignisconsumer verwendet einen Satz von persistenten Objekten und Filtern, um ein WMI-Ereignis zu erfassen. Wie bei einem temporären Ereignisconsumer richten Sie eine Reihe von WMI-Objekten und filtern ein, die ein WMI-Ereignis erfassen. Wenn ein Ereignis auftritt, das einem Filter entspricht, lädt WMI den permanenten Ereignisconsumer und benachrichtigt ihn über das Ereignis. Da ein dauerhafter Consumer im WMI-Repository implementiert ist und eine ausführbare Datei ist, die in WMI registriert ist, wird der permanente Ereignisconsumer nach der Erstellung und auch nach einem Neustart des Betriebssystems, solange WMI ausgeführt wird, nach einem Neustart des Betriebssystems ausgeführt. Weitere Informationen finden Sie [unter empfangen von Ereignissen zu allen Zeit](receiving-events-at-all-times.md)Punkten.

Skripts oder Anwendungen, die Ereignisse empfangen, haben besondere Sicherheitsüberlegungen. Weitere Informationen finden Sie unter [Sichern von WMI-Ereignissen](securing-wmi-events.md).

Eine Anwendung oder ein Skript kann einen integrierten WMI-Ereignis Anbieter verwenden, der [Standard Consumerklassen](standard-consumer-classes.md)bereitstellt. Jede Standard Consumerklasse antwortet auf ein Ereignis mit einer anderen Aktion, indem eine e-Mail-Nachricht gesendet oder ein Skript ausgeführt wird. Sie müssen keinen Anbieter Code schreiben, um eine Standard Consumerklasse zum Erstellen eines permanenten Ereignisconsumer zu verwenden. Weitere Informationen finden Sie unter über [wachen und reagieren auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.

## <a name="providing-events"></a>Bereitstellen von Ereignissen

Ein Ereignis Anbieter ist eine COM-Komponente, die ein Ereignis an WMI sendet. Sie können einen Ereignis Anbieter erstellen, um ein Ereignis in einer C++-oder c#-Anwendung zu senden. Die meisten Ereignis Anbieter verwalten ein Objekt für WMI, z. b. eine Anwendung oder ein Hardware Element. Weitere Informationen finden Sie unter [Schreiben eines Ereignis Anbieters](writing-an-event-provider.md).

Ein zeitgesteuertes oder sich wiederholendes Ereignis ist ein Ereignis, das zu einem bestimmten Zeitpunkt auftritt.

WMI bietet die folgenden Möglichkeiten, um zeitgesteuerte oder sich wiederholende Ereignisse für Ihre Anwendungen zu erstellen:

-   Die standardmäßige Microsoft-Ereignis Infrastruktur.
-   Eine spezialisierte Timer-Klasse.

Weitere Informationen finden Sie unter [empfangen eines zeitgesteuerten oder wiederholten Ereignisses](receiving-a-timed-or-repeating-event.md). Wenn Sie einen Ereignis Anbieter schreiben, sollten Sie die Sicherheitsinformationen beachten, die bei der [sicheren Bereitstellung von Ereignissen](providing-events-securely.md)identifiziert werden

Es wird empfohlen, dass permanente Ereignis Abonnements in den Namespace des Stamm Abonnements kompiliert werden \\ \\ . Weitere Informationen finden Sie unter [Implementieren von Abonnements für permanente Namespace-Ereignisse](implementing-cross-namespace-permanent-event-subscriptions.md).

## <a name="subscription-quotas"></a>Abonnement Kontingente

Durch das Abrufen von Ereignissen kann die Leistung für Anbieter beeinträchtigt werden, die Abfragen für große Datasets unterstützen. Außerdem kann jeder Benutzer, der über Lesezugriff auf einen Namespace mit dynamischen Anbietern verfügt, einen Denial-of-Service-Angriff (DOS) durchführen. WMI verwaltet Kontingente für alle Benutzer zusammen und für jeden Ereignisconsumer in der einzelnen Instanz von " [**\_ \_ arbiatorconfiguration**](--arbitratorconfiguration.md) ", die sich im Stamm \\ Namespace befindet. Diese Kontingente sind global und nicht für jeden Namespace. Die Kontingente können nicht geändert werden.

WMI erzwingt derzeit Kontingente mithilfe der Eigenschaften von " [**\_ \_ arbiatorconfiguration**](--arbitratorconfiguration.md)". Jedes Kontingent verfügt über einen pro-Benutzer und eine Gesamt Version, die alle Benutzer kombiniert und nicht pro Namespace umfasst. In der folgenden Tabelle sind die Kontingente aufgelistet, die für die Eigenschaften von " **\_ \_ arbiatorconfiguration** " gelten.



| Gesamt/Benutzer                                                                   | Kontingent                                                                       |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| Temporaryabonnemenzstotal<br/> Temporaryabonnemenamtionsperuser<br/> | 10.000<br/> 1\.000<br/>                                          |
| Permanent abonniert<br/> Permanentabonneptionsperuser<br/> | 10.000<br/> 1\.000<br/>                                          |
| Pollinginstructionstotal<br/> Pollinginstructionsperuser<br/>       | 10.000<br/> 1\.000<br/>                                          |
| Pollingmemorytotal<br/> Pollingmemoryperuser<br/>                   | 10 Millionen (0x989680) Bytes<br/> 5 Millionen (0x4cb40) Bytes<br/> |



 

Ein Administrator oder Benutzer mit **Vollständiger \_ Schreib** Berechtigung im-Namespace kann die Singleton-Instanz von " [**\_ \_ arbiatorconfiguration**](--arbitratorconfiguration.md)" ändern. WMI verfolgt das Kontingent pro Benutzer.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von WMI](using-wmi.md)
</dt> </dl>

 

