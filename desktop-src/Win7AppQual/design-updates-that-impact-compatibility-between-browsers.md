---
description: .
ms.assetid: F2C13FEC-5537-4B0D-BFDB-E17A42A289CB
title: Entwerfen von Updates, die sich auf die Kompatibilität zwischen Browsern auswirken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da217d761a603e2edf8f799ab638561b357151c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363414"
---
# <a name="design-updates-that-impact-compatibility-between-browsers"></a><span data-ttu-id="fc964-103">Entwerfen von Updates, die sich auf die Kompatibilität zwischen Browsern auswirken</span><span class="sxs-lookup"><span data-stu-id="fc964-103">Design Updates that Impact Compatibility between Browsers</span></span>

<span data-ttu-id="fc964-104">In diesem Abschnitt und in der folgenden Tabelle sind die vier Hauptbereiche der Kompatibilität (nicht in der Reihenfolge von vorkommen oder Rangfolge von Priorität) aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="fc964-104">This section and the following table show the four major areas of compatibility (not in order of incidence or ranking of priority).</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="fc964-105">Änderungen von Internet Explorer 6 zu Internet Explorer 7</span><span class="sxs-lookup"><span data-stu-id="fc964-105">Changes from Internet Explorer 6 to Internet Explorer 7</span></span></th>
<th><span data-ttu-id="fc964-106">Änderungen von Internet Explorer 7 in Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="fc964-106">Changes from Internet Explorer 7 to Internet Explorer 8</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fc964-107"><a href="versioning.md">Versionsverwaltung</a></span><span class="sxs-lookup"><span data-stu-id="fc964-107"><a href="versioning.md">Versioning</a></span></span></td>
<td><ul>
<li><span data-ttu-id="fc964-108">Versionsvektoren</span><span class="sxs-lookup"><span data-stu-id="fc964-108">Version Vectors</span></span></li>
<li><span data-ttu-id="fc964-109">Zeichenfolge des Benutzer-Agents</span><span class="sxs-lookup"><span data-stu-id="fc964-109">User Agent String</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="fc964-110">Versionsvektoren</span><span class="sxs-lookup"><span data-stu-id="fc964-110">Version Vectors</span></span></li>
<li><span data-ttu-id="fc964-111">Zeichenfolge des Benutzer-Agents</span><span class="sxs-lookup"><span data-stu-id="fc964-111">User Agent String</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc964-112"><a href="standards.md">Standards</a></span><span class="sxs-lookup"><span data-stu-id="fc964-112"><a href="standards.md">Standards</a></span></span></td>
<td><ul>
<li><span data-ttu-id="fc964-113">HTML 4.01-Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="fc964-113">HTML 4.01 improvements</span></span></li>
<li><span data-ttu-id="fc964-114">CSS 2.1-Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="fc964-114">CSS 2.1 improvements</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="fc964-115">Zusätzliche HTML 4.01-Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="fc964-115">Additional HTML 4.01 improvements</span></span></li>
<li><span data-ttu-id="fc964-116">Vollständige CSS 2.1-Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="fc964-116">Full CSS 2.1 compliance</span></span></li>
<li><span data-ttu-id="fc964-117">Eingeschränkte HTML 5.0-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="fc964-117">Some HTML 5.0 support</span></span></li>
<li><span data-ttu-id="fc964-118">Unterstützung der 3. Edition von ECMAScript und eingeschränkte Unterstützung der 5. Edition von ECMAScript (einschließlich systemeigenes JSON)</span><span class="sxs-lookup"><span data-stu-id="fc964-118">ECMAScript 3rd edition support and some ECMAScript 5th edition support (including native JSON)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc964-119"><a href="security.md">Security</a></span><span class="sxs-lookup"><span data-stu-id="fc964-119"><a href="security.md">Security</a></span></span></td>
<td><ul>
<li><span data-ttu-id="fc964-120">HTTPS-Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="fc964-120">HTTPS improvements</span></span></li>
<li><span data-ttu-id="fc964-121">Sicherere Skripterstellung</span><span class="sxs-lookup"><span data-stu-id="fc964-121">More secure scripting</span></span></li>
<li><span data-ttu-id="fc964-122">Geschützter Modus (Windows Vista und spätere Versionen)</span><span class="sxs-lookup"><span data-stu-id="fc964-122">Protected Mode (Windows Vista and later versions)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="fc964-123">Besserer Schutz vor Schadsoftware</span><span class="sxs-lookup"><span data-stu-id="fc964-123">Better protection from malware</span></span></li>
<li><span data-ttu-id="fc964-124">DEP/NX- und XSS-Filter standardmäßig aktiviert</span><span class="sxs-lookup"><span data-stu-id="fc964-124">DEP/NX & XSS filter on by default</span></span></li>
<li><span data-ttu-id="fc964-125">Gemischter HTTP/HTTPS-Modus</span><span class="sxs-lookup"><span data-stu-id="fc964-125">HTTP/HTTPS mixed mode</span></span></li>
<li><span data-ttu-id="fc964-126">Sichereres AJAX</span><span class="sxs-lookup"><span data-stu-id="fc964-126">AJAX more secure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc964-127"><a href="architecture.md">Architektur</a></span><span class="sxs-lookup"><span data-stu-id="fc964-127"><a href="architecture.md">Architecture</a></span></span></td>

<td><ul>
<li><span data-ttu-id="fc964-128">Lose gekoppelter Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="fc964-128">Loosely coupled Internet Explorer</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="fc964-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fc964-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc964-130">Adressierung der Anwendungskompatibilität beim Migrieren zu Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="fc964-130">Addressing Application Compatibility When Migrating to Internet Explorer 8</span></span>](addressing-application-compatibility-when-migrating-to-internet-explorer-8.md)
</dt> </dl>

 

 



