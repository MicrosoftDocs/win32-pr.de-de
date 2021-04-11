---
description: System Administratoren können WMI zum Überwachen von Ereignissen in einem Netzwerk verwenden.
ms.assetid: 871d4add-a7b1-4ec9-a202-3821fdf09e9f
ms.tgt_platform: multiple
title: Überwachen von Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea5d9fc6f9a12f4aa1fb7bc0ff6f66fc4dd4a7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130393"
---
# <a name="monitoring-events"></a>Überwachen von Ereignissen

System Administratoren können WMI zum Überwachen von Ereignissen in einem Netzwerk verwenden. Beispiel:

-   Ein Dienst wird unerwartet beendet.
-   Ein Server steht nicht mehr zur Verfügung.
-   Ein Laufwerk füllt die Kapazität von 80% aus.
-   Sicherheitsereignisse werden einem NT-Ereignisprotokoll gemeldet.

WMI unterstützt Ereigniserkennung und-Übermittlung an Ereignisconsumer, da einige WMI-Anbieter Ereignis Anbieter sind. Weitere Informationen finden Sie unter [empfangen eines WMI-Ereignisses](receiving-a-wmi-event.md).

[*Ereignisconsumer*](gloss-e.md) sind Anwendungen oder Skripts, die eine Benachrichtigung über Ereignisse anfordern und dann Aufgaben ausführen, wenn bestimmte Ereignisse auftreten. Sie können Ereignis Überwachungs Skripts oder-Anwendungen erstellen, die vorübergehend überwachen, wann Ereignisse auftreten. WMI stellt außerdem eine Reihe vorinstallierter dauerhafter Ereignis Anbieter und die permanenten Consumerklassen bereit, die es Ihnen ermöglichen, Ereignisse dauerhaft zu überwachen. Weitere Informationen finden Sie unter über [wachen und reagieren auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [Verwenden temporärer Ereignisconsumer](#using-temporary-event-consumers)
-   [Verwenden von permanenten Ereignisverbrauchern](#using-permanent-event-consumers)

## <a name="using-temporary-event-consumers"></a>Verwenden temporärer Ereignisconsumer

Temporäre Ereignisconsumer sind Skripts oder Anwendungen, die die Ereignisse zurückgeben, die einer Ereignis Abfrage oder einem Filter entsprechen. Temporäre Ereignis Abfragen verwenden in der Regel entweder [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) in C++-Anwendungen oder [**SWbemServices.Execnotificationquery**](swbemservices-execnotificationquery.md) in Skripts und Visual Basic.

Eine Ereignis Abfrage fordert Instanzen einer Ereignisklasse an, die einen bestimmten Ereignistyp angibt, z. b. [**Win32 \_ processtrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) oder [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).

Im folgenden VBScript-Codebeispiel wird eine Benachrichtigung angefordert, wenn eine Instanz von [**Win32 \_ processtrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) erstellt wird. Eine Instanz dieser Klasse wird generiert, wenn ein Prozess gestartet oder beendet wird.

Um das Skript auszuführen, kopieren Sie es in eine Datei mit dem Namen event.vbs, und verwenden Sie die folgende Befehlszeile: **cscript event.vbs**. Sie können die Ausgabe des Skripts anzeigen, indem Sie Notepad.exe oder einen anderen Prozess starten. Das Skript wird beendet, nachdem fünf Prozesse gestartet oder beendet wurden.

Dieses Skript ruft [**SWbemServices.Execnotificationquery**](swbemservices-execnotificationquery.md)auf, bei dem es sich um die [*semisynchrone*](gloss-s.md) Version der-Methode handelt. Im nächsten Skript finden Sie ein Beispiel für das Einrichten eines asynchronen temporären Ereignis Abonnements durch Aufrufen von [**SWbemServices.Execnotificationqueryasync**](swbemservices-execnotificationqueryasync.md). Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md). Das Skript ruft die Datei " [**errbemeventsource. NextEvent**](swbemeventsource-nextevent.md) " auf, um jedes Ereignis beim Eintreffen abzurufen und zu verarbeiten. Speichern Sie das Skript in einer Datei mit der Erweiterung. VSB, und führen Sie das Skript mit cscript: **cscript file.vbs** in einer Befehlszeile aus.


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



Temporäre Ereignisconsumer müssen manuell gestartet werden und müssen nicht über WMI-Neustarts oder Betriebssystem Neustarts hinweg beibehalten werden. Ein temporärer Ereignisconsumer kann Ereignisse nur verarbeiten, während er ausgeführt wird.

Im folgenden Verfahren wird beschrieben, wie ein temporärer Ereignisconsumer erstellt wird.

**So erstellen Sie einen temporären Ereignisconsumer**

1.  Entscheiden Sie, welche Programmiersprache verwendet werden soll.

    Die Programmiersprache bestimmt die zu verwendende API.

    -   Verwenden Sie für die Programmiersprache C++ die [com-API für WMI](com-api-for-wmi.md).
    -   Verwenden Sie für Visual Basic-oder Skriptsprachen die [Skript-API für WMI](scripting-api-for-wmi.md).

2.  Beginnen Sie mit dem Programmieren einer temporären ereignisconsumeranwendung auf dieselbe Weise, wie Sie eine WMI-Anwendung starten.

    Die ersten Schritte der Codierung hängen von der Programmiersprache ab. In der Regel melden Sie sich bei WMI an und richten die Sicherheitseinstellungen ein. Weitere Informationen finden Sie unter [Erstellen einer WMI-Anwendung oder eines Skripts](creating-a-wmi-application-or-script.md).

3.  Definieren Sie die Ereignis Abfrage, die Sie verwenden möchten.

    Um einige Arten von Leistungsdaten zu erhalten, müssen Sie möglicherweise Klassen verwenden, die von Hochleistungs Anbietern bereitgestellt werden. Weitere Informationen finden Sie unter über [Wachen von Leistungsdaten](monitoring-performance-data.md), [bestimmen der Art des](determining-the-type-of-event-to-receive.md)empfangenden Ereignisses und [Abfragen mit WQL](querying-with-wql.md).

4.  Entscheiden Sie sich für einen asynchronen oder einen semisynchronen aufrufsbefehl, und wählen Sie die API-Methode aus.

    Mit asynchronen aufrufen können Sie den Aufwand für das Abrufen von Daten vermeiden. Semisynchrone Aufrufe bieten jedoch eine ähnliche Leistung mit größerer Sicherheit. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

5.  Führen Sie den asynchronen oder semisynchronen Methoden aufrufsbefehl aus, und schließen Sie eine Ereignis Abfrage *als den Parameter* "" "

    Für C++-Anwendungen werden die folgenden Methoden aufgerufen:

    -   [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery)
    -   [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)

    Bei Skripts werden die folgenden Methoden aufgerufen:

    -   [**CnotificationquerySWbemServices.Exe**](swbemservices-execnotificationquery.md)
    -   [**SWbemServices.Execnotificationqueryasync**](swbemservices-execnotificationqueryasync.md)

6.  Schreiben Sie den Code, um das zurückgegebene Ereignis Objekt zu verarbeiten.

    Fügen Sie für asynchrone Ereignis Abfragen den Code in die verschiedenen Methoden oder Ereignisse der Objekt Senke ein. Bei semisynchronen Ereignis Abfragen wird jedes Objekt zurückgegeben, da es von WMI abgerufen wird, sodass sich der Code in der Schleife befinden muss, die jedes Objekt verarbeitet.

Das folgende Skriptcode Beispiel ist eine asynchrone Version des [**Win32 \_ processtrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) -Skripts. Da asynchrone Vorgänge sofort zurückgegeben werden, wird das Skript in einem Dialogfeld aktiv, während es auf Ereignisse wartet.

Anstatt " [**slibemeventsource. NextEvent**](swbemeventsource-nextevent.md) " aufzurufen, um die einzelnen Ereignisse zu empfangen, verfügt das Skript über einen Ereignishandler für das Ereignis " [**slibemsink onobjectready**](swbemsink-onobjectready.md) ".


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
> Ein asynchroner Rückruf (z. b. ein Rückruf, der von der `SINK_OnObjectReady` Unterroutine verarbeitet wird) ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke. Verwenden Sie für eine bessere Sicherheit entweder die semisynchrone Kommunikation oder die synchrone Kommunikation. Weitere Informationen finden Sie unter den folgenden Themen:
>
> -   [Erstellen eines semisynchronen Aufrufes mit C++](making-a-semisynchronous-call-with-c--.md)
> -   [Erstellen eines semisynchronen Aufrufes mit VBScript](making-a-semisynchronous-call-with-vbscript.md)
> -   [Erstellen eines asynchronen Aufrufes mit C++](making-an-asynchronous-call-with-c--.md)
> -   [Erstellen eines asynchronen Aufrufes mit VBScript](making-an-asynchronous-call-with-vbscript.md)
> -   [Festlegen der Sicherheit für einen asynchronen-Befehl](setting-security-on-an-asynchronous-call.md)
> -   [Sichern von Skript Clients](securing-scripting-clients.md)

 

## <a name="using-permanent-event-consumers"></a>Verwenden von permanenten Ereignisverbrauchern

Ein dauerhafter Ereignisconsumer wird ausgeführt, bis die Registrierung explizit abgebrochen wird, und startet dann, wenn WMI oder das System neu gestartet wird.

Ein dauerhafter Ereignisconsumer ist eine Kombination aus WMI-Klassen,-Filtern und COM-Objekten in einem System.

In der folgenden Liste sind die erforderlichen Komponenten zum Erstellen eines permanenten Ereignisconsumers aufgeführt:

-   Ein COM-Objekt, das den Code enthält, der den permanenten Consumer implementiert.
-   Eine neue permanente Consumerklasse.
-   Eine Instanz der permanenten Consumer-Klasse.
-   Ein Filter, der die Abfrage für Ereignisse enthält.
-   Eine Verknüpfung zwischen dem Consumer und dem Filter.

Weitere Informationen finden Sie [unter empfangen von Ereignissen zu allen Zeit](--filtertoconsumerbinding.md)Punkten.

WMI bietet mehrere permanente Consumer. Die Consumerklassen und das COM-Objekt, das den Code enthält, sind vorinstalliert. Beispielsweise können Sie eine Instanz der [**activescripteventconsumer**](activescripteventconsumer.md) -Klasse erstellen und konfigurieren, um ein Skript auszuführen, wenn ein Ereignis auftritt. Weitere Informationen finden Sie unter über [wachen und reagieren auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern. Ein Beispiel für die Verwendung von **activescripteventconsumer** finden Sie unter [Ausführen eines Skripts auf der Grundlage eines Ereignisses](running-a-script-based-on-an-event.md).

Im folgenden Verfahren wird beschrieben, wie ein dauerhafter Ereignisconsumer erstellt wird.

**So erstellen Sie einen permanenten Ereignisconsumer**

1.  [Registrieren Sie den Ereignis Anbieter](registering-a-provider.md) bei dem Namespace, den Sie verwenden.

    Einige Ereignis Anbieter können nur einen bestimmten Namespace verwenden. [**\_ \_ Instancecreationevent**](--instancecreationevent.md) ist beispielsweise ein System internes Ereignis, das vom Win32- [Anbieter](/windows/desktop/CIMWin32Prov/win32-provider) unterstützt wird und standardmäßig mit dem \\ root \\ CIMV2-Namespace registriert wird.

    > [!Note]  
    > Sie können die **eventnamespace** -Eigenschaft des [**\_ \_ eventfilters**](--eventfilter.md) verwenden, die in der Registrierung verwendet wird, um ein Cross-Namespace-Abonnement zu erstellen. Weitere Informationen finden Sie unter [Implementieren von Abonnements für permanente Namespace-Ereignisse](implementing-cross-namespace-permanent-event-subscriptions.md).

     

2.  [Registrieren Sie den ereignishandleranbieter](registering-an-event-consumer-provider.md) bei dem Namespace, in dem sich Ereignis Klassen befinden.

    WMI verwendet einen Ereignisconsumeranbieter, um einen permanenten Ereignisconsumer zu finden. Der permanente Ereignisconsumer ist die Anwendung, die von WMI beim Empfang eines Ereignisses gestartet wird. Um Ereignisconsumer zu registrieren, erstellen Anbieter Instanzen von [**\_ \_ eventconsumerproviderregistration**](--eventconsumerproviderregistration.md).

3.  Erstellen Sie eine Instanz der-Klasse, die den dauerhaften Ereignisconsumer darstellt, den Sie verwenden möchten.

    Ereignisconsumerklassen werden von der [**\_ \_ eventconsumer**](--eventconsumer.md)-Klasse abgeleitet. Legen Sie die Eigenschaften fest, die die ereignisconsumerinstanz benötigt.

4.  Registrieren Sie den Consumer mit com mithilfe des **regsvr32** -Hilfsprogramms.
5.  Erstellen Sie eine Instanz der Ereignis Filterklasse [**\_ \_ EventFilter**](--eventfilter.md).

    Legen Sie die erforderlichen Felder für die Ereignis Filter Instanz fest. Die erforderlichen Felder für [**\_ \_ EventFilter**](--eventfilter.md) sind " **Name**", " **QueryLanguage**" und " **Query**". Die **Name** -Eigenschaft kann ein beliebiger eindeutiger Name für eine Instanz dieser Klasse sein. Die **QueryLanguage** -Eigenschaft ist immer auf "WQL" festgelegt. Die **Query** -Eigenschaft ist eine Zeichenfolge, die eine Ereignis Abfrage enthält. Ein Ereignis wird generiert, wenn die Abfrage eines permanenten Ereignisconsumers fehlschlägt. Die Quelle des Ereignisses ist WinMgmt, die Ereignis-ID ist 10, und der Ereignistyp ist Fehler.

6.  Erstellen Sie eine Instanz der [**\_ \_ filtertoconsumerbinding**](--filtertoconsumerbinding.md) -Klasse, um einen logischen Ereignisconsumer einem Ereignis Filter zuzuordnen.

    WMI verwendet eine Zuordnung, um den Ereignisconsumer zu finden, der dem Ereignis zugeordnet ist, das den im Ereignis Filter angegebenen Kriterien entspricht. WMI verwendet den Ereignisconsumeranbieter, um zu starten, um die Anwendung für die permanente Ereignisconsumer zu finden

 

 
