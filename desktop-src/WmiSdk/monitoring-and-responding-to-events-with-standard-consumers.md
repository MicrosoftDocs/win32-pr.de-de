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
# <a name="monitoring-and-responding-to-events-with-standard-consumers"></a><span data-ttu-id="81c04-103">Überwachen von und reagieren auf Ereignisse mit Standard Consumern</span><span class="sxs-lookup"><span data-stu-id="81c04-103">Monitoring and Responding to Events with Standard Consumers</span></span>

<span data-ttu-id="81c04-104">Sie können die installierten [Standard Consumerklassen](standard-consumer-classes.md) verwenden, um Aktionen auf der Grundlage von Ereignissen in einem Betriebssystem auszuführen.</span><span class="sxs-lookup"><span data-stu-id="81c04-104">You can use the installed [standard consumer classes](standard-consumer-classes.md) to perform actions based on events in an operating system.</span></span> <span data-ttu-id="81c04-105">Standard Consumer sind einfache Klassen, die bereits registriert sind und permanente Consumerklassen definieren.</span><span class="sxs-lookup"><span data-stu-id="81c04-105">Standard consumers are simple classes that are already registered, and they define permanent consumer classes.</span></span> <span data-ttu-id="81c04-106">Jeder Standard Consumer nimmt eine bestimmte Aktion vor, nachdem er eine Ereignis Benachrichtigung erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="81c04-106">Each standard consumer takes a specific action after it receives an event notification.</span></span> <span data-ttu-id="81c04-107">Beispielsweise können Sie eine Instanz von [**activescripteventconsumer**](activescripteventconsumer.md) definieren, um ein Skript auszuführen, wenn der freie Speicherplatz auf einem Computer von einer angegebenen Größe abweicht.</span><span class="sxs-lookup"><span data-stu-id="81c04-107">For example, you can define an instance of [**ActiveScriptEventConsumer**](activescripteventconsumer.md) to execute a script when free disk space on a computer is different from a specified size.</span></span>

<span data-ttu-id="81c04-108">WMI kompiliert die Standardconsumer in Standardnamespaces, die vom Betriebssystem abhängig sind, z. b.:</span><span class="sxs-lookup"><span data-stu-id="81c04-108">WMI compiles the standard consumers into default namespaces that depend on the operating system, for example:</span></span>

-   <span data-ttu-id="81c04-109">In Windows Server 2003 werden standardmäßig alle Standard Consumer in den Namespace "root- \\ Abonnement" kompiliert.</span><span class="sxs-lookup"><span data-stu-id="81c04-109">In Windows Server 2003, all of the standard consumers are compiled by default into the "Root\\Subscription" namespace.</span></span>

> [!Note]  
> <span data-ttu-id="81c04-110">Informationen zu den Standardnamespaces und Betriebssystemen, die für die einzelnen WMI-klassenspezifisch sind, finden Sie in den Abschnitten "Hinweise und Anforderungen" der einzelnen Klassen Themen.</span><span class="sxs-lookup"><span data-stu-id="81c04-110">For the default namespaces and operating systems that are specific for each WMI class, see the Remarks and Requirements sections of each class topic.</span></span>

 

<span data-ttu-id="81c04-111">In der folgenden Tabelle werden die WMI-Standardconsumer aufgelistet und beschrieben.</span><span class="sxs-lookup"><span data-stu-id="81c04-111">The following table lists and describes the WMI standard consumers.</span></span>



| <span data-ttu-id="81c04-112">Standard Consumer</span><span class="sxs-lookup"><span data-stu-id="81c04-112">Standard consumer</span></span>                                              | <span data-ttu-id="81c04-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="81c04-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="81c04-114">**Activescripteventconsumer**</span><span class="sxs-lookup"><span data-stu-id="81c04-114">**ActiveScriptEventConsumer**</span></span>](activescripteventconsumer.md) | <span data-ttu-id="81c04-115">Führt ein Skript aus, wenn eine Ereignis Benachrichtigung empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="81c04-115">Executes a script when it receives an event notification.</span></span> <span data-ttu-id="81c04-116">Weitere Informationen finden Sie unter [Ausführen eines Skripts auf der Grundlage eines Ereignisses](running-a-script-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="81c04-116">For more information, see [Running a Script Based on an Event](running-a-script-based-on-an-event.md).</span></span>                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="81c04-117">**Logfileeventconsumer**</span><span class="sxs-lookup"><span data-stu-id="81c04-117">**LogFileEventConsumer**</span></span>](logfileeventconsumer.md)           | <span data-ttu-id="81c04-118">Schreibt angepasste Zeichen folgen in eine Text Protokolldatei, wenn eine Ereignis Benachrichtigung empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="81c04-118">Writes customized strings to a text log file when it receives an event notification.</span></span> <span data-ttu-id="81c04-119">Weitere Informationen finden Sie unter [Schreiben in eine Protokolldatei auf Grundlage eines Ereignisses](writing-to-a-log-file-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="81c04-119">For more information, see [Writing to a Log File Based on an Event](writing-to-a-log-file-based-on-an-event.md).</span></span>                                                                                                                                                                                                                  |
| [<span data-ttu-id="81c04-120">**Nteventlogeventconsumer**</span><span class="sxs-lookup"><span data-stu-id="81c04-120">**NTEventLogEventConsumer**</span></span>](nteventlogeventconsumer.md)     | <span data-ttu-id="81c04-121">Protokolliert eine bestimmte Meldung im Anwendungs Ereignisprotokoll.</span><span class="sxs-lookup"><span data-stu-id="81c04-121">Logs a specific message to the Application event log.</span></span> <span data-ttu-id="81c04-122">Weitere Informationen finden Sie unter [Protokollierung in NT-Ereignisprotokoll basierend auf einem Ereignis](logging-to-nt-event-log-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="81c04-122">For more information, see [Logging to NT Event Log Based on an Event](logging-to-nt-event-log-based-on-an-event.md).</span></span>                                                                                                                                                                                                                                             |
| [<span data-ttu-id="81c04-123">**Smtpeer-Consumer**</span><span class="sxs-lookup"><span data-stu-id="81c04-123">**SMTPEventConsumer**</span></span>](smtpeventconsumer.md)                 | <span data-ttu-id="81c04-124">Sendet bei jedem übermitteln eines Ereignisses eine e-Mail-Nachricht mithilfe von SMTP.</span><span class="sxs-lookup"><span data-stu-id="81c04-124">Sends an email message by using SMTP each time an event is delivered to it.</span></span> <span data-ttu-id="81c04-125">Weitere Informationen finden Sie unter [Senden von e-Mails auf der Grundlage eines Ereignisses](sending-e-mail-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="81c04-125">For more information, see [Sending Email Based on an Event](sending-e-mail-based-on-an-event.md).</span></span>                                                                                                                                                                                                                                          |
| [<span data-ttu-id="81c04-126">**Commandlineeventconsumer**</span><span class="sxs-lookup"><span data-stu-id="81c04-126">**CommandLineEventConsumer**</span></span>](commandlineeventconsumer.md)   | <span data-ttu-id="81c04-127">Hiermit wird ein Prozess gestartet, wenn ein Ereignis an ein lokales System übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="81c04-127">Launches a process when an event is delivered to a local system.</span></span> <span data-ttu-id="81c04-128">Die ausführbare Datei muss sich an einem sicheren Speicherort befinden oder mit einer starken Zugriffs Steuerungs Liste (ACL) gesichert werden, um zu verhindern, dass nicht autorisierte Benutzer ihre ausführbare Datei durch eine andere ausführbare Datei ersetzen.</span><span class="sxs-lookup"><span data-stu-id="81c04-128">The executable file must be in a secure location, or secured with a strong access control list (ACL) to prevent an unauthorized user from replacing your executable with a different executable.</span></span> <span data-ttu-id="81c04-129">Weitere Informationen finden Sie unter [Ausführen eines Programms in der Befehlszeile auf der Grundlage eines Ereignisses](running-a-program-from-the-command-line-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="81c04-129">For more information, see [Running a Program from the Command Line Based on an Event](running-a-program-from-the-command-line-based-on-an-event.md).</span></span> |



 

<span data-ttu-id="81c04-130">Im folgenden Verfahren wird beschrieben, wie Sie Ereignisse mithilfe eines standardconsumers überwachen und darauf reagieren.</span><span class="sxs-lookup"><span data-stu-id="81c04-130">The following procedure describes how to monitor and respond to events by using a standard consumer.</span></span> <span data-ttu-id="81c04-131">Beachten Sie, dass die Prozedur für eine Managed Object Format (MOF)-Datei, ein Skript oder eine Anwendung identisch ist.</span><span class="sxs-lookup"><span data-stu-id="81c04-131">Note that the procedure is the same for a Managed Object Format (MOF) file, script, or application.</span></span>

<span data-ttu-id="81c04-132">**So überwachen Sie Ereignisse mit einem Standard Consumer und reagieren darauf**</span><span class="sxs-lookup"><span data-stu-id="81c04-132">**To monitor and respond to events with a standard consumer**</span></span>

1.  <span data-ttu-id="81c04-133">Geben Sie den Namespace in einer MOF-Datei mit dem MOF-Präprozessorbefehl- [ \# pragma-Namespace](pragma-namespace.md)an.</span><span class="sxs-lookup"><span data-stu-id="81c04-133">Specify the namespace in a MOF file by using the MOF preprocessor command [\#pragma namespace](pragma-namespace.md).</span></span> <span data-ttu-id="81c04-134">Geben Sie in einem Skript oder einer Anwendung den Namespace im Code an, der eine Verbindung mit WMI herstellt.</span><span class="sxs-lookup"><span data-stu-id="81c04-134">In a script or application, specify the namespace in the code that connects to WMI.</span></span>

    <span data-ttu-id="81c04-135">Im folgenden MOF-Codebeispiel wird gezeigt, wie der \\ Namespace des Stamm Abonnements angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="81c04-135">The following MOF code example shows how to specify the root\\subscription namespace.</span></span>

    ```syntax
    #pragma namespace ("\\\\.\\root\\subscription")
    ```

    <span data-ttu-id="81c04-136">Die meisten systeminternen [*Ereignisse*](gloss-i.md) werden Änderungen an Klassen Instanzen im root \\ CIMV2-Namespace zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="81c04-136">Most [*intrinsic events*](gloss-i.md) are associated with changes to class instances in the root\\cimv2 namespace.</span></span> <span data-ttu-id="81c04-137">Registrierungs Ereignisse, wie z. b. [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) , werden jedoch \\ vom [System Registrierungs Anbieter](/previous-versions/windows/desktop/regprov/system-registry-provider)im Stamm-Standard Namespace ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="81c04-137">However, registry events such as [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) are fired in the root\\default namespace by the [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider).</span></span>

    <span data-ttu-id="81c04-138">Ein Consumer kann in anderen Namespaces befindliche Ereignis Klassen einschließen, indem er in der [**\_ \_ EventFilter**](--eventfilter.md) -Abfrage für Ereignisse den Namespace in der **eventnamespace** -Eigenschaft angibt.</span><span class="sxs-lookup"><span data-stu-id="81c04-138">A consumer can include event classes located in other namespaces by specifying the namespace in the **EventNamespace** property in the [**\_\_EventFilter**](--eventfilter.md) query for events.</span></span> <span data-ttu-id="81c04-139">Die systeminternen [*Ereignis*](gloss-i.md) Klassen, z. b. [**\_ \_ instanceoperationevent**](--instanceoperationevent.md) , sind in jedem Namespace verfügbar.</span><span class="sxs-lookup"><span data-stu-id="81c04-139">The [*intrinsic events*](gloss-i.md) classes, such as [**\_\_InstanceOperationEvent**](--instanceoperationevent.md) are available in every namespace.</span></span>

2.  <span data-ttu-id="81c04-140">Erstellen Sie eine Instanz einer standardconsumerklasse, und füllen Sie Sie auf.</span><span class="sxs-lookup"><span data-stu-id="81c04-140">Create and populate an instance of a standard consumer class.</span></span>

    <span data-ttu-id="81c04-141">Diese Instanz kann einen eindeutigen Wert in der **Name** -Eigenschaft aufweisen.</span><span class="sxs-lookup"><span data-stu-id="81c04-141">This instance may have a unique value in the **Name** property.</span></span> <span data-ttu-id="81c04-142">Sie können einen vorhandenen Consumer aktualisieren, indem Sie denselben Namen wieder verwenden.</span><span class="sxs-lookup"><span data-stu-id="81c04-142">You can update an existing consumer by reusing the same name.</span></span>

    <span data-ttu-id="81c04-143">**Insertionstringtemplates** enthält den Text, der in ein Ereignis eingefügt werden soll, das Sie in **eventType** angeben.</span><span class="sxs-lookup"><span data-stu-id="81c04-143">**InsertionStringTemplates** contains the text to insert in an event that you specify in **EventType**.</span></span> <span data-ttu-id="81c04-144">Sie können Literalzeichenfolgen verwenden oder direkt auf eine Eigenschaft verweisen.</span><span class="sxs-lookup"><span data-stu-id="81c04-144">You can use literal strings or refer directly to a property.</span></span> <span data-ttu-id="81c04-145">Weitere Informationen finden Sie unter [Verwenden von Standard Zeichenfolgen-Vorlagen](using-standard-string-templates.md) und [SELECT-Anweisung für Ereignis Abfragen](select-statement-for-event-queries.md).</span><span class="sxs-lookup"><span data-stu-id="81c04-145">For more information, see [Using Standard String Templates](using-standard-string-templates.md) and [SELECT Statement for Event Queries](select-statement-for-event-queries.md).</span></span>

    <span data-ttu-id="81c04-146">Verwenden Sie eine vorhandene Quelle für das Ereignisprotokoll, das eine Einfügezeichenfolge ohne zugehörigen Text unterstützt.</span><span class="sxs-lookup"><span data-stu-id="81c04-146">Use an existing source for the event log that supports an insertion string without associated text.</span></span>

    <span data-ttu-id="81c04-147">Im folgenden MOF-Codebeispiel wird gezeigt, wie eine vorhandene Quelle von WSH und der **EventID-** Wert 8 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="81c04-147">The following MOF code example shows how to use an existing source of WSH and an **EventID** value of 8.</span></span>

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

3.  <span data-ttu-id="81c04-148">Erstellen Sie eine Instanz von [**\_ \_ EventFilter**](--eventfilter.md) , und definieren Sie eine Abfrage für Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="81c04-148">Create an instance of [**\_\_EventFilter**](--eventfilter.md) and define a query for events.</span></span>

    <span data-ttu-id="81c04-149">Im folgenden Beispiel überwacht der Filter den Registrierungsschlüssel, in dem Start Programme registriert sind.</span><span class="sxs-lookup"><span data-stu-id="81c04-149">In the following example, the filter monitors the registry key where startup programs are registered.</span></span> <span data-ttu-id="81c04-150">Das Überwachen dieses Registrierungsschlüssels ist möglicherweise wichtig, da sich ein nicht autorisiertes Programm unter dem Schlüssel registrieren kann, was dazu veranlasst, dass es beim Starten des Computers gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="81c04-150">Monitoring this registry key may be important because an unauthorized program can register itself under the key, which causes it to be launched when the computer boots.</span></span>

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

4.  <span data-ttu-id="81c04-151">Identifizieren Sie ein Ereignis, um eine Ereignis Abfrage zu überwachen und zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="81c04-151">Identify an event to monitor and create an event query.</span></span>

    <span data-ttu-id="81c04-152">Sie können überprüfen, ob ein System internes oder ein extrinsisches Ereignis verwendet, das verwendet.</span><span class="sxs-lookup"><span data-stu-id="81c04-152">You can check to see if there is an intrinsic or extrinsic event that use.</span></span> <span data-ttu-id="81c04-153">Verwenden Sie z. b. die [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) -Klasse des Registrierungs Anbieters, um Änderungen an der Systemregistrierung zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="81c04-153">For example, use the [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) class of the Registry provider to monitor changes to the system registry.</span></span>

    <span data-ttu-id="81c04-154">Wenn eine Klasse nicht vorhanden ist, die ein Ereignis beschreibt, das Sie überwachen müssen, müssen Sie einen eigenen Ereignis Anbieter erstellen und neue System externe-Ereignis Klassen definieren.</span><span class="sxs-lookup"><span data-stu-id="81c04-154">If a class does not exist that describes an event you need to monitor, you must create your own event provider, and define new extrinsic event classes.</span></span> <span data-ttu-id="81c04-155">Weitere Informationen finden Sie unter [Schreiben eines Ereignis Anbieters](writing-an-event-provider.md).</span><span class="sxs-lookup"><span data-stu-id="81c04-155">For more information, see [Writing an Event Provider](writing-an-event-provider.md).</span></span>

    <span data-ttu-id="81c04-156">In einer MOF-Datei können Sie einen [*Alias*](gloss-a.md) für den Filter und den Consumer definieren, der eine einfache Möglichkeit bietet, die Instanzpfade zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="81c04-156">In a MOF file, you can define an [*alias*](gloss-a.md) for the filter and consumer, which provides an easy way to describe the instance paths.</span></span>

    <span data-ttu-id="81c04-157">Im folgenden Beispiel wird gezeigt, wie Sie einen [*Alias*](gloss-a.md) für den Filter und den Consumer definieren.</span><span class="sxs-lookup"><span data-stu-id="81c04-157">The following example shows how to define an [*alias*](gloss-a.md) for the filter and consumer.</span></span>

    ```syntax
    instance of __EventFilter as $FILTER
    instance of LogFileEventConsumer as $CONSUMER
    ```

5.  <span data-ttu-id="81c04-158">Erstellen Sie eine Instanz von [**\_ \_ filtertoconsumerbinding**](--filtertoconsumerbinding.md) , um den Filter und die Consumerklassen zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="81c04-158">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter and the consumer classes.</span></span> <span data-ttu-id="81c04-159">Diese Instanz bestimmt, dass bei Auftreten eines Ereignisses, das mit dem angegebenen Filter übereinstimmt, die vom Consumer angegebene Aktion erfolgen muss.</span><span class="sxs-lookup"><span data-stu-id="81c04-159">This instance determines that when an event occurs that matches the specified filter, the action specified by the consumer must occur.</span></span> <span data-ttu-id="81c04-160">[**\_ \_ EventFilter**](--eventfilter.md), [**\_ \_ eventconsumer**](--eventconsumer.md)und **\_ \_ filtertoconsumerbinding** müssen die gleiche individuelle Sicherheits-ID (SID) in der Eigenschaft " **kreatorsid** " aufweisen.</span><span class="sxs-lookup"><span data-stu-id="81c04-160">[**\_\_EventFilter**](--eventfilter.md), [**\_\_EventConsumer**](--eventconsumer.md), and **\_\_FilterToConsumerBinding** must have the same individual security identifier (SID) in the **CreatorSID** property.</span></span> <span data-ttu-id="81c04-161">Weitere Informationen finden Sie unter [Binden eines Ereignis Filters mit einem logischen Consumer](binding-an-event-filter-with-a-logical-consumer.md).</span><span class="sxs-lookup"><span data-stu-id="81c04-161">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md).</span></span>

    <span data-ttu-id="81c04-162">Im folgenden Beispiel wird gezeigt, wie eine Instanz anhand des Objekt Pfads identifiziert wird, oder ein Alias als Kurzform Ausdruck für den Objekt Pfad verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="81c04-162">The following example shows how to identify an instance by the object path, or use an alias as a shorthand expression for the object path.</span></span>

    ```syntax
    instance of __EventFilter as $FILTER
    instance of NTEventLogEventConsumer as $CONSUMER
    ```

    <span data-ttu-id="81c04-163">Im folgenden Beispiel wird der Filter mithilfe von Aliasen an den Consumer gebunden.</span><span class="sxs-lookup"><span data-stu-id="81c04-163">The following example binds the filter to the consumer by using aliases.</span></span>

    ```syntax
    instance of __FilterToConsumerBinding
    {
        Filter = $FILTER;
        Consumer = $CONSUMER;
        
    };
    ```

    <span data-ttu-id="81c04-164">Sie können einen Filter an mehrere Consumer binden. Dies bedeutet, dass beim Auftreten von übereinstimmenden Ereignissen mehrere Aktionen ausgeführt werden müssen. oder Sie können einen Consumer an mehrere Filter binden, was darauf hinweist, dass die Aktion ausgeführt werden muss, wenn Ereignisse auftreten, die einem der Filter entsprechen.</span><span class="sxs-lookup"><span data-stu-id="81c04-164">You can bind one filter to several consumers, which indicates that when matching events occur, several actions must be taken; or you can bind one consumer to several filters, which indicates that the action must be taken when events that match one of the filters occur.</span></span>

    <span data-ttu-id="81c04-165">Die folgenden Aktionen werden basierend auf der Bedingung der Consumer und Ereignisse ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="81c04-165">The following actions are taken based on the condition of consumers and events:</span></span>

    -   <span data-ttu-id="81c04-166">Wenn einer der permanenten Verbraucher ausfällt, erhalten andere Consumer, die das Ereignis anfordern, eine Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="81c04-166">If one of the permanent consumers fails, other consumers that request the event receive notification.</span></span>
    -   <span data-ttu-id="81c04-167">Wenn ein Ereignis gelöscht wird, löst WMI [**\_ \_ eventdroppedevent**](--eventdroppedevent.md)aus.</span><span class="sxs-lookup"><span data-stu-id="81c04-167">If an event is dropped, WMI fires [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>
    -   <span data-ttu-id="81c04-168">Wenn Sie dieses Ereignis abonnieren, wird das gelöschte Ereignis zurückgegeben, und ein Verweis auf den [**\_ \_ eventconsumer**](--eventconsumer.md) stellt den fehlgeschlagenen Consumer dar.</span><span class="sxs-lookup"><span data-stu-id="81c04-168">If you subscribe to this event, it returns the event that is dropped, and a reference to the [**\_\_EventConsumer**](--eventconsumer.md) represents the failed consumer.</span></span>
    -   <span data-ttu-id="81c04-169">Wenn ein Consumer ausfällt, löst WMI [**\_ \_ consumerfailureevent**](--consumerfailureevent.md)aus, das möglicherweise weitere Informationen in den Eigenschaften **errorCode**, **ErrorDescription** und **ErrorObject** enthält.</span><span class="sxs-lookup"><span data-stu-id="81c04-169">If a consumer fails, WMI fires [**\_\_ConsumerFailureEvent**](--consumerfailureevent.md), which may contain more information in the **ErrorCode**, **ErrorDescription** and **ErrorObject** properties.</span></span>

    <span data-ttu-id="81c04-170">Weitere Informationen finden Sie unter [Binden eines Ereignis Filters mit einem logischen Consumer](binding-an-event-filter-with-a-logical-consumer.md).</span><span class="sxs-lookup"><span data-stu-id="81c04-170">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md).</span></span>

## <a name="example"></a><span data-ttu-id="81c04-171">Beispiel</span><span class="sxs-lookup"><span data-stu-id="81c04-171">Example</span></span>

<span data-ttu-id="81c04-172">Das folgende Beispiel zeigt das MOF für eine Instanz von [**nteventlogeventconsumer**](nteventlogeventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="81c04-172">The following example shows the MOF for an instance of [**NTEventLogEventConsumer**](nteventlogeventconsumer.md).</span></span> <span data-ttu-id="81c04-173">Nachdem Sie diese MOF kompiliert haben, wird bei jedem Versuch, einen Wert im Registrierungs Pfad **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\** zu erstellen, zu löschen oder zu ändern, ein Eintrag im Anwendungs Ereignisprotokoll unter der Quelle "WSH" protokolliert.</span><span class="sxs-lookup"><span data-stu-id="81c04-173">After you compile this MOF, any attempt to create, delete, or modify a value in the Registry path **HKEY\_LOCAL\_MACHINE\\ Software\\Microsoft\\Windows\\CurrentVersion\\Run** logs an entry in the Application eventlog, under the source "WSH".</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="81c04-174">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="81c04-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81c04-175">Sicheres empfangen von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="81c04-175">Receiving Events Securely</span></span>](receiving-events-securely.md)
</dt> </dl>

 

 
