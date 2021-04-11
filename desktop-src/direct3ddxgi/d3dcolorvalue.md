---
description: Stellt einen Farbwert mit Alpha dar, der für Transparenz verwendet wird.
ms.assetid: 27A86A10-FC0E-421E-BEA7-2DEB539849BB
title: D3DCOLORVALUE-Struktur (dxgitype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLORVALUE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: 2b7d768af9e471f3183c6a400622c2b0e0719a2f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354757"
---
# <a name="d3dcolorvalue-structure-dxgitypeh"></a><span data-ttu-id="29f55-103">D3DCOLORVALUE-Struktur (dxgitype. h)</span><span class="sxs-lookup"><span data-stu-id="29f55-103">D3DCOLORVALUE structure (Dxgitype.h)</span></span>

<span data-ttu-id="29f55-104">Stellt einen Farbwert mit Alpha dar, der für Transparenz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="29f55-104">Represents a color value with alpha, which is used for transparency.</span></span>

## <a name="syntax"></a><span data-ttu-id="29f55-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="29f55-105">Syntax</span></span>


```C++
typedef struct _D3DCOLORVALUE {
  float r;
  float g;
  float b;
  float a;
} D3DCOLORVALUE;
```



## <a name="members"></a><span data-ttu-id="29f55-106">Member</span><span class="sxs-lookup"><span data-stu-id="29f55-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="29f55-107">**r**</span><span class="sxs-lookup"><span data-stu-id="29f55-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="29f55-108">Ein Gleit Komma Wert, der die rote Komponente einer Farbe angibt.</span><span class="sxs-lookup"><span data-stu-id="29f55-108">Floating-point value that specifies the red component of a color.</span></span> <span data-ttu-id="29f55-109">Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0.</span><span class="sxs-lookup"><span data-stu-id="29f55-109">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="29f55-110">Der Wert 0,0 gibt das vollständige Fehlen der roten Komponente an, während der Wert 1,0 angibt, dass Rot vollständig vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="29f55-110">A value of 0.0 indicates the complete absence of the red component, while a value of 1.0 indicates that red is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="29f55-111">**g**</span><span class="sxs-lookup"><span data-stu-id="29f55-111">**g**</span></span>
</dt> <dd>

<span data-ttu-id="29f55-112">Ein Gleit Komma Wert, der die grüne Komponente einer Farbe angibt.</span><span class="sxs-lookup"><span data-stu-id="29f55-112">Floating-point value that specifies the green component of a color.</span></span> <span data-ttu-id="29f55-113">Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0.</span><span class="sxs-lookup"><span data-stu-id="29f55-113">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="29f55-114">Der Wert 0,0 gibt das vollständige Fehlen der grünen Komponente an, während der Wert 1,0 angibt, dass grün vollständig vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="29f55-114">A value of 0.0 indicates the complete absence of the green component, while a value of 1.0 indicates that green is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="29f55-115">**b**</span><span class="sxs-lookup"><span data-stu-id="29f55-115">**b**</span></span>
</dt> <dd>

<span data-ttu-id="29f55-116">Ein Gleit Komma Wert, der die blaue Komponente einer Farbe angibt.</span><span class="sxs-lookup"><span data-stu-id="29f55-116">Floating-point value that specifies the blue component of a color.</span></span> <span data-ttu-id="29f55-117">Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0.</span><span class="sxs-lookup"><span data-stu-id="29f55-117">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="29f55-118">Der Wert 0,0 gibt das vollständige Fehlen der blauen Komponente an, während der Wert 1,0 angibt, dass Blue vollständig vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="29f55-118">A value of 0.0 indicates the complete absence of the blue component, while a value of 1.0 indicates that blue is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="29f55-119">**ein**</span><span class="sxs-lookup"><span data-stu-id="29f55-119">**a**</span></span>
</dt> <dd>

<span data-ttu-id="29f55-120">Ein Gleit Komma Wert, der die Alpha Komponente einer Farbe angibt.</span><span class="sxs-lookup"><span data-stu-id="29f55-120">Floating-point value that specifies the alpha component of a color.</span></span> <span data-ttu-id="29f55-121">Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0.</span><span class="sxs-lookup"><span data-stu-id="29f55-121">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="29f55-122">Der Wert 0,0 gibt vollständig transparent an, während der Wert 1,0 vollständig deckend angibt.</span><span class="sxs-lookup"><span data-stu-id="29f55-122">A value of 0.0 indicates fully transparent, while a value of 1.0 indicates fully opaque.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="29f55-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29f55-123">Remarks</span></span>

<span data-ttu-id="29f55-124">Sie können die Member dieser Struktur auf Werte außerhalb des Bereichs von 0 bis 1 festlegen, um ungewöhnliche Effekte zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="29f55-124">You can set the members of this structure to values outside the range of 0 through 1 to implement some unusual effects.</span></span> <span data-ttu-id="29f55-125">Werte, die größer als 1 sind, führen zu starken Lichtern, die tendenziell eine Szene auslagern.</span><span class="sxs-lookup"><span data-stu-id="29f55-125">Values greater than 1 produce strong lights that tend to wash out a scene.</span></span> <span data-ttu-id="29f55-126">Durch negative Werte werden dunkle Lichter erzeugt, die das Licht aus einer Szene entfernen.</span><span class="sxs-lookup"><span data-stu-id="29f55-126">Negative values produce dark lights that actually remove light from a scene.</span></span>

<span data-ttu-id="29f55-127">Der dxgitype. h-Headertyp: definiert [**DXGI \_ RGBA**](dxgi-rgba.md) als Alias von **D3DCOLORVALUE** wie folgt:</span><span class="sxs-lookup"><span data-stu-id="29f55-127">The DXGItype.h header type-defines [**DXGI\_RGBA**](dxgi-rgba.md) as an alias of **D3DCOLORVALUE**, as follows:</span></span>


```
typedef D3DCOLORVALUE DXGI_RGBA;
```



<span data-ttu-id="29f55-128">Sie können D3DCOLORVALUE oder [**DXGI \_ RGBA**](dxgi-rgba.md) mit [**IDXGISwapChain1:: SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1:: getbackgroundcolor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)und dem [**DXGI \_ alpha- \_ Modus**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode)verwenden.</span><span class="sxs-lookup"><span data-stu-id="29f55-128">You can use D3DCOLORVALUE or [**DXGI\_RGBA**](dxgi-rgba.md) with [**IDXGISwapChain1::SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1::GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor), and [**DXGI\_ALPHA\_MODE**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).</span></span>

## <a name="requirements"></a><span data-ttu-id="29f55-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29f55-129">Requirements</span></span>



| <span data-ttu-id="29f55-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29f55-130">Requirement</span></span> | <span data-ttu-id="29f55-131">Wert</span><span class="sxs-lookup"><span data-stu-id="29f55-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="29f55-132">Header</span><span class="sxs-lookup"><span data-stu-id="29f55-132">Header</span></span><br/> | <dl> <span data-ttu-id="29f55-133"><dt>Dxgitype. h</dt></span><span class="sxs-lookup"><span data-stu-id="29f55-133"><dt>Dxgitype.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29f55-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29f55-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29f55-135">DXGI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="29f55-135">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> <dt>

[<span data-ttu-id="29f55-136">**DXGI- \_ RGBA**</span><span class="sxs-lookup"><span data-stu-id="29f55-136">**DXGI\_RGBA**</span></span>](dxgi-rgba.md)
</dt> </dl>

 

 




