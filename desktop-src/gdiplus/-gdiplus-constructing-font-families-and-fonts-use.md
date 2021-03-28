---
description: Windows GDI+ gruppiert Schriftarten mit derselben Schriftart, aber unterschiedlichen Stilen in Schriftfamilien.
ms.assetid: 57428fae-6af4-47a5-a499-717dc378767a
title: Erstellen von Schriftfamilien und Schriftarten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2761923847a15be6b1ad51eec0d683129b70b349
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994295"
---
# <a name="constructing-font-families-and-fonts"></a><span data-ttu-id="9dd27-103">Erstellen von Schriftfamilien und Schriftarten</span><span class="sxs-lookup"><span data-stu-id="9dd27-103">Constructing Font Families and Fonts</span></span>

<span data-ttu-id="9dd27-104">Windows GDI+ gruppiert Schriftarten mit derselben Schriftart, aber unterschiedlichen Stilen in Schriftfamilien.</span><span class="sxs-lookup"><span data-stu-id="9dd27-104">Windows GDI+ groups fonts with the same typeface but different styles into font families.</span></span> <span data-ttu-id="9dd27-105">Beispielsweise enthält die Familie "Arial Font" die folgenden Schriftarten:</span><span class="sxs-lookup"><span data-stu-id="9dd27-105">For example, the Arial font family contains the following fonts:</span></span>

-   <span data-ttu-id="9dd27-106">Arial Normal</span><span class="sxs-lookup"><span data-stu-id="9dd27-106">Arial Regular</span></span>
-   <span data-ttu-id="9dd27-107">Arial Fett</span><span class="sxs-lookup"><span data-stu-id="9dd27-107">Arial Bold</span></span>
-   <span data-ttu-id="9dd27-108">Arial kursiv</span><span class="sxs-lookup"><span data-stu-id="9dd27-108">Arial Italic</span></span>
-   <span data-ttu-id="9dd27-109">Arial Fett kursiv</span><span class="sxs-lookup"><span data-stu-id="9dd27-109">Arial Bold Italic</span></span>

<span data-ttu-id="9dd27-110">GDI+ verwendet vier Stile zum bilden von Familien: regulär, Fett, kursiv und fett formatiert.</span><span class="sxs-lookup"><span data-stu-id="9dd27-110">GDI+ uses four styles to form families: regular, bold, italic, and bold italic.</span></span> <span data-ttu-id="9dd27-111">Adjektive, z. b. *schmale* und *abgerundete* , werden nicht als Stile betrachtet. Sie sind nicht Teil des Familiennamens.</span><span class="sxs-lookup"><span data-stu-id="9dd27-111">Adjectives such as *narrow* and *rounded* are not considered styles; rather they are part of the family name.</span></span> <span data-ttu-id="9dd27-112">Beispielsweise ist Arial Narrow eine Schriftfamilie, deren Member wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="9dd27-112">For example, Arial Narrow is a font family whose members are the following:</span></span>

-   <span data-ttu-id="9dd27-113">Arial schmale reguläre</span><span class="sxs-lookup"><span data-stu-id="9dd27-113">Arial Narrow Regular</span></span>
-   <span data-ttu-id="9dd27-114">Arial schmale Fett Formatierung</span><span class="sxs-lookup"><span data-stu-id="9dd27-114">Arial Narrow Bold</span></span>
-   <span data-ttu-id="9dd27-115">Arial, schmale kursiv</span><span class="sxs-lookup"><span data-stu-id="9dd27-115">Arial Narrow Italic</span></span>
-   <span data-ttu-id="9dd27-116">Arial schmale Fett kursiv</span><span class="sxs-lookup"><span data-stu-id="9dd27-116">Arial Narrow Bold Italic</span></span>

<span data-ttu-id="9dd27-117">Bevor Sie Text mit GDI+ zeichnen können, müssen Sie ein [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) -Objekt und ein [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) -Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="9dd27-117">Before you can draw text with GDI+, you need to construct a [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object and a [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object.</span></span> <span data-ttu-id="9dd27-118">Das **FontFamily** -Objekt gibt die Schriftart (z. b. Arial) an, und das **Font** -Objekt gibt die Größe, den Stil und die Einheiten an.</span><span class="sxs-lookup"><span data-stu-id="9dd27-118">The **FontFamily** objects specifies the typeface (for example, Arial), and the **Font** object specifies the size, style, and units.</span></span>

<span data-ttu-id="9dd27-119">Im folgenden Beispiel wird eine Schriftart mit einem regulären Stil mit einer Größe von 16 Pixeln erstellt:</span><span class="sxs-lookup"><span data-stu-id="9dd27-119">The following example constructs a regular style Arial font with a size of 16 pixels:</span></span>


```
FontFamily fontFamily(L"Arial");
Font font(&fontFamily, 16, FontStyleRegular, UnitPixel);
            
```



<span data-ttu-id="9dd27-120">Im vorangehenden Code ist das erste Argument, das an den [**Schriftart**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) -Konstruktor übergeben wird, die Adresse des [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="9dd27-120">In the preceding code, the first argument passed to the [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) constructor is the address of the [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object.</span></span> <span data-ttu-id="9dd27-121">Das zweite Argument gibt die Größe der Schriftart an, die in Einheiten gemessen wird, die durch das vierte Argument identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="9dd27-121">The second argument specifies the size of the font measured in units identified by the fourth argument.</span></span> <span data-ttu-id="9dd27-122">Das dritte Argument identifiziert den Stil.</span><span class="sxs-lookup"><span data-stu-id="9dd27-122">The third argument identifies the style.</span></span>

<span data-ttu-id="9dd27-123">[\* \* \* \* Unitpixel \* \* \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-unit) \* ist ein Member der **Unit** -Enumeration, und [\* \* \* \* fontstyleregfeiner \* \* \* \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-fontstyle) ist ein Member der **FontStyle** -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="9dd27-123">[\*\*\*\*UnitPixel\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-unit) is a member of the **Unit** enumeration, and [\*\*\*\*FontStyleRegular\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-fontstyle) is a member of the **FontStyle** enumeration.</span></span> <span data-ttu-id="9dd27-124">Beide Enumerationen werden in "gdiplusenums. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="9dd27-124">Both enumerations are declared in Gdiplusenums.h.</span></span>

 

 



