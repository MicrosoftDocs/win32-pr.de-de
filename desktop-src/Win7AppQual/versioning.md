---
description: Versionierung (Cookbook zur Anwendungsqualität für Windows 7 und Windows Server 2008 R2)
ms.assetid: d1014801-a93a-40e8-ae96-31784c192753
title: Versionierung (Cookbook zur Anwendungsqualität für Windows 7 und Windows Server 2008 R2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9c3bc1f63dc236c706fd8d9bd6a6053371dd363
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103698"
---
# <a name="versioning-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a><span data-ttu-id="1c13a-103">Versionierung (Windows 7 und Windows Server 2008 R2 Application Quality Cookbook)</span><span class="sxs-lookup"><span data-stu-id="1c13a-103">Versioning (Windows 7 and Windows Server 2008 R2 Application Quality Cookbook)</span></span>

<span data-ttu-id="1c13a-104">Eines der häufigsten Anwendungskompatibilitätsprobleme für Windows Internet Explorer sind Benutzer-Agent-Zeichenfolgen (UA) und Versionsvektoren.</span><span class="sxs-lookup"><span data-stu-id="1c13a-104">One of the most common application compatibility issues for Windows Internet Explorer is User Agent (UA) Strings and Version Vectors.</span></span> <span data-ttu-id="1c13a-105">Windows Internet Explorer 8 führt eine neue UA-Zeichenfolge ein, mit der Anwendungen erkennen können, welche Version von Benutzern ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1c13a-105">Windows Internet Explorer 8 introduces a new UA String to help applications detect which version that users are running.</span></span> <span data-ttu-id="1c13a-106">Zusätzlich zum einfachen Erhöhen des MSIE-Werts, der Internet Explorer in der UA-Zeichenfolge zugeordnet ist, fügt Internet Explorer 8 einen Trident/4.0-Wert hinzu, damit Sie erkennen können, ob Internet Explorer 8 im Kompatibilitätsansicht Modus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1c13a-106">In addition to simply increasing the MSIE value that is associated with Internet Explorer in the UA String, Internet Explorer 8 adds a Trident/4.0 value to help you detect if Internet Explorer 8 is running in Compatibility View mode.</span></span> <span data-ttu-id="1c13a-107">Diese Änderungen sowie hartcodierte Versionsüberprüfungen können zu Kompatibilitätsproblemen zwischen Browsern führen.</span><span class="sxs-lookup"><span data-stu-id="1c13a-107">These changes, plus hardcoded version checks, can potentially introduce compatibility issues between browsers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c13a-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1c13a-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c13a-109">Entwurfsupdates, die sich auf die Kompatibilität zwischen Browsern auswirken</span><span class="sxs-lookup"><span data-stu-id="1c13a-109">Design Updates that Impact Compatibility between Browsers</span></span>](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 



