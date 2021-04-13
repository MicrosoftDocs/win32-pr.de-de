---
title: Client-und Server Kompatibilität-Windows 8
description: Kompatibilität von Windows 8-und Windows Server 2012-Clients und-Servern
ms.assetid: 5067219A-EBA2-4FAF-8C17-7AB22C5EADD0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca5b685ae10b97a7b8197737944ea7231d226514
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2019
ms.locfileid: "104313968"
---
# <a name="windows-8-and-windows-server-2012-client-and-server-compatibility"></a><span data-ttu-id="134e9-103">Kompatibilität von Windows 8-und Windows Server 2012-Clients und-Servern</span><span class="sxs-lookup"><span data-stu-id="134e9-103">Windows 8 and Windows Server 2012 client and server compatibility</span></span>

<span data-ttu-id="134e9-104">In diesem Abschnitt werden Änderungen im Betriebssystem beschrieben, auf die Sie besonders achten sollten, wenn Sie sich auf die potenziellen Auswirkungen auf vorhandene apps auswirken, und wie neue apps auf Clients, auf Servern oder auf Clients und Servern entworfen werden sollten.</span><span class="sxs-lookup"><span data-stu-id="134e9-104">This section describes changes in the operating system that you should pay special attention to due to the potential impacts on existing apps and how new apps should be designed on clients, on servers, or on both clients and servers.</span></span> <span data-ttu-id="134e9-105">Im folgenden finden Sie eine Liste der Themen, die in diesem Abschnitt gruppiert nach Funktionsbereich behandelt werden:</span><span class="sxs-lookup"><span data-stu-id="134e9-105">Following is the list of topics covered in this section, grouped by feature area:</span></span>

<span data-ttu-id="134e9-106">**AppCompat**</span><span class="sxs-lookup"><span data-stu-id="134e9-106">**AppCompat**</span></span>

-   <span data-ttu-id="134e9-107">Aktualisieren von Erkennungsregeln für Sicherheitsanwendungen</span><span class="sxs-lookup"><span data-stu-id="134e9-107">Security app detection rules update</span></span>
-   <span data-ttu-id="134e9-108">Bestimmen des Shim-Status</span><span class="sxs-lookup"><span data-stu-id="134e9-108">Determining shim status</span></span>
-   <span data-ttu-id="134e9-109">Server-apps müssen ohne die servergrafikshell ausgeführt werden können</span><span class="sxs-lookup"><span data-stu-id="134e9-109">Server apps must be able to run without the Server Graphical Shell</span></span>
-   <span data-ttu-id="134e9-110">RDS-Serverkomponenten werden aus Windows 8 entfernt</span><span class="sxs-lookup"><span data-stu-id="134e9-110">RDS server components are removed from Windows 8</span></span>
-   <span data-ttu-id="134e9-111">Dateityp-und Protokoll Zuordnungs Modell</span><span class="sxs-lookup"><span data-stu-id="134e9-111">File type and protocol associations model</span></span>
-   <span data-ttu-id="134e9-112">Desktopaktivitätenmoderator</span><span class="sxs-lookup"><span data-stu-id="134e9-112">Desktop Activity Moderator</span></span>
-   <span data-ttu-id="134e9-113">.NET Framework 4,5 ist Standard, und .NET Framework 3,5 ist optional.</span><span class="sxs-lookup"><span data-stu-id="134e9-113">.NET Framework 4.5 is default and .NET Framework 3.5 is optional</span></span>
-   <span data-ttu-id="134e9-114">Desktop-Apps sind nach dem Starten des Standard Webbrowser möglicherweise nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="134e9-114">Desktop apps may not be visible after launching the default web browser</span></span>
-   <span data-ttu-id="134e9-115">Modus mit hohem Kontrast</span><span class="sxs-lookup"><span data-stu-id="134e9-115">High-contrast mode</span></span>
-   <span data-ttu-id="134e9-116">App-Manifest (ausführbare Datei)</span><span class="sxs-lookup"><span data-stu-id="134e9-116">App (executable) manifest</span></span>
-   <span data-ttu-id="134e9-117">Ein in der Warteschlange vorhandenes Modell ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="134e9-117">Queued present model is being deprecated</span></span>
-   <span data-ttu-id="134e9-118">Szenarios für den Programmkompatibilitäts-Assistenten für Windows 8</span><span class="sxs-lookup"><span data-stu-id="134e9-118">Program Compatibility Assistant scenarios for Windows 8</span></span>
-   <span data-ttu-id="134e9-119">Desktop-Mini Anwendungen entfernt</span><span class="sxs-lookup"><span data-stu-id="134e9-119">Desktop gadgets removed</span></span>

<span data-ttu-id="134e9-120">**Speicher und Datei System**</span><span class="sxs-lookup"><span data-stu-id="134e9-120">**Storage and File System**</span></span>

-   <span data-ttu-id="134e9-121">Update der Datenträger Kompatibilität im erweiterten Format (4K)</span><span class="sxs-lookup"><span data-stu-id="134e9-121">Advanced format (4K) disk compatibility update</span></span>
-   <span data-ttu-id="134e9-122">Schlanke Speicherzuweisung logischer Einheiten</span><span class="sxs-lookup"><span data-stu-id="134e9-122">Thin provisioning of logical units</span></span>
-   <span data-ttu-id="134e9-123">Erweiterter Speicher ist jetzt optional für Windows Preinstallation Environment (WinPE) und Server-SKU.</span><span class="sxs-lookup"><span data-stu-id="134e9-123">Enhanced storage is now optional for Windows Preinstallation Environment (WinPE) and server SKU</span></span>
-   <span data-ttu-id="134e9-124">Der Dienst für virtuelle Datenträger wird in die WMI-basierte Windows-Speicherverwaltungs-API (Windows-Verwaltungsinstrumentation) übertragen.</span><span class="sxs-lookup"><span data-stu-id="134e9-124">Virtual Disk Service is transitioning to the Windows Management Instrumentation (WMI)-based Windows Storage Management API</span></span>
-   <span data-ttu-id="134e9-125">Die Benutzeroberfläche der früheren Versionen wurde für lokale Volumes entfernt.</span><span class="sxs-lookup"><span data-stu-id="134e9-125">Previous versions UI removed for local volumes</span></span>
-   <span data-ttu-id="134e9-126">Storahci ersetzt msahci</span><span class="sxs-lookup"><span data-stu-id="134e9-126">StorAHCI replaces MSAHCI</span></span>
-   <span data-ttu-id="134e9-127">Windows 7-Sicherung und-Wiederherstellung als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="134e9-127">Windows 7 backup and restore deprecated</span></span>
-   <span data-ttu-id="134e9-128">Offloaded-Datenübertragungen</span><span class="sxs-lookup"><span data-stu-id="134e9-128">Offloaded data transfers</span></span>

<span data-ttu-id="134e9-129">**Andere**</span><span class="sxs-lookup"><span data-stu-id="134e9-129">**Other**</span></span>

-   <span data-ttu-id="134e9-130">Desktopfenster-Manager ist immer on.</span><span class="sxs-lookup"><span data-stu-id="134e9-130">Desktop Window Manager is always on</span></span>
-   <span data-ttu-id="134e9-131">Direct2D bietet keine Unterstützung für das Rendering in "Rich"-Metadateien in Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="134e9-131">Direct2D does not support rendering to "rich" metafiles in Internet Explorer 9</span></span>
-   <span data-ttu-id="134e9-132">Änderungen in DX9 Legacy Hardwareunterstützung</span><span class="sxs-lookup"><span data-stu-id="134e9-132">Changes in DX9 legacy hardware support</span></span>
-   <span data-ttu-id="134e9-133">MSAA ist für Windows Store-Apps nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="134e9-133">MSAA is not available to Windows Store apps</span></span>
-   <span data-ttu-id="134e9-134">Port 3 ist für NDIS 6,30-Treiber veraltet</span><span class="sxs-lookup"><span data-stu-id="134e9-134">Port 3 is deprecated for NDIS 6.30 drivers</span></span>

 

 
