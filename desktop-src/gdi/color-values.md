---
description: Farbe ist als eine Kombination aus drei Primärfarben Rot, grün und Blau definiert.
ms.assetid: 6e44935c-2b3b-4062-8273-f1f3e70300d2
title: Farbwerte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67e46cd7ee87871c660702bed120958e7096745d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130809"
---
# <a name="color-values"></a><span data-ttu-id="4e566-103">Farbwerte</span><span class="sxs-lookup"><span data-stu-id="4e566-103">Color Values</span></span>

<span data-ttu-id="4e566-104">Farbe ist als eine Kombination aus drei Primärfarben Rot, grün und Blau definiert.</span><span class="sxs-lookup"><span data-stu-id="4e566-104">Color is defined as a combination of three primary colors red, green, and blue.</span></span> <span data-ttu-id="4e566-105">Das System identifiziert eine Farbe, indem es einen Farbwert (manchmal als RGB-dreier bezeichnet) angibt, der aus 3 8-Bit-Werten besteht, die die Intensitäten der Farbkomponenten angeben.</span><span class="sxs-lookup"><span data-stu-id="4e566-105">the system identifies a color by giving it a color value (sometimes called an RGB triplet), which consists of three 8-bit values specifying the intensities of its color components.</span></span> <span data-ttu-id="4e566-106">Schwarz hat die minimale Intensität für Rot, grün und blau, sodass der Farbwert für schwarz (0,0) ist.</span><span class="sxs-lookup"><span data-stu-id="4e566-106">Black has the minimum intensity for red, green, and blue, so the color value for black is (0, 0, 0).</span></span> <span data-ttu-id="4e566-107">Weiß hat die maximale Intensität für Rot, grün und blau, sodass der Farbwert (255, 255, 255) ist.</span><span class="sxs-lookup"><span data-stu-id="4e566-107">White has the maximum intensity for red, green, and blue, so its color value is (255, 255, 255).</span></span>

> [!Note]  
> <span data-ttu-id="4e566-108">Wenn Bild Farbabgleich aktiviert ist, hängt die Definition der Farbe und die Bedeutung eines Farbwerts vom Typ des Farbraum ab, der derzeit für den Gerätekontext festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4e566-108">If image color matching is enabled, the definition of color and the meaning of a color value depends on the type of color space that is currently set for the device context.</span></span>

 

<span data-ttu-id="4e566-109">Das System und die Anwendungen verwenden Parameter und Variablen mit dem [COLORREF](colorref.md) -Typ, um Farbwerte zu übergeben und zu speichern.</span><span class="sxs-lookup"><span data-stu-id="4e566-109">The system and applications use parameters and variables having the [COLORREF](colorref.md) type to pass and store color values.</span></span> <span data-ttu-id="4e566-110">Beispielsweise identifiziert die [**enumubjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) -Funktion die Farbe jedes Stifts, indem der **lopncolor** -Member in einer [**logpen**](/windows/win32/api/wingdi/ns-wingdi-logpen) -Struktur auf einen Farbwert festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="4e566-110">For example, the [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) function identifies the color of each pen by setting the **lopnColor** member in a [**LOGPEN**](/windows/win32/api/wingdi/ns-wingdi-logpen) structure to a color value.</span></span> <span data-ttu-id="4e566-111">Anwendungen können die einzelnen Werte der roten, grünen und blauen Komponenten aus einem Farbwert extrahieren, indem Sie die-Makros [**getrvalue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue), [**getgvalue**](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)und [**getbvalue**](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) verwenden.</span><span class="sxs-lookup"><span data-stu-id="4e566-111">Applications can extract the individual values of the red, green, and blue components from a color value by using the [**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue), [**GetGValue**](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue), and [**GetBValue**](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) macros, respectively.</span></span> <span data-ttu-id="4e566-112">Anwendungen können mit dem [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) -Makro einen Farbwert aus einzelnen Komponenten Werten erstellen.</span><span class="sxs-lookup"><span data-stu-id="4e566-112">Applications can create a color value from individual component values by using the [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) macro.</span></span> <span data-ttu-id="4e566-113">Beim Erstellen oder untersuchen einer logischen Palette verwendet eine Anwendung die [**rgbquad**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) -Struktur, um Farbwerte zu definieren und einzelne Komponenten Werte zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="4e566-113">When creating or examining a logical palette, an application uses the [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structure to define color values and to examine individual component values.</span></span>

 

 



