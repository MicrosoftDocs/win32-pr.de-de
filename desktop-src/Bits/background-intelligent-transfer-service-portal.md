---
title: Intelligenter Hintergrundübertragungsdienst (Background Intelligent Transfer Service, BITS)
description: Mit dem intelligenten Hintergrundübertragungsdienst (Background Intelligent Transfer Service, BITS) werden Dateien zwischen einem Client und einem Server übertragen (Downloads oder Uploads). Dabei werden Statusinformationen zu den Übertragungsvorgängen angezeigt.
ms.assetid: ce91f87c-8273-4a1c-99e0-ef55e2a50334
keywords:
- Intelligenter Hintergrundübertragungsdienst (Background Intelligent Transfer Service, BITS)
- Background Intelligent Transfer Service, Startseite
- Bits (siehe Background Intelligent Transfer Service)
- Herunterladen von Dateien Bits
- Hintergrunddatei-Übertragungs Bits
- Hochladen von Dateien in Bits
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: a531821665490735b391ab2714f5b37146c6bc1e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948988"
---
# <a name="background-intelligent-transfer-service"></a><span data-ttu-id="1f730-109">Intelligenter Hintergrundübertragungsdienst (Background Intelligent Transfer Service, BITS)</span><span class="sxs-lookup"><span data-stu-id="1f730-109">Background Intelligent Transfer Service</span></span>

## <a name="purpose"></a><span data-ttu-id="1f730-110">Zweck</span><span class="sxs-lookup"><span data-stu-id="1f730-110">Purpose</span></span>

<span data-ttu-id="1f730-111">Background Intelligent Transfer Service (Bits) wird von Programmierern und Systemadministratoren verwendet, um Dateien aus HTTP-Webservern und SMB-Dateifreigaben herunterzuladen oder in diese hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="1f730-111">Background Intelligent Transfer Service (BITS) is used by programmers and system administrators to download files from or upload files to HTTP web servers and SMB file shares.</span></span> <span data-ttu-id="1f730-112">Bits übernimmt die Kosten für die Übertragung sowie die Netzwerk Auslastung, sodass die Vordergrund Arbeit des Benutzers so wenig wie möglich wirkt.</span><span class="sxs-lookup"><span data-stu-id="1f730-112">BITS will take the cost of the transfer into consideration, as well as the network usage so that the user's foreground work has as little impact as possible.</span></span> <span data-ttu-id="1f730-113">Bits übernimmt auch nach einem Neustart das Übertragen von Netzwerk Überläufen, das Anhalten und Fortsetzen von Übertragungen.</span><span class="sxs-lookup"><span data-stu-id="1f730-113">BITS also handles network interuptions, pausing and automatically resuming transfers, even after a reboot.</span></span> <span data-ttu-id="1f730-114">Bits umfasst PowerShell-Cmdlets zum Erstellen und Verwalten von Übertragungen sowie das Befehlszeilenprogramm BITSAdmin.</span><span class="sxs-lookup"><span data-stu-id="1f730-114">BITS includes PowerShell cmdlets for creating and managing transfers as well as the BitsAdmin command-line utility.</span></span>

> [!Note]  
> <span data-ttu-id="1f730-115">Bits können von Windows verwendet werden, um Updates auf Ihr lokales System herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="1f730-115">BITS can be used by Windows to download updates to your local system.</span></span> <span data-ttu-id="1f730-116">Wenn Sie ein Endbenutzer sind, der nach Methoden zur Problembehandlung bei der Bits-Installation sucht, finden Sie weitere Informationen unter [Beheben von Windows Update Problemen](https://support.microsoft.com/help/10164/fix-windows-update-errors).</span><span class="sxs-lookup"><span data-stu-id="1f730-116">If you are an end-user searching for ways to troubleshoot your BITS installation, see [Fix Windows Update Issues](https://support.microsoft.com/help/10164/fix-windows-update-errors).</span></span> 
 

## <a name="where-applicable"></a><span data-ttu-id="1f730-117">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="1f730-117">Where applicable</span></span>

<span data-ttu-id="1f730-118">Verwenden Sie Bits für Anwendungen, die Folgendes erfordern:</span><span class="sxs-lookup"><span data-stu-id="1f730-118">Use BITS for applications that need to:</span></span>

-   <span data-ttu-id="1f730-119">Herunterladen von oder Hochladen von Dateien auf einen HTTP-oder Rest-Webserver oder einen SMB-Dateiserver.</span><span class="sxs-lookup"><span data-stu-id="1f730-119">Download from or upload files to an HTTP or REST web server or SMB file server.</span></span>
-   <span data-ttu-id="1f730-120">Automatisches fortsetzen von Dateiübertragungen nach dem Trennen des Netzwerks und Neustarts des Computers.</span><span class="sxs-lookup"><span data-stu-id="1f730-120">Automatically resume file transfers after network disconnects and computer restarts.</span></span>
-   <span data-ttu-id="1f730-121">Bewahren Sie die Reaktionsfähigkeit anderer Netzwerkanwendungen auf.</span><span class="sxs-lookup"><span data-stu-id="1f730-121">Preserve the responsiveness of other network applications.</span></span>
-   <span data-ttu-id="1f730-122">Berücksichtigen Sie die Netzwerkkosten, z. b. roamingnetzwerke</span><span class="sxs-lookup"><span data-stu-id="1f730-122">Be mindful of the network cost on e.g. roaming networks</span></span>
-   <span data-ttu-id="1f730-123">Optionales arbeiten mit [BranchCache](/windows-server/networking/branchcache/branchcache) zur Optimierung des WAN-Verkehrs (Wide Area Network)</span><span class="sxs-lookup"><span data-stu-id="1f730-123">Optionally work with [BranchCache](/windows-server/networking/branchcache/branchcache) to optimize wide area network (WAN) traffic</span></span>

## <a name="developer-audience"></a><span data-ttu-id="1f730-124">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="1f730-124">Developer audience</span></span>

<span data-ttu-id="1f730-125">Bits ist eine für C-und C++-Entwickler entwickelte com-Schnittstelle, die auch von .NET-Entwicklern verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="1f730-125">BITS is a COM interface designed for C and C++ developers that can also be used by .NET developers.</span></span> <span data-ttu-id="1f730-126">UWP-Entwickler sollten die [Windows. Networking. backgroundtransfer](/uwp/api/Windows.Networking.BackgroundTransfer) -API und nicht die Bits-API verwenden.</span><span class="sxs-lookup"><span data-stu-id="1f730-126">UWP developers should use the [Windows.Networking.BackgroundTransfer](/uwp/api/Windows.Networking.BackgroundTransfer) API and not the BITS API.</span></span>

## <a name="bits-versions"></a><span data-ttu-id="1f730-127">Bits-Versionen</span><span class="sxs-lookup"><span data-stu-id="1f730-127">BITS versions</span></span>

<span data-ttu-id="1f730-128">[Den](what-s-new.md)vollständigen Versionsverlauf und Informationen zum früheren Betriebssystem finden Sie unter Neuigkeiten.</span><span class="sxs-lookup"><span data-stu-id="1f730-128">For complete version history and information on earlier operating system, see [What's New](what-s-new.md).</span></span>


## <a name="in-this-section"></a><span data-ttu-id="1f730-129">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="1f730-129">In this section</span></span>



| <span data-ttu-id="1f730-130">Thema</span><span class="sxs-lookup"><span data-stu-id="1f730-130">Topic</span></span>                                                           | <span data-ttu-id="1f730-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1f730-131">Description</span></span>                                                                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1f730-132">Informationen zu BITS</span><span class="sxs-lookup"><span data-stu-id="1f730-132">About BITS</span></span>](about-bits.md)<br/>                         | <span data-ttu-id="1f730-133">Allgemeine Informationen zu Bits.</span><span class="sxs-lookup"><span data-stu-id="1f730-133">General information about BITS.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="1f730-134">Verwenden von Bits</span><span class="sxs-lookup"><span data-stu-id="1f730-134">Using BITS</span></span>](using-bits.md)<br/>                         | <span data-ttu-id="1f730-135">Verfahrens Leit Faden zum Entwickeln von BITS-Clients, die Dateien zwischen einem Client und einem Server übertragen.</span><span class="sxs-lookup"><span data-stu-id="1f730-135">Procedural guide for developing BITS clients that transfer files between a client and server.</span></span><br/>                                                                        |
| [<span data-ttu-id="1f730-136">BITS-Referenz</span><span class="sxs-lookup"><span data-stu-id="1f730-136">BITS Reference</span></span>](bits-reference.md)<br/>                 | <span data-ttu-id="1f730-137">Referenzinformationen für die Bits-Programmierschnittstellen.</span><span class="sxs-lookup"><span data-stu-id="1f730-137">Reference information for the BITS programming interfaces.</span></span> <span data-ttu-id="1f730-138">Enthält außerdem Informationen zu Beispielen, Tools, Servereinstellungen für Uploadaufträge und das uploadprotokoll.</span><span class="sxs-lookup"><span data-stu-id="1f730-138">Also contains information about samples, tools, server settings for upload jobs, and the upload protocol.</span></span><br/> |
| [<span data-ttu-id="1f730-139">Bewährte Methoden</span><span class="sxs-lookup"><span data-stu-id="1f730-139">Best Practices</span></span>](best-practices-when-using-bits.md)<br/> | <span data-ttu-id="1f730-140">Beim Entwerfen einer Anwendung, die Bits verwendet, zu berücksichtigende Informationen.</span><span class="sxs-lookup"><span data-stu-id="1f730-140">Information to consider when designing an application that uses BITS.</span></span><br/>                                                                                                |



 

## <a name="additional-resources"></a><span data-ttu-id="1f730-141">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1f730-141">Additional resources</span></span>

<span data-ttu-id="1f730-142">Im folgenden finden Sie weitere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="1f730-142">The following are additional resources.</span></span>


|             |                                                                                                                                                 |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f730-143">.Net-Referenz-dll</span><span class="sxs-lookup"><span data-stu-id="1f730-143">.NET Reference DLL</span></span>   | <span data-ttu-id="1f730-144">Informationen zur Verwendung von Bits aus .NET mithilfe von Verweis-DLLs finden Sie unter [Aufrufen von Bits aus .NET mithilfe von Verweis-DLLs](/windows/desktop/Bits/bits-dot-net) .</span><span class="sxs-lookup"><span data-stu-id="1f730-144">For information on using BITS from .NET using reference DLLs, see [Calling into BITS from .NET using Reference DLLs](/windows/desktop/Bits/bits-dot-net)</span></span>      |
| <span data-ttu-id="1f730-145">.Net-Wrapper</span><span class="sxs-lookup"><span data-stu-id="1f730-145">.NET Wrapper</span></span>   | <span data-ttu-id="1f730-146">Für andere .net-Wrapper für Bits können Sie [nuget](https://www.nuget.org/packages?q=Tags%3A%22BITS%22) nach Projekten durchsuchen, die mit dem Bits-Tag markiert sind.</span><span class="sxs-lookup"><span data-stu-id="1f730-146">For other .NET wrappers for BITS, you can search [nuget](https://www.nuget.org/packages?q=Tags%3A%22BITS%22) for projects tagged with the BITS tag.</span></span>        |



 

 

