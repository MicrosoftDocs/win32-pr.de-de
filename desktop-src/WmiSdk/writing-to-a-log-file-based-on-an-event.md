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
# <a name="writing-to-a-log-file-based-on-an-event"></a><span data-ttu-id="ce614-104">Schreiben in eine Protokolldatei auf Grundlage eines Ereignisses</span><span class="sxs-lookup"><span data-stu-id="ce614-104">Writing to a Log File Based on an Event</span></span>

<span data-ttu-id="ce614-105">Die [**logfileeventconsumer**](logfileeventconsumer.md) -Klasse kann vordefinierten Text in eine Protokolldatei schreiben, wenn ein bestimmtes Ereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="ce614-105">The [**LogFileEventConsumer**](logfileeventconsumer.md) class can write predefined text to a log file when a specified event occurs.</span></span> <span data-ttu-id="ce614-106">Diese Klasse ist ein Standard Ereignisconsumer, den WMI bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="ce614-106">This class is a standard event consumer that WMI provides.</span></span>

<span data-ttu-id="ce614-107">Das grundlegende Verfahren für die Verwendung von Standardconsumern ist immer identisch und befindet sich in [Überwachung und Reaktion auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.</span><span class="sxs-lookup"><span data-stu-id="ce614-107">The basic procedure for using standard consumers is always the same, and is located in [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="ce614-108">Das folgende Verfahren fügt dem grundlegenden Verfahren, ist spezifisch für die [**logfileeventconsumer**](logfileeventconsumer.md) -Klasse, und beschreibt, wie ein Ereignisconsumer erstellt wird, der ein Programm ausführt.</span><span class="sxs-lookup"><span data-stu-id="ce614-108">The following procedure adds to the basic procedure, is specific to the [**LogFileEventConsumer**](logfileeventconsumer.md) class, and describes how to create an event consumer that runs a program.</span></span>

<span data-ttu-id="ce614-109">**So erstellen Sie einen Ereignisconsumer, der in eine Protokolldatei schreibt**</span><span class="sxs-lookup"><span data-stu-id="ce614-109">**To create an event consumer that writes to a log file**</span></span>

1.  <span data-ttu-id="ce614-110">Erstellen Sie in der MOF-Datei (Managed Object Format) eine Instanz von [**logfileeventconsumer**](logfileeventconsumer.md) , um die Ereignisse zu empfangen, die Sie in der Abfrage anfordern, benennen Sie die Instanz in der **Name** -Eigenschaft, und platzieren Sie dann den Pfad zur Protokolldatei in der **filename** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ce614-110">In the Managed Object Format (MOF) file, create an instance of [**LogFileEventConsumer**](logfileeventconsumer.md) to receive the events you request in the query, name the instance in the **Name** property, and then place the path to the log file in the **Filename** property.</span></span>

    <span data-ttu-id="ce614-111">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="ce614-111">For more information, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

2.  <span data-ttu-id="ce614-112">Stellen Sie die Textvorlage bereit, die in die Protokolldatei in der Text-Eigenschaft geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="ce614-112">Provide the text template to write to the log file in the Text property.</span></span>

    <span data-ttu-id="ce614-113">Weitere Informationen finden Sie unter [Verwenden von Standard Zeichenfolgen-Vorlagen](using-standard-string-templates.md).</span><span class="sxs-lookup"><span data-stu-id="ce614-113">For more information, see [Using Standard String Templates](using-standard-string-templates.md).</span></span>

3.  <span data-ttu-id="ce614-114">Erstellen Sie eine Instanz von [**\_ \_ EventFilter**](--eventfilter.md) , und definieren Sie eine Abfrage, um die Ereignisse anzugeben, die den Consumer aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ce614-114">Create an instance of [**\_\_EventFilter**](--eventfilter.md) and define a query to specify the events that will activate the consumer.</span></span>

    <span data-ttu-id="ce614-115">Weitere Informationen finden Sie unter [Abfragen mit WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="ce614-115">For more information, see [Querying with WQL](querying-with-wql.md).</span></span>

4.  <span data-ttu-id="ce614-116">Erstellen Sie eine Instanz von [**\_ \_ filtertoconsumerbinding**](--filtertoconsumerbinding.md) , um den Filter der Instanz von [**logfileeventconsumer**](logfileeventconsumer.md)zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="ce614-116">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter with the instance of [**LogFileEventConsumer**](logfileeventconsumer.md).</span></span>
5.  <span data-ttu-id="ce614-117">Legen Sie die Sicherheit für das Verzeichnis, in dem sich das Protokoll befindet, auf die erforderliche Ebene fest, um zu steuern, wer die Protokolldatei liest oder in diese schreibt.</span><span class="sxs-lookup"><span data-stu-id="ce614-117">To control who reads or writes to your log file, set the security on the directory where the log is located to the required level.</span></span>
6.  <span data-ttu-id="ce614-118">Kompilieren Sie die MOF-Datei mit [**Mofcomp.exe**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="ce614-118">Compile your MOF file using [**Mofcomp.exe**](mofcomp.md).</span></span>

## <a name="example"></a><span data-ttu-id="ce614-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ce614-119">Example</span></span>

<span data-ttu-id="ce614-120">Das Beispiel in diesem Abschnitt ist ein MOF-Code, aber Sie können die Instanzen Programm gesteuert mithilfe der [Skript-API für WMI](scripting-api-for-wmi.md) oder der [com-API für WMI](com-api-for-wmi.md)erstellen.</span><span class="sxs-lookup"><span data-stu-id="ce614-120">The example in this section is in MOF code, but you can create the instances programmatically by using the [Scripting API for WMI](scripting-api-for-wmi.md) or the [COM API for WMI](com-api-for-wmi.md).</span></span> <span data-ttu-id="ce614-121">Das Beispiel verwendet den logfileeventconsumer Standard, um eine Consumerklasse mit dem Namen logfileevent zu erstellen, die eine Zeile in die Datei c: \\ logfile. Log schreibt, wenn eine Instanz der Klasse logfileevent erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ce614-121">The example uses the standard LogFileEventConsumer to create a consumer class named LogFileEvent that writes a line to the file c:\\Logfile.log when an instance of the class LogFileEvent is created.</span></span>

<span data-ttu-id="ce614-122">Im folgenden Verfahren wird beschrieben, wie das Beispiel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ce614-122">The following procedure describes how to use the example.</span></span>

<span data-ttu-id="ce614-123">**So verwenden Sie das Beispiel**</span><span class="sxs-lookup"><span data-stu-id="ce614-123">**To use the example**</span></span>

1.  <span data-ttu-id="ce614-124">Kopieren Sie das unten aufgeführte MOF-Listenfeld in eine Textdatei, und speichern Sie es mit der Erweiterung MOF.</span><span class="sxs-lookup"><span data-stu-id="ce614-124">Copy the MOF listing below into a text file and save it with a .mof extension.</span></span>
2.  <span data-ttu-id="ce614-125">Kompilieren Sie die MOF-Datei in einem Befehlsfenster mit dem folgenden Befehl.</span><span class="sxs-lookup"><span data-stu-id="ce614-125">In a command window, compile the MOF file by using the following command.</span></span>

    <span data-ttu-id="ce614-126">" **Mamacomp** *filename \* \* *. MOF* "*</span><span class="sxs-lookup"><span data-stu-id="ce614-126">**Mofcomp** *filename\*\*\*.mof*\*</span></span>

3.  <span data-ttu-id="ce614-127">Öffnen Sie Logfile. log, um die durch LogFileEvent.Name angegebene Zeile anzuzeigen: "Logfile ereignisconsumerereignis".</span><span class="sxs-lookup"><span data-stu-id="ce614-127">Open Logfile.log to see the line specified by LogFileEvent.Name: "Logfile Event Consumer event".</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="ce614-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ce614-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce614-129">Überwachen von und reagieren auf Ereignisse mit Standard Consumern</span><span class="sxs-lookup"><span data-stu-id="ce614-129">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



