---
description: Sie können die installierten Standard-Consumerklassen verwenden, um Aktionen basierend auf Ereignissen in einem Betriebssystem durchzuführen.
ms.assetid: 1979dc55-a440-4c31-832b-36fa84def4c9
ms.tgt_platform: multiple
title: Überwachen und Reagieren auf Ereignisse mit Standardverbrauchern
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b0b7e7b1d1e79e64fb1eb83f17f3aa2d118a9eb53b23c19cbdfd624e2c501a84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992780"
---
# <a name="monitoring-and-responding-to-events-with-standard-consumers"></a>Überwachen und Reagieren auf Ereignisse mit Standardverbrauchern

Sie können die installierten [Standard-Consumerklassen verwenden,](standard-consumer-classes.md) um Aktionen basierend auf Ereignissen in einem Betriebssystem durchzuführen. Standard-Consumer sind einfache Klassen, die bereits registriert sind und permanente Consumerklassen definieren. Jeder Standardverbraucher führt eine bestimmte Aktion aus, nachdem er eine Ereignisbenachrichtigung erhalten hat. Sie können z. B. eine Instanz von [**ActiveScriptEventConsumer**](activescripteventconsumer.md) definieren, um ein Skript auszuführen, wenn sich der freie Speicherplatz auf einem Computer von einer angegebenen Größe unterscheiden soll.

WMI kompiliert die Standardverbraucher in Standardnamespaces, die vom Betriebssystem abhängig sind. Beispiel:

-   In Windows Server 2003 werden alle Standardverbraucher standardmäßig in den Namespace "Root \\ Subscription" kompiliert.

> [!Note]  
> Informationen zu den Standardnamespaces und Betriebssystemen, die für jede WMI-Klasse spezifisch sind, finden Sie in den Abschnitten Hinweise und Anforderungen der einzelnen Klassen.

 

In der folgenden Tabelle werden die WMI-Standardverbraucher aufgeführt und beschrieben.



| Standard-Consumer                                              | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActiveScriptEventConsumer**](activescripteventconsumer.md) | Führt ein Skript aus, wenn es eine Ereignisbenachrichtigung empfängt. Weitere Informationen finden Sie unter [Ausführen eines Skripts basierend auf einem Ereignis.](running-a-script-based-on-an-event.md)                                                                                                                                                                                                                                                       |
| [**LogFileEventConsumer**](logfileeventconsumer.md)           | Schreibt benutzerdefinierte Zeichenfolgen in eine Textdatei, wenn sie eine Ereignisbenachrichtigung empfängt. Weitere Informationen finden Sie unter [Schreiben in eine Protokolldatei basierend auf einem Ereignis.](writing-to-a-log-file-based-on-an-event.md)                                                                                                                                                                                                                  |
| [**NTEventLogEventConsumer**](nteventlogeventconsumer.md)     | Protokolliert eine bestimmte Meldung im Anwendungsereignisprotokoll. Weitere Informationen finden Sie unter [Protokollierung im NT-Ereignisprotokoll basierend auf einem Ereignis.](logging-to-nt-event-log-based-on-an-event.md)                                                                                                                                                                                                                                             |
| [**SMTPEventConsumer**](smtpeventconsumer.md)                 | Sendet eine E-Mail-Nachricht mithilfe von SMTP jedes Mal, wenn ein Ereignis an sie übermittelt wird. Weitere Informationen finden Sie unter [Senden von E-Mails basierend auf einem Ereignis.](sending-e-mail-based-on-an-event.md)                                                                                                                                                                                                                                          |
| [**CommandLineEventConsumer**](commandlineeventconsumer.md)   | Startet einen Prozess, wenn ein Ereignis an ein lokales System übermittelt wird. Die ausführbare Datei muss sich an einem sicheren Speicherort befinden oder mit einer starken Zugriffssteuerungsliste (ACL) geschützt werden, um zu verhindern, dass ein nicht autorisierter Benutzer Ihre ausführbare Datei durch eine andere ausführbare Datei ersetzt. Weitere Informationen finden Sie unter [Ausführen eines Programms über die Befehlszeile basierend auf einem Ereignis.](running-a-program-from-the-command-line-based-on-an-event.md) |



 

Im folgenden Verfahren wird beschrieben, wie Ereignisse mithilfe eines Standard-Consumers überwacht und darauf reagiert werden. Beachten Sie, dass die Prozedur für eine mof Managed Object Format-Datei, ein Skript oder eine Anwendung identisch ist.

**So überwachen Sie Ereignisse mit einem Standardverbraucher und reagieren darauf**

1.  Geben Sie den Namespace in einer MOF-Datei mithilfe des MOF-Präprozessorbefehls [ \# pragma namespace an.](pragma-namespace.md) Geben Sie in einem Skript oder einer Anwendung den Namespace im Code an, der eine Verbindung mit WMI herstellt.

    Das folgende MOF-Codebeispiel zeigt, wie der Namespace des Stammabonnements \\ angegeben wird.

    ```syntax
    #pragma namespace ("\\\\.\\root\\subscription")
    ```

    Die [*meisten systeminternen*](gloss-i.md) Ereignisse sind Änderungen an Klasseninstanzen im \\ Cimv2-Stammnamespace zugeordnet. Registrierungsereignisse wie [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) werden jedoch vom Systemregistrierungsanbieter im \\ [Stamm-Standardnamespace ausgelöst.](/previous-versions/windows/desktop/regprov/system-registry-provider)

    Ein Consumer kann Ereignisklassen in anderen Namespaces enthalten, indem der Namespace in der **EventNamespace-Eigenschaft** in der [**\_ \_ EventFilter-Abfrage**](--eventfilter.md) für Ereignisse angegeben wird. Die [*systeminternen*](gloss-i.md) Ereignisklassen wie [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md) sind in jedem Namespace verfügbar.

2.  Erstellen sie eine Instanz einer Standard-Consumerklasse, und füllen Sie sie auf.

    Diese Instanz kann einen eindeutigen Wert in der **Name-Eigenschaft** haben. Sie können einen vorhandenen Consumer aktualisieren, indem Sie denselben Namen wiederverwenden.

    **InsertionStringTemplates enthält** den Text, der in ein Ereignis eingefügt werden soll, das Sie in **EventType angeben.** Sie können Literalzeichenfolgen verwenden oder direkt auf eine Eigenschaft verweisen. Weitere Informationen finden Sie unter [Verwenden von Standardzeichenfolgenvorlagen und](using-standard-string-templates.md) [SELECT-Anweisung für Ereignisabfragen.](select-statement-for-event-queries.md)

    Verwenden Sie eine vorhandene Quelle für das Ereignisprotokoll, die eine Einfügezeichenfolge ohne zugeordneten Text unterstützt.

    Im folgenden MOF-Codebeispiel wird die Verwendung einer vorhandenen WSH-Quelle und eines **EventID-Werts** von 8 veranschaulicht.

    ```syntax
    instance of NTEventLogEventConsumer as $Consumer
    {
        Name = "RunKeyEventlogConsumer";
        SourceName = "WSH";               
        EventID = 8;
        // Warning                              
        EventType = 2;
        // One string supplies the entire message          
        NumberOfInsertionStrings = 1;             
        // the %Hive% and %KeyPath% are properties of
        // the RegistryKeyChangeEvent instance 
        InsertionStringTemplates = 
            {"The key %Hive%\\%RootPath% has been modified."
            "Check if the change is intentional"};
    };
    ```

3.  Erstellen Sie eine Instanz von [**\_ \_ EventFilter,**](--eventfilter.md) und definieren Sie eine Abfrage für Ereignisse.

    Im folgenden Beispiel überwacht der Filter den Registrierungsschlüssel, in dem Startprogramme registriert sind. Die Überwachung dieses Registrierungsschlüssels kann wichtig sein, da sich ein nicht autorisiertes Programm unter dem Schlüssel registrieren kann, wodurch er beim Starten des Computers gestartet wird.

    ```syntax
    instance of __EventFilter as $Filter
    {
    Name = "RunKeyFilter";
    QueryLanguage = "WQL"; 
    Query = "Select * from RegistryTreeChangeEvent"
        " where (Hive = \"HKEY_LOCAL_MACHINE\" and "
        "RootPath = \"Software\\\\Microsoft\\\\Windows"
        "\\\\CurrentVersion\\\\Run\")";

    // RegistryTreeChangeEvents only fire in root\default namespace
    EventNamespace = "root\\default";                       
    };
    ```

4.  Identifizieren Sie ein Ereignis, das überwacht und eine Ereignisabfrage erstellt werden soll.

    Sie können überprüfen, ob ein systeminternes oder extrinsisches Ereignis verwendet wird. Verwenden Sie beispielsweise die [**RegistryTreeChangeEvent-Klasse**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) des Registrierungsanbieters, um Änderungen an der Systemregistrierung zu überwachen.

    Wenn keine Klasse vorhanden ist, die ein Ereignis beschreibt, das Sie überwachen müssen, müssen Sie einen eigenen Ereignisanbieter erstellen und neue extrinsische Ereignisklassen definieren. Weitere Informationen finden Sie unter [Schreiben eines Ereignisanbieters.](writing-an-event-provider.md)

    In einer MOF-Datei können [](gloss-a.md) Sie einen Alias für den Filter und Consumer definieren, der eine einfache Möglichkeit zum Beschreiben der Instanzpfade bietet.

    Das folgende Beispiel zeigt, wie Sie einen Alias [*für*](gloss-a.md) den Filter und consumer definieren.

    ```syntax
    instance of __EventFilter as $FILTER
    instance of LogFileEventConsumer as $CONSUMER
    ```

5.  Erstellen Sie eine Instanz von [**\_ \_ FilterToConsumerBinding,**](--filtertoconsumerbinding.md) um den Filter und die Consumerklassen zu verknüpfen. Diese Instanz bestimmt, dass beim Auftreten eines Ereignisses, das dem angegebenen Filter entspricht, die vom Consumer angegebene Aktion erfolgen muss. [**\_ \_ EventFilter,**](--eventfilter.md) [**\_ \_ EventConsumer**](--eventconsumer.md)und **\_ \_ FilterToConsumerBinding** müssen dieselbe einzelne Sicherheits-ID (SID) in der **CreatorSID-Eigenschaft** aufweisen. Weitere Informationen finden Sie unter [Binden eines Ereignisfilters mit einem logischen Consumer.](binding-an-event-filter-with-a-logical-consumer.md)

    Das folgende Beispiel zeigt, wie Sie eine -Instanz durch den Objektpfad identifizieren oder einen Alias als Kurzformausdruck für den Objektpfad verwenden.

    ```syntax
    instance of __EventFilter as $FILTER
    instance of NTEventLogEventConsumer as $CONSUMER
    ```

    Im folgenden Beispiel wird der Filter mithilfe von Aliasen an den Consumer gebunden.

    ```syntax
    instance of __FilterToConsumerBinding
    {
        Filter = $FILTER;
        Consumer = $CONSUMER;
        
    };
    ```

    Sie können einen Filter an mehrere Consumers binden. Dies bedeutet, dass beim Auftreten von übereinstimmenden Ereignissen mehrere Aktionen durchgeführt werden müssen. Oder Sie können einen Consumer an mehrere Filter binden. Dies bedeutet, dass die Aktion erfolgen muss, wenn Ereignisse auftreten, die mit einem der Filter übereinstimmen.

    Die folgenden Aktionen werden basierend auf der Bedingung von Consumers und Ereignissen durchgeführt:

    -   Wenn einer der permanenten Consumers ausfällt, erhalten andere Verbraucher, die das Ereignis anfordern, eine Benachrichtigung.
    -   Wenn ein Ereignis gelöscht wird, gibt WMI [**\_ \_ EventDroppedEvent aus.**](--eventdroppedevent.md)
    -   Wenn Sie dieses Ereignis abonnieren, wird das gelöschte Ereignis zurückgegeben, und ein Verweis auf [**\_ \_ EventConsumer**](--eventconsumer.md) stellt den fehlerhaften Consumer dar.
    -   Wenn ein Consumer ausfällt, wird von WMI [**\_ \_ ConsumerFailureEvent**](--consumerfailureevent.md)ausgelöst, das möglicherweise weitere Informationen in den **Eigenschaften ErrorCode,** **ErrorDescription** und **ErrorObject enthält.**

    Weitere Informationen finden Sie unter [Binden eines Ereignisfilters mit einem logischen Consumer.](binding-an-event-filter-with-a-logical-consumer.md)

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt die MOF für eine Instanz von [**NTEventLogEventConsumer.**](nteventlogeventconsumer.md) Nachdem Sie diese MOF kompiliert haben, protokolliert jeder Versuch, einen Wert im Registrierungspfad **HKEY \_ LOCAL MACHINE Software Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion \\ Run** zu erstellen, zu löschen oder zu ändern, einen Eintrag im Anwendungsereignisprotokoll unter der Quelle "WSH".


```mof
#pragma namespace ("\\\\.\\root\\subscription")
 
instance of __EventFilter as $Filter
{
    Name = "RunKeyFilter";
    QueryLanguage = "WQL";
    Query = "Select * from RegistryTreeChangeEvent"
            " where (Hive = \"HKEY_LOCAL_MACHINE\" and "
            "KeyPath = \"Software\\\\Microsoft\\\\Windows"
            "\\\\CurrentVersion\\\\Run\")";

    // RegistryTreeChangeEvents only fire
    // in root\default namespace
    EventNamespace = "root\\default";   
};
 
instance of NTEventLogEventConsumer as $Consumer
{
    Name = "RunKeyEventlogConsumer";
    SourceName = "WSH";               
    EventID = 8;
    EventType = 2;                            // Warning
    Category = 0;
    NumberOfInsertionStrings = 1;

    // the %Hive% and %KeyPath% are properties
    // of the RegistryKeyChangeEvent instance 
    InsertionStringTemplates = {"The key %Hive%\\%RootPath% "
        "has been modified. Check if the change is intentional"};
};
 

// Bind the filter to the consumer
instance of __FilterToConsumerBinding
{
    Filter = $Filter;
    Consumer = $Consumer;
};
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sicheres Empfangen von Ereignissen](receiving-events-securely.md)
</dt> </dl>

 

 
