---
title: Font-Anweisung
description: Definiert die Schriftart, mit der das System Text im Dialogfeld zeichnet. Die Schriftart muss bereits geladen worden sein. beispielsweise durch Aufrufen der LoadResource-Funktion.
ms.assetid: d7b0f382-bc45-4405-a30e-0b571fdfd1db
keywords:
- Font-Anweisungs Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- FONT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4b31b280a5a973301e8410f1f74340138af07ba
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104473052"
---
# <a name="font-statement"></a><span data-ttu-id="61ca9-105">Font-Anweisung</span><span class="sxs-lookup"><span data-stu-id="61ca9-105">FONT statement</span></span>

<span data-ttu-id="61ca9-106">Definiert die Schriftart, mit der das System Text im Dialogfeld zeichnet.</span><span class="sxs-lookup"><span data-stu-id="61ca9-106">Defines the font with which the system will draw text in the dialog box.</span></span> <span data-ttu-id="61ca9-107">Die Schriftart muss bereits geladen worden sein. beispielsweise durch Aufrufen der [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="61ca9-107">The font must have been previously loaded; for example, by calling the [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) function.</span></span>

``` syntax
FONT pointsize, "typeface", weight, italic, charset
```

<dl> <dt>

<span data-ttu-id="61ca9-108"><span id="pointsize"></span><span id="POINTSIZE"></span>*pointsize*</span><span class="sxs-lookup"><span data-stu-id="61ca9-108"><span id="pointsize"></span><span id="POINTSIZE"></span>*pointsize*</span></span>
</dt> <dd>

<span data-ttu-id="61ca9-109">Die Größe der Schriftart in Punkten.</span><span class="sxs-lookup"><span data-stu-id="61ca9-109">The size of the font, in points.</span></span>

</dd> <dt>

<span data-ttu-id="61ca9-110"><span id="typeface"></span><span id="TYPEFACE"></span>*Gotik*</span><span class="sxs-lookup"><span data-stu-id="61ca9-110"><span id="typeface"></span><span id="TYPEFACE"></span>*typeface*</span></span>
</dt> <dd>

<span data-ttu-id="61ca9-111">Der Name der Schriftart.</span><span class="sxs-lookup"><span data-stu-id="61ca9-111">The name of the typeface.</span></span> <span data-ttu-id="61ca9-112">Dieser Parameter muss in Anführungszeichen (") eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="61ca9-112">This parameter must be enclosed in quotes (").</span></span>

</dd> <dt>

<span data-ttu-id="61ca9-113"><span id="weight"></span><span id="WEIGHT"></span>*Gewicht*</span><span class="sxs-lookup"><span data-stu-id="61ca9-113"><span id="weight"></span><span id="WEIGHT"></span>*weight*</span></span>
</dt> <dd>

<span data-ttu-id="61ca9-114">Die Gewichtung der Schriftart im Bereich von 0 bis 1000.</span><span class="sxs-lookup"><span data-stu-id="61ca9-114">The weight of the font in the range 0 through 1000.</span></span> <span data-ttu-id="61ca9-115">400 ist z. b. Normal, und 700 ist fett formatiert.</span><span class="sxs-lookup"><span data-stu-id="61ca9-115">For example, 400 is normal and 700 is bold.</span></span> <span data-ttu-id="61ca9-116">Wenn dieser Wert 0 ist, wird die Standard Gewichtung verwendet.</span><span class="sxs-lookup"><span data-stu-id="61ca9-116">If this value is 0, the default weight is used.</span></span> <span data-ttu-id="61ca9-117">Eine Liste der vordefinierten Werte finden Sie in den in WinGDI. h definierten **FW \_ \*** -Werten.</span><span class="sxs-lookup"><span data-stu-id="61ca9-117">For a list of predefined values, see the **FW\_\*** values defined in WinGDI.h.</span></span>

</dd> <dt>

<span data-ttu-id="61ca9-118"><span id="italic"></span><span id="ITALIC"></span>*Kursiv*</span><span class="sxs-lookup"><span data-stu-id="61ca9-118"><span id="italic"></span><span id="ITALIC"></span>*italic*</span></span>
</dt> <dd>

<span data-ttu-id="61ca9-119">Gibt eine kursiv Schrift an, wenn auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="61ca9-119">Indicates an italic font if set to TRUE.</span></span>

</dd> <dt>

<span data-ttu-id="61ca9-120"><span id="charset"></span><span id="CHARSET"></span>*charset*</span><span class="sxs-lookup"><span data-stu-id="61ca9-120"><span id="charset"></span><span id="CHARSET"></span>*charset*</span></span>
</dt> <dd>

<span data-ttu-id="61ca9-121">Der Zeichensatz.</span><span class="sxs-lookup"><span data-stu-id="61ca9-121">The character set.</span></span> <span data-ttu-id="61ca9-122">Eine Liste der Werte finden Sie unter dem **lfCharSet** -Member der [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="61ca9-122">For a list of values, see the **lfCharSet** member of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="61ca9-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="61ca9-123">Examples</span></span>

<span data-ttu-id="61ca9-124">Im folgenden Beispiel wird die Verwendung der **Font** -Anweisung veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="61ca9-124">The following example demonstrates the use of the **FONT** statement:</span></span>

``` syntax
FONT 12, "MS Shell Dlg"
```

## <a name="see-also"></a><span data-ttu-id="61ca9-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61ca9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61ca9-126">**LoadResource**</span><span class="sxs-lookup"><span data-stu-id="61ca9-126">**LoadResource**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource)
</dt> </dl>

 

 