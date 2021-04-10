---
description: Die logfileeventconsumer-Klasse kann vordefinierten Text in eine Protokolldatei schreiben, wenn ein bestimmtes Ereignis auftritt. Diese Klasse ist ein Standard Ereignisconsumer, den WMI bereitstellt.
ms.assetid: c337e9f7-f40c-4d7d-a180-c053e24c882b
ms.tgt_platform: multiple
title: Schreiben in eine Protokolldatei auf Grundlage eines Ereignisses
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 33cc82925b6afc1690f2cd87607f21e9ea02fdbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215437"
---
# <a name="writing-to-a-log-file-based-on-an-event"></a>Schreiben in eine Protokolldatei auf Grundlage eines Ereignisses

Die [**logfileeventconsumer**](logfileeventconsumer.md) -Klasse kann vordefinierten Text in eine Protokolldatei schreiben, wenn ein bestimmtes Ereignis auftritt. Diese Klasse ist ein Standard Ereignisconsumer, den WMI bereitstellt.

Das grundlegende Verfahren für die Verwendung von Standardconsumern ist immer identisch und befindet sich in [Überwachung und Reaktion auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.

Das folgende Verfahren fügt dem grundlegenden Verfahren, ist spezifisch für die [**logfileeventconsumer**](logfileeventconsumer.md) -Klasse, und beschreibt, wie ein Ereignisconsumer erstellt wird, der ein Programm ausführt.

**So erstellen Sie einen Ereignisconsumer, der in eine Protokolldatei schreibt**

1.  Erstellen Sie in der MOF-Datei (Managed Object Format) eine Instanz von [**logfileeventconsumer**](logfileeventconsumer.md) , um die Ereignisse zu empfangen, die Sie in der Abfrage anfordern, benennen Sie die Instanz in der **Name** -Eigenschaft, und platzieren Sie dann den Pfad zur Protokolldatei in der **filename** -Eigenschaft.

    Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](designing-managed-object-format--mof--classes.md).

2.  Stellen Sie die Textvorlage bereit, die in die Protokolldatei in der Text-Eigenschaft geschrieben werden soll.

    Weitere Informationen finden Sie unter [Verwenden von Standard Zeichenfolgen-Vorlagen](using-standard-string-templates.md).

3.  Erstellen Sie eine Instanz von [**\_ \_ EventFilter**](--eventfilter.md) , und definieren Sie eine Abfrage, um die Ereignisse anzugeben, die den Consumer aktivieren.

    Weitere Informationen finden Sie unter [Abfragen mit WQL](querying-with-wql.md).

4.  Erstellen Sie eine Instanz von [**\_ \_ filtertoconsumerbinding**](--filtertoconsumerbinding.md) , um den Filter der Instanz von [**logfileeventconsumer**](logfileeventconsumer.md)zuzuordnen.
5.  Legen Sie die Sicherheit für das Verzeichnis, in dem sich das Protokoll befindet, auf die erforderliche Ebene fest, um zu steuern, wer die Protokolldatei liest oder in diese schreibt.
6.  Kompilieren Sie die MOF-Datei mit [**Mofcomp.exe**](mofcomp.md).

## <a name="example"></a>Beispiel

Das Beispiel in diesem Abschnitt ist ein MOF-Code, aber Sie können die Instanzen Programm gesteuert mithilfe der [Skript-API für WMI](scripting-api-for-wmi.md) oder der [com-API für WMI](com-api-for-wmi.md)erstellen. Das Beispiel verwendet den logfileeventconsumer Standard, um eine Consumerklasse mit dem Namen logfileevent zu erstellen, die eine Zeile in die Datei c: \\ logfile. Log schreibt, wenn eine Instanz der Klasse logfileevent erstellt wird.

Im folgenden Verfahren wird beschrieben, wie das Beispiel verwendet wird.

**So verwenden Sie das Beispiel**

1.  Kopieren Sie das unten aufgeführte MOF-Listenfeld in eine Textdatei, und speichern Sie es mit der Erweiterung MOF.
2.  Kompilieren Sie die MOF-Datei in einem Befehlsfenster mit dem folgenden Befehl.

    " **Mamacomp** *filename * * *. MOF* "*

3.  Öffnen Sie Logfile. log, um die durch LogFileEvent.Name angegebene Zeile anzuzeigen: "Logfile ereignisconsumerereignis".

``` syntax
// Set the namespace as root\subscription.
// The LogFileEventConsumer is already compiled 
//     in the root\subscription namespace. 

#pragma namespace ("\\\\.\\Root\\subscription")

class LogFileEvent
{
    [key]string Name;
};

// Create an instance of the standard log
// file consumer and give it the alias $CONSUMER

instance of LogFileEventConsumer as $CONSUMER
{
    // If the file does not already exist, it is created.
    Filename = "c:\\Logfile.log";  
    IsUnicode = FALSE;
    // Name of this instance of LogFileEventConsumer
    Name = "LogfileEventConsumer_Example";  
    // See "Using Standard String Templates"; 
    Text = "%TargetInstance.Name%"; 
    // TargetInstance is the instance of LogFileEvent 
    //    requested in the filter        
                                         
};

// Create an instance of the event filter 
// and give it the alias $FILTER
// Query for any instance operation type,
// such as instance creation, for LogFileEvent class

instance of __EventFilter as $FILTER
{
    Name = "LogFileFilter";
    Query = "SELECT * FROM __InstanceOperationEvent "
        "WHERE TargetInstance.__class = \"LogFileEvent\"";
    QueryLanguage = "WQL";
};

// Create an instance of the binding.

instance of __FilterToConsumerBinding
{
    Consumer=$CONSUMER;
    Filter=$FILTER;
 DeliverSynchronously=FALSE;
};

// Create an instance of this class right now
// Look at the file c:\Logfile.log to see
// that a line has been written.

instance of LogFileEvent
{
 Name = "Logfile Event Consumer event";  
};
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Überwachen von und reagieren auf Ereignisse mit Standard Consumern](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



