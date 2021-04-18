---
description: Die commandlineeventconsumer-Klasse führt ein angegebenes ausführbares Programm von einer Befehlszeile aus, wenn ein bestimmtes Ereignis auftritt. Diese Klasse ist ein Standard Ereignisconsumer, den WMI bereitstellt.
ms.assetid: b912a4a1-7b1c-43a9-b098-fcfd62a2c2db
ms.tgt_platform: multiple
title: Ausführen eines Programms von der Befehlszeile auf der Grundlage eines Ereignisses
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: de7f4fb5e679a6b5767635c70e2ffb5eda3ba800
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347069"
---
# <a name="running-a-program-from-the-command-line-based-on-an-event"></a><span data-ttu-id="086c3-104">Ausführen eines Programms von der Befehlszeile auf der Grundlage eines Ereignisses</span><span class="sxs-lookup"><span data-stu-id="086c3-104">Running a Program from the Command Line Based on an Event</span></span>

<span data-ttu-id="086c3-105">Die [**commandlineeventconsumer**](commandlineeventconsumer.md) -Klasse führt ein angegebenes ausführbares Programm von einer Befehlszeile aus, wenn ein bestimmtes Ereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="086c3-105">The [**CommandLineEventConsumer**](commandlineeventconsumer.md) class runs a specified executable program from a command line when a specified event occurs.</span></span> <span data-ttu-id="086c3-106">Diese Klasse ist ein Standard Ereignisconsumer, den WMI bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="086c3-106">This class is a standard event consumer that WMI provides.</span></span>

<span data-ttu-id="086c3-107">Wenn Sie [**commandlineeventconsumer**](commandlineeventconsumer.md)verwenden, sollten Sie die ausführbare Datei sichern, die Sie starten möchten.</span><span class="sxs-lookup"><span data-stu-id="086c3-107">When you use [**CommandLineEventConsumer**](commandlineeventconsumer.md), you should secure the executable that you want to start.</span></span> <span data-ttu-id="086c3-108">Wenn sich die ausführbare Datei nicht an einem sicheren Speicherort befindet oder nicht mit einer starken Zugriffs Steuerungs Liste (ACL) geschützt ist, kann ein Benutzer ohne Zugriffsberechtigungen die ausführbare Datei durch eine andere ausführbare Datei ersetzen.</span><span class="sxs-lookup"><span data-stu-id="086c3-108">If the executable is not in a secure location or not secured with a strong access control list (ACL), a user without access privileges can replace your executable with a different executable.</span></span> <span data-ttu-id="086c3-109">Sie können die [**Win32 \_ logicalfilesecuritysetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting) -oder [**Win32 \_ logicalsharesecuritysetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting) -Klassen verwenden, um die Sicherheit einer Datei oder Freigabe Programm gesteuert zu ändern.</span><span class="sxs-lookup"><span data-stu-id="086c3-109">You can use the [**Win32\_LogicalFileSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting) or [**Win32\_LogicalShareSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting) classes to change programmatically the security of a file or share.</span></span> <span data-ttu-id="086c3-110">Weitere Informationen finden Sie unter [Erstellen einer Sicherheits Beschreibung für ein neues Objekt in C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="086c3-110">For more information, see [Creating a Security Descriptor for a New Object in C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

<span data-ttu-id="086c3-111">Die grundlegende Vorgehensweise für die Verwendung von Standardconsumern ist immer identisch und befindet sich in [Überwachung und Reaktion auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.</span><span class="sxs-lookup"><span data-stu-id="086c3-111">The basic procedure to use standard consumers is always the same, and is located in [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span> <span data-ttu-id="086c3-112">Das folgende Verfahren fügt der grundlegenden Prozedur, ist spezifisch für die [**commandlineeventconsumer**](commandlineeventconsumer.md) -Klasse, und beschreibt, wie ein Ereignisconsumer erstellt wird, der ein Programm ausführt.</span><span class="sxs-lookup"><span data-stu-id="086c3-112">The following procedure adds to the basic procedure, is specific to the [**CommandLineEventConsumer**](commandlineeventconsumer.md) class, and describes how to create an event consumer that runs a program.</span></span>

> [!Caution]
>
> <span data-ttu-id="086c3-113">Die [**commandlineeventconsumer**](commandlineeventconsumer.md) -Klasse verfügt über besondere Sicherheitseinschränkungen.</span><span class="sxs-lookup"><span data-stu-id="086c3-113">The [**CommandLineEventConsumer**](commandlineeventconsumer.md) class has special security constraints.</span></span> <span data-ttu-id="086c3-114">Dieser Standardconsumer muss von einem lokalen Mitglied der Gruppe "Administratoren" auf dem lokalen Computer konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="086c3-114">This standard consumer must be configured by a local member of the Administrators group on the local computer.</span></span> <span data-ttu-id="086c3-115">Wenn Sie ein Domänen Konto zum Erstellen des Abonnements verwenden, muss das LocalSystem-Konto über die erforderlichen Berechtigungen für die Domäne verfügen, um sicherzustellen, dass der Ersteller Mitglied der lokalen Administratoren Gruppe ist.</span><span class="sxs-lookup"><span data-stu-id="086c3-115">If you use a domain account to create the subscription, the LocalSystem account must have the necessary permissions on the domain to verify that the creator is a member of the local Administrators group.</span></span>
>
> <span data-ttu-id="086c3-116">[**Commandlineeventconsumer**](commandlineeventconsumer.md) kann nicht verwendet werden, um einen Prozess zu starten, der interaktiv ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="086c3-116">[**CommandLineEventConsumer**](commandlineeventconsumer.md) cannot be used to start a process that runs interactively.</span></span>

 

<span data-ttu-id="086c3-117">Im folgenden Verfahren wird beschrieben, wie Sie einen Ereignisconsumer erstellen, der einen Prozess über eine Befehlszeile ausführt.</span><span class="sxs-lookup"><span data-stu-id="086c3-117">The following procedure describes how to create an event consumer that runs a process from a command line.</span></span>

<span data-ttu-id="086c3-118">**So erstellen Sie einen Ereignisconsumer, der einen Prozess über eine Befehlszeile ausführt**</span><span class="sxs-lookup"><span data-stu-id="086c3-118">**To create an event consumer that runs a process from a command line**</span></span>

1.  <span data-ttu-id="086c3-119">Erstellen Sie in der MOF-Datei (Managed Object Format) eine Instanz von [**commandlineeventconsumer**](commandlineeventconsumer.md) , um die Ereignisse zu empfangen, die Sie in der Abfrage anfordern.</span><span class="sxs-lookup"><span data-stu-id="086c3-119">In the Managed Object Format (MOF) file, create an instance of [**CommandLineEventConsumer**](commandlineeventconsumer.md) to receive the events you request in the query.</span></span> <span data-ttu-id="086c3-120">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="086c3-120">For more information, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>
2.  <span data-ttu-id="086c3-121">Erstellen Sie eine Instanz von [**\_ \_ EventFilter**](--eventfilter.md) , und benennen Sie Sie mit einem Namen.</span><span class="sxs-lookup"><span data-stu-id="086c3-121">Create an instance of [**\_\_EventFilter**](--eventfilter.md) and give it a name.</span></span>
3.  <span data-ttu-id="086c3-122">Erstellen Sie eine Abfrage, um den Ereignistyp anzugeben.</span><span class="sxs-lookup"><span data-stu-id="086c3-122">Create a query to specify the type of event.</span></span> <span data-ttu-id="086c3-123">Weitere Informationen finden Sie unter [Abfragen mit WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="086c3-123">For more information, see [Querying with WQL](querying-with-wql.md).</span></span>
4.  <span data-ttu-id="086c3-124">Erstellen Sie eine Instanz von [**\_ \_ filtertoconsumerbinding**](--filtertoconsumerbinding.md) , um den Filter der Instanz von [**commandlineeventconsumer**](commandlineeventconsumer.md)zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="086c3-124">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter with the instance of [**CommandLineEventConsumer**](commandlineeventconsumer.md).</span></span>
5.  <span data-ttu-id="086c3-125">Kompilieren Sie die MOF-Datei mit [**Mofcomp.exe**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="086c3-125">Compile your MOF file by using [**Mofcomp.exe**](mofcomp.md).</span></span>

## <a name="example"></a><span data-ttu-id="086c3-126">Beispiel</span><span class="sxs-lookup"><span data-stu-id="086c3-126">Example</span></span>

<span data-ttu-id="086c3-127">Im folgenden Codebeispiel wird eine neue Klasse mit dem Namen "mycmdlineconsumer" erstellt, um Ereignisse zu generieren, wenn eine Instanz der neuen Klasse am Ende einer MOF-Klasse erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="086c3-127">The following code example creates a new class called "MyCmdLineConsumer" to generate events when an instance of the new class is created at the end of a MOF.</span></span> <span data-ttu-id="086c3-128">Das Beispiel ist ein MOF-Code, aber Sie können die Instanzen Programm gesteuert mithilfe der [Skript-API für WMI](scripting-api-for-wmi.md) oder der [com-API für WMI](com-api-for-wmi.md)erstellen.</span><span class="sxs-lookup"><span data-stu-id="086c3-128">The example is in MOF code, but you can create the instances programmatically by using the [Scripting API for WMI](scripting-api-for-wmi.md) or the [COM API for WMI](com-api-for-wmi.md).</span></span>

<span data-ttu-id="086c3-129">Im folgenden Verfahren wird beschrieben, wie eine neue Klasse mit dem Namen mycmdlineconsumer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="086c3-129">The following procedure describes how to create a new class called MyCmdLineConsumer.</span></span>

<span data-ttu-id="086c3-130">**So erstellen Sie eine neue Klasse mit dem Namen mycmdlineconsumer**</span><span class="sxs-lookup"><span data-stu-id="086c3-130">**To create a new class called MyCmdLineConsumer**</span></span>

1.  <span data-ttu-id="086c3-131">Erstellen Sie die Datei c: \\ CmdLine \_test.bat mit einem Befehl, der ein sichtbares Programm ausführt, z. b. "calc.exe".</span><span class="sxs-lookup"><span data-stu-id="086c3-131">Create the c:\\cmdline\_test.bat file with a command that executes a visible program, such as "calc.exe" .</span></span>
2.  <span data-ttu-id="086c3-132">Kopieren Sie die MOF-Datei in eine Textdatei, und speichern Sie Sie mit der Erweiterung MOF.</span><span class="sxs-lookup"><span data-stu-id="086c3-132">Copy the MOF to a text file and save it with a .mof extension.</span></span>
3.  <span data-ttu-id="086c3-133">Kompilieren Sie in einem Befehlsfenster die MOF-Datei mit dem folgenden Befehl: " **Datei Name Dateiname. MOF**".</span><span class="sxs-lookup"><span data-stu-id="086c3-133">In a Command window, compile the MOF file by using the following command: **Mofcomp filename.mof**.</span></span>

> [!Note]  
> <span data-ttu-id="086c3-134">Das in der cmdline- \_test.bat angegebene Programm sollte ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="086c3-134">The program specified in cmdline\_test.bat should execute.</span></span>

 

``` syntax
// Set the namespace as root\subscription.
// The CommandLineEventConsumer is already compiled
// in the root\subscription namespace. 
#pragma namespace ("\\\\.\\Root\\subscription")

class MyCmdLineConsumer
{
 [key]string Name;
};

// Create an instance of the command line consumer
// and give it the alias $CMDLINECONSUMER

instance of CommandLineEventConsumer as $CMDLINECONSUMER
{
 Name = "CmdLineConsumer_Example";
 CommandLineTemplate = "c:\\cmdline_test.bat";
 RunInteractively = True;
 WorkingDirectory = "c:\\";
};    

// Create an instance of the event filter
// and give it the alias $CMDLINEFILTER
// The filter queries for instance creation event
// for instances of the MyCmdLineConsumer class

instance of __EventFilter as $CMDLINEFILTER
{
    Name = "CmdLineFilter";
    Query = "SELECT * FROM __InstanceCreationEvent"
        " WHERE TargetInstance.__class = \"MyCmdLineConsumer\"";
    QueryLanguage = "WQL";
};

// Create an instance of the binding
// between filter and consumer instances.

instance of __FilterToConsumerBinding
{
     Consumer = $CMDLINECONSUMER;
     Filter = $CMDLINEFILTER;
};

// Create an instance of this class right now. 
// The commands in c:\\cmdline_test.bat execute
// as the result of creating the instance
// of MyCmdLineConsumer.
 
instance of MyCmdLineConsumer
{
     Name = "CmdLineEventConsumer test";
};
```

## <a name="related-topics"></a><span data-ttu-id="086c3-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="086c3-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="086c3-136">Überwachen von und reagieren auf Ereignisse mit Standard Consumern</span><span class="sxs-lookup"><span data-stu-id="086c3-136">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 
