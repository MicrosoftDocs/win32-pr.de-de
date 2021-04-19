---
description: .
ms.assetid: d1014801-a93a-40e8-ae96-31784c192753
title: Versionsverwaltung (Windows 7 und Windows Server 2008 R2 Anwendungsqualität Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2da50dae53fd2309f1a5de10996c57a2b4ac29c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355467"
---
# <a name="versioning-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a><span data-ttu-id="7f6a6-103">Versionsverwaltung (Windows 7 und Windows Server 2008 R2 Anwendungsqualität Cookbook)</span><span class="sxs-lookup"><span data-stu-id="7f6a6-103">Versioning (Windows 7 and Windows Server 2008 R2 Application Quality Cookbook)</span></span>

<span data-ttu-id="7f6a6-104">Eines der häufigsten Anwendungs Kompatibilitätsprobleme bei Windows Internet Explorer sind die Zeichen Folgen des Benutzer-Agents (UA) und Versions Vektoren.</span><span class="sxs-lookup"><span data-stu-id="7f6a6-104">One of the most common application compatibility issues for Windows Internet Explorer is User Agent (UA) Strings and Version Vectors.</span></span> <span data-ttu-id="7f6a6-105">Windows Internet Explorer 8 führt eine neue UA-Zeichenfolge ein, um Anwendungen bei der Ermittlung zu unterstützen, welche Version Benutzer ausführen.</span><span class="sxs-lookup"><span data-stu-id="7f6a6-105">Windows Internet Explorer 8 introduces a new UA String to help applications detect which version that users are running.</span></span> <span data-ttu-id="7f6a6-106">Zusätzlich zum einfachen erhöhen des MSIE-Werts, der Internet Explorer in der UA-Zeichenfolge zugeordnet ist, fügt Internet Explorer 8 einen Wert für den Wert "Wert/4.0" hinzu, um zu ermitteln, ob Internet Explorer 8 im Kompatibilitäts Ansichtsmodus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7f6a6-106">In addition to simply increasing the MSIE value that is associated with Internet Explorer in the UA String, Internet Explorer 8 adds a Trident/4.0 value to help you detect if Internet Explorer 8 is running in Compatibility View mode.</span></span> <span data-ttu-id="7f6a6-107">Diese Änderungen sowie hart codierte Versions Prüfungen können möglicherweise Kompatibilitätsprobleme zwischen Browsern mit sich bringen.</span><span class="sxs-lookup"><span data-stu-id="7f6a6-107">These changes, plus hardcoded version checks, can potentially introduce compatibility issues between browsers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f6a6-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7f6a6-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f6a6-109">Entwerfen von Updates, die sich auf die Kompatibilität zwischen Browsern auswirken</span><span class="sxs-lookup"><span data-stu-id="7f6a6-109">Design Updates that Impact Compatibility between Browsers</span></span>](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 



