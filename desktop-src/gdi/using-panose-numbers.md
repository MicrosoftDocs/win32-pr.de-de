---
description: TrueType-Schriftart Dateien enthalten Panose-Zahlen, die Anwendungen verwenden können, um eine Schriftart auszuwählen, die ihren Spezifikationen genau entspricht.
ms.assetid: 39fd56da-c744-432d-9623-92fc7d9bf5f5
title: Verwenden von Panose-Zahlen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dfa6a185e2afb05aec5fdf0e200300c7cf686a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217708"
---
# <a name="using-panose-numbers"></a><span data-ttu-id="5e8b0-103">Verwenden von Panose-Zahlen</span><span class="sxs-lookup"><span data-stu-id="5e8b0-103">Using PANOSE Numbers</span></span>

<span data-ttu-id="5e8b0-104">TrueType-Schriftart Dateien enthalten Panose-Zahlen, die Anwendungen verwenden können, um eine Schriftart auszuwählen, die ihren Spezifikationen genau entspricht.</span><span class="sxs-lookup"><span data-stu-id="5e8b0-104">TrueType font files include PANOSE numbers, which applications can use to choose a font that closely matches their specifications.</span></span> <span data-ttu-id="5e8b0-105">Das Panose-System klassifiziert Gesichter um 10 verschiedene Attribute.</span><span class="sxs-lookup"><span data-stu-id="5e8b0-105">The PANOSE system classifies faces by 10 different attributes.</span></span> <span data-ttu-id="5e8b0-106">Weitere Informationen zu diesen Attributen finden Sie unter [**Panose**](/windows/win32/api/wingdi/ns-wingdi-panose).</span><span class="sxs-lookup"><span data-stu-id="5e8b0-106">For more information about these attributes, see [**PANOSE**](/windows/win32/api/wingdi/ns-wingdi-panose).</span></span> <span data-ttu-id="5e8b0-107">Eine **Panose** -Struktur ist Teil der [**outlinetextmetric**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) -Struktur (deren Werte durch Aufrufen der [**getoutlinetextmetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) -Funktion ausgefüllt werden).</span><span class="sxs-lookup"><span data-stu-id="5e8b0-107">A **PANOSE** structure is part of the [**OUTLINETEXTMETRIC**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) structure (whose values are filled in by calling the [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) function).</span></span>

<span data-ttu-id="5e8b0-108">Die Panose-Attribute werden einzeln auf einer Skala bewertet.</span><span class="sxs-lookup"><span data-stu-id="5e8b0-108">The PANOSE attributes are rated individually on a scale.</span></span> <span data-ttu-id="5e8b0-109">Die resultierenden Werte werden verkettet, um eine Zahl zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5e8b0-109">The resulting values are concatenated to produce a number.</span></span> <span data-ttu-id="5e8b0-110">Wenn diese Zahl für eine Schriftart und eine mathematische Metrik zum Messen der Entfernungen im Panose-Bereich festgelegt ist, kann eine Anwendung die nächsten Nachbarn ermitteln.</span><span class="sxs-lookup"><span data-stu-id="5e8b0-110">Given this number for a font and a mathematical metric to measure distances in the PANOSE space, an application can determine the nearest neighbors.</span></span>

 

 



