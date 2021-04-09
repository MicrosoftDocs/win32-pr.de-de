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
# <a name="logging-to-nt-event-log-based-on-an-event"></a><span data-ttu-id="6bccc-104">Protokollierung in NT-Ereignisprotokoll basierend auf einem Ereignis</span><span class="sxs-lookup"><span data-stu-id="6bccc-104">Logging to NT Event Log Based on an Event</span></span>

<span data-ttu-id="6bccc-105">Die [**nteventlogeventconsumer**](nteventlogeventconsumer.md) -Klasse schreibt eine Meldung in das Windows-Ereignisprotokoll, wenn ein bestimmtes Ereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="6bccc-105">The [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) class writes a message to the Windows Event log when a specified event occurs.</span></span> <span data-ttu-id="6bccc-106">Diese Klasse ist ein Standard Ereignisconsumer, den WMI bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="6bccc-106">This class is a standard event consumer that WMI provides.</span></span>

> [!Note]  
> <span data-ttu-id="6bccc-107">Authentifizierte Benutzer können Ereignisse standardmäßig nicht im Anwendungsprotokoll auf einem Remote Computer protokollieren.</span><span class="sxs-lookup"><span data-stu-id="6bccc-107">Authenticated users cannot, by default, log events to the Application log on a remote computer.</span></span> <span data-ttu-id="6bccc-108">Das in diesem Thema beschriebene Beispiel schlägt daher fehl, wenn Sie die **uncservername** -Eigenschaft der [**nteventlogeventconsumer**](nteventlogeventconsumer.md) -Klasse verwenden und einen Remote Computer als Wert angeben.</span><span class="sxs-lookup"><span data-stu-id="6bccc-108">As a result, the example described in this topic will fail if you use the **UNCServerName** property of the [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) class and specify a remote computer as its value.</span></span> <span data-ttu-id="6bccc-109">Weitere Informationen zum Ändern der Ereignisprotokoll Sicherheit finden Sie in diesem [KB-Artikel](https://support.microsoft.com/kb/323076).</span><span class="sxs-lookup"><span data-stu-id="6bccc-109">To learn how to change event log security, consult this [KB article](https://support.microsoft.com/kb/323076).</span></span>

 

<span data-ttu-id="6bccc-110">Das grundlegende Verfahren für die Verwendung eines standardconsumers wird unter über [wachen und reagieren auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6bccc-110">The basic procedure for using a standard consumer is described in [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span> <span data-ttu-id="6bccc-111">Im folgenden finden Sie zusätzliche Schritte, die über das grundlegende Verfahren hinausgehen, das bei Verwendung der [**nteventlogeventconsumer**](nteventlogeventconsumer.md) -Klasse erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="6bccc-111">The following are additional steps beyond the basic procedure, required when using the [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) class.</span></span> <span data-ttu-id="6bccc-112">In den Schritten wird beschrieben, wie Sie einen Ereignisconsumer erstellen, der in das Anwendungs Ereignisprotokoll schreibt.</span><span class="sxs-lookup"><span data-stu-id="6bccc-112">The steps describe how to create an event consumer that writes to the Application event log.</span></span>

<span data-ttu-id="6bccc-113">Im folgenden Verfahren wird beschrieben, wie Sie einen Ereignisconsumer erstellen, der in das NT-Ereignisprotokoll schreibt.</span><span class="sxs-lookup"><span data-stu-id="6bccc-113">The following procedure describes how to create an event consumer that writes to the NT Event Log.</span></span>

<span data-ttu-id="6bccc-114">**So erstellen Sie einen Ereignisconsumer, der in das Windows-Ereignisprotokoll schreibt**</span><span class="sxs-lookup"><span data-stu-id="6bccc-114">**To create an event consumer that writes to the Windows Event Log**</span></span>

1.  <span data-ttu-id="6bccc-115">Erstellen Sie in einer MOF-Datei (Managed Object Format) eine Instanz von [**nteventlogeventconsumer**](nteventlogeventconsumer.md) , um die Ereignisse zu empfangen, die Sie in der Abfrage anfordern.</span><span class="sxs-lookup"><span data-stu-id="6bccc-115">In a Managed Object Format (MOF) file, create an instance of [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) to receive the events you request in the query.</span></span> <span data-ttu-id="6bccc-116">Weitere Informationen zum Schreiben von MOF-Code finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="6bccc-116">For more information about writing MOF code, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>
2.  <span data-ttu-id="6bccc-117">Erstellen Sie eine Instanz von [**\_ \_ EventFilter**](--eventfilter.md), und benennen Sie Sie, und erstellen Sie dann eine Abfrage, um den Ereignistyp anzugeben, der von das Schreiben in das NT-Ereignisprotokoll auslöst.</span><span class="sxs-lookup"><span data-stu-id="6bccc-117">Create, and name, an instance of [**\_\_EventFilter**](--eventfilter.md), and then create a query to specify the type of event which triggers writing to the NT Event Log.</span></span>

    <span data-ttu-id="6bccc-118">Weitere Informationen finden Sie unter [Abfragen mit WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="6bccc-118">For more information see, [Querying with WQL](querying-with-wql.md).</span></span>

3.  <span data-ttu-id="6bccc-119">Erstellen Sie eine Instanz von [**\_ \_ filtertoconsumerbinding**](--filtertoconsumerbinding.md) , um den Filter der Instanz von [**nteventlogeventconsumer**](nteventlogeventconsumer.md)zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="6bccc-119">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter with the instance of [**NTEventLogEventConsumer**](nteventlogeventconsumer.md).</span></span>
4.  <span data-ttu-id="6bccc-120">Kompilieren Sie die MOF-Datei mit [**Mofcomp.exe**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="6bccc-120">Compile the MOF file by using [**Mofcomp.exe**](mofcomp.md).</span></span>

## <a name="example"></a><span data-ttu-id="6bccc-121">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6bccc-121">Example</span></span>

<span data-ttu-id="6bccc-122">Das Beispiel in diesem Abschnitt ist ein MOF-Code, aber Sie können die Instanzen Programm gesteuert mithilfe der [Skript-API für WMI](scripting-api-for-wmi.md) oder der [com-API für WMI](com-api-for-wmi.md)erstellen.</span><span class="sxs-lookup"><span data-stu-id="6bccc-122">The example in this section is in MOF code, but you can create the instances programmatically by using the [Scripting API for WMI](scripting-api-for-wmi.md) or the [COM API for WMI](com-api-for-wmi.md).</span></span> <span data-ttu-id="6bccc-123">Das Beispiel zeigt, wie ein Consumer erstellt wird, um mithilfe von [**nteventlogeventconsumer**](nteventlogeventconsumer.md)in das Anwendungs Ereignisprotokoll zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="6bccc-123">The example shows how to create a consumer to write to the Application event log by using [**NTEventLogEventConsumer**](nteventlogeventconsumer.md).</span></span> <span data-ttu-id="6bccc-124">Das MOF erstellt eine neue Klasse mit dem Namen "ntlogcons \_ example", einen Ereignis Filter zum Abfragen von Vorgängen, z. b. die Erstellung, eine Instanz dieser neuen Klasse und eine Bindung zwischen Filter und Consumer.</span><span class="sxs-lookup"><span data-stu-id="6bccc-124">The MOF creates a new class named "NTLogCons\_Example", an event filter to query for operations, such as creation, on an instance of this new class, and a binding between filter and consumer.</span></span> <span data-ttu-id="6bccc-125">Da die letzte Aktion in der MOF-Datei das Erstellen einer Instanz des ntlogcons- \_ Beispiels ist, können Sie das Ereignis sofort im Anwendungs Ereignisprotokoll sehen, indem Sie Eventvwr.exe ausführen.</span><span class="sxs-lookup"><span data-stu-id="6bccc-125">Because the last action in the MOF is to create an instance of NTLogCons\_Example, you can immediately see the event in the Application event log by running Eventvwr.exe.</span></span>

<span data-ttu-id="6bccc-126">Der `EventID=0x0A for SourceName="WinMgmt"` identifiziert eine Meldung mit dem folgenden Text.</span><span class="sxs-lookup"><span data-stu-id="6bccc-126">The `EventID=0x0A for SourceName="WinMgmt"` identifies a message with the following text.</span></span> <span data-ttu-id="6bccc-127">"%1", "%2", "%3", sind Platzhalter für entsprechende Zeichen folgen, die im insertionstringtemplates-Array angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="6bccc-127">The "%1", "%2", "%3" are placeholders for corresponding strings specified in InsertionStringTemplates array.</span></span>

``` syntax
Event filter with query "%2" could not be [re]activated in 
namespace "%1" because of error %3. Events may not be delivered 
through this filter until the problem is corrected.
```

<span data-ttu-id="6bccc-128">Im folgenden Verfahren wird beschrieben, wie das Beispiel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6bccc-128">The following procedure describes how to use the example.</span></span>

<span data-ttu-id="6bccc-129">**So verwenden Sie das Beispiel**</span><span class="sxs-lookup"><span data-stu-id="6bccc-129">**To use the example**</span></span>

1.  <span data-ttu-id="6bccc-130">Kopieren Sie das unten aufgeführte MOF-Listenfeld in eine Textdatei, und speichern Sie es mit der Erweiterung MOF.</span><span class="sxs-lookup"><span data-stu-id="6bccc-130">Copy the MOF listing below into a text file and save it with a .mof extension.</span></span>
2.  <span data-ttu-id="6bccc-131">Kompilieren Sie in einem Befehlsfenster die MOF-Datei mit dem folgenden Befehl:</span><span class="sxs-lookup"><span data-stu-id="6bccc-131">In a Command window, compile the MOF file by using the following command:</span></span>

    <span data-ttu-id="6bccc-132">" **Mamacomp** *filename \* \* *. MOF* "*</span><span class="sxs-lookup"><span data-stu-id="6bccc-132">**Mofcomp** *filename\*\*\*.mof*\*</span></span>

3.  <span data-ttu-id="6bccc-133">Führen Sie Eventvwr.exe aus.</span><span class="sxs-lookup"><span data-stu-id="6bccc-133">Run Eventvwr.exe.</span></span> <span data-ttu-id="6bccc-134">Sehen Sie sich das Anwendungs Ereignisprotokoll an.</span><span class="sxs-lookup"><span data-stu-id="6bccc-134">Look at the Application event log.</span></span> <span data-ttu-id="6bccc-135">Es sollte ein Ereignis mit der ID = 10 ( **EventID**), Source = "WMI" und Type = Error angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6bccc-135">You should see an event with ID = 10 (the **EventID**), Source = "WMI", and Type = Error.</span></span>
4.  <span data-ttu-id="6bccc-136">Doppelklicken Sie in der Spalte **Ereignis** auf die **Information Type** -Meldung von WMI mit 10.</span><span class="sxs-lookup"><span data-stu-id="6bccc-136">Double-click the **Information type** message from WMI with 10 in the **Event** column.</span></span> <span data-ttu-id="6bccc-137">Die folgende Beschreibung wird für das-Ereignis angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6bccc-137">The following description will be displayed for the event.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="6bccc-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6bccc-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6bccc-139">Überwachen von und reagieren auf Ereignisse mit Standard Consumern</span><span class="sxs-lookup"><span data-stu-id="6bccc-139">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



