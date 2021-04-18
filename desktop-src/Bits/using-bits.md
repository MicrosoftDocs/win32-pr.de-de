---
title: Verwenden von Bits
description: Verwenden von Bits
ms.assetid: 65b69ccb-b413-4690-ac0d-774d88608bdf
keywords:
- Intelligenter Hintergrundübertragungsdienst (Background Intelligent Transfer Service, BITS)
- Background Intelligent Transfer Service, Aufgaben
- Datei Übertragungs Bits
- Verwenden von Bits-Bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5158e183ef7e7c142a481f1d89e329a9b04f422b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340523"
---
# <a name="using-bits"></a><span data-ttu-id="bf417-107">Verwenden von Bits</span><span class="sxs-lookup"><span data-stu-id="bf417-107">Using BITS</span></span>

<span data-ttu-id="bf417-108">In den folgenden Schritten wird gezeigt, wie eine Dateiübertragung mithilfe der  [Schnittstellen](bits-interfaces.md)Background Intelligent Transfer Service (Bits) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bf417-108">The following steps show how to perform a file transfer using the Background Intelligent Transfer Service (BITS)  [interfaces](bits-interfaces.md).</span></span>

<span data-ttu-id="bf417-109">**So führen Sie eine Dateiübertragung aus**</span><span class="sxs-lookup"><span data-stu-id="bf417-109">**To perform a file transfer**</span></span>

1.  [<span data-ttu-id="bf417-110">Herstellen einer Verbindung mit dem BITS-Dienst</span><span class="sxs-lookup"><span data-stu-id="bf417-110">Connect to the BITS service</span></span>](connecting-to-the-bits-service.md)
2.  [<span data-ttu-id="bf417-111">Erstellen eines Übertragungs Auftrags</span><span class="sxs-lookup"><span data-stu-id="bf417-111">Create a transfer job</span></span>](creating-a-job.md)
3.  [<span data-ttu-id="bf417-112">Hinzufügen von Dateien zum Auftrag</span><span class="sxs-lookup"><span data-stu-id="bf417-112">Add files to the job</span></span>](adding-files-to-a-job.md)
4.  [<span data-ttu-id="bf417-113">Starten des Auftrags</span><span class="sxs-lookup"><span data-stu-id="bf417-113">Start the job</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume)
5.  [<span data-ttu-id="bf417-114">Ermitteln, ob Bits die Dateien erfolgreich übertragen haben</span><span class="sxs-lookup"><span data-stu-id="bf417-114">Determine if BITS successfully transferred the files</span></span>](determining-the-status-of-a-job.md)
6.  [<span data-ttu-id="bf417-115">Auftrag beenden</span><span class="sxs-lookup"><span data-stu-id="bf417-115">Complete the job</span></span>](completing-and-canceling-a-job.md)

<span data-ttu-id="bf417-116">In den vorherigen Schritten wird gezeigt, wie Sie Dateien mithilfe der Standardeigenschaftswerte für einen Auftrag übertragen.</span><span class="sxs-lookup"><span data-stu-id="bf417-116">The previous steps show how to transfer files using the default property values for a job.</span></span> <span data-ttu-id="bf417-117">Sie können das Standardverhalten ändern, indem Sie einen oder mehrere der Eigenschaftswerte des Auftrags ändern.</span><span class="sxs-lookup"><span data-stu-id="bf417-117">You can change the default behavior by changing one or more of the job's property values.</span></span> <span data-ttu-id="bf417-118">Beispielsweise können Sie die Priorität ändern, mit der der Auftrag in Bezug auf andere Aufträge in der Warteschlange verarbeitet wird, eine eigene Proxy Einstellung angeben und registrieren, um eine Ereignis Benachrichtigung zu erhalten, wenn die Dateien von Bits übertragen wurden.</span><span class="sxs-lookup"><span data-stu-id="bf417-118">For example, you can change the priority that the job is processed relative to other jobs in the queue, specify your own proxy setting, and register to receive event notification when BITS has transferred the files.</span></span> <span data-ttu-id="bf417-119">Weitere Informationen finden Sie unter [festlegen und Abrufen der Eigenschaften eines Auftrags](setting-and-retrieving-the-properties-of-a-job.md).</span><span class="sxs-lookup"><span data-stu-id="bf417-119">For more information, see [Setting and Retrieving the Properties of a Job](setting-and-retrieving-the-properties-of-a-job.md).</span></span>

<span data-ttu-id="bf417-120">Windows PowerShell bietet einen einfachen Mechanismus zum Verwalten von vielen Bits-Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="bf417-120">Windows PowerShell provides a simple mechanism to manage many BITS tasks.</span></span> <span data-ttu-id="bf417-121">Dieser Abschnitt enthält die folgenden Themen, die zeigen, wie Windows PowerShell-Cmdlets mit Bits verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="bf417-121">This section contains the following topics that show how to use Windows PowerShell cmdlets with BITS:</span></span>

-   [<span data-ttu-id="bf417-122">Erstellen von BITS-Übertragungsaufträgen mithilfe von Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="bf417-122">Using Windows PowerShell to Create BITS Transfer Jobs</span></span>](using-windows-powershell-to-create-bits-transfer-jobs.md)
-   [<span data-ttu-id="bf417-123">Verwenden von WinRM Windows PowerShell-Cmdlets zum Verwalten von BITS-Übertragungsaufträgen</span><span class="sxs-lookup"><span data-stu-id="bf417-123">Using WinRM Windows PowerShell Cmdlets to Manage BITS Transfer Jobs</span></span>](using-winrm-windows-powershell-cmdlets-to-manage-bits-transfer-jobs.md)
-   [<span data-ttu-id="bf417-124">Verwenden von WMI-Windows PowerShell-Cmdlets zum Verwalten des BITS Compact-Servers</span><span class="sxs-lookup"><span data-stu-id="bf417-124">Using WMI Windows PowerShell Cmdlets to Manage the BITS Compact Server</span></span>](using-wmi-windows-powershell-cmdlets-to-manage-the-bits-compact-server.md)

> [!Note]
>
> <span data-ttu-id="bf417-125">Ab Windows 10, Version 1607, können Sie auch PowerShell-Cmdlets ausführen und BITSAdmin oder andere Anwendungen verwenden, die die Bits- [Schnittstellen](bits-interfaces.md) über eine PowerShell-Remote Befehlszeile verwenden, die mit einem anderen Computer (physisch oder virtuell) verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="bf417-125">Starting with Windows 10, version 1607, you can also run PowerShell Cmdlets and use BITSAdmin or other applications that use the BITS [interfaces](bits-interfaces.md) from a PowerShell Remote command line connected to another machine (physical or virtual).</span></span> <span data-ttu-id="bf417-126">Diese Funktion ist nicht verfügbar, wenn Sie eine [PowerShell Direct](/virtualization/hyper-v-on-windows/user_guide/vmsession) -Befehlszeile für eine virtuelle Maschine auf demselben physischen Computer verwenden, und Sie ist nicht verfügbar, wenn Sie WinRM-Cmdlets verwenden.</span><span class="sxs-lookup"><span data-stu-id="bf417-126">This capability is not available when using a [PowerShell Direct](/virtualization/hyper-v-on-windows/user_guide/vmsession) command line to a virtual machine on the same physical machine, and it is not available when using WinRM cmdlets.</span></span>
>
> <span data-ttu-id="bf417-127">Ein aus einer PowerShell-Remote Sitzung erstellter BITS-Auftrag wird unter dem Benutzerkonto Kontext der Sitzung ausgeführt und wird nur fortgesetzt, wenn mindestens eine aktive lokale Anmelde Sitzung oder eine PowerShell-Remote Sitzung mit diesem Benutzerkonto verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="bf417-127">A BITS Job created from a Remote PowerShell session will run under that session’s user account context and will only make progress when there is at least one active local logon session or Remote PowerShell session associated with that user account.</span></span> <span data-ttu-id="bf417-128">Weitere Informationen finden [Sie unter So verwalten Sie PowerShell-Remote Sitzungen](using-windows-powershell-to-create-bits-transfer-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="bf417-128">For more information, see [To manage PowerShell Remote sessions](using-windows-powershell-to-create-bits-transfer-jobs.md).</span></span>

 

<span data-ttu-id="bf417-129">Dieser Abschnitt enthält auch die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="bf417-129">This section also contains the following topics:</span></span>

-   [<span data-ttu-id="bf417-130">Bewährte Methoden bei der Verwendung von Bits</span><span class="sxs-lookup"><span data-stu-id="bf417-130">Best Practices When Using BITS</span></span>](best-practices-when-using-bits.md)
-   [<span data-ttu-id="bf417-131">Auflisten von Aufträgen in der Übertragungs Warteschlange</span><span class="sxs-lookup"><span data-stu-id="bf417-131">Enumerating jobs in the transfer queue</span></span>](enumerating-jobs-in-the-transfer-queue.md)
-   [<span data-ttu-id="bf417-132">Auflisten von Dateien in einem Auftrag</span><span class="sxs-lookup"><span data-stu-id="bf417-132">Enumerating files in a job</span></span>](enumerating-files-in-a-job.md)
-   [<span data-ttu-id="bf417-133">Behandlung von Fehlern</span><span class="sxs-lookup"><span data-stu-id="bf417-133">Handling errors</span></span>](handling-errors.md)
-   [<span data-ttu-id="bf417-134">Abrufen der Antwort von einem Upload-Antwort-Auftrag</span><span class="sxs-lookup"><span data-stu-id="bf417-134">Retrieve the reply from an upload-reply job</span></span>](retrieving-the-reply-from-an-upload-reply-job.md)

<span data-ttu-id="bf417-135">Beispielcode, der die Bits-Schnittstellen verwendet, finden Sie unter [Bits-Beispiele und-Tools](bits-samples-and-tools.md).</span><span class="sxs-lookup"><span data-stu-id="bf417-135">For sample code that uses the BITS interfaces, see [BITS Samples and Tools](bits-samples-and-tools.md).</span></span>

 

 