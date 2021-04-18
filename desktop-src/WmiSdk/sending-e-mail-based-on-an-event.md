---
description: Mithilfe der Klasse smtpeer-Consumer können Sie eine e-Mail an einen bestimmten Benutzer senden, wenn ein bestimmtes Ereignis eintritt. Diese Klasse ist ein Standard Ereignisconsumer, den WMI bereitstellt.
ms.assetid: ed10e6f7-8e18-4cde-bd46-a7791547c7da
ms.tgt_platform: multiple
title: Senden von e-Mails auf der Grundlage eines Ereignisses
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4929b7c8c29d514d73a6e4c9d14049a19f306233
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358514"
---
# <a name="sending-email-based-on-an-event"></a><span data-ttu-id="d7651-104">Senden von e-Mails auf der Grundlage eines Ereignisses</span><span class="sxs-lookup"><span data-stu-id="d7651-104">Sending Email Based on an Event</span></span>

<span data-ttu-id="d7651-105">Mithilfe der Klasse [smtpeer-Consumer](smtpeventconsumer.md) können Sie eine e-Mail an einen bestimmten Benutzer senden, wenn ein bestimmtes Ereignis eintritt.</span><span class="sxs-lookup"><span data-stu-id="d7651-105">By using the [SMTPEventConsumer](smtpeventconsumer.md) class, you can send email to a designated user when a specified event occurs.</span></span> <span data-ttu-id="d7651-106">Diese Klasse ist ein [Standard Ereignisconsumer](standard-consumer-classes.md) , den WMI bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="d7651-106">This class is a [standard event consumer](standard-consumer-classes.md) that WMI provides.</span></span>

<span data-ttu-id="d7651-107">Die Klasse [smtpventconsumer](smtpeventconsumer.md) erfordert die folgenden Bedingungen, um eine e-Mail-Nachricht als Antwort auf ein Ereignis zu senden:</span><span class="sxs-lookup"><span data-stu-id="d7651-107">The [SMTPEventConsumer](smtpeventconsumer.md) class requires the following conditions to send an email message in response to an event:</span></span>

-   <span data-ttu-id="d7651-108">Die Klasse [smtpeer-Consumer](smtpeventconsumer.md) muss in den richtigen Namespace kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="d7651-108">The [SMTPEventConsumer](smtpeventconsumer.md) class must be compiled into the correct namespace.</span></span> <span data-ttu-id="d7651-109">Weitere Informationen finden Sie unter über [wachen und reagieren auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.</span><span class="sxs-lookup"><span data-stu-id="d7651-109">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>
-   <span data-ttu-id="d7651-110">Ein SMTP-Server muss im Netzwerk vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="d7651-110">An SMTP server must exist on the network.</span></span>
-   <span data-ttu-id="d7651-111">Die e-Mail-Nachricht darf keine Anlage enthalten.</span><span class="sxs-lookup"><span data-stu-id="d7651-111">The email message cannot have an attachment.</span></span>
-   <span data-ttu-id="d7651-112">Die e-Mail-Nachricht muss in US-ASCII codiert werden.</span><span class="sxs-lookup"><span data-stu-id="d7651-112">The email message must be encoded in US-ASCII.</span></span>

<span data-ttu-id="d7651-113">Das grundlegende Verfahren für die Verwendung von Standardconsumern ist immer identisch und befindet sich in [Überwachung und Reaktion auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.</span><span class="sxs-lookup"><span data-stu-id="d7651-113">The basic procedure for using standard consumers is always the same, and is located in [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span> <span data-ttu-id="d7651-114">Das folgende Verfahren fügt dem grundlegenden Verfahren hinzu. ist spezifisch für die Klasse [smtpeer Event Consumer](smtpeventconsumer.md) . und beschreibt, wie ein Ereignisconsumer erstellt wird, der eine e-Mail sendet.</span><span class="sxs-lookup"><span data-stu-id="d7651-114">The following procedure adds to the basic procedure; is specific to the [SMTPEventConsumer](smtpeventconsumer.md) class; and describes how to create an event consumer that sends email.</span></span>

<span data-ttu-id="d7651-115">Im folgenden Verfahren wird beschrieben, wie ein Ereignisconsumer erstellt wird, der eine e-Mail sendet.</span><span class="sxs-lookup"><span data-stu-id="d7651-115">The following procedure describes how to create an event consumer that sends email.</span></span>

<span data-ttu-id="d7651-116">**So erstellen Sie einen Ereignisconsumer, der eine e-Mail sendet**</span><span class="sxs-lookup"><span data-stu-id="d7651-116">**To create an event consumer that sends email**</span></span>

1.  <span data-ttu-id="d7651-117">Installieren und registrieren Sie ggf. die Klasse [smtpventconsumer](smtpeventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="d7651-117">Install and register the [SMTPEventConsumer](smtpeventconsumer.md) class, if necessary.</span></span>

    <span data-ttu-id="d7651-118">Die Klasse [smtpventconsumer](smtpeventconsumer.md) wird \\ vom WMI-Setup Programm in den Namespace des Stamm Abonnements kompiliert.</span><span class="sxs-lookup"><span data-stu-id="d7651-118">The [SMTPEventConsumer](smtpeventconsumer.md) class is compiled into the root\\subscription namespace by the WMI setup program.</span></span>

2.  <span data-ttu-id="d7651-119">Identifizieren Sie das Ereignis, das Sie überwachen möchten, und erstellen Sie die Ereignis Abfrage.</span><span class="sxs-lookup"><span data-stu-id="d7651-119">Identify the event that you want to monitor and create the event query.</span></span>

    <span data-ttu-id="d7651-120">Möglicherweise ist ein System internes Ereignis vorhanden, das zum Überwachen Ihres Ereignisses verwendet.</span><span class="sxs-lookup"><span data-stu-id="d7651-120">There might be an existing intrinsic event that use to monitor your event.</span></span> <span data-ttu-id="d7651-121">Die meisten systeminternen Ereignisse werden Änderungen an Klassen Instanzen im \\ Namespace "root cimv2" zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d7651-121">Most intrinsic events are associated with changes to class instances in the "root\\cimv2" namespace.</span></span> <span data-ttu-id="d7651-122">Wenn Sie die Klassen in der [WMI-Klassen](wmi-classes.md) Referenz analysieren, finden Sie wahrscheinlich eine Klasse, die das Ereignis identifiziert, das Sie überwachen möchten.</span><span class="sxs-lookup"><span data-stu-id="d7651-122">By analyzing the classes in the [WMI Classes](wmi-classes.md) reference, you can probably find a class that identifies the event you want to monitor.</span></span> <span data-ttu-id="d7651-123">Verwenden Sie z. b. die [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse, um Änderungen an einem Festplattenlaufwerk zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="d7651-123">For example, use the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class to monitor changes to a hard disk drive.</span></span>

    <span data-ttu-id="d7651-124">Wenn keine systeminternen Ereignisse vorhanden sind, die verwenden, kann möglicherweise ein System externe-Ereignis Anbieter funktionieren.</span><span class="sxs-lookup"><span data-stu-id="d7651-124">If there are no existing intrinsic events that use, there might be an extrinsic event provider that can work.</span></span> <span data-ttu-id="d7651-125">Verwenden Sie z. b. die [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) -Klasse des Registrierungs Anbieters, um Änderungen an der Systemregistrierung zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="d7651-125">For example, use the [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) class of the Registry provider to monitor changes to the system registry.</span></span>

    <span data-ttu-id="d7651-126">Wenn keine Klasse vorhanden ist, die das Ereignis identifiziert, das Sie überwachen möchten, müssen Sie einen eigenen Ereignis Anbieter erstellen und neue System externe-Ereignis Klassen definieren.</span><span class="sxs-lookup"><span data-stu-id="d7651-126">If a class does not exist that identifies the event you want to monitor, you must create your own event provider and define new extrinsic event classes.</span></span> <span data-ttu-id="d7651-127">Weitere Informationen finden Sie unter [Schreiben eines Ereignis Anbieters](writing-an-event-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d7651-127">For more information, see [Writing an Event Provider](writing-an-event-provider.md).</span></span>

3.  <span data-ttu-id="d7651-128">Erstellen Sie in der MOF-Datei (Managed Object Format) eine Instanz von [smtpeer-Consumer](smtpeventconsumer.md) , um Ereignisse zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="d7651-128">In the Managed Object Format (MOF) file, create an instance of the [SMTPEventConsumer](smtpeventconsumer.md) to receive events.</span></span>

    <span data-ttu-id="d7651-129">Verwenden Sie die Eigenschaften der-Instanz, um die e-Mail-Nachricht zu definieren, die bei einem Ereignis gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="d7651-129">Use the properties of the instance to define the email message to send when an event occurs.</span></span> <span data-ttu-id="d7651-130">Die **Toline** -Eigenschaft definiert z. b. die e-Mail-Adresse, und die **Message** -Eigenschaft definiert den Text der e-Mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="d7651-130">For example, the **ToLine** property defines the email address, and the **Message** property defines the text of the email message.</span></span> <span data-ttu-id="d7651-131">Sie müssen die e-Mail-Adresse, den Betreff und den Text einer Nachricht definieren, aber eine e-Mail-Nachricht kann keine Anlage enthalten.</span><span class="sxs-lookup"><span data-stu-id="d7651-131">You must define the email address, subject, and text of a message, but an email message cannot have an attachment.</span></span> <span data-ttu-id="d7651-132">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="d7651-132">For more information, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

4.  <span data-ttu-id="d7651-133">Erstellen Sie eine Ereignis Abfrage, mit der die Ereignisse angegeben werden, die Sie überwachen möchten.</span><span class="sxs-lookup"><span data-stu-id="d7651-133">Create an event query that specifies the events you want to monitor.</span></span>

    <span data-ttu-id="d7651-134">Weitere Informationen finden Sie unter [Abfragen mit WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="d7651-134">For more information, see [Querying with WQL](querying-with-wql.md).</span></span>

5.  <span data-ttu-id="d7651-135">Erstellen Sie eine Instanz von [**\_ \_ EventFilter**](--eventfilter.md) , und speichern Sie die Abfrage in der **Query** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d7651-135">Create an instance of [**\_\_EventFilter**](--eventfilter.md) and store your query in the **Query** property.</span></span>

    <span data-ttu-id="d7651-136">Weitere Informationen finden Sie unter [Abfragen mit WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="d7651-136">For more information see, [Querying with WQL](querying-with-wql.md).</span></span>

6.  <span data-ttu-id="d7651-137">Erstellen Sie eine Instanz von [**\_ \_ filtertoconsumerbinding**](--filtertoconsumerbinding.md) , um den Filter und den Consumer zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="d7651-137">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter and the consumer.</span></span>
7.  <span data-ttu-id="d7651-138">Kompilieren Sie die MOF-Datei mit [**Mofcomp.exe**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="d7651-138">Compile the MOF file by using [**Mofcomp.exe**](mofcomp.md).</span></span>


## <a name="example"></a><span data-ttu-id="d7651-139">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d7651-139">Example</span></span>

<span data-ttu-id="d7651-140">Das Beispiel in diesem Abschnitt ist ein MOF-Code, aber Sie können die Instanzen Programm gesteuert mithilfe der [Skript-API für WMI](scripting-api-for-wmi.md) oder der [com-API für WMI](com-api-for-wmi.md)erstellen.</span><span class="sxs-lookup"><span data-stu-id="d7651-140">The example in this section is in MOF code, but you can create the instances programmatically by using the [Scripting API for WMI](scripting-api-for-wmi.md) or the [COM API for WMI](com-api-for-wmi.md).</span></span>

<span data-ttu-id="d7651-141">Im folgenden Verfahren wird beschrieben, wie das Beispiel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d7651-141">The following procedure describes how to use the example.</span></span>

<span data-ttu-id="d7651-142">**So verwenden Sie das Beispiel**</span><span class="sxs-lookup"><span data-stu-id="d7651-142">**To use the example**</span></span>

1.  <span data-ttu-id="d7651-143">Kopieren Sie die folgende MOF-Datei in eine Textdatei, und speichern Sie Sie mit der Erweiterung MOF.</span><span class="sxs-lookup"><span data-stu-id="d7651-143">Copy the following MOF to a text file and save it with a .mof extension.</span></span>
2.  <span data-ttu-id="d7651-144">Kompilieren Sie die MOF-Datei in einem Eingabe Aufforderungs Fenster mit dem folgenden Befehl:</span><span class="sxs-lookup"><span data-stu-id="d7651-144">In a command prompt window, compile the MOF file by using the following command:</span></span>

    <span data-ttu-id="d7651-145">" **Mamacomp** *filename \* \* *. MOF* "*</span><span class="sxs-lookup"><span data-stu-id="d7651-145">**Mofcomp** *filename\*\*\*.mof*\*</span></span>

> [!Note]  
> <span data-ttu-id="d7651-146">Wenn der MOF-Code in den Namespace des Stamm Abonnements kompiliert wird \\ , wird der [smtpeer-Consumer](smtpeventconsumer.md) in den gleichen Namespace kompiliert.</span><span class="sxs-lookup"><span data-stu-id="d7651-146">When MOF code is compiled into the root\\subscription namespace, the [SMTPEventConsumer](smtpeventconsumer.md) is compiled into the same namespace.</span></span>

 

``` syntax
#pragma namespace ("\\\\.\\root\\subscription")

instance of __EventFilter as $FILTER
{
    Name = "LowDiskspaceFilter";
    
    EventNamespace = "\\\\.\\root\\cimv2";  

    Query = "SELECT * FROM __InstanceModificationEvent WITHIN 10 "
            "WHERE TargetInstance ISA \"Win32_LogicalDisk\" "
            "AND TargetInstance.FreeSpace < 846000000 "
            "AND PreviousInstance.FreeSpace >= 846000000 "
            "AND (TargetInstance.DeviceID = \"C:\" "
            "OR TargetInstance.DeviceID = \"D:\")";
    QueryLanguage = "WQL";
};


instance of SMTPEventConsumer as $CONSUMER
{
    Name = "LowDisk";
    ToLine = "SysAd@MyCompany.com, MyAlias@MyCompany.com";
    CcLine = "MyHome@MyISP.com";
    ReplyToLine = "MyAlias@MyCompany.com";
    SMTPServer = "SmartHost";
    Subject = "WARNING: Low disk space";
    Message = "WARNING: Your %TargetInstance.DeviceID% is"
        " getting dangerously low.";
};

instance of __FilterToConsumerBinding
{
    Consumer = $CONSUMER ;
    Filter = $FILTER ;
};
```

## <a name="related-topics"></a><span data-ttu-id="d7651-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d7651-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7651-148">Überwachen von und reagieren auf Ereignisse mit Standard Consumern</span><span class="sxs-lookup"><span data-stu-id="d7651-148">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 
