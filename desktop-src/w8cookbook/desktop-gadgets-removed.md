---
title: Desktop-Mini Anwendungen entfernt
description: Desktop-Mini Anwendungen entfernt
ms.assetid: 0074204B-F568-4F9B-A0F7-3E330B91E4CD
keywords:
- Geschenken
- Desktop Gadgets
- Windows-Rand Leiste
- Seitenleiste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c37c058a75aca82d7727566041af4c30f3bb474
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "104391105"
---
# <a name="desktop-gadgets-removed"></a><span data-ttu-id="0bc55-107">Desktop-Mini Anwendungen entfernt</span><span class="sxs-lookup"><span data-stu-id="0bc55-107">Desktop gadgets removed</span></span>

## <a name="platforms"></a><span data-ttu-id="0bc55-108">Plattformen</span><span class="sxs-lookup"><span data-stu-id="0bc55-108">Platforms</span></span>

 <span data-ttu-id="0bc55-109">**Clients** -Windows 8</span><span class="sxs-lookup"><span data-stu-id="0bc55-109">**Clients** - Windows 8</span></span>  
<span data-ttu-id="0bc55-110">**Server** -Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0bc55-110">**Servers** - Windows Server 2012</span></span>  



## <a name="description"></a><span data-ttu-id="0bc55-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0bc55-111">Description</span></span>

<span data-ttu-id="0bc55-112">Aus Funktionalitäts Sicht wurden Gadgets bereits als veraltet markiert und werden von neuen Live-Kacheln und-apps ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="0bc55-112">From a functionality standpoint, Gadgets have already been deprecated and are outclassed by new live tiles and apps.</span></span> <span data-ttu-id="0bc55-113">Mini Anwendungen stellen auch ein Sicherheitsrisiko für Benutzer dar.</span><span class="sxs-lookup"><span data-stu-id="0bc55-113">Gadgets also present a security risk to users.</span></span> <span data-ttu-id="0bc55-114">Als Plattform gibt es Sicherheitsrisiken, sodass selbst gutartige Gadgets ausgenutzt werden könnten.</span><span class="sxs-lookup"><span data-stu-id="0bc55-114">As a platform, vulnerabilities exist such that even benign Gadgets could be exploited.</span></span> <span data-ttu-id="0bc55-115">Um Windows 8 als modernes und sicheres Betriebssystem zu unterstützen, haben wir daher entschieden, Gadgets vollständig aus dem Betriebssystem zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="0bc55-115">Therefore, in order to uphold Windows 8 as our most modern and secure operating system, we have chosen to remove Gadgets from the operating system entirely.</span></span> <span data-ttu-id="0bc55-116">Windows 7-Benutzer mit Mini Anwendungen auf Ihrem Desktop werden benachrichtigt, und Gadgets werden deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="0bc55-116">Windows 7 users with Gadgets on their Desktop will be notified and Gadgets will be uninstalled.</span></span>

## <a name="manifestation"></a><span data-ttu-id="0bc55-117">Ausstrahlung</span><span class="sxs-lookup"><span data-stu-id="0bc55-117">Manifestation</span></span>

<span data-ttu-id="0bc55-118">Desktop Gadgets sind auf dem Windows-Desktop nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0bc55-118">Desktop Gadgets will not be available on the Windows Desktop.</span></span>

## <a name="mitigation"></a><span data-ttu-id="0bc55-119">Minderung</span><span class="sxs-lookup"><span data-stu-id="0bc55-119">Mitigation</span></span>

<span data-ttu-id="0bc55-120">Die Desktop Gadgets-API und die Ordnerstruktur bleiben für Windows 8 vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0bc55-120">The Desktop Gadgets API and folder structure will remain in place for Windows 8.</span></span> <span data-ttu-id="0bc55-121">Anwendungen, die Gadgets mithilfe dieser API Programm gesteuert installieren und ausführen, werden weiterhin ohne Fehler ausgeführt (obwohl die Gadgets selbst dies nicht tun werden).</span><span class="sxs-lookup"><span data-stu-id="0bc55-121">Applications which programmatically install and run Gadgets using this API will continue to run without fail (although the Gadgets themselves will not).</span></span>

## <a name="solution"></a><span data-ttu-id="0bc55-122">Lösung</span><span class="sxs-lookup"><span data-stu-id="0bc55-122">Solution</span></span>

<span data-ttu-id="0bc55-123">Entwickler von Desktop-Apps sollten Gadgets nicht in ihren Installationsprogrammen verpacken.</span><span class="sxs-lookup"><span data-stu-id="0bc55-123">Desktop app developers should not package Gadgets in their installers.</span></span> <span data-ttu-id="0bc55-124">Diese Mini Anwendungen belegen nur Speicherplatz für den Benutzer und können nicht im System ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0bc55-124">These Gadgets will just take up space for the user and will not be able to be run in the system.</span></span>

## <a name="tests"></a><span data-ttu-id="0bc55-125">Tests</span><span class="sxs-lookup"><span data-stu-id="0bc55-125">Tests</span></span>

<span data-ttu-id="0bc55-126">Entwickler können die Kompatibilität dieser Änderung testen, indem Sie die optionale Komponente für Desktop Gadgets in Windows 7 deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="0bc55-126">Developers are able to test compatibility of this change by disabling the optional component for Desktop Gadgets in Windows 7.</span></span> <span data-ttu-id="0bc55-127">Um Mini Anwendungen auf einem Windows 7-PC zu deaktivieren, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="0bc55-127">To disable Gadgets on a Windows 7 PC, follow the steps below:</span></span>

1.  <span data-ttu-id="0bc55-128">Navigieren Sie in der Systemsteuerung zum Aktivieren oder Deaktivieren von Windows-Features.</span><span class="sxs-lookup"><span data-stu-id="0bc55-128">Navigate to Turn Windows Features on or off from the Control Panel.</span></span>
2.  <span data-ttu-id="0bc55-129">Deaktivieren Sie das Kontrollkästchen neben "Windows Gadget Platform".</span><span class="sxs-lookup"><span data-stu-id="0bc55-129">Uncheck the box next to “Windows Gadget Platform”.</span></span>
3.  <span data-ttu-id="0bc55-130">Klicken Sie auf OK, und befolgen Sie alle zusätzlichen Anweisungen auf dem Bildschirm.</span><span class="sxs-lookup"><span data-stu-id="0bc55-130">Click OK and follow any additional on-screen instructions.</span></span>

## <a name="resources"></a><span data-ttu-id="0bc55-131">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0bc55-131">Resources</span></span>

[<span data-ttu-id="0bc55-132">Sicherheitsanfälligkeiten in Gadgets können Remote Code Ausführung ermöglichen</span><span class="sxs-lookup"><span data-stu-id="0bc55-132">Vulnerabilities in Gadgets Could Allow Remote Code Execution</span></span>](https://support.microsoft.com/kb/2719662)

 

 




