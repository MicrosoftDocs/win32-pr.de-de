---
description: Alpha Blending wird zum Anzeigen einer Alpha Bitmap verwendet, bei der es sich um eine Bitmap mit transparenten oder semitransparenten Pixeln handelt.
ms.assetid: 52a044cc-a471-4951-adbe-32319b8e3129
title: Alpha Mischung (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f68cb34d189fb80d23cbb5eeec9d9006aa93a1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978825"
---
# <a name="alpha-blending-windows-gdi"></a><span data-ttu-id="be080-103">Alpha Mischung (Windows GDI)</span><span class="sxs-lookup"><span data-stu-id="be080-103">Alpha Blending (Windows GDI)</span></span>

<span data-ttu-id="be080-104">*Alpha Blending* wird zum Anzeigen einer Alpha Bitmap verwendet, bei der es sich um eine Bitmap mit transparenten oder semitransparenten Pixeln handelt.</span><span class="sxs-lookup"><span data-stu-id="be080-104">*Alpha blending* is used to display an alpha bitmap, which is a bitmap that has transparent or semi-transparent pixels.</span></span> <span data-ttu-id="be080-105">Zusätzlich zu einem roten, grünen und blauen Farbkanal weist jedes Pixel in einer Alpha Bitmap eine Transparenz Komponente auf, die als *Alphakanal* bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="be080-105">In addition to a red, green, and blue color channel, each pixel in an alpha bitmap has a transparency component known as its *alpha channel*.</span></span> <span data-ttu-id="be080-106">Der Alphakanal enthält in der Regel so viele Bits wie ein Farbkanal.</span><span class="sxs-lookup"><span data-stu-id="be080-106">The alpha channel typically contains as many bits as a color channel.</span></span> <span data-ttu-id="be080-107">Ein 8-Bit-Alphakanal kann z. b. 256 Ebenen der Transparenz darstellen, von 0 (die gesamte Bitmap ist transparent) bis 255 (die gesamte Bitmap ist nicht transparent).</span><span class="sxs-lookup"><span data-stu-id="be080-107">For example, an 8-bit alpha channel can represent 256 levels of transparency, from 0 (the entire bitmap is transparent) to 255 (the entire bitmap is opaque).</span></span>

<span data-ttu-id="be080-108">Alpha Mischungs Mechanismen werden aufgerufen, indem [**AlphaBlend**](/windows/desktop/api/WinGdi/nf-wingdi-alphablend)aufgerufen wird, das auf die [**BLENDFUNCTION**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) -Struktur verweist.</span><span class="sxs-lookup"><span data-stu-id="be080-108">Alpha blending mechanisms are invoked by calling [**AlphaBlend**](/windows/desktop/api/WinGdi/nf-wingdi-alphablend), which references the [**BLENDFUNCTION**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) structure.</span></span>

<span data-ttu-id="be080-109">Alpha Werte pro Pixel werden nur für 32-bpp-BI-RGB unterstützt \_ .</span><span class="sxs-lookup"><span data-stu-id="be080-109">Alpha values per pixel are only supported for 32-bpp BI\_RGB.</span></span> <span data-ttu-id="be080-110">Diese Formel wird wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="be080-110">This formula is defined as:</span></span>


```C++
typedef struct {
  BYTE   Blue;
  BYTE   Green;
  BYTE   Red;
  BYTE   Alpha;
};
```



<span data-ttu-id="be080-111">Dies wird im Arbeitsspeicher dargestellt, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="be080-111">This is represented in memory as shown in the following table.</span></span>



|       |       |       |       |
|-------|-------|-------|-------|
| <span data-ttu-id="be080-112">31:24</span><span class="sxs-lookup"><span data-stu-id="be080-112">31:24</span></span> | <span data-ttu-id="be080-113">23:16</span><span class="sxs-lookup"><span data-stu-id="be080-113">23:16</span></span> | <span data-ttu-id="be080-114">15:08</span><span class="sxs-lookup"><span data-stu-id="be080-114">15:08</span></span> | <span data-ttu-id="be080-115">07:00</span><span class="sxs-lookup"><span data-stu-id="be080-115">07:00</span></span> |
| <span data-ttu-id="be080-116">Alpha</span><span class="sxs-lookup"><span data-stu-id="be080-116">Alpha</span></span> | <span data-ttu-id="be080-117">Red</span><span class="sxs-lookup"><span data-stu-id="be080-117">Red</span></span>   | <span data-ttu-id="be080-118">Grün</span><span class="sxs-lookup"><span data-stu-id="be080-118">Green</span></span> | <span data-ttu-id="be080-119">Blau</span><span class="sxs-lookup"><span data-stu-id="be080-119">Blue</span></span>  |



 

<span data-ttu-id="be080-120">Bitmaps können auch mit einem auf die gesamte Bitmap angewendeten Transparenz Faktor angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="be080-120">Bitmaps may also be displayed with a transparency factor applied to the entire bitmap.</span></span> <span data-ttu-id="be080-121">Jedes Bitmap-Format kann mit einem globalen Konstanten Alpha Wert angezeigt werden, indem **SourceConstantAlpha** in der [**BLENDFUNCTION**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) -Struktur festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="be080-121">Any bitmap format can be displayed with a global constant alpha value by setting **SourceConstantAlpha** in the [**BLENDFUNCTION**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) structure.</span></span> <span data-ttu-id="be080-122">Der Wert der globalen Konstanten Alpha-Wert hat 256 Ebenen der Transparenz, von 0 (gesamte Bitmap ist vollständig transparent) bis 255 (gesamte Bitmap ist vollständig deckend).</span><span class="sxs-lookup"><span data-stu-id="be080-122">The global constant alpha value has 256 levels of transparency, from 0 (entire bitmap is completely transparent) to 255 (entire bitmap is completely opaque).</span></span> <span data-ttu-id="be080-123">Der Wert der globalen Konstanten Alpha-Wert wird mit dem Alpha Wert pro Pixel kombiniert.</span><span class="sxs-lookup"><span data-stu-id="be080-123">The global constant alpha value is combined with the per-pixel alpha value.</span></span>

<span data-ttu-id="be080-124">Ein Beispiel finden Sie unter [Alpha Blending a Bitmap](alpha-blending-a-bitmap.md).</span><span class="sxs-lookup"><span data-stu-id="be080-124">For an example, see [Alpha Blending a Bitmap](alpha-blending-a-bitmap.md).</span></span>

 

 



