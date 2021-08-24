---
description: Die LogFileEventConsumer-Klasse kann vordefinierten Text in eine Protokolldatei schreiben, wenn ein angegebenes Ereignis auftritt. Diese Klasse ist ein Standardereignis-Consumer, den WMI bietet.
ms.assetid: c337e9f7-f40c-4d7d-a180-c053e24c882b
ms.tgt_platform: multiple
title: Schreiben in eine Protokolldatei basierend auf einem Ereignis
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 881435986a1097c2ba97160693ed15e28bae3d86019fb703adf6bf1e8b07f8a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049728"
---
# <a name="writing-to-a-log-file-based-on-an-event"></a>Schreiben in eine Protokolldatei basierend auf einem Ereignis

Die [**LogFileEventConsumer-Klasse**](logfileeventconsumer.md) kann vordefinierten Text in eine Protokolldatei schreiben, wenn ein angegebenes Ereignis auftritt. Diese Klasse ist ein Standardereignis-Consumer, den WMI bietet.

Das grundlegende Verfahren für die Verwendung von Standardverbrauchern ist immer identisch und befindet sich unter Überwachung und Reaktion auf Ereignisse [mit Standardverbrauchern.](monitoring-and-responding-to-events-with-standard-consumers.md)

Die folgende Prozedur fügt der grundlegenden Prozedur hinzu, ist spezifisch für die [**LogFileEventConsumer-Klasse**](logfileeventconsumer.md) und beschreibt, wie ein Ereignisconsumer erstellt wird, der ein Programm ausgeführt.

**So erstellen Sie einen Ereignisverbraucher, der in eine Protokolldatei schreibt**

1.  Erstellen Sie in der MOF-Datei (Managed Object Format) eine Instanz von [**LogFileEventConsumer,**](logfileeventconsumer.md) um die ereignisse zu empfangen, die Sie in der Abfrage anfordern, benennen Sie die Instanz in der **Name-Eigenschaft,** und platzieren Sie dann den Pfad zur Protokolldatei in der **Filename-Eigenschaft.**

    Weitere Informationen finden Sie unter [Entwerfen Managed Object Format -Klassen (MOF).](designing-managed-object-format--mof--classes.md)

2.  Geben Sie die Textvorlage an, die in die Protokolldatei in der Text-Eigenschaft geschrieben werden soll.

    Weitere Informationen finden Sie unter [Verwenden von Standardzeichenfolgenvorlagen.](using-standard-string-templates.md)

3.  Erstellen Sie eine Instanz von [**\_ \_ EventFilter, und**](--eventfilter.md) definieren Sie eine Abfrage, um die Ereignisse anzugeben, die den Consumer aktivieren.

    Weitere Informationen finden Sie unter [Abfragen mit WQL.](querying-with-wql.md)

4.  Erstellen Sie eine Instanz von [**\_ \_ FilterToConsumerBinding,**](--filtertoconsumerbinding.md) um den Filter der Instanz von [**LogFileEventConsumer zu zuordnen.**](logfileeventconsumer.md)
5.  Um zu steuern, wer die Protokolldatei liest oder schreibt, legen Sie die Sicherheit für das Verzeichnis, in dem sich das Protokoll befindet, auf die erforderliche Ebene fest.
6.  Kompilieren Sie ihre MOF-Datei [**mitMofcomp.exe**](mofcomp.md).

## <a name="example"></a>Beispiel

Das Beispiel in diesem Abschnitt befindet sich im MOF-Code, aber Sie können die Instanzen programmgesteuert erstellen, indem Sie die [Skript-API](scripting-api-for-wmi.md) für WMI oder die [COM-API für WMI verwenden.](com-api-for-wmi.md) Im Beispiel wird der LogFileEventConsumer-Standard verwendet, um eine Consumerklasse namens LogFileEvent zu erstellen, die eine Zeile in die Datei c: Logfile.log schreibt, wenn eine Instanz der \\ Klasse LogFileEvent erstellt wird.

Im folgenden Verfahren wird die Verwendung des Beispiels beschrieben.

**So verwenden Sie das Beispiel**

1.  Kopieren Sie die mof-Auflistung unten in eine Textdatei, und speichern Sie sie mit der Erweiterung MOF.
2.  Kompilieren Sie die MOF-Datei in einem Befehlsfenster mit dem folgenden Befehl.

     *Mofcomp-Dateiname**.mof**

3.  Öffnen Sie Logfile.log, um die zeile zu sehen, die von LogFileEvent.Name" angegeben wird: "Logfile Event Consumer event".

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

[Überwachen und Reagieren auf Ereignisse mit Standardverbrauchern](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



