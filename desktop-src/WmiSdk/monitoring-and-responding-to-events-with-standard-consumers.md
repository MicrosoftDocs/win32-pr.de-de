---
description: Sie können die installierten Standard Consumerklassen verwenden, um Aktionen auf der Grundlage von Ereignissen in einem Betriebssystem auszuführen.
ms.assetid: 1979dc55-a440-4c31-832b-36fa84def4c9
ms.tgt_platform: multiple
title: Überwachen von und reagieren auf Ereignisse mit Standard Consumern
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5bd1d329cd861fa45c99851707177322d0b9d12f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "103870220"
---
# <a name="monitoring-and-responding-to-events-with-standard-consumers"></a>Überwachen von und reagieren auf Ereignisse mit Standard Consumern

Sie können die installierten [Standard Consumerklassen](standard-consumer-classes.md) verwenden, um Aktionen auf der Grundlage von Ereignissen in einem Betriebssystem auszuführen. Standard Consumer sind einfache Klassen, die bereits registriert sind und permanente Consumerklassen definieren. Jeder Standard Consumer nimmt eine bestimmte Aktion vor, nachdem er eine Ereignis Benachrichtigung erhalten hat. Beispielsweise können Sie eine Instanz von [**activescripteventconsumer**](activescripteventconsumer.md) definieren, um ein Skript auszuführen, wenn der freie Speicherplatz auf einem Computer von einer angegebenen Größe abweicht.

WMI kompiliert die Standardconsumer in Standardnamespaces, die vom Betriebssystem abhängig sind, z. b.:

-   In Windows Server 2003 werden standardmäßig alle Standard Consumer in den Namespace "root- \\ Abonnement" kompiliert.

> [!Note]  
> Informationen zu den Standardnamespaces und Betriebssystemen, die für die einzelnen WMI-klassenspezifisch sind, finden Sie in den Abschnitten "Hinweise und Anforderungen" der einzelnen Klassen Themen.

 

In der folgenden Tabelle werden die WMI-Standardconsumer aufgelistet und beschrieben.



| Standard Consumer                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Activescripteventconsumer**](activescripteventconsumer.md) | Führt ein Skript aus, wenn eine Ereignis Benachrichtigung empfangen wird. Weitere Informationen finden Sie unter [Ausführen eines Skripts auf der Grundlage eines Ereignisses](running-a-script-based-on-an-event.md).                                                                                                                                                                                                                                                       |
| [**Logfileeventconsumer**](logfileeventconsumer.md)           | Schreibt angepasste Zeichen folgen in eine Text Protokolldatei, wenn eine Ereignis Benachrichtigung empfangen wird. Weitere Informationen finden Sie unter [Schreiben in eine Protokolldatei auf Grundlage eines Ereignisses](writing-to-a-log-file-based-on-an-event.md).                                                                                                                                                                                                                  |
| [**Nteventlogeventconsumer**](nteventlogeventconsumer.md)     | Protokolliert eine bestimmte Meldung im Anwendungs Ereignisprotokoll. Weitere Informationen finden Sie unter [Protokollierung in NT-Ereignisprotokoll basierend auf einem Ereignis](logging-to-nt-event-log-based-on-an-event.md).                                                                                                                                                                                                                                             |
| [**Smtpeer-Consumer**](smtpeventconsumer.md)                 | Sendet bei jedem übermitteln eines Ereignisses eine e-Mail-Nachricht mithilfe von SMTP. Weitere Informationen finden Sie unter [Senden von e-Mails auf der Grundlage eines Ereignisses](sending-e-mail-based-on-an-event.md).                                                                                                                                                                                                                                          |
| [**Commandlineeventconsumer**](commandlineeventconsumer.md)   | Hiermit wird ein Prozess gestartet, wenn ein Ereignis an ein lokales System übermittelt wird. Die ausführbare Datei muss sich an einem sicheren Speicherort befinden oder mit einer starken Zugriffs Steuerungs Liste (ACL) gesichert werden, um zu verhindern, dass nicht autorisierte Benutzer ihre ausführbare Datei durch eine andere ausführbare Datei ersetzen. Weitere Informationen finden Sie unter [Ausführen eines Programms in der Befehlszeile auf der Grundlage eines Ereignisses](running-a-program-from-the-command-line-based-on-an-event.md). |



 

Im folgenden Verfahren wird beschrieben, wie Sie Ereignisse mithilfe eines standardconsumers überwachen und darauf reagieren. Beachten Sie, dass die Prozedur für eine Managed Object Format (MOF)-Datei, ein Skript oder eine Anwendung identisch ist.

**So überwachen Sie Ereignisse mit einem Standard Consumer und reagieren darauf**

1.  Geben Sie den Namespace in einer MOF-Datei mit dem MOF-Präprozessorbefehl- [ \# pragma-Namespace](pragma-namespace.md)an. Geben Sie in einem Skript oder einer Anwendung den Namespace im Code an, der eine Verbindung mit WMI herstellt.

    Im folgenden MOF-Codebeispiel wird gezeigt, wie der \\ Namespace des Stamm Abonnements angegeben wird.

    ```syntax
    #pragma namespace ("\\\\.\\root\\subscription")
    ```

    Die meisten systeminternen [*Ereignisse*](gloss-i.md) werden Änderungen an Klassen Instanzen im root \\ CIMV2-Namespace zugeordnet. Registrierungs Ereignisse, wie z. b. [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) , werden jedoch \\ vom [System Registrierungs Anbieter](/previous-versions/windows/desktop/regprov/system-registry-provider)im Stamm-Standard Namespace ausgelöst.

    Ein Consumer kann in anderen Namespaces befindliche Ereignis Klassen einschließen, indem er in der [**\_ \_ EventFilter**](--eventfilter.md) -Abfrage für Ereignisse den Namespace in der **eventnamespace** -Eigenschaft angibt. Die systeminternen [*Ereignis*](gloss-i.md) Klassen, z. b. [**\_ \_ instanceoperationevent**](--instanceoperationevent.md) , sind in jedem Namespace verfügbar.

2.  Erstellen Sie eine Instanz einer standardconsumerklasse, und füllen Sie Sie auf.

    Diese Instanz kann einen eindeutigen Wert in der **Name** -Eigenschaft aufweisen. Sie können einen vorhandenen Consumer aktualisieren, indem Sie denselben Namen wieder verwenden.

    **Insertionstringtemplates** enthält den Text, der in ein Ereignis eingefügt werden soll, das Sie in **eventType** angeben. Sie können Literalzeichenfolgen verwenden oder direkt auf eine Eigenschaft verweisen. Weitere Informationen finden Sie unter [Verwenden von Standard Zeichenfolgen-Vorlagen](using-standard-string-templates.md) und [SELECT-Anweisung für Ereignis Abfragen](select-statement-for-event-queries.md).

    Verwenden Sie eine vorhandene Quelle für das Ereignisprotokoll, das eine Einfügezeichenfolge ohne zugehörigen Text unterstützt.

    Im folgenden MOF-Codebeispiel wird gezeigt, wie eine vorhandene Quelle von WSH und der **EventID-** Wert 8 verwendet werden.

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

3.  Erstellen Sie eine Instanz von [**\_ \_ EventFilter**](--eventfilter.md) , und definieren Sie eine Abfrage für Ereignisse.

    Im folgenden Beispiel überwacht der Filter den Registrierungsschlüssel, in dem Start Programme registriert sind. Das Überwachen dieses Registrierungsschlüssels ist möglicherweise wichtig, da sich ein nicht autorisiertes Programm unter dem Schlüssel registrieren kann, was dazu veranlasst, dass es beim Starten des Computers gestartet wird.

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

4.  Identifizieren Sie ein Ereignis, um eine Ereignis Abfrage zu überwachen und zu erstellen.

    Sie können überprüfen, ob ein System internes oder ein extrinsisches Ereignis verwendet, das verwendet. Verwenden Sie z. b. die [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) -Klasse des Registrierungs Anbieters, um Änderungen an der Systemregistrierung zu überwachen.

    Wenn eine Klasse nicht vorhanden ist, die ein Ereignis beschreibt, das Sie überwachen müssen, müssen Sie einen eigenen Ereignis Anbieter erstellen und neue System externe-Ereignis Klassen definieren. Weitere Informationen finden Sie unter [Schreiben eines Ereignis Anbieters](writing-an-event-provider.md).

    In einer MOF-Datei können Sie einen [*Alias*](gloss-a.md) für den Filter und den Consumer definieren, der eine einfache Möglichkeit bietet, die Instanzpfade zu beschreiben.

    Im folgenden Beispiel wird gezeigt, wie Sie einen [*Alias*](gloss-a.md) für den Filter und den Consumer definieren.

    ```syntax
    instance of __EventFilter as $FILTER
    instance of LogFileEventConsumer as $CONSUMER
    ```

5.  Erstellen Sie eine Instanz von [**\_ \_ filtertoconsumerbinding**](--filtertoconsumerbinding.md) , um den Filter und die Consumerklassen zuzuordnen. Diese Instanz bestimmt, dass bei Auftreten eines Ereignisses, das mit dem angegebenen Filter übereinstimmt, die vom Consumer angegebene Aktion erfolgen muss. [**\_ \_ EventFilter**](--eventfilter.md), [**\_ \_ eventconsumer**](--eventconsumer.md)und **\_ \_ filtertoconsumerbinding** müssen die gleiche individuelle Sicherheits-ID (SID) in der Eigenschaft " **kreatorsid** " aufweisen. Weitere Informationen finden Sie unter [Binden eines Ereignis Filters mit einem logischen Consumer](binding-an-event-filter-with-a-logical-consumer.md).

    Im folgenden Beispiel wird gezeigt, wie eine Instanz anhand des Objekt Pfads identifiziert wird, oder ein Alias als Kurzform Ausdruck für den Objekt Pfad verwendet wird.

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

    Sie können einen Filter an mehrere Consumer binden. Dies bedeutet, dass beim Auftreten von übereinstimmenden Ereignissen mehrere Aktionen ausgeführt werden müssen. oder Sie können einen Consumer an mehrere Filter binden, was darauf hinweist, dass die Aktion ausgeführt werden muss, wenn Ereignisse auftreten, die einem der Filter entsprechen.

    Die folgenden Aktionen werden basierend auf der Bedingung der Consumer und Ereignisse ausgeführt:

    -   Wenn einer der permanenten Verbraucher ausfällt, erhalten andere Consumer, die das Ereignis anfordern, eine Benachrichtigung.
    -   Wenn ein Ereignis gelöscht wird, löst WMI [**\_ \_ eventdroppedevent**](--eventdroppedevent.md)aus.
    -   Wenn Sie dieses Ereignis abonnieren, wird das gelöschte Ereignis zurückgegeben, und ein Verweis auf den [**\_ \_ eventconsumer**](--eventconsumer.md) stellt den fehlgeschlagenen Consumer dar.
    -   Wenn ein Consumer ausfällt, löst WMI [**\_ \_ consumerfailureevent**](--consumerfailureevent.md)aus, das möglicherweise weitere Informationen in den Eigenschaften **errorCode**, **ErrorDescription** und **ErrorObject** enthält.

    Weitere Informationen finden Sie unter [Binden eines Ereignis Filters mit einem logischen Consumer](binding-an-event-filter-with-a-logical-consumer.md).

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt das MOF für eine Instanz von [**nteventlogeventconsumer**](nteventlogeventconsumer.md). Nachdem Sie diese MOF kompiliert haben, wird bei jedem Versuch, einen Wert im Registrierungs Pfad **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\** zu erstellen, zu löschen oder zu ändern, ein Eintrag im Anwendungs Ereignisprotokoll unter der Quelle "WSH" protokolliert.


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

[Sicheres empfangen von Ereignissen](receiving-events-securely.md)
</dt> </dl>

 

 
