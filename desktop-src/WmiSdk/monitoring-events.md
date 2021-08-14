---
description: Systemadministratoren können WMI verwenden, um Ereignisse in einem Netzwerk zu überwachen.
ms.assetid: 871d4add-a7b1-4ec9-a202-3821fdf09e9f
ms.tgt_platform: multiple
title: Überwachen von Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb90a0a6eef87f88543e8f2414bc38bdea4f7d89c577471d79d23393f331b053
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118317114"
---
# <a name="monitoring-events"></a>Überwachen von Ereignissen

Systemadministratoren können WMI verwenden, um Ereignisse in einem Netzwerk zu überwachen. Beispiel:

-   Ein Dienst wird unerwartet beendet.
-   Ein Server ist nicht mehr verfügbar.
-   Ein Laufwerk füllt eine Kapazität von 80 %.
-   Sicherheitsereignisse werden an ein NT-Ereignisprotokoll gemeldet.

WMI unterstützt die Ereigniserkennung und -übermittlung an Ereignisverbraucher, da einige WMI-Anbieter Ereignisanbieter sind. Weitere Informationen finden Sie unter [Empfangen eines WMI-Ereignisses.](receiving-a-wmi-event.md)

[*Ereignisverbraucher*](gloss-e.md) sind Anwendungen oder Skripts, die Benachrichtigungen über Ereignisse anfordern und dann Aufgaben ausführen, wenn bestimmte Ereignisse auftreten. Sie können Skripts oder Anwendungen für die Ereignisüberwachung erstellen, die vorübergehend überwachen, wann Ereignisse auftreten. WMI stellt auch eine Reihe von vorinstallierten permanenten Ereignisanbietern und die permanenten Consumerklassen zur Verfügung, mit denen Sie Ereignisse dauerhaft überwachen können. Weitere Informationen finden Sie unter [Überwachen und Reagieren auf Ereignisse mit Standardverbrauchern.](monitoring-and-responding-to-events-with-standard-consumers.md)

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [Verwenden temporärer Ereignisverbraucher](#using-temporary-event-consumers)
-   [Verwenden von permanenten Ereignisverbrauchern](#using-permanent-event-consumers)

## <a name="using-temporary-event-consumers"></a>Verwenden temporärer Ereignisverbraucher

Temporäre Ereignisverbraucher sind Skripts oder Anwendungen, die die Ereignisse zurückgeben, die mit einer Ereignisabfrage oder einem Ereignisfilter übereinstimmen. Temporäre Ereignisabfragen verwenden in der Regel [**entweder IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) in C++-Anwendungen oder [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) in Skripts und Visual Basic.

Eine Ereignisabfrage fordert Instanzen einer Ereignisklasse an, die einen bestimmten Ereignistyp angibt, z. B. [**Win32 \_ ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) oder [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).

Das folgende VBScript-Codebeispiel fordert eine Benachrichtigung an, wenn eine Instanz von [**Win32 \_ ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) erstellt wird. Eine Instanz dieser Klasse wird generiert, wenn ein Prozess gestartet oder beendet wird.

Um das Skript auszuführen, kopieren Sie es in eine Datei namens event.vbs und verwenden die folgende **Befehlszeile: cscript event.vbs**. Sie können die Ausgabe des Skripts sehen, indem Sie Notepad.exe oder einen anderen Prozess starten. Das Skript wird beendet, nachdem fünf Prozesse gestartet oder beendet wurden.

Dieses Skript ruft [**SWbemServices.ExecNotificationQuery auf.**](swbemservices-execnotificationquery.md)Dies ist die [*semisynchrone*](gloss-s.md) Version der -Methode. Im nächsten Skript finden Sie ein Beispiel für das Einrichten eines asynchronen temporären Ereignisabonnements durch AufrufenSWbemServices.Exe [**cNotificationQueryAsync.**](swbemservices-execnotificationqueryasync.md) Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md) Das Skript ruft [**SWbemEventSource.NextEvent auf,**](swbemeventsource-nextevent.md) um jedes Ereignis beim Eintreffen zu erhalten und zu verarbeiten. Speichern Sie das Skript in einer Datei mit der Erweiterung .vbs, und führen Sie das Skript über die Befehlszeile aus, indem Sie CScript: **cscript** file.vbs.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" _
    & strComputer & "\root\CIMV2") 
Set objEvents = objWMIService.ExecNotificationQuery _
    ("SELECT * FROM Win32_ProcessTrace")

Wscript.Echo "Waiting for events ..."
i = 0
Do Until i=5
    Set objReceivedEvent = objEvents.NextEvent
    'report an event
    Wscript.Echo "Win32_ProcessTrace event occurred" & VBNewLine _
        & "Process Name = " _
            & objReceivedEvent.ProcessName & VBNewLine _
        & "Process ID = " _
            & objReceivedEvent.Processid & VBNewLine _
        & "Session ID = " & objReceivedEvent.SessionID 
i = i+ 1
Loop
```



Temporäre Ereignisverbraucher müssen manuell gestartet werden und dürfen nicht über WMI-Neustarts oder Betriebssystemneustarts hinweg beibehalten werden. Ein temporärer Ereignisverbraucher kann Ereignisse nur verarbeiten, während er ausgeführt wird.

Im folgenden Verfahren wird beschrieben, wie ein temporärer Ereignisverbraucher erstellt wird.

**So erstellen Sie einen temporären Ereignisverbraucher**

1.  Entscheiden Sie, welche Programmiersprache sie verwenden soll.

    Die Programmiersprache bestimmt die zu verwendende API.

    -   Verwenden Sie für die Programmiersprache C++ die [COM-API für WMI.](com-api-for-wmi.md)
    -   Verwenden Visual Basic Skripterstellungs-API für WMI für [Skriptsprachen oder Skriptsprachen.](scripting-api-for-wmi.md)

2.  Beginnen Sie mit dem Codieren einer temporären Ereignisverbraucheranwendung auf die gleiche Weise wie beim Starten einer WMI-Anwendung.

    Die ersten Schritte der Programmierung hängen von der Programmiersprache ab. In der Regel melden Sie sich bei WMI an und richten die Sicherheitseinstellungen ein. Weitere Informationen finden Sie unter [Erstellen einer WMI-Anwendung oder Skript.](creating-a-wmi-application-or-script.md)

3.  Definieren Sie die Ereignisabfrage, die Sie verwenden möchten.

    Um einige Arten von Leistungsdaten zu erhalten, müssen Sie möglicherweise Klassen verwenden, die von Hochleistungsanbietern bereitgestellt werden. Weitere Informationen finden Sie unter Überwachen von [Leistungsdaten](monitoring-performance-data.md), [Bestimmen des](determining-the-type-of-event-to-receive.md)Typs des zu empfangenden Ereignisses und [Abfragen mit WQL.](querying-with-wql.md)

4.  Entscheiden Sie sich für einen asynchronen aufruf oder einen semisynchronen Aufruf, und wählen Sie die API-Methode aus.

    Mit asynchronen Aufrufen können Sie den Mehraufwand für das Abrufen von Daten vermeiden. Semisynchrone Aufrufe bieten jedoch eine ähnliche Leistung mit höherer Sicherheit. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

5.  Nehmen Sie den asynchronen oder semisynchronen Methodenaufruf vor, und schließen Sie eine Ereignisabfrage als *strQuery-Parameter* ein.

    Rufen Sie für C++-Anwendungen die folgenden Methoden auf:

    -   [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery)
    -   [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)

    Rufen Sie für Skripts die folgenden Methoden auf:

    -   [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)
    -   [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md)

6.  Schreiben Sie den Code, um das zurückgegebene Ereignisobjekt zu verarbeiten.

    Legen Sie für asynchrone Ereignisabfragen den Code in die verschiedenen Methoden oder Ereignisse der Objektsenke ein. Bei semisynchronen Ereignisabfragen wird jedes Objekt zurückgegeben, wenn WMI es erhält, sodass sich der Code in der Schleife befindet, die jedes Objekt behandelt.

Das folgende Skriptcodebeispiel ist eine asynchrone Version des [**Win32 \_ ProcessTrace-Skripts.**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) Da asynchrone Vorgänge sofort zurückgeben, hält ein Dialogfeld das Skript aktiv, während es auf Ereignisse wartet.

Anstatt [**SWbemEventSource.NextEvent auf**](swbemeventsource-nextevent.md) aufruft, um jedes Ereignis zu empfangen, verfügt das Skript über einen Ereignishandler für das [**SWbemSink OnObjectReady-Ereignis.**](swbemsink-onobjectready.md)


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\CIMV2") 
Set EventSink = WScript.CreateObject( _
    "WbemScripting.SWbemSink","SINK_")

objWMIservice.ExecNotificationQueryAsync EventSink, _
    "SELECT * FROM Win32_ProcessTrace WITHIN 10"
WScript.Echo "Waiting for events..."

i = 0
While (True)
    Wscript.Sleep(1000)
Wend

Sub SINK_OnObjectReady(objObject, objAsyncContext)
    Wscript.Echo "Win32_ProcessTrace event has occurred."
    i = i+1
    If i = 3 Then WScript.Quit 0 
End Sub

```



> [!Note]
>
> Ein asynchroner Rückruf, z. B. ein Rückruf, der von der Unterroutine verarbeitet wird, ermöglicht es einem nicht authentifizierten Benutzer, Daten für die `SINK_OnObjectReady` Senke zur Verfügung zu stellen. Verwenden Sie für eine bessere Sicherheit entweder die semisynchrone Kommunikation oder die synchrone Kommunikation. Weitere Informationen finden Sie in den folgenden Themen:
>
> -   [Semisynchroner Aufruf mit C++](making-a-semisynchronous-call-with-c--.md)
> -   [Semisynchroner Aufruf mit VBScript](making-a-semisynchronous-call-with-vbscript.md)
> -   [Ausführen eines asynchronen Aufrufs mit C++](making-an-asynchronous-call-with-c--.md)
> -   [Ausführen eines asynchronen Aufrufs mit VBScript](making-an-asynchronous-call-with-vbscript.md)
> -   [Festlegen der Sicherheit für einen asynchronen Aufruf](setting-security-on-an-asynchronous-call.md)
> -   [Sichern von Skriptclients](securing-scripting-clients.md)

 

## <a name="using-permanent-event-consumers"></a>Verwenden von permanenten Ereignisverbrauchern

Ein permanenter Ereignisverbraucher wird ausgeführt, bis seine Registrierung explizit abgebrochen wird, und startet dann, wenn WMI oder das System neu gestartet wird.

Ein permanenter Ereignisverbraucher ist eine Kombination aus WMI-Klassen, Filtern und COM-Objekten auf einem System.

In der folgenden Liste sind die Teile aufgeführt, die zum Erstellen eines permanenten Ereignisverbraucher erforderlich sind:

-   Ein COM-Objekt, das den Code enthält, der den permanenten Consumer implementiert.
-   Eine neue permanente Consumerklasse.
-   Eine Instanz der permanenten Consumerklasse.
-   Ein Filter, der die Abfrage für Ereignisse enthält.
-   Ein Link zwischen dem Consumer und dem Filter.

Weitere Informationen finden Sie unter [Empfangen von Ereignissen zu allen Zeiten.](--filtertoconsumerbinding.md)

WMI bietet mehrere permanente Verbraucher. Die Consumerklassen und das COM-Objekt, die den Code enthalten, sind vorinstalliert. Beispielsweise können Sie eine Instanz der [**ActiveScriptEventConsumer-Klasse**](activescripteventconsumer.md) erstellen und konfigurieren, um ein Skript auszuführen, wenn ein Ereignis auftritt. Weitere Informationen finden Sie unter [Überwachen und Reagieren auf Ereignisse mit Standardverbrauchern.](monitoring-and-responding-to-events-with-standard-consumers.md) Ein Beispiel für die Verwendung von **ActiveScriptEventConsumer finden** Sie unter [Ausführen eines Skripts basierend auf einem Ereignis.](running-a-script-based-on-an-event.md)

Im folgenden Verfahren wird beschrieben, wie ein permanenter Ereignisverbraucher erstellt wird.

**So erstellen Sie einen permanenten Ereignisverbraucher**

1.  [Registrieren Sie den Ereignisanbieter](registering-a-provider.md) mit dem Namespace, den Sie verwenden.

    Einige Ereignisanbieter können nur einen bestimmten Namespace verwenden. [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) ist beispielsweise ein systeminternes Ereignis, das vom [Win32-Anbieter](/windows/desktop/CIMWin32Prov/win32-provider) unterstützt wird und standardmäßig beim \\ \\ Cimv2-Stammnamespace registriert wird.

    > [!Note]  
    > Sie können die **EventNamespace-Eigenschaft** des in der Registrierung verwendeten [**\_ \_ EventFilter**](--eventfilter.md) verwenden, um ein namespaceübergreifendes Abonnement zu erstellen. Weitere Informationen finden Sie unter [Implementing Cross-Namespace Permanent Event Subscriptions](implementing-cross-namespace-permanent-event-subscriptions.md).

     

2.  [Registrieren Sie den Ereignisverbraucheranbieter](registering-an-event-consumer-provider.md) mit dem Namespace, in dem sich Ereignisklassen befinden.

    WMI verwendet einen Ereignisverbraucheranbieter, um einen dauerhaften Ereignis consumer zu finden. Der permanente Ereignisverbraucher ist die Anwendung, die WMI startet, wenn ein Ereignis empfangen wird. Zum Registrieren des Ereignisconsumers erstellen Anbieter Instanzen von [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md).

3.  Erstellen Sie eine Instanz der -Klasse, die den dauerhaften Ereignisverbraucher darstellt, den Sie verwenden möchten.

    Ereignisconsumerklassen werden von der [**\_ \_ Klasse EventConsumer**](--eventconsumer.md)abgeleitet. Legen Sie die Eigenschaften fest, die für die Ereignisverbraucherinstanz erforderlich sind.

4.  Registrieren Sie den Consumer mithilfe des Hilfsprogramms **regsvr32** bei COM.
5.  Erstellen Sie eine Instanz der Ereignisfilterklasse [**\_ \_ EventFilter**](--eventfilter.md).

    Legen Sie die erforderlichen Felder für die Ereignisfilterinstanz fest. Die erforderlichen Felder für [**\_ \_ EventFilter**](--eventfilter.md) sind **Name,** **QueryLanguage** und **Query.** Die **Name-Eigenschaft** kann ein beliebiger eindeutiger Name für eine Instanz dieser Klasse sein. Die **QueryLanguage-Eigenschaft** ist immer auf "WQL" festgelegt. Die **Query-Eigenschaft** ist eine Zeichenfolge, die eine Ereignisabfrage enthält. Ein Ereignis wird generiert, wenn die Abfrage eines permanenten Ereignisverbrauchers fehlschlägt. Die Quelle des Ereignisses ist WinMgmt, die Ereignis-ID ist 10, und der Ereignistyp ist Error.

6.  Erstellen Sie eine Instanz der [**\_ \_ FilterToConsumerBinding-Klasse,**](--filtertoconsumerbinding.md) um einem Ereignisfilter einen logischen Ereignisconsumer zuzuordnen.

    WMI verwendet eine Zuordnung, um den Ereignisverbraucher zu suchen, der dem Ereignis zugeordnet ist, das den im Ereignisfilter angegebenen Kriterien entspricht. WMI verwendet den Ereignisverbraucheranbieter, um die permanente Ereignisverbraucheranwendung zu suchen, die gestartet werden soll.

 

 
