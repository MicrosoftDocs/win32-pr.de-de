---
title: Intelligenter Hintergrundübertragungsdienst (Background Intelligent Transfer Service, BITS)
description: Mit dem intelligenten Hintergrundübertragungsdienst (Background Intelligent Transfer Service, BITS) werden Dateien zwischen einem Client und einem Server übertragen (Downloads oder Uploads). Dabei werden Statusinformationen zu den Übertragungsvorgängen angezeigt.
ms.assetid: ce91f87c-8273-4a1c-99e0-ef55e2a50334
keywords:
- Intelligenter Hintergrundübertragungsdienst (Background Intelligent Transfer Service, BITS)
- Background Intelligent Transfer Service, Startseite
- BITS (siehe Background Intelligent Transfer Service)
- Herunterladen von Dateien BITS
- Bits für die Hintergrunddateiübertragung
- Hochladen von Dateien mit BITS
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 9483e297e8b48ad6466846c7eceb8d53b57d3278
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424210"
---
# <a name="background-intelligent-transfer-service"></a><span data-ttu-id="b91ef-109">Intelligenter Hintergrundübertragungsdienst (Background Intelligent Transfer Service, BITS)</span><span class="sxs-lookup"><span data-stu-id="b91ef-109">Background Intelligent Transfer Service</span></span>

## <a name="purpose"></a><span data-ttu-id="b91ef-110">Zweck</span><span class="sxs-lookup"><span data-stu-id="b91ef-110">Purpose</span></span>

<span data-ttu-id="b91ef-111">Background Intelligent Transfer Service (BITS) wird von Programmierern und Systemadministratoren verwendet, um Dateien von HTTP-Webservern und SMB-Dateifreigaben herunterzuladen oder auf diese hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="b91ef-111">Background Intelligent Transfer Service (BITS) is used by programmers and system administrators to download files from or upload files to HTTP web servers and SMB file shares.</span></span> <span data-ttu-id="b91ef-112">BITS berücksichtigt die Kosten der Übertragung sowie die Netzwerknutzung, sodass die Vordergrundarbeit des Benutzers so wenig Auswirkungen wie möglich hat.</span><span class="sxs-lookup"><span data-stu-id="b91ef-112">BITS will take the cost of the transfer into consideration, as well as the network usage so that the user's foreground work has as little impact as possible.</span></span> <span data-ttu-id="b91ef-113">BITS verarbeitet auch Netzwerküberlagerungen, wobei Übertragungen auch nach einem Neustart angehalten und automatisch fortgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="b91ef-113">BITS also handles network interuptions, pausing and automatically resuming transfers, even after a reboot.</span></span> <span data-ttu-id="b91ef-114">BITS enthält PowerShell-Cmdlets zum Erstellen und Verwalten von Übertragungen sowie das Befehlszeilenprogramm BitsAdmin.</span><span class="sxs-lookup"><span data-stu-id="b91ef-114">BITS includes PowerShell cmdlets for creating and managing transfers as well as the BitsAdmin command-line utility.</span></span>

> [!Note]  
> <span data-ttu-id="b91ef-115">BITS kann von Windows verwendet werden, um Updates auf Ihr lokales System herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="b91ef-115">BITS can be used by Windows to download updates to your local system.</span></span> <span data-ttu-id="b91ef-116">Wenn Sie ein Endbenutzer sind, der nach Möglichkeiten zur Problembehandlung ihrer BITS-Installation sucht, finden Sie weitere Informationen unter [Beheben Windows Update Probleme.](https://support.microsoft.com/help/10164/fix-windows-update-errors)</span><span class="sxs-lookup"><span data-stu-id="b91ef-116">If you are an end-user searching for ways to troubleshoot your BITS installation, see [Fix Windows Update Issues](https://support.microsoft.com/help/10164/fix-windows-update-errors).</span></span> 
 

## <a name="where-applicable"></a><span data-ttu-id="b91ef-117">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="b91ef-117">Where applicable</span></span>

<span data-ttu-id="b91ef-118">Verwenden Sie BITS für Anwendungen, die:</span><span class="sxs-lookup"><span data-stu-id="b91ef-118">Use BITS for applications that need to:</span></span>

-   <span data-ttu-id="b91ef-119">Laden Sie Dateien von einem HTTP-, REST-Webserver oder SMB-Dateiserver herunter, oder laden Sie sie hoch.</span><span class="sxs-lookup"><span data-stu-id="b91ef-119">Download from or upload files to an HTTP or REST web server or SMB file server.</span></span>
-   <span data-ttu-id="b91ef-120">Automatisches Fortsetzen von Dateiübertragungen, nachdem die Netzwerkverbindung getrennt und der Computer neu gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="b91ef-120">Automatically resume file transfers after network disconnects and computer restarts.</span></span>
-   <span data-ttu-id="b91ef-121">Beibehalten der Reaktionsfähigkeit anderer Netzwerkanwendungen.</span><span class="sxs-lookup"><span data-stu-id="b91ef-121">Preserve the responsiveness of other network applications.</span></span>
-   <span data-ttu-id="b91ef-122">Berücksichtigen Sie die Netzwerkkosten für z. B. Roamingnetzwerke.</span><span class="sxs-lookup"><span data-stu-id="b91ef-122">Be mindful of the network cost on e.g. roaming networks</span></span>
-   <span data-ttu-id="b91ef-123">Arbeiten Sie optional mit [BranchCache,](/windows-server/networking/branchcache/branchcache) um WAN-Datenverkehr (Wide Area Network) zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="b91ef-123">Optionally work with [BranchCache](/windows-server/networking/branchcache/branchcache) to optimize wide area network (WAN) traffic</span></span>

## <a name="developer-audience"></a><span data-ttu-id="b91ef-124">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="b91ef-124">Developer audience</span></span>

<span data-ttu-id="b91ef-125">BITS ist eine COM-Schnittstelle für C- und C++-Entwickler, die auch von .NET-Entwicklern verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b91ef-125">BITS is a COM interface designed for C and C++ developers that can also be used by .NET developers.</span></span> <span data-ttu-id="b91ef-126">UWP-Entwickler sollten die [Windows.Networking.BackgroundTransfer-API](/uwp/api/Windows.Networking.BackgroundTransfer) und nicht die BITS-API verwenden.</span><span class="sxs-lookup"><span data-stu-id="b91ef-126">UWP developers should use the [Windows.Networking.BackgroundTransfer](/uwp/api/Windows.Networking.BackgroundTransfer) API and not the BITS API.</span></span>

## <a name="bits-versions"></a><span data-ttu-id="b91ef-127">BITS-Versionen</span><span class="sxs-lookup"><span data-stu-id="b91ef-127">BITS versions</span></span>

<span data-ttu-id="b91ef-128">Den vollständigen Versionsverlauf und Informationen zu früheren Betriebssystemen finden Sie unter [Neues.](what-s-new.md)</span><span class="sxs-lookup"><span data-stu-id="b91ef-128">For complete version history and information on earlier operating system, see [What's New](what-s-new.md).</span></span>


## <a name="in-this-section"></a><span data-ttu-id="b91ef-129">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="b91ef-129">In this section</span></span>



| <span data-ttu-id="b91ef-130">Thema</span><span class="sxs-lookup"><span data-stu-id="b91ef-130">Topic</span></span>                                                           | <span data-ttu-id="b91ef-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b91ef-131">Description</span></span>                                                                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b91ef-132">Informationen zu BITS</span><span class="sxs-lookup"><span data-stu-id="b91ef-132">About BITS</span></span>](about-bits.md)<br/>                         | <span data-ttu-id="b91ef-133">Allgemeine Informationen zu BITS.</span><span class="sxs-lookup"><span data-stu-id="b91ef-133">General information about BITS.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="b91ef-134">Verwenden von BITS</span><span class="sxs-lookup"><span data-stu-id="b91ef-134">Using BITS</span></span>](using-bits.md)<br/>                         | <span data-ttu-id="b91ef-135">Anleitung zum Entwickeln von BITS-Clients, die Dateien zwischen einem Client und einem Server übertragen.</span><span class="sxs-lookup"><span data-stu-id="b91ef-135">Procedural guide for developing BITS clients that transfer files between a client and server.</span></span><br/>                                                                        |
| [<span data-ttu-id="b91ef-136">BITS-Referenz</span><span class="sxs-lookup"><span data-stu-id="b91ef-136">BITS Reference</span></span>](bits-reference.md)<br/>                 | <span data-ttu-id="b91ef-137">Referenzinformationen für die BITS-Programmierschnittstellen.</span><span class="sxs-lookup"><span data-stu-id="b91ef-137">Reference information for the BITS programming interfaces.</span></span> <span data-ttu-id="b91ef-138">Enthält auch Informationen zu Beispielen, Tools, Servereinstellungen für Uploadaufträge und das Uploadprotokoll.</span><span class="sxs-lookup"><span data-stu-id="b91ef-138">Also contains information about samples, tools, server settings for upload jobs, and the upload protocol.</span></span><br/> |
| [<span data-ttu-id="b91ef-139">Bewährte Methoden</span><span class="sxs-lookup"><span data-stu-id="b91ef-139">Best Practices</span></span>](best-practices-when-using-bits.md)<br/> | <span data-ttu-id="b91ef-140">Informationen, die beim Entwerfen einer Anwendung zu berücksichtigen sind, die BITS verwendet.</span><span class="sxs-lookup"><span data-stu-id="b91ef-140">Information to consider when designing an application that uses BITS.</span></span><br/>                                                                                                |



 

## <a name="additional-resources"></a><span data-ttu-id="b91ef-141">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b91ef-141">Additional resources</span></span>

<span data-ttu-id="b91ef-142">Im Folgenden finden Sie weitere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="b91ef-142">The following are additional resources.</span></span>


|    <span data-ttu-id="b91ef-143">Ressource</span><span class="sxs-lookup"><span data-stu-id="b91ef-143">Resource</span></span>         |    <span data-ttu-id="b91ef-144">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b91ef-144">Description</span></span>                                                                                                                                     |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b91ef-145">.NET-Referenz-DLL</span><span class="sxs-lookup"><span data-stu-id="b91ef-145">.NET Reference DLL</span></span>   | <span data-ttu-id="b91ef-146">Informationen zur Verwendung von BITS aus .NET mithilfe von Verweis-DLLs finden Sie unter Aufrufen von BITS aus [.NET mithilfe von Verweis-DLLs.](/windows/desktop/Bits/bits-dot-net)</span><span class="sxs-lookup"><span data-stu-id="b91ef-146">For information on using BITS from .NET using reference DLLs, see [Calling into BITS from .NET using Reference DLLs](/windows/desktop/Bits/bits-dot-net)</span></span>      |
| <span data-ttu-id="b91ef-147">.NET Wrapper</span><span class="sxs-lookup"><span data-stu-id="b91ef-147">.NET Wrapper</span></span>   | <span data-ttu-id="b91ef-148">Für andere .NET-Wrapper für BITS können Sie [nuget](https://www.nuget.org/packages?q=Tags%3A%22BITS%22) nach Projekten suchen, die mit dem BITS-Tag gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="b91ef-148">For other .NET wrappers for BITS, you can search [nuget](https://www.nuget.org/packages?q=Tags%3A%22BITS%22) for projects tagged with the BITS tag.</span></span>        |



 

 

