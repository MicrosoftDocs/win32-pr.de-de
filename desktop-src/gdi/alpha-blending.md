---
description: Alphablending wird verwendet, um eine Alphabitmap anzuzeigen, bei der es sich um eine Bitmap mit transparenten oder halbtransparenten Pixeln handelt.
ms.assetid: 52a044cc-a471-4951-adbe-32319b8e3129
title: Alphablending (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4add2aca8ac4e2d7e1b24988eb5d40f80bac259c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120285"
---
# <a name="alpha-blending-windows-gdi"></a><span data-ttu-id="0600d-103">Alphablending (Windows GDI)</span><span class="sxs-lookup"><span data-stu-id="0600d-103">Alpha Blending (Windows GDI)</span></span>

<span data-ttu-id="0600d-104">*Alphablending* wird verwendet, um eine Alphabitmap anzuzeigen, bei der es sich um eine Bitmap mit transparenten oder halbtransparenten Pixeln handelt.</span><span class="sxs-lookup"><span data-stu-id="0600d-104">*Alpha blending* is used to display an alpha bitmap, which is a bitmap that has transparent or semi-transparent pixels.</span></span> <span data-ttu-id="0600d-105">Zusätzlich zu einem roten, grünen und blauen Farbkanal verfügt jedes Pixel in einer Alphabitmap über eine Transparenzkomponente, die als *Alphakanal bezeichnet wird.*</span><span class="sxs-lookup"><span data-stu-id="0600d-105">In addition to a red, green, and blue color channel, each pixel in an alpha bitmap has a transparency component known as its *alpha channel*.</span></span> <span data-ttu-id="0600d-106">Der Alphakanal enthält in der Regel so viele Bits wie ein Farbkanal.</span><span class="sxs-lookup"><span data-stu-id="0600d-106">The alpha channel typically contains as many bits as a color channel.</span></span> <span data-ttu-id="0600d-107">Beispielsweise kann ein 8-Bit-Alphakanal 256 Transparenzebenen darstellen, von 0 (die gesamte Bitmap ist transparent) bis 255 (die gesamte Bitmap ist nicht transparent).</span><span class="sxs-lookup"><span data-stu-id="0600d-107">For example, an 8-bit alpha channel can represent 256 levels of transparency, from 0 (the entire bitmap is transparent) to 255 (the entire bitmap is opaque).</span></span>

<span data-ttu-id="0600d-108">Alphablendingmechanismen werden durch Aufrufen von [**AlphaBlend**](/windows/desktop/api/WinGdi/nf-wingdi-alphablend)aufgerufen, das auf die [**BLENDFUNCTION-Struktur**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) verweist.</span><span class="sxs-lookup"><span data-stu-id="0600d-108">Alpha blending mechanisms are invoked by calling [**AlphaBlend**](/windows/desktop/api/WinGdi/nf-wingdi-alphablend), which references the [**BLENDFUNCTION**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) structure.</span></span>

<span data-ttu-id="0600d-109">Alphawerte pro Pixel werden nur für 32-bpp BI \_ RGB unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0600d-109">Alpha values per pixel are only supported for 32-bpp BI\_RGB.</span></span> <span data-ttu-id="0600d-110">Diese Formel ist definiert als:</span><span class="sxs-lookup"><span data-stu-id="0600d-110">This formula is defined as:</span></span>


```C++
typedef struct {
  BYTE   Blue;
  BYTE   Green;
  BYTE   Red;
  BYTE   Alpha;
};
```



<span data-ttu-id="0600d-111">Dies wird im Arbeitsspeicher dargestellt, wie in der folgenden Tabelle gezeigt.</span><span class="sxs-lookup"><span data-stu-id="0600d-111">This is represented in memory as shown in the following table.</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="0600d-112">31:24</span><span class="sxs-lookup"><span data-stu-id="0600d-112">31:24</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="0600d-113">23:16</span><span class="sxs-lookup"><span data-stu-id="0600d-113">23:16</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="0600d-114">15:08</span><span class="sxs-lookup"><span data-stu-id="0600d-114">15:08</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="0600d-115">07:00</span><span class="sxs-lookup"><span data-stu-id="0600d-115">07:00</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="0600d-116">Alpha</span><span class="sxs-lookup"><span data-stu-id="0600d-116">Alpha</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="0600d-117">Red</span><span class="sxs-lookup"><span data-stu-id="0600d-117">Red</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="0600d-118">Grün</span><span class="sxs-lookup"><span data-stu-id="0600d-118">Green</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="0600d-119">Blau</span><span class="sxs-lookup"><span data-stu-id="0600d-119">Blue</span></span>
    :::column-end:::
:::row-end:::

<span data-ttu-id="0600d-120">Bitmaps können auch mit einem Transparenzfaktor angezeigt werden, der auf die gesamte Bitmap angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="0600d-120">Bitmaps may also be displayed with a transparency factor applied to the entire bitmap.</span></span> <span data-ttu-id="0600d-121">Jedes Bitmapformat kann mit einem globalen konstanten Alphawert angezeigt werden, indem **SourceConstantAlpha** in der [**BLENDFUNCTION-Struktur festlegen.**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction)</span><span class="sxs-lookup"><span data-stu-id="0600d-121">Any bitmap format can be displayed with a global constant alpha value by setting **SourceConstantAlpha** in the [**BLENDFUNCTION**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) structure.</span></span> <span data-ttu-id="0600d-122">Der globale konstante Alphawert hat 256 Transparenzebenen, von 0 (gesamte Bitmap ist vollständig transparent) bis 255 (die gesamte Bitmap ist vollständig deckend).</span><span class="sxs-lookup"><span data-stu-id="0600d-122">The global constant alpha value has 256 levels of transparency, from 0 (entire bitmap is completely transparent) to 255 (entire bitmap is completely opaque).</span></span> <span data-ttu-id="0600d-123">Der globale konstante Alphawert wird mit dem Alphawert pro Pixel kombiniert.</span><span class="sxs-lookup"><span data-stu-id="0600d-123">The global constant alpha value is combined with the per-pixel alpha value.</span></span>

<span data-ttu-id="0600d-124">Ein Beispiel finden Sie unter [AlphaBlending a Bitmap (Alphablending einer Bitmap).](alpha-blending-a-bitmap.md)</span><span class="sxs-lookup"><span data-stu-id="0600d-124">For an example, see [Alpha Blending a Bitmap](alpha-blending-a-bitmap.md).</span></span>

 

 



