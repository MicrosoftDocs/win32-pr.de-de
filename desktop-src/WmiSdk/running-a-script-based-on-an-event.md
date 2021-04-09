---
description: Der Standardconsumer, der von der activescripteventconsumer-Klasse implementiert wird, ermöglicht einem Computer das Ausführen eines Skripts und das Ausführen von Maßnahmen, wenn wichtige Ereignisse auftreten, um sicherzustellen, dass ein Computer automatisch Probleme erkennen und beheben kann.
ms.assetid: 0d2ac139-3e2b-4089-ae9c-289d376e27a2
ms.tgt_platform: multiple
title: Ausführen eines Skripts auf der Grundlage eines Ereignisses
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4dbb1e55c7828a79d6541182eff5ce20147a82c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868132"
---
# <a name="running-a-script-based-on-an-event"></a><span data-ttu-id="ad983-103">Ausführen eines Skripts auf der Grundlage eines Ereignisses</span><span class="sxs-lookup"><span data-stu-id="ad983-103">Running a Script Based on an Event</span></span>

<span data-ttu-id="ad983-104">Der Standardconsumer, der von der [**activescripteventconsumer**](activescripteventconsumer.md) -Klasse implementiert wird, ermöglicht einem Computer das Ausführen eines Skripts und das Ausführen von Maßnahmen, wenn wichtige Ereignisse auftreten, um sicherzustellen, dass ein Computer automatisch Probleme erkennen und beheben kann.</span><span class="sxs-lookup"><span data-stu-id="ad983-104">The standard consumer that is implemented by the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class allows a computer to run a script and take action when important events occur to ensure that a computer can detect and resolve problems automatically.</span></span>

<span data-ttu-id="ad983-105">Dieser Consumer wird standardmäßig im Namespace des Stamm **\\ Abonnements** geladen.</span><span class="sxs-lookup"><span data-stu-id="ad983-105">This consumer is loaded by default in the **root\\subscription** namespace.</span></span>

<span data-ttu-id="ad983-106">Sie können die Leistung aller Instanzen von [**activescripteventconsumer**](activescripteventconsumer.md) auf einem System konfigurieren, indem Sie die Werte der **Timeout** -oder **maximumscripts** -Eigenschaft in einer einzelnen Instanz von [**scriptingstandardconsumersetting**](scriptingstandardconsumersetting.md)festlegen.</span><span class="sxs-lookup"><span data-stu-id="ad983-106">You can configure the performance of all instances of [**ActiveScriptEventConsumer**](activescripteventconsumer.md) on a system by setting the values of the **Timeout** or **MaximumScripts** property in a single instance of [**ScriptingStandardConsumerSetting**](scriptingstandardconsumersetting.md).</span></span>

<span data-ttu-id="ad983-107">Das grundlegende Verfahren für die Verwendung von Standardconsumern ist immer identisch und befindet sich in [Überwachung und Reaktion auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.</span><span class="sxs-lookup"><span data-stu-id="ad983-107">The basic procedure for using standard consumers is always the same, and is located in [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span> <span data-ttu-id="ad983-108">Das folgende Verfahren, das der Basis Prozedur hinzugefügt wird, ist spezifisch für die [**activescripteventconsumer**](activescripteventconsumer.md) -Klasse und beschreibt, wie ein Ereignisconsumer erstellt wird, der ein Skript ausführt.</span><span class="sxs-lookup"><span data-stu-id="ad983-108">The following procedure that adds to the basic procedure, is specific to the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class, and describes how to create an event consumer that runs a script.</span></span>

> [!Caution]  
> <span data-ttu-id="ad983-109">Die [**activescripteventconsumer**](activescripteventconsumer.md) -Klasse verfügt über besondere Sicherheitseinschränkungen.</span><span class="sxs-lookup"><span data-stu-id="ad983-109">The [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class has special security constraints.</span></span> <span data-ttu-id="ad983-110">Dieser Standardconsumer muss von einem lokalen Mitglied der Gruppe "Administratoren" auf dem lokalen Computer konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="ad983-110">This standard consumer must be configured by a local member of the Administrators group on the local computer.</span></span> <span data-ttu-id="ad983-111">Wenn Sie ein Domänen Konto zum Erstellen des Abonnements verwenden, muss das LocalSystem-Konto über die erforderlichen Berechtigungen für die Domäne verfügen, um sicherzustellen, dass der Ersteller Mitglied der lokalen Administratoren Gruppe ist.</span><span class="sxs-lookup"><span data-stu-id="ad983-111">If you use a domain account to create the subscription, the LocalSystem account must have the necessary permissions on the domain to verify that the creator is a member of the local Administrators group.</span></span>

 

<span data-ttu-id="ad983-112">Im folgenden Verfahren wird beschrieben, wie ein Ereignisconsumer erstellt wird, der ein Skript ausführt.</span><span class="sxs-lookup"><span data-stu-id="ad983-112">The following procedure describes how to create an event consumer that executes a script.</span></span>

<span data-ttu-id="ad983-113">**So erstellen Sie einen Ereignisconsumer, der ein Skript ausführt**</span><span class="sxs-lookup"><span data-stu-id="ad983-113">**To create an event consumer that executes a script**</span></span>

1.  <span data-ttu-id="ad983-114">Schreiben Sie das Skript, das ausgeführt wird, wenn ein Ereignis stattfindet.</span><span class="sxs-lookup"><span data-stu-id="ad983-114">Write the script to run when an event takes place.</span></span>

    <span data-ttu-id="ad983-115">Sie können das Skript in einer beliebigen Sprache schreiben, aber stellen Sie sicher, dass eine Skript-Engine für die Sprache, die Sie auswählen, auf dem Computer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ad983-115">You can write the script in any language, but ensure that a scripting engine for the language that you choose is installed on your machine.</span></span> <span data-ttu-id="ad983-116">Das Skript muss keine WMI-Skript Objekte verwenden.</span><span class="sxs-lookup"><span data-stu-id="ad983-116">The script does not have to use WMI scripting objects.</span></span>

    <span data-ttu-id="ad983-117">Nur ein Administrator kann einen skriptconsumer einrichten, und das Skript wird unter den LocalSystem-Anmelde Informationen ausgeführt, die dem Consumer mit Ausnahme des Netzwerk Zugriffs umfassende Funktionen bieten.</span><span class="sxs-lookup"><span data-stu-id="ad983-117">Only an administrator can set up a script consumer, and the script runs under LocalSystem credentials, which gives broad capabilities to the consumer except for network access.</span></span> <span data-ttu-id="ad983-118">Das Skript hat jedoch keinen Zugriff auf bestimmte Benutzer Anmeldedaten, z. b. Umgebungsvariablen und Netzwerkfreigaben.</span><span class="sxs-lookup"><span data-stu-id="ad983-118">However, the script does not have access to specific user logon data, for example, environment variables and network shares.</span></span>

2.  <span data-ttu-id="ad983-119">Erstellen Sie in der MOF-Datei (Managed Object Format) eine Instanz von [**activescripteventconsumer**](activescripteventconsumer.md) , um die Ereignisse zu empfangen, die Sie in der Abfrage anfordern.</span><span class="sxs-lookup"><span data-stu-id="ad983-119">In the Managed Object Format (MOF) file, create an instance of [**ActiveScriptEventConsumer**](activescripteventconsumer.md) to receive the events you request in the query.</span></span>

    <span data-ttu-id="ad983-120">Sie können den Text des Skripts in **ScriptText** einfügen, oder Sie können den Pfad und den Dateinamen des Skripts in **scriptfilename** angeben.</span><span class="sxs-lookup"><span data-stu-id="ad983-120">You can put the text of the script in **ScriptText**, or you can specify the path and filename of the script in **ScriptFileName**.</span></span> <span data-ttu-id="ad983-121">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="ad983-121">For more information, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

3.  <span data-ttu-id="ad983-122">Erstellen Sie eine Instanz von [**\_ \_ EventFilter**](--eventfilter.md), benennen Sie Sie, und erstellen Sie dann eine Abfrage, um den Ereignistyp anzugeben, der die Ausführung des Skripts auslöst.</span><span class="sxs-lookup"><span data-stu-id="ad983-122">Create an instance of [**\_\_EventFilter**](--eventfilter.md), name it, and then create a query to specify the type of event, which triggers executing the script.</span></span>

    <span data-ttu-id="ad983-123">Weitere Informationen finden Sie unter [Abfragen mit WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="ad983-123">For more information see, [Querying with WQL](querying-with-wql.md).</span></span>

4.  <span data-ttu-id="ad983-124">Erstellen Sie eine Instanz von [**\_ \_ filtertoconsumerbinding**](--filtertoconsumerbinding.md) , um den Filter der [**activescripteventconsumer**](activescripteventconsumer.md)-Instanz zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="ad983-124">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter with the instance of [**ActiveScriptEventConsumer**](activescripteventconsumer.md).</span></span>
5.  <span data-ttu-id="ad983-125">Kompilieren Sie die MOF-Datei mit [**Mofcomp.exe**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="ad983-125">Compile the MOF file by using [**Mofcomp.exe**](mofcomp.md).</span></span>

<span data-ttu-id="ad983-126">In den Beispielen im folgenden Abschnitt werden zwei Möglichkeiten zum Implementieren eines ereignisgesteuerten Skripts veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="ad983-126">The examples in the following section show two ways to implement an event-driven script.</span></span> <span data-ttu-id="ad983-127">Im ersten Beispiel wird ein Skript verwendet, das in einer externen Datei definiert ist, und im zweiten Beispiel wird ein Skript verwendet, das in den MOF-Code integriert ist.</span><span class="sxs-lookup"><span data-stu-id="ad983-127">The first example uses a script that is defined in an external file, and the second example uses a script that is built into the MOF code.</span></span> <span data-ttu-id="ad983-128">Die Beispiele sind in MOF-Code, aber Sie können die Instanzen Programm gesteuert erstellen, indem Sie entweder die [Skript-API für WMI](scripting-api-for-wmi.md) oder die [com-API für WMI](com-api-for-wmi.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="ad983-128">The examples are in MOF code, but you can create the instances programmatically by using either the [Scripting API for WMI](scripting-api-for-wmi.md) or the [COM API for WMI](com-api-for-wmi.md).</span></span>

## <a name="example-using-an-external-script"></a><span data-ttu-id="ad983-129">Beispiel für die Verwendung eines externen Skripts</span><span class="sxs-lookup"><span data-stu-id="ad983-129">Example Using an External Script</span></span>

<span data-ttu-id="ad983-130">Im folgenden Verfahren wird beschrieben, wie das Beispiel für ein externes Skript verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ad983-130">The following procedure describes how to use the external script example.</span></span>

<span data-ttu-id="ad983-131">**So verwenden Sie das externe Skript Beispiel**</span><span class="sxs-lookup"><span data-stu-id="ad983-131">**To use the external script example**</span></span>

1.  <span data-ttu-id="ad983-132">Erstellen Sie eine Datei mit dem Namen "c: \\Asec.vbs", und kopieren Sie dann das Skript in diesem Beispiel hinein.</span><span class="sxs-lookup"><span data-stu-id="ad983-132">Create a file named c:\\Asec.vbs, and then copy the script in this example into it.</span></span>
2.  <span data-ttu-id="ad983-133">Kopieren Sie die MOF-Liste in eine Textdatei, und speichern Sie Sie mit der Erweiterung MOF.</span><span class="sxs-lookup"><span data-stu-id="ad983-133">Copy the MOF list into a text file and save it with a .mof extension.</span></span>
3.  <span data-ttu-id="ad983-134">Kompilieren Sie die MOF-Datei in einem Eingabe Aufforderungs Fenster mit dem folgenden Befehl.</span><span class="sxs-lookup"><span data-stu-id="ad983-134">In a command prompt window, compile the MOF file by using the following command.</span></span>

    <span data-ttu-id="ad983-135">" **Mamacomp** *filename \* \* *. MOF* "*</span><span class="sxs-lookup"><span data-stu-id="ad983-135">**Mofcomp** *filename\*\*\*.mof*\*</span></span>

4.  <span data-ttu-id="ad983-136">Führen Sie den Rechner aus, mit dem ein calc.exe Prozess erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ad983-136">Run the Calculator, which creates a calc.exe process.</span></span> <span data-ttu-id="ad983-137">Warten Sie länger als fünf Sekunden, schließen Sie das Rechner Fenster, und suchen Sie dann im Verzeichnis "C:" \\ nach einer Datei mit dem Namen "ASEC. log".</span><span class="sxs-lookup"><span data-stu-id="ad983-137">Wait for more than five seconds, close the Calculator window, and then look in the C:\\ directory for a file named ASEC.log.</span></span>

    <span data-ttu-id="ad983-138">Der folgende Text ähnelt dem Text, der in der Datei "ASEC. log" enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="ad983-138">The following text is similar to the text that will be contained in the ASEC.log file.</span></span>

    ``` syntax
    Time: 12/31/2002 2:56:33 PM; Entry made by: ASEC
    Application closed. UserModeTime:  1562500; 
    KernelModeTime: 3125000 [hundreds of nanoseconds]
    ```

<span data-ttu-id="ad983-139">Das folgende VBScript-Codebeispiel zeigt das Skript, das aufgerufen wird, wenn ein Ereignis vom permanenten Consumer empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="ad983-139">The following VBScript code example shows the script that is called when an event is received by the permanent consumer.</span></span> <span data-ttu-id="ad983-140">Das **targetevent** -Objekt ist eine [**\_ \_ instancedeletionevent**](--instancedeletionevent.md) -Instanz, sodass Sie eine Eigenschaft mit dem Namen **TargetInstance** hat, die eine [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process) Instanz ist, die zum Auslösen des Ereignisses verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ad983-140">The **TargetEvent** object is an [**\_\_InstanceDeletionEvent**](--instancedeletionevent.md) instance so it has a property named **TargetInstance**, which is a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) instance used to fire the event.</span></span> <span data-ttu-id="ad983-141">Die **Win32- \_ Prozess** Klasse verfügt über die Eigenschaften **UserModeTime** und **kernelmodetime** , die in der vom Skript erstellten Protokolldatei abgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ad983-141">The **Win32\_Process** class has the **UserModeTime** and **KernelModeTime** properties that are put into the log file created by the script.</span></span>


```VB
' asec.vbs script
Dim objFS, objFile
Set objFS = CreateObject("Scripting.FileSystemObject")
Set objFile = objFS.OpenTextFile("C:\ASEC.log", 8, true)
objFile.WriteLine "Time: " & Now & "; Entry made by: ASEC"

objFile.WriteLine "Application closed. UserModeTime:  " & _
    TargetEvent.TargetInstance.UserModeTime & _
    "; KernelModeTime: " & _
    TargetEvent.TargetInstance.KernelModeTime & _
    " [hundreds of nanoseconds]"
objFile.Close
```



<span data-ttu-id="ad983-142">Im folgenden MOF-Codebeispiel wird das Skript aufgerufen, wenn ein Ereignis empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="ad983-142">The following MOF code example calls the script when an event is received.</span></span> <span data-ttu-id="ad983-143">Er erstellt den Filter, den Consumer und die Bindung zwischen diesen im Namespace des Stamm **\\ Abonnements** .</span><span class="sxs-lookup"><span data-stu-id="ad983-143">It creates the filter, consumer, and the binding between them in the **root\\subscription** namespace.</span></span>

``` syntax
#pragma namespace ("\\\\.\\root\\subscription")

instance of ActiveScriptEventConsumer as $Cons
{
    Name = "ASEC";
    ScriptingEngine = "VBScript";
    ScriptFileName = "c:\\asec2.vbs";
};

instance of __EventFilter as $Filt
{
    Name = "EF";
    Query = "SELECT * FROM __InstanceDeletionEvent WITHIN 5 "
        "WHERE TargetInstance ISA \"Win32_Process\" "
        "AND TargetInstance.Name = \"calc.exe\"";
    QueryLanguage = "WQL";
    EventNamespace = "root\\cimv2";
};

instance of __FilterToConsumerBinding
{
    Filter = $Filt;
    Consumer = $Cons;
};
```

## <a name="example-using-inline-script"></a><span data-ttu-id="ad983-144">Beispiel für die Verwendung von Inline Skript</span><span class="sxs-lookup"><span data-stu-id="ad983-144">Example Using Inline Script</span></span>

<span data-ttu-id="ad983-145">Im folgenden Verfahren wird beschrieben, wie Sie das Beispiel für Inline Skripts verwenden.</span><span class="sxs-lookup"><span data-stu-id="ad983-145">The following procedure describes how to use the inline script example.</span></span>

<span data-ttu-id="ad983-146">**So verwenden Sie das Inline Skript Beispiel**</span><span class="sxs-lookup"><span data-stu-id="ad983-146">**To use the inline script example**</span></span>

1.  <span data-ttu-id="ad983-147">Kopieren Sie die MOF-Liste in diesem Abschnitt in eine Textdatei, und speichern Sie Sie mit der Erweiterung MOF.</span><span class="sxs-lookup"><span data-stu-id="ad983-147">Copy the MOF list in this section into a text file, and save it with a .mof extension.</span></span>
2.  <span data-ttu-id="ad983-148">Kompilieren Sie die MOF-Datei in einem Eingabe Aufforderungs Fenster mit dem folgenden Befehl.</span><span class="sxs-lookup"><span data-stu-id="ad983-148">In a command prompt window, compile the MOF file by using the following command.</span></span>

    <span data-ttu-id="ad983-149">" **Mamacomp** *filename \* \* *. MOF* "*</span><span class="sxs-lookup"><span data-stu-id="ad983-149">**Mofcomp** *filename\*\*\*.mof*\*</span></span>

<span data-ttu-id="ad983-150">Das folgende MOF-Codebeispiel erstellt den Filter, den Consumer und die Bindung zwischen Ihnen und enthält außerdem das Skript Inline.</span><span class="sxs-lookup"><span data-stu-id="ad983-150">The following MOF code example creates the filter, consumer, and the binding between them and also contains the script inline.</span></span>

``` syntax
#pragma namespace ("\\\\.\\root\\subscription")

instance of ActiveScriptEventConsumer as $Cons
{
    Name = "ASEC";
    ScriptingEngine = "VBScript";
    
    ScriptText =
        "Dim objFS, objFile\n"
        "Set objFS = CreateObject(\"Scripting.FileSystemObject\")\n"
        "Set objFile = objFS.OpenTextFile(\"C:\\ASEC.log\","
        " 8, true)\nobjFile.WriteLine \"Time: \" & Now & \";"
        " Entry made by: ASEC\"\nobjFile.WriteLine"
        " \"Application closed. UserModeTime:  \" & "
        "TargetEvent.TargetInstance.UserModeTime &_\n"
        "\"; KernelModeTime: \" & "
        "TargetEvent.TargetInstance.KernelModeTime "
        "& \" [hundreds of nanoseconds]\"\n"
        "objFile.Close\n";
};

instance of __EventFilter as $Filt
{
    Name = "EF";
    Query = "SELECT * FROM __InstanceDeletionEvent WITHIN 5 "
        "WHERE TargetInstance ISA \"Win32_Process\" "
        "AND TargetInstance.Name = \"calc.exe\"";
    QueryLanguage = "WQL";
    EventNamespace = "root\\cimv2";
};

instance of __FilterToConsumerBinding
{
    Filter = $Filt;
    Consumer = $Cons;
};
```

## <a name="related-topics"></a><span data-ttu-id="ad983-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ad983-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad983-152">Überwachen von und reagieren auf Ereignisse mit Standard Consumern</span><span class="sxs-lookup"><span data-stu-id="ad983-152">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 
