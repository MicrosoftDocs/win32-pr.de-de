---
description: WMI enthält eine Ereignisinfrastruktur, die Benachrichtigungen über Änderungen an WMI-Daten und -Diensten erzeugt. WMI-Ereignisklassen bieten Benachrichtigungen, wenn bestimmte Ereignisse auftreten.
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
ms.openlocfilehash: 5dac8aba93cc841211cbdc02bc5e75773ab444eaa2763c4b0367fbd36ada37b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992590"
---
# <a name="receiving-a-wmi-event"></a>Empfangen eines WMI-Ereignisses

WMI enthält eine Ereignisinfrastruktur, die Benachrichtigungen über Änderungen an WMI-Daten und -Diensten erzeugt. [*WMI-Ereignisklassen bieten*](gloss-e.md) Benachrichtigungen, wenn bestimmte Ereignisse auftreten.

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [Ereignisabfragen](#event-queries)
-   [Beispiel](#example)
-   [Ereignisverbraucher](#event-consumers)
-   [Bereitstellen von Ereignissen](#providing-events)
-   [Abonnementkontingente](#subscription-quotas)
-   [Zugehörige Themen](#related-topics)

## <a name="event-queries"></a>Ereignisabfragen

Sie können eine [semisynchrone](receiving-synchronous-and-semisynchronous-event-notifications.md) oder asynchrone Abfrage erstellen, um Änderungen an Ereignisprotokollen, der Prozesserstellung, dem Dienststatus, der Computerverfügbarkeit oder dem freien Speicherplatz auf dem Datenträger sowie an anderen Entitäten oder Ereignissen zu überwachen. [](receiving-asynchronous-event-notifications.md) Bei der Skripterstellung wird [**dieSWbemServices.ExecNotificationQuery-Methode**](swbemservices-execnotificationquery.md) verwendet, um Ereignisse zu abonnieren. In C++ wird [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) verwendet. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

Die Benachrichtigung über eine Änderung im WMI-Standarddatenmodell wird als [*systeminternes Ereignis bezeichnet.*](gloss-i.md) [**\_ \_ InstanceCreationEvent oder**](--instancecreationevent.md) [**\_ \_ NamespaceDeletionEvent sind**](--namespacedeletionevent.md) Beispiele für systeminterne Ereignisse. Die Benachrichtigung über eine Änderung, die ein Anbieter zum Definieren eines Anbieterereignis vor sich geht, wird als [*extrinsisches Ereignis bezeichnet.*](gloss-e.md) Beispielsweise definieren der [Systemregistrierungsanbieter,](/previous-versions/windows/desktop/regprov/system-registry-provider) [der Energieverwaltungsereignisanbieter](/windows/desktop/CIMWin32Prov/power-management-event-provider)und der [Win32-Anbieter](/windows/desktop/CIMWin32Prov/win32-provider) eigene Ereignisse. Weitere Informationen finden Sie unter [Bestimmen des Ereignistyps, der empfangen werden soll.](determining-the-type-of-event-to-receive.md)

## <a name="example"></a>Beispiel

Das folgende Skriptcodebeispiel ist eine Abfrage für das [**\_ \_ systeminterne InstanceCreationEvent**](--instancecreationevent.md) der [**Ereignisklasse Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent). Sie können dieses Programm im Hintergrund ausführen, und wenn ein Ereignis auftritt, wird eine Meldung angezeigt. Wenn Sie das Dialogfeld **Warten auf Ereignisse** schließen, wartet das Programm nicht mehr auf Ereignisse. Beachten Sie, dass **SeSecurityPrivilege** aktiviert sein muss.


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





Das folgende VBScript-Codebeispiel zeigt das vom Registrierungsanbieter definierte extrinsische Ereignis [ \_ \_ RegistryValueChangeEvent.](registering-for-system-registry-events.md) Das Skript erstellt einen temporären Consumer mithilfe des Aufrufs von [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md)und empfängt Nur-Ereignisse, wenn das Skript ausgeführt wird. Das folgende Skript wird unbegrenzt ausgeführt, bis der Computer neu gestartet, WMI beendet oder das Skript beendet wird. Um das Skript manuell zu beenden, verwenden Sie Task-Manager, um den Prozess zu beenden. Verwenden Sie zum programmgesteuerten Beenden die [**Terminate-Methode**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) in der Win32 \_ Process-Klasse. Weitere Informationen finden Sie unter [Festlegen der Sicherheit für einen asynchronen Aufruf](setting-security-on-an-asynchronous-call.md)von .


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

Sie können Ereignisse mithilfe der folgenden Benutzer überwachen oder nutzen, während ein Skript oder eine Anwendung ausgeführt wird:

-   Temporäre Ereignisverbraucher

    Ein [*temporärer Consumer*](gloss-t.md) ist eine WMI-Clientanwendung, die ein WMI-Ereignis empfängt. WMI enthält eine eindeutige Schnittstelle, die verwendet, um die Ereignisse anzugeben, die WMI an eine Clientanwendung senden soll. Ein temporärer Ereignisverbraucher gilt als temporär, da er nur funktioniert, wenn er speziell von einem Benutzer geladen wird. Weitere Informationen finden Sie unter [Empfangen von Ereignissen für die Dauer Ihrer Anwendung.](receiving-events-for-the-duration-of-your-application.md)

-   Permanente Ereignisverbraucher

    Ein [*permanenter Consumer*](gloss-p.md) ist ein COM-Objekt, das jederzeit ein WMI-Ereignis empfangen kann. Ein permanenter Ereignisverbraucher verwendet einen Satz persistenter Objekte und Filter, um ein WMI-Ereignis zu erfassen. Wie ein temporärer Ereignisverbraucher richten Sie eine Reihe von WMI-Objekten und -Filtern ein, die ein WMI-Ereignis erfassen. Wenn ein Ereignis auftritt, das einem Filter entspricht, lädt WMI den permanenten Ereignisverbraucher und benachrichtigt ihn über das Ereignis. Da ein permanenter Consumer im WMI-Repository implementiert ist und eine ausführbare Datei ist, die in WMI registriert ist, arbeitet der permanente Ereignisverbraucher nach derEntstellung und auch nach einem Neustart des Betriebssystems, solange WMI ausgeführt wird, und empfängt Ereignisse. Weitere Informationen finden Sie unter [Empfangen von Ereignissen zu allen Zeiten.](receiving-events-at-all-times.md)

Skripts oder Anwendungen, die Ereignisse empfangen, haben besondere Sicherheitsüberlegungen. Weitere Informationen finden Sie unter [Sichern von WMI-Ereignissen.](securing-wmi-events.md)

Eine Anwendung oder ein Skript kann einen integrierten WMI-Ereignisanbieter verwenden, der [Standardverbraucherklassen an stellt.](standard-consumer-classes.md) Jede Standard-Consumerklasse antwortet auf ein Ereignis mit einer anderen Aktion, indem eine E-Mail-Nachricht gesendet oder ein Skript ausgeführt wird. Sie müssen keinen Anbietercode schreiben, um eine Standard-Consumerklasse zum Erstellen eines permanenten Ereignisverbraucher zu verwenden. Weitere Informationen finden Sie unter [Überwachen und Reagieren auf Ereignisse mit Standardverbrauchern.](monitoring-and-responding-to-events-with-standard-consumers.md)

## <a name="providing-events"></a>Bereitstellen von Ereignissen

Ein Ereignisanbieter ist eine COM-Komponente, die ein Ereignis an WMI sendet. Sie können einen Ereignisanbieter erstellen, um ein Ereignis in einer C++- oder C#-Anwendung zu senden. Die meisten Ereignisanbieter verwalten ein Objekt für WMI, z. B. eine Anwendung oder ein Hardwareelement. Weitere Informationen finden Sie unter [Schreiben eines Ereignisanbieters.](writing-an-event-provider.md)

Ein Zeit- oder Wiederholungsereignis ist ein Ereignis, das zu einem vordefinierten Zeitpunkt auftritt.

WMI bietet die folgenden Möglichkeiten zum Erstellen von Zeit- oder Wiederholungsereignissen für Ihre Anwendungen:

-   Die standardmäßige Microsoft-Ereignisinfrastruktur.
-   Eine spezialisierte Timerklasse.

Weitere Informationen finden Sie unter [Empfangen eines Zeit- oder Wiederholungsereigniss.](receiving-a-timed-or-repeating-event.md) Berücksichtigen Sie beim Schreiben eines Ereignisanbieters die Sicherheitsinformationen, die unter [Sicheres Bereitstellen von Ereignissen identifiziert werden.](providing-events-securely.md)

Es wird empfohlen, permanente Ereignisabonnements in den \\ Stammabonnementnamespace \\ zu kompilieren. Weitere Informationen finden Sie unter [Implementing Cross-Namespace Permanent Event Subscriptions](implementing-cross-namespace-permanent-event-subscriptions.md).

## <a name="subscription-quotas"></a>Abonnementkontingente

Das Abfragen von Ereignissen kann die Leistung von Anbietern beeinträchtigen, die Abfragen für große Datensätze unterstützen. Darüber hinaus kann jeder Benutzer, der über Lesezugriff auf einen Namespace mit dynamischen Anbietern verfügt, einen Denial-of-Service-Angriff (DoS) ausführen. WMI verwaltet Kontingente für alle Kombinierten Benutzer und für jeden Ereignisverbraucher in der einzelnen Instanz von [**\_ \_ "Ungconfiguration"**](--arbitratorconfiguration.md) im \\ Stammnamespace. Diese Kontingente sind global und nicht für jeden Namespace. Sie können die Kontingente nicht ändern.

WMI erzwingt derzeit Kontingente mithilfe der Eigenschaften von [**\_ \_ "Configuration".**](--arbitratorconfiguration.md) Jedes Kontingent verfügt über eine pro Benutzer und eine Gesamtversion, die alle Benutzer kombiniert und nicht pro Namespace enthält. In der folgenden Tabelle sind die Kontingente aufgeführt, die für die **\_ \_ Eigenschaften von "Configuration" gelten.**



| Total/PerUser                                                                   | Kontingent                                                                       |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| TemporarySubscriptionsTotal<br/> TemporarySubscriptionsPerUser<br/> | 10.000<br/> 1\.000<br/>                                          |
| PermanentSubscriptionsTotal<br/> PermanentSubscriptionsPerUser<br/> | 10.000<br/> 1\.000<br/>                                          |
| PollingInstructionsTotal<br/> PollingInstructionsPerUser<br/>       | 10.000<br/> 1\.000<br/>                                          |
| PollingMemoryTotal<br/> PollingMemoryPerUser<br/>                   | 10.000.000 (0x989680) Bytes<br/> 5.000.000 (0x4CB40) Bytes<br/> |



 

Ein Administrator oder ein Benutzer mit **der BERECHTIGUNG FULL \_ WRITE** im -Namespace kann die Singletoninstanz von [**\_ \_ "Vorkonfigurierung" ändern.**](--arbitratorconfiguration.md) WMI verfolgt das Kontingent pro Benutzer nach.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von WMI](using-wmi.md)
</dt> </dl>

 

