---
title: Lauschen auf Menü Band Ereignisse
description: Das Windows-Menü Band Framework verwendet die Infrastruktur der Ereignis Ablauf Verfolgung für Windows (Event Tracing for Windows, etw), damit Entwickler lernen können, wie Benutzer mit dem Menüband Ihrer Anwendung interagieren.
ms.assetid: F29A8E41-C902-410E-BD28-653E078320E9
keywords:
- Windows-Menüband, Ereignisse
- Multifunktionsleiste, Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcbfb2c6417c1423cb785b6b80de4396146535c2
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "104316616"
---
# <a name="listening-for-ribbon-events"></a><span data-ttu-id="4d3cc-105">Lauschen auf Menü Band Ereignisse</span><span class="sxs-lookup"><span data-stu-id="4d3cc-105">Listening for Ribbon Events</span></span>

<span data-ttu-id="4d3cc-106">Das Windows-Menü Band Framework verwendet die Infrastruktur der [Ereignis Ablauf Verfolgung für Windows (Event Tracing for Windows, etw)](../etw/event-tracing-portal.md) , damit Entwickler lernen können, wie Benutzer mit dem Menüband Ihrer Anwendung interagieren.</span><span class="sxs-lookup"><span data-stu-id="4d3cc-106">The Windows Ribbon framework uses the [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) infrastructure to enable developers to learn how users are interacting with their application's ribbon.</span></span>

## <a name="introduction"></a><span data-ttu-id="4d3cc-107">Einführung</span><span class="sxs-lookup"><span data-stu-id="4d3cc-107">Introduction</span></span>

<span data-ttu-id="4d3cc-108">Der Menüband Framework-Ereignis Mechanismus ist so konzipiert, dass das Framework Multifunktionsleisten-Benutzeroberflächen Ereignisse an die Anwendung meldet, damit Sie die Benutzeraktivität überwachen, ihre Interaktionsmuster erlernen und Verwendungs Trends bewerten können.</span><span class="sxs-lookup"><span data-stu-id="4d3cc-108">The Ribbon framework event mechanism is designed such that the framework reports ribbon UI events to the application so you can monitor user activity, learn their interaction patterns, and assess usage trends.</span></span> <span data-ttu-id="4d3cc-109">Diese Informationen können verwendet werden, um die Benutzer Funktionen für zukünftige Iterationen der Menüband-APP zu verfeinern.</span><span class="sxs-lookup"><span data-stu-id="4d3cc-109">This information can be used to refine the user experience for future iterations of your ribbon app.</span></span>

<span data-ttu-id="4d3cc-110">Die Verwendung der Menü Band Framework-Ereignisse umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="4d3cc-110">Using the Ribbon framework events involves the following:</span></span>

1.  <span data-ttu-id="4d3cc-111">Die Multifunktionsleistenanwendung muss einen [etw-Listener (Event Tracing for Windows, Ereignis Ablauf Verfolgung für Windows)](../etw/event-tracing-portal.md) registrieren, um Benachrichtigungen über das Menüband-Ereignis Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="4d3cc-111">The ribbon application must register an [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) listener to receive ribbon event notifications from the Ribbon framework.</span></span>
2.  <span data-ttu-id="4d3cc-112">Das Menüband Framework löst Ereignis Rückrufe für Multifunktionsleisten-Benutzeroberflächen zur Laufzeit aus, wenn die Anwendung einen [etw-Listener (Event Tracing for Windows)](../etw/event-tracing-portal.md) registriert hat.</span><span class="sxs-lookup"><span data-stu-id="4d3cc-112">The Ribbon framework fires ribbon UI event callbacks at run time, if the application has registered an [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) listener.</span></span>

## <a name="supported-events"></a><span data-ttu-id="4d3cc-113">Unterstützte Ereignisse</span><span class="sxs-lookup"><span data-stu-id="4d3cc-113">Supported events</span></span>

<span data-ttu-id="4d3cc-114">Die für Menüband-Anwendungen verfügbar gemachten Ereignisse werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4d3cc-114">The events exposed to ribbon applications are described in the following table.</span></span> 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4d3cc-115">Ereignis</span><span class="sxs-lookup"><span data-stu-id="4d3cc-115">Event</span></span></th>
<th><span data-ttu-id="4d3cc-116">Ereignisbericht</span><span class="sxs-lookup"><span data-stu-id="4d3cc-116">Event report</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4d3cc-117">Aktivierte Registerkarte</span><span class="sxs-lookup"><span data-stu-id="4d3cc-117">Tab activated</span></span></td>
<td><span data-ttu-id="4d3cc-118">Befehls-ID</span><span class="sxs-lookup"><span data-stu-id="4d3cc-118">Command ID</span></span><br/> <span data-ttu-id="4d3cc-119">Befehlsname</span><span class="sxs-lookup"><span data-stu-id="4d3cc-119">Command name</span></span><br/> <span data-ttu-id="4d3cc-120">Ereignis Verb</span><span class="sxs-lookup"><span data-stu-id="4d3cc-120">Event verb</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d3cc-121">Kontext Registerkarte aktiviert</span><span class="sxs-lookup"><span data-stu-id="4d3cc-121">Contextual tab activated</span></span></td>
<td><span data-ttu-id="4d3cc-122">Befehls-ID</span><span class="sxs-lookup"><span data-stu-id="4d3cc-122">Command ID</span></span><br/> <span data-ttu-id="4d3cc-123">Befehlsname</span><span class="sxs-lookup"><span data-stu-id="4d3cc-123">Command name</span></span><br/> <span data-ttu-id="4d3cc-124">Ereignis Verb</span><span class="sxs-lookup"><span data-stu-id="4d3cc-124">Event verb</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d3cc-125">Anwendungsmenü geöffnet</span><span class="sxs-lookup"><span data-stu-id="4d3cc-125">Application Menu opened</span></span></td>
<td><span data-ttu-id="4d3cc-126">Ereignis Verb</span><span class="sxs-lookup"><span data-stu-id="4d3cc-126">Event verb</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d3cc-127">Anwendungsmenü geschlossen</span><span class="sxs-lookup"><span data-stu-id="4d3cc-127">Application Menu closed</span></span></td>
<td><span data-ttu-id="4d3cc-128">Ereignis Verb</span><span class="sxs-lookup"><span data-stu-id="4d3cc-128">Event verb</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d3cc-129">Menü (regulär oder Galerie) geöffnet</span><span class="sxs-lookup"><span data-stu-id="4d3cc-129">Menu (regular or gallery) opened</span></span></td>
<td><span data-ttu-id="4d3cc-130">Befehls-ID</span><span class="sxs-lookup"><span data-stu-id="4d3cc-130">Command ID</span></span><br/> <span data-ttu-id="4d3cc-131">Befehlsname</span><span class="sxs-lookup"><span data-stu-id="4d3cc-131">Command name</span></span><br/> <span data-ttu-id="4d3cc-132">Ereignis Verb</span><span class="sxs-lookup"><span data-stu-id="4d3cc-132">Event verb</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4d3cc-133">QAT-Menü Ereignisse werden nicht verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="4d3cc-133">QAT menu events are not exposed.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d3cc-134">Menü (regulär oder Katalog) geschlossen</span><span class="sxs-lookup"><span data-stu-id="4d3cc-134">Menu (regular or gallery) closed</span></span></td>
<td><span data-ttu-id="4d3cc-135">Befehls-ID</span><span class="sxs-lookup"><span data-stu-id="4d3cc-135">Command ID</span></span><br/> <span data-ttu-id="4d3cc-136">Befehlsname</span><span class="sxs-lookup"><span data-stu-id="4d3cc-136">Command name</span></span><br/> <span data-ttu-id="4d3cc-137">Ereignis Verb</span><span class="sxs-lookup"><span data-stu-id="4d3cc-137">Event verb</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4d3cc-138">QAT-Menü Ereignisse werden nicht verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="4d3cc-138">QAT menu events are not exposed.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d3cc-139">Get-Help</span><span class="sxs-lookup"><span data-stu-id="4d3cc-139">Command</span></span></td>
<td><span data-ttu-id="4d3cc-140">Befehls-ID</span><span class="sxs-lookup"><span data-stu-id="4d3cc-140">Command ID</span></span><br/> <span data-ttu-id="4d3cc-141">Befehlsname</span><span class="sxs-lookup"><span data-stu-id="4d3cc-141">Command name</span></span><br/> <span data-ttu-id="4d3cc-142">Ereignis Verb</span><span class="sxs-lookup"><span data-stu-id="4d3cc-142">Event verb</span></span><br/> <span data-ttu-id="4d3cc-143">Einer der folgenden Ereignisspeicher Orte:</span><span class="sxs-lookup"><span data-stu-id="4d3cc-143">One of the following event locations:</span></span>
<ul>
<li><span data-ttu-id="4d3cc-144">Band</span><span class="sxs-lookup"><span data-stu-id="4d3cc-144">RIBBON</span></span></li>
<li><span data-ttu-id="4d3cc-145">Quickaccesstoolbar</span><span class="sxs-lookup"><span data-stu-id="4d3cc-145">QUICKACCESSTOOLBAR</span></span></li>
<li><span data-ttu-id="4d3cc-146">Applicationmenu</span><span class="sxs-lookup"><span data-stu-id="4d3cc-146">APPLICATIONMENU</span></span></li>
<li><span data-ttu-id="4d3cc-147">Contextpopup</span><span class="sxs-lookup"><span data-stu-id="4d3cc-147">CONTEXTPOPUP</span></span></li>
</ul>
<br/> <span data-ttu-id="4d3cc-148">ID des übergeordneten Befehls</span><span class="sxs-lookup"><span data-stu-id="4d3cc-148">Parent Command ID</span></span><br/> <span data-ttu-id="4d3cc-149">Name des übergeordneten Befehls</span><span class="sxs-lookup"><span data-stu-id="4d3cc-149">Parent Command name</span></span><br/> <span data-ttu-id="4d3cc-150">Eine der folgenden Methoden zum Aufrufen:</span><span class="sxs-lookup"><span data-stu-id="4d3cc-150">One of the following invoke methods:</span></span>
<ul>
<li><span data-ttu-id="4d3cc-151">KLICKEN</span><span class="sxs-lookup"><span data-stu-id="4d3cc-151">CLICK</span></span></li>
<li><span data-ttu-id="4d3cc-152">KEYTIP</span><span class="sxs-lookup"><span data-stu-id="4d3cc-152">KEYTIP</span></span></li>
<li><span data-ttu-id="4d3cc-153">Gewünschte</span><span class="sxs-lookup"><span data-stu-id="4d3cc-153">KEYBOARD</span></span></li>
<li><span data-ttu-id="4d3cc-154">Ansprechen</span><span class="sxs-lookup"><span data-stu-id="4d3cc-154">TOUCH</span></span></li>
</ul>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4d3cc-155">Element Kataloge und Kombinations Felder enthalten den ausgewählten Element Index, enthalten aber keine Zeichen folgen-und ganzzahligen Werte.</span><span class="sxs-lookup"><span data-stu-id="4d3cc-155">Item galleries and combo boxes include the selected item index but do not include string and integer values.</span></span> <span data-ttu-id="4d3cc-156">Spinner enthalten nicht den ganzzahligen Wert.</span><span class="sxs-lookup"><span data-stu-id="4d3cc-156">Spinners do not include the integer value.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d3cc-157">Multifunktionsleiste minimiert</span><span class="sxs-lookup"><span data-stu-id="4d3cc-157">Ribbon minimized</span></span></td>
<td><span data-ttu-id="4d3cc-158">Ereignis Verb</span><span class="sxs-lookup"><span data-stu-id="4d3cc-158">Event verb</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d3cc-159">Menü Band erweitert (erweitern Sie die Schaltfläche, auf die geklickt wird oder tippen</span><span class="sxs-lookup"><span data-stu-id="4d3cc-159">Ribbon expanded (expand button clicked or tap pinned)</span></span></td>
<td><span data-ttu-id="4d3cc-160">Ereignis Verb</span><span class="sxs-lookup"><span data-stu-id="4d3cc-160">Event verb</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d3cc-161">Anwendungsmodus gewechselt</span><span class="sxs-lookup"><span data-stu-id="4d3cc-161">Application mode switched</span></span></td>
<td><span data-ttu-id="4d3cc-162">Ereignis Verb</span><span class="sxs-lookup"><span data-stu-id="4d3cc-162">Event verb</span></span><br/> <span data-ttu-id="4d3cc-163">Mode-ID (durch <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes"><strong>setmodes</strong></a>fest gelegungswert)</span><span class="sxs-lookup"><span data-stu-id="4d3cc-163">Mode ID (value set through <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes"><strong>SetModes</strong></a>)</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4d3cc-164">Die Anwendung ist dafür verantwortlich, diese Ganzzahl zu entpacken, um zu bestimmen, welche Modi festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="4d3cc-164">The application is responsible for unpacking this integer to determine which modes were set.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d3cc-165">QuickInfo angezeigt</span><span class="sxs-lookup"><span data-stu-id="4d3cc-165">Tooltip displayed</span></span></td>
<td><span data-ttu-id="4d3cc-166">Ereignis Verb</span><span class="sxs-lookup"><span data-stu-id="4d3cc-166">Event verb</span></span><br/> <span data-ttu-id="4d3cc-167">ID des übergeordneten Befehls</span><span class="sxs-lookup"><span data-stu-id="4d3cc-167">Parent Command ID</span></span><br/> <span data-ttu-id="4d3cc-168">Name des übergeordneten Befehls</span><span class="sxs-lookup"><span data-stu-id="4d3cc-168">Parent Command name</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="4d3cc-169">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4d3cc-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d3cc-170">Entwickler Handbücher für Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="4d3cc-170">Windows Ribbon Framework Developer Guides</span></span>](windowsribbon-guides-entry.md)
</dt> <dt>

[<span data-ttu-id="4d3cc-171">Deklarieren von Befehlen und Steuerelementen mit Menüband-Markup</span><span class="sxs-lookup"><span data-stu-id="4d3cc-171">Declaring Commands and Controls with Ribbon Markup</span></span>](./windowsribbon-schema.md)
</dt> <dt>

[<span data-ttu-id="4d3cc-172">Multifunktionsleisten-Benutzeroberflächen Richtlinien</span><span class="sxs-lookup"><span data-stu-id="4d3cc-172">Ribbon User Experience Guidelines</span></span>](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[<span data-ttu-id="4d3cc-173">Menüband-Entwurfsprozess</span><span class="sxs-lookup"><span data-stu-id="4d3cc-173">Ribbon Design Process</span></span>](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

