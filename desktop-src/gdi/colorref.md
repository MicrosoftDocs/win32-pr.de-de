---
Description: Der COLORREF-Wert wird verwendet, um eine RGB-Farbe anzugeben.
ms.assetid: b87d3de2-7a13-44ef-8253-c6851a75fa54
title: COLORREF (WINDEF. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 6836cfcc1b18d0b20d5e347fb83206551b27de06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "104996458"
---
# <a name="colorref"></a><span data-ttu-id="cdc5a-103">COLORREF</span><span class="sxs-lookup"><span data-stu-id="cdc5a-103">COLORREF</span></span>

<span data-ttu-id="cdc5a-104">Der COLORREF-Wert wird verwendet, um eine [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) -Farbe anzugeben.</span><span class="sxs-lookup"><span data-stu-id="cdc5a-104">The COLORREF value is used to specify an [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) color.</span></span>


```C++
typedef DWORD COLORREF;
typedef DWORD* LPCOLORREF;
```



## <a name="remarks"></a><span data-ttu-id="cdc5a-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cdc5a-105">Remarks</span></span>

<span data-ttu-id="cdc5a-106">Beim Angeben einer expliziten [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) -Farbe hat der **COLORREF** -Wert die folgende hexadezimale Form:</span><span class="sxs-lookup"><span data-stu-id="cdc5a-106">When specifying an explicit [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) color, the **COLORREF** value has the following hexadecimal form:</span></span>

`0x00bbggrr`

<span data-ttu-id="cdc5a-107">Das nieder wertige Byte enthält einen Wert für die relative Intensität von rot. Das zweite Byte enthält einen Wert für grün; Das dritte Byte enthält einen Wert für blau.</span><span class="sxs-lookup"><span data-stu-id="cdc5a-107">The low-order byte contains a value for the relative intensity of red; the second byte contains a value for green; and the third byte contains a value for blue.</span></span> <span data-ttu-id="cdc5a-108">Das höchst wertige Byte muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="cdc5a-108">The high-order byte must be zero.</span></span> <span data-ttu-id="cdc5a-109">Der maximale Wert für ein einzelnes Byte ist 0xFF.</span><span class="sxs-lookup"><span data-stu-id="cdc5a-109">The maximum value for a single byte is 0xFF.</span></span>

<span data-ttu-id="cdc5a-110">Um einen **COLORREF** -Farbwert zu erstellen, verwenden Sie das [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) -Makro.</span><span class="sxs-lookup"><span data-stu-id="cdc5a-110">To create a **COLORREF** color value, use the [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) macro.</span></span> <span data-ttu-id="cdc5a-111">Um die einzelnen Werte für die roten, grünen und blauen Komponenten eines Farbwerts zu extrahieren, verwenden Sie die Makros [**getrvalue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue), [getgvalue](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)und [getbvalue](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) .</span><span class="sxs-lookup"><span data-stu-id="cdc5a-111">To extract the individual values for the red, green, and blue components of a color value, use the [**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue), [GetGValue](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue), and [GetBValue](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) macros, respectively.</span></span>

## <a name="example"></a><span data-ttu-id="cdc5a-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="cdc5a-112">Example</span></span>

```cpp
// Color constants.
const COLORREF rgbRed   =  0x000000FF;
const COLORREF rgbGreen =  0x0000FF00;
const COLORREF rgbBlue  =  0x00FF0000;
const COLORREF rgbBlack =  0x00000000;
const COLORREF rgbWhite =  0x00FFFFFF;
```

<span data-ttu-id="cdc5a-113">Beispiel aus [klassischen Windows-Beispielen](https://github.com/microsoft/Windows-classic-samples) auf GitHub.</span><span class="sxs-lookup"><span data-stu-id="cdc5a-113">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples) on GitHub.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdc5a-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="cdc5a-114">Requirements</span></span>



| <span data-ttu-id="cdc5a-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cdc5a-115">Requirement</span></span> | <span data-ttu-id="cdc5a-116">Wert</span><span class="sxs-lookup"><span data-stu-id="cdc5a-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdc5a-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cdc5a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cdc5a-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cdc5a-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="cdc5a-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cdc5a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cdc5a-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cdc5a-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cdc5a-121">Header</span><span class="sxs-lookup"><span data-stu-id="cdc5a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdc5a-122"><dt>WINDEF. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cdc5a-122"><dt>Windef.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdc5a-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cdc5a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdc5a-124">Übersicht über Farben</span><span class="sxs-lookup"><span data-stu-id="cdc5a-124">Colors Overview</span></span>](colors.md)
</dt> <dt>

[<span data-ttu-id="cdc5a-125">Farbstrukturen</span><span class="sxs-lookup"><span data-stu-id="cdc5a-125">Color Structures</span></span>](color-structures.md)
</dt> <dt>

[<span data-ttu-id="cdc5a-126">Getbvalue</span><span class="sxs-lookup"><span data-stu-id="cdc5a-126">GetBValue</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue)
</dt> <dt>

[<span data-ttu-id="cdc5a-127">Getgvalue</span><span class="sxs-lookup"><span data-stu-id="cdc5a-127">GetGValue</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)
</dt> <dt>

[<span data-ttu-id="cdc5a-128">**Getrvalue**</span><span class="sxs-lookup"><span data-stu-id="cdc5a-128">**GetRValue**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue)
</dt> <dt>

[<span data-ttu-id="cdc5a-129">RGB</span><span class="sxs-lookup"><span data-stu-id="cdc5a-129">RGB</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-rgb)
</dt> </dl>

 

 




