---
description: Die nteventlogeventconsumer-Klasse schreibt eine Meldung in das Windows-Ereignisprotokoll, wenn ein bestimmtes Ereignis auftritt. Diese Klasse ist ein Standard Ereignisconsumer, den WMI bereitstellt.
ms.assetid: ca998a91-d9f7-44ff-bb83-5ba92d68f31e
ms.tgt_platform: multiple
title: Protokollierung in NT-Ereignisprotokoll basierend auf einem Ereignis
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 69bf24c0d64c95a012b8681b88bde34dc28fa179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866872"
---
# <a name="logging-to-nt-event-log-based-on-an-event"></a>Protokollierung in NT-Ereignisprotokoll basierend auf einem Ereignis

Die [**nteventlogeventconsumer**](nteventlogeventconsumer.md) -Klasse schreibt eine Meldung in das Windows-Ereignisprotokoll, wenn ein bestimmtes Ereignis auftritt. Diese Klasse ist ein Standard Ereignisconsumer, den WMI bereitstellt.

> [!Note]  
> Authentifizierte Benutzer können Ereignisse standardmäßig nicht im Anwendungsprotokoll auf einem Remote Computer protokollieren. Das in diesem Thema beschriebene Beispiel schlägt daher fehl, wenn Sie die **uncservername** -Eigenschaft der [**nteventlogeventconsumer**](nteventlogeventconsumer.md) -Klasse verwenden und einen Remote Computer als Wert angeben. Weitere Informationen zum Ändern der Ereignisprotokoll Sicherheit finden Sie in diesem [KB-Artikel](https://support.microsoft.com/kb/323076).

 

Das grundlegende Verfahren für die Verwendung eines standardconsumers wird unter über [wachen und reagieren auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern beschrieben. Im folgenden finden Sie zusätzliche Schritte, die über das grundlegende Verfahren hinausgehen, das bei Verwendung der [**nteventlogeventconsumer**](nteventlogeventconsumer.md) -Klasse erforderlich ist. In den Schritten wird beschrieben, wie Sie einen Ereignisconsumer erstellen, der in das Anwendungs Ereignisprotokoll schreibt.

Im folgenden Verfahren wird beschrieben, wie Sie einen Ereignisconsumer erstellen, der in das NT-Ereignisprotokoll schreibt.

**So erstellen Sie einen Ereignisconsumer, der in das Windows-Ereignisprotokoll schreibt**

1.  Erstellen Sie in einer MOF-Datei (Managed Object Format) eine Instanz von [**nteventlogeventconsumer**](nteventlogeventconsumer.md) , um die Ereignisse zu empfangen, die Sie in der Abfrage anfordern. Weitere Informationen zum Schreiben von MOF-Code finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](designing-managed-object-format--mof--classes.md).
2.  Erstellen Sie eine Instanz von [**\_ \_ EventFilter**](--eventfilter.md), und benennen Sie Sie, und erstellen Sie dann eine Abfrage, um den Ereignistyp anzugeben, der von das Schreiben in das NT-Ereignisprotokoll auslöst.

    Weitere Informationen finden Sie unter [Abfragen mit WQL](querying-with-wql.md).

3.  Erstellen Sie eine Instanz von [**\_ \_ filtertoconsumerbinding**](--filtertoconsumerbinding.md) , um den Filter der Instanz von [**nteventlogeventconsumer**](nteventlogeventconsumer.md)zuzuordnen.
4.  Kompilieren Sie die MOF-Datei mit [**Mofcomp.exe**](mofcomp.md).

## <a name="example"></a>Beispiel

Das Beispiel in diesem Abschnitt ist ein MOF-Code, aber Sie können die Instanzen Programm gesteuert mithilfe der [Skript-API für WMI](scripting-api-for-wmi.md) oder der [com-API für WMI](com-api-for-wmi.md)erstellen. Das Beispiel zeigt, wie ein Consumer erstellt wird, um mithilfe von [**nteventlogeventconsumer**](nteventlogeventconsumer.md)in das Anwendungs Ereignisprotokoll zu schreiben. Das MOF erstellt eine neue Klasse mit dem Namen "ntlogcons \_ example", einen Ereignis Filter zum Abfragen von Vorgängen, z. b. die Erstellung, eine Instanz dieser neuen Klasse und eine Bindung zwischen Filter und Consumer. Da die letzte Aktion in der MOF-Datei das Erstellen einer Instanz des ntlogcons- \_ Beispiels ist, können Sie das Ereignis sofort im Anwendungs Ereignisprotokoll sehen, indem Sie Eventvwr.exe ausführen.

Der `EventID=0x0A for SourceName="WinMgmt"` identifiziert eine Meldung mit dem folgenden Text. "%1", "%2", "%3", sind Platzhalter für entsprechende Zeichen folgen, die im insertionstringtemplates-Array angegeben sind.

``` syntax
Event filter with query "%2" could not be [re]activated in 
namespace "%1" because of error %3. Events may not be delivered 
through this filter until the problem is corrected.
```

Im folgenden Verfahren wird beschrieben, wie das Beispiel verwendet wird.

**So verwenden Sie das Beispiel**

1.  Kopieren Sie das unten aufgeführte MOF-Listenfeld in eine Textdatei, und speichern Sie es mit der Erweiterung MOF.
2.  Kompilieren Sie in einem Befehlsfenster die MOF-Datei mit dem folgenden Befehl:

    " **Mamacomp** *filename * * *. MOF* "*

3.  Führen Sie Eventvwr.exe aus. Sehen Sie sich das Anwendungs Ereignisprotokoll an. Es sollte ein Ereignis mit der ID = 10 ( **EventID**), Source = "WMI" und Type = Error angezeigt werden.
4.  Doppelklicken Sie in der Spalte **Ereignis** auf die **Information Type** -Meldung von WMI mit 10. Die folgende Beschreibung wird für das-Ereignis angezeigt.

    ``` syntax
    Event filter with query "STRING2" could not be [re]activated in 
    namespace "STRING1" because of error STRING3. Events cannot be 
    delivered through this filter until the problem is corrected.
    ```

``` syntax
// Set the namespace as root\subscription.
// The NTEventLogEventConsumer is already
// compiled in the root\subscription namespace. 

#pragma namespace ("\\\\.\\Root\\subscription")
class NTLogCons_Example
{
 [key] string name;
 string InsertionString;
};

// Create an instance of the NT Event log consumer
// and give it the alias $CONSUMER

instance of NTEventLogEventConsumer as $CONSUMER
{
    // Unique instance name
    Name = "NTConsumerTest"; 
    // System component that generates the event
    SourceName = "WinMgmt";
    // Event message WBEM_MC_CANNOT_ACTIVATE_FILTER
    EventID = 0xC000000A;
    // EVENTLOG_ERROR_TYPE
    EventType = 1;
    // WMI event messages do not have multiple categories
    Category = 0;
    // Number of strings in InsertionStringTemplates property
    NumberOfInsertionStrings = 3;

    InsertionStringTemplates =
       {"%TargetInstance.Name%",
        "%TargetInstance.InsertionString%",
        "STRING3"};
};

// Create an instance of the event filter
// and give it the alias $FILTER
// The filter queries for any instance operation event
// for instances of the NTLogCons_Example class

instance of __EventFilter as $FILTER
{
    // Unique instance name
    Name = "NTLogConsFilter";
    Query = "SELECT * from __InstanceOperationEvent"
            " WHERE TargetInstance ISA \"NTLogCons_Example\"";
    QueryLanguage = "WQL";
};

// Create an instance of the binding
// between filter and consumer instances.

instance of __FilterToConsumerBinding
{
    Consumer = $CONSUMER;
    Filter = $FILTER;
};

// Create an instance of this class right now. 

instance of NTLogCons_Example
{
   Name = "STRING1";
   InsertionString = "STRING2";
};
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Überwachen von und reagieren auf Ereignisse mit Standard Consumern](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



