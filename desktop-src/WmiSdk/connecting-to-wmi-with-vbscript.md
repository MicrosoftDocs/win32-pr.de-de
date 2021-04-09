---
description: WMI-Skripts können viele der Schritte, die in einem C++-Programm erforderlich sind, zusammenfassen.
ms.assetid: 77168079-7253-4DB1-8252-7016F5A58DBA
ms.tgt_platform: multiple
title: Herstellen einer Verbindung mit WMI mit VBScript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6952c42a024ebedd10d9ec8ced0bc4946d808c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866896"
---
# <a name="connecting-to-wmi-with-vbscript"></a><span data-ttu-id="0589f-103">Herstellen einer Verbindung mit WMI mit VBScript</span><span class="sxs-lookup"><span data-stu-id="0589f-103">Connecting to WMI with VBScript</span></span>

<span data-ttu-id="0589f-104">WMI-Skripts können viele der Schritte, die in einem C++-Programm erforderlich sind, zusammenfassen.</span><span class="sxs-lookup"><span data-stu-id="0589f-104">WMI scripts can condense many of the steps required in a C++ program.</span></span> <span data-ttu-id="0589f-105">Sie können eine Verbindung mit WMI herstellen, nicht nur über ein " [**Swap**](swbemlocator.md) "-Objekt, sondern auch über den Moniker "winmgmts:".</span><span class="sxs-lookup"><span data-stu-id="0589f-105">They can connect to WMI, not only through an [**SWbemLocator**](swbemlocator.md) object, but also through the moniker "winmgmts:".</span></span> <span data-ttu-id="0589f-106">Ein Moniker ist ein Kurzname, der einen Namespace, eine Klasse oder eine Instanz in WMI sucht.</span><span class="sxs-lookup"><span data-stu-id="0589f-106">A moniker is a short name that locates a namespace, class, or instance in WMI.</span></span> <span data-ttu-id="0589f-107">Der Name "winmgmts:" ist der WMI-Moniker, der den Windows Script-Host anweist, die WMI-Objekte zu verwenden, eine Verbindung mit dem Standard Namespace herstellt und ein [**Swap Services**](swbemservices.md) -Objekt abruft.</span><span class="sxs-lookup"><span data-stu-id="0589f-107">The name "winmgmts:" is the WMI moniker that tells the Windows Script Host to use the WMI objects, connects to the default namespace, and obtains an [**SWbemServices**](swbemservices.md) object.</span></span> <span data-ttu-id="0589f-108">Andere Verbindungsinformationen (z. b. eine Identitätswechsel Ebene oder eine bestimmte Klasse oder Instanz) werden in der Zeichenfolge nach dem monikernamen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0589f-108">Other connection information, such as an impersonation level or a specific class or instance, appears in the string following the moniker name.</span></span> <span data-ttu-id="0589f-109">Sie können Moniker in Aufrufen verwenden, die WMI-Objekte erstellen oder erhalten.</span><span class="sxs-lookup"><span data-stu-id="0589f-109">You can use monikers in calls that either create or get WMI objects.</span></span> <span data-ttu-id="0589f-110">Weitere Informationen finden Sie unter [Erstellen einer Monikerzeichenfolge](constructing-a-moniker-string.md).</span><span class="sxs-lookup"><span data-stu-id="0589f-110">For more information, see [Constructing a Moniker String](constructing-a-moniker-string.md).</span></span>

<span data-ttu-id="0589f-111">Im folgenden Verfahren wird beschrieben, wie mithilfe von " **Swap-Locator**" eine Verbindung mit WMI hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="0589f-111">The following procedure describes how to connect to WMI using **SWbemLocator**.</span></span>

<span data-ttu-id="0589f-112">**So stellen Sie mithilfe von "Swap Login" eine Verbindung mit WMI her**</span><span class="sxs-lookup"><span data-stu-id="0589f-112">**To connect to WMI using SWbemLocator**</span></span>

1.  <span data-ttu-id="0589f-113">Abrufen eines Serverlocatorpunkt [-Objekts mit einem Aufrufen von "](/previous-versions//xzysf6hc(v=vs.85))"</span><span class="sxs-lookup"><span data-stu-id="0589f-113">Retrieve a locator object with a call to [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).</span></span>

    ```VB
    Set Locator = CreateObject("WbemScripting.SWbemLocator")
    ```

    

2.  <span data-ttu-id="0589f-114">Melden Sie sich beim-Namespace an, indem Sie die [**ConnectServer**](swbemlocator-connectserver.md) -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="0589f-114">Log on to the namespace using a call to the [**ConnectServer**](swbemlocator-connectserver.md) method.</span></span>

    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objService = objLocator.ConnectServer(".", "root\cimv2")
    ```

    

    <span data-ttu-id="0589f-115">Wenn Sie im [**Anschluss an ConnectServer**](swbemlocator-connectserver.md)keinen Computer angeben, wird von WMI eine Verbindung mit dem lokalen Computer hergestellt.</span><span class="sxs-lookup"><span data-stu-id="0589f-115">If you do not specify a computer in the call to [**ConnectServer**](swbemlocator-connectserver.md), then WMI connects to the local computer.</span></span> <span data-ttu-id="0589f-116">Wenn Sie keinen Namespace angeben, stellt WMI eine Verbindung mit dem Namespace her, der im Registrierungsschlüssel angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="0589f-116">If you do not specify a namespace, then WMI connects to the namespace specified in the registry key.</span></span>

    <span data-ttu-id="0589f-117">**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **Scripting** \\ **Standard Namespace**</span><span class="sxs-lookup"><span data-stu-id="0589f-117">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**Scripting**\\**Default Namespace**</span></span>

    <span data-ttu-id="0589f-118">Der Standard Namespace ist \\ root \\ CIMV2.</span><span class="sxs-lookup"><span data-stu-id="0589f-118">The default namespace is \\root\\cimv2.</span></span> <span data-ttu-id="0589f-119">Weitere Informationen zu Namespaces finden Sie unter [Erstellen von Hierarchien in WMI](creating-hierarchies-within-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="0589f-119">For more information about namespaces, see [Creating Hierarchies Within WMI](creating-hierarchies-within-wmi.md).</span></span>

3.  <span data-ttu-id="0589f-120">Legen Sie die Identitätswechsel Ebene mit einem aufzurufenden Befehl der Methode " [**Swap Services. Security \_**](swbemservices-security-.md) " fest.</span><span class="sxs-lookup"><span data-stu-id="0589f-120">Set the impersonation level with a call to the [**SWbemServices.Security\_**](swbemservices-security-.md) method.</span></span>

    ```VB
    objService.Security_.ImpersonationLevel = 3 
    ```

    

    <span data-ttu-id="0589f-121">Weitere Informationen finden Sie unter [Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="0589f-121">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

4.  <span data-ttu-id="0589f-122">Implementieren Sie den Zweck des Skripts.</span><span class="sxs-lookup"><span data-stu-id="0589f-122">Implement the purpose of your script.</span></span>

    <span data-ttu-id="0589f-123">WMI macht eine Vielzahl von Skript Objekten verfügbar, die für den Zugriff auf und die Bearbeitung von Daten in Ihrem Netzwerk verwenden.</span><span class="sxs-lookup"><span data-stu-id="0589f-123">WMI exposes a variety of scripting objects that use to access and manipulate data across your network.</span></span> <span data-ttu-id="0589f-124">Weitere Informationen finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md) und der [Skript-API für WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="0589f-124">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md) and [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objService = objLocator.ConnectServer(".", "root\cimv2")
    objService.Security_.ImpersonationLevel = 3
    Set Jobs = objService.ExecQuery("SELECT * FROM Win32_ScheduledJob")
    i=0
    For each Job in Jobs
        i = i+1   
        WScript.Echo Job.JobId & "  " & Job.Command & VBNewLine
    Next
    If i = 0 Then
        WScript.Echo "No Jobs Scheduled with the AT command were found"
    End If
    ```

    

<span data-ttu-id="0589f-125">Im folgenden Verfahren wird beschrieben, wie eine Verbindung mit WMI hergestellt und ein Objekt mithilfe eines Monikers abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="0589f-125">The following procedure describes how to connect to WMI and retrieve an object using a moniker.</span></span>

<span data-ttu-id="0589f-126">**So stellen Sie eine Verbindung mit WMI her und rufen ein Objekt mithilfe eines Monikers ab**</span><span class="sxs-lookup"><span data-stu-id="0589f-126">**To connect to WMI and retrieve an object using a moniker**</span></span>

1.  <span data-ttu-id="0589f-127">Aufrufen von [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) mit einem Moniker im Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="0589f-127">Call [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) with a moniker in the input parameter.</span></span>

    ```VB
    'the simple version
    Set MyObject = GetObject("winMgmts::Win32_scheduledJob")

    'Or the more complex version
    strComputer = "."
    Set MyObject = GetObject("winMgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2:Win32_ScheduledJob")
    ```

    

    <span data-ttu-id="0589f-128">Der-Muker enthält eine Reihe von Elementen, die Sie zum Herstellen einer Verbindung mit WMI verwenden können:</span><span class="sxs-lookup"><span data-stu-id="0589f-128">The moiniker contains a number of elements that you can use to connect to WMI:</span></span>

    -   <span data-ttu-id="0589f-129">"Winmgmts:" weist WSH an, [Skript-API-Objekte](scripting-api-objects.md)zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="0589f-129">The "winmgmts:" tells WSH to use [Scripting API objects](scripting-api-objects.md).</span></span> <span data-ttu-id="0589f-130">In diesem speziellen Beispiel weiß das WSH, dass es ein-Objekt zurückgeben sollte, das das erste Win32 \_ ScheduledJob-Objekt im System beschreibt.</span><span class="sxs-lookup"><span data-stu-id="0589f-130">In this particular example, the WSH will know that it should return an SWbemObject that describes the first Win32\_scheduledJob on the system.</span></span> <span data-ttu-id="0589f-131">Andere mögliche Objekte, die zurückgegeben werden können, sind ein Austausch Auflistungs-oder ein [**Swap Services**](swbemservices.md) -Objekt, je nachdem, was der Moniker beschreibt.</span><span class="sxs-lookup"><span data-stu-id="0589f-131">Other possible objects to return would be an SWbemCollection or an [**SWbemServices**](swbemservices.md) object, depending on what the moniker described.</span></span>

    -   <span data-ttu-id="0589f-132">Optional können Sie die Sicherheitsebenen für die Verbindung festlegen.</span><span class="sxs-lookup"><span data-stu-id="0589f-132">You can optionally set the security levels for the connection.</span></span> <span data-ttu-id="0589f-133">Beachten Sie, dass Sie die Namen-und Kenn Wort Informationen jedoch nicht in einem Moniker festlegen können.</span><span class="sxs-lookup"><span data-stu-id="0589f-133">Note that you cannot set name and password information in a moniker, however.</span></span> <span data-ttu-id="0589f-134">Weitere Informationen finden Sie unter [Sichern von Skript Clients](securing-scripting-clients.md).</span><span class="sxs-lookup"><span data-stu-id="0589f-134">For more information, see [Securing Scripting Clients](securing-scripting-clients.md).</span></span>

    -   <span data-ttu-id="0589f-135">Sie können optional den Pfad zum WMI-Objekt definieren.</span><span class="sxs-lookup"><span data-stu-id="0589f-135">You can optionally define the path to the WMI object.</span></span> <span data-ttu-id="0589f-136">Dies schließt entweder den lokalen Computer oder den Remote Computer, den Namespace sowie den Namen der Klasse ein.</span><span class="sxs-lookup"><span data-stu-id="0589f-136">This includes either the local or remote computer, the namespace, as well as the name of the class.</span></span> <span data-ttu-id="0589f-137">Weitere Informationen zur Verwendung des "VBScript"- [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) in WMI-Skripts finden Sie unter [Erstellen einer Instanz](creating-an-instance.md) und [Abrufen einer WMI-Instanz](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="0589f-137">For more information about using the VBScript [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) in WMI scripts, see [Creating an Instance](creating-an-instance.md) and [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

2.  <span data-ttu-id="0589f-138">Anstatt ein einzelnes Element oder eine Auflistung abzurufen, können Sie auch das Objekt " [**Swap Services**](swbemservices.md) " (wie im vorherigen Beispiel beschrieben) abrufen.</span><span class="sxs-lookup"><span data-stu-id="0589f-138">Instead of retrieving a single item or collection, you can also choose to retrieve the [**SWbemServices**](swbemservices.md) object (as described in the previous example).</span></span> <span data-ttu-id="0589f-139">Anschließend können Sie zusätzliche Abfragen für das zurückgegebene Objekt aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="0589f-139">Afterwards, you can then call additional queries on the returned object.</span></span>

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
    Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
    For Each objJob in colScheduledJobs
        Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
    Next
    ```

    

    <span data-ttu-id="0589f-140">Im vorherigen Beispiel ist "Identitätswechsel" oder "Identitätswechsel Ebene = 3" die Standardprozess-Sicherheitsstufe.</span><span class="sxs-lookup"><span data-stu-id="0589f-140">In the previous example, impersonate, or impersonationLevel=3, is the default process security level.</span></span> <span data-ttu-id="0589f-141">Im folgenden Beispiel ist es nicht erforderlich, diese Prozess Sicherheitsebene anzugeben, es sei denn, Sie müssen die Prozesssicherheit in **delegieren** ändern.</span><span class="sxs-lookup"><span data-stu-id="0589f-141">In the following example, it is not necessary to specify this process security level unless you need to change the process security to **delegate**.</span></span> <span data-ttu-id="0589f-142">Weitere Informationen finden Sie unter [Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="0589f-142">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0589f-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0589f-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0589f-144">Skripterstellung in WMI</span><span class="sxs-lookup"><span data-stu-id="0589f-144">Scripting in WMI</span></span>](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> </dl>

 

 
