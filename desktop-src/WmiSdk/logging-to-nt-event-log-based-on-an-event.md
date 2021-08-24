---
description: Die NTEventLogEventConsumer-Klasse schreibt eine Nachricht in das Windows Ereignisprotokoll, wenn ein angegebenes Ereignis auftritt. Diese Klasse ist ein Standardereignis-Consumer, der von WMI zur Verfügung steht.
ms.assetid: ca998a91-d9f7-44ff-bb83-5ba92d68f31e
ms.tgt_platform: multiple
title: Protokollierung im NT-Ereignisprotokoll basierend auf einem Ereignis
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c8c070b1a52fe41f32b8610ff0931d33be7feb33f9f5cd6f6067652e963f6824
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050708"
---
# <a name="logging-to-nt-event-log-based-on-an-event"></a>Protokollierung im NT-Ereignisprotokoll basierend auf einem Ereignis

Die [**NTEventLogEventConsumer-Klasse**](nteventlogeventconsumer.md) schreibt eine Nachricht in das Windows Ereignisprotokoll, wenn ein angegebenes Ereignis auftritt. Diese Klasse ist ein Standardereignis-Consumer, der von WMI zur Verfügung steht.

> [!Note]  
> Authentifizierte Benutzer können standardmäßig keine Ereignisse im Anwendungsprotokoll auf einem Remotecomputer protokollieren. Daher schlägt das in diesem Thema beschriebene Beispiel fehl, wenn Sie die **UNCServerName-Eigenschaft** der [**NTEventLogEventConsumer-Klasse**](nteventlogeventconsumer.md) verwenden und einen Remotecomputer als Wert angeben. Informationen zum Ändern der Sicherheit von Ereignisprotokollen finden Sie in diesem [KB-Artikel.](https://support.microsoft.com/kb/323076)

 

Das grundlegende Verfahren für die Verwendung eines Standard-Consumers wird unter [Überwachen und Reagieren auf Ereignisse mit Standardverbrauchern](monitoring-and-responding-to-events-with-standard-consumers.md)beschrieben. Im Folgenden finden Sie zusätzliche Schritte, die über die grundlegende Prozedur hinausgehen und bei Verwendung der [**NTEventLogEventConsumer-Klasse**](nteventlogeventconsumer.md) erforderlich sind. In den Schritten wird beschrieben, wie Sie einen Ereignisverbraucher erstellen, der in das Anwendungsereignisprotokoll schreibt.

Im folgenden Verfahren wird beschrieben, wie sie einen Ereignisverbraucher erstellen, der in das NT-Ereignisprotokoll schreibt.

**So erstellen Sie einen Ereignisverbraucher, der in das Windows Ereignisprotokoll schreibt**

1.  Erstellen Sie in einer MOF-Datei (Managed Object Format) eine Instanz von [**NTEventLogEventConsumer,**](nteventlogeventconsumer.md) um die Ereignisse zu empfangen, die Sie in der Abfrage anfordern. Weitere Informationen zum Schreiben von MOF-Code finden Sie unter [Entwerfen von MOF-Klassen (Managed Object Format).](designing-managed-object-format--mof--classes.md)
2.  Erstellen Und benennen Sie eine Instanz von [**\_ \_ EventFilter,**](--eventfilter.md)und erstellen Sie dann eine Abfrage, um den Ereignistyp anzugeben, der das Schreiben in das NT-Ereignisprotokoll auslöst.

    Weitere Informationen finden Sie unter [Abfragen mit WQL.](querying-with-wql.md)

3.  Erstellen Sie eine Instanz von [**\_ \_ FilterToConsumerBinding,**](--filtertoconsumerbinding.md) um den Filter der Instanz von [**NTEventLogEventConsumer**](nteventlogeventconsumer.md)zuzuordnen.
4.  Kompilieren Sie die MOF-Datei mithilfe [**Mofcomp.exe**](mofcomp.md).

## <a name="example"></a>Beispiel

Das Beispiel in diesem Abschnitt befindet sich im MOF-Code. Sie können die Instanzen jedoch programmgesteuert erstellen, indem Sie die [Skript-API für WMI](scripting-api-for-wmi.md) oder die [COM-API für WMI](com-api-for-wmi.md)verwenden. Das Beispiel zeigt, wie ein Consumer erstellt wird, um mit [**NTEventLogEventConsumer**](nteventlogeventconsumer.md)in das Anwendungsereignisprotokoll zu schreiben. Die MOF erstellt eine neue Klasse namens "NTLogCons \_ Example", einen Ereignisfilter zum Abfragen von Vorgängen wie der Erstellung für eine Instanz dieser neuen Klasse und eine Bindung zwischen Filter und Consumer. Da die letzte Aktion im MOF darin besteht, eine Instanz von NTLogCons Example zu \_ erstellen, können Sie das Ereignis sofort im Anwendungsereignisprotokoll anzeigen, indem Sie Eventvwr.exe ausführen.

Identifiziert `EventID=0x0A for SourceName="WinMgmt"` eine Nachricht mit dem folgenden Text. "%1", "%2", "%3" sind Platzhalter für entsprechende Zeichenfolgen, die im InsertionStringTemplates-Array angegeben sind.

``` syntax
Event filter with query "%2" could not be [re]activated in 
namespace "%1" because of error %3. Events may not be delivered 
through this filter until the problem is corrected.
```

Im folgenden Verfahren wird die Verwendung des Beispiels beschrieben.

**So verwenden Sie das Beispiel**

1.  Kopieren Sie die unten stehende MOF-Auflistung in eine Textdatei, und speichern Sie sie mit der Erweiterung MOF.
2.  Kompilieren Sie in einem Befehlsfenster die MOF-Datei mit dem folgenden Befehl:

     *Mofcomp-Dateiname}.mof**

3.  Führen Sie Eventvwr.exe aus. Sehen Sie sich das Anwendungsereignisprotokoll an. Es sollte ein Ereignis mit der ID = 10 **(eventID),** Source = "WMI" und Type = Error angezeigt werden.
4.  Doppelklicken Sie in der Spalte **Ereignis** auf die Meldung **Informationstyp** von WMI mit 10. Die folgende Beschreibung wird für das Ereignis angezeigt.

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

[Überwachen und Reagieren auf Ereignisse mit Standard-Consumern](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



