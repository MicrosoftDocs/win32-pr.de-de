---
description: 'D3DCOLORVALUE-Struktur (Dxgitype.h): Stellt einen Farbwert mit Alpha dar, der zur Transparenz verwendet wird.'
ms.assetid: 27A86A10-FC0E-421E-BEA7-2DEB539849BB
title: D3DCOLORVALUE-Struktur (Dxgitype.h)
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
ms.openlocfilehash: 83ca500493a04f04de5352185c240d20a19009f5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107148"
---
# <a name="d3dcolorvalue-structure-dxgitypeh"></a><span data-ttu-id="ad826-103">D3DCOLORVALUE-Struktur (Dxgitype.h)</span><span class="sxs-lookup"><span data-stu-id="ad826-103">D3DCOLORVALUE structure (Dxgitype.h)</span></span>

<span data-ttu-id="ad826-104">Stellt einen Farbwert mit Alpha dar, der zur Transparenz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ad826-104">Represents a color value with alpha, which is used for transparency.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad826-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad826-105">Syntax</span></span>


```C++
typedef struct _D3DCOLORVALUE {
  float r;
  float g;
  float b;
  float a;
} D3DCOLORVALUE;
```



## <a name="members"></a><span data-ttu-id="ad826-106">Member</span><span class="sxs-lookup"><span data-stu-id="ad826-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ad826-107">**r**</span><span class="sxs-lookup"><span data-stu-id="ad826-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="ad826-108">Gleitkommawert, der die rote Komponente einer Farbe angibt.</span><span class="sxs-lookup"><span data-stu-id="ad826-108">Floating-point value that specifies the red component of a color.</span></span> <span data-ttu-id="ad826-109">Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0.</span><span class="sxs-lookup"><span data-stu-id="ad826-109">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="ad826-110">Der Wert 0,0 gibt das vollständige Fehlen der roten Komponente an, während der Wert 1,0 angibt, dass Rot vollständig vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ad826-110">A value of 0.0 indicates the complete absence of the red component, while a value of 1.0 indicates that red is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="ad826-111">**g**</span><span class="sxs-lookup"><span data-stu-id="ad826-111">**g**</span></span>
</dt> <dd>

<span data-ttu-id="ad826-112">Gleitkommawert, der die grüne Komponente einer Farbe angibt.</span><span class="sxs-lookup"><span data-stu-id="ad826-112">Floating-point value that specifies the green component of a color.</span></span> <span data-ttu-id="ad826-113">Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0.</span><span class="sxs-lookup"><span data-stu-id="ad826-113">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="ad826-114">Der Wert 0,0 gibt das vollständige Fehlen der grünen Komponente an, während der Wert 1,0 angibt, dass grün vollständig vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ad826-114">A value of 0.0 indicates the complete absence of the green component, while a value of 1.0 indicates that green is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="ad826-115">**b**</span><span class="sxs-lookup"><span data-stu-id="ad826-115">**b**</span></span>
</dt> <dd>

<span data-ttu-id="ad826-116">Gleitkommawert, der die blaue Komponente einer Farbe angibt.</span><span class="sxs-lookup"><span data-stu-id="ad826-116">Floating-point value that specifies the blue component of a color.</span></span> <span data-ttu-id="ad826-117">Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0.</span><span class="sxs-lookup"><span data-stu-id="ad826-117">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="ad826-118">Der Wert 0,0 gibt das vollständige Fehlen der blauen Komponente an, während der Wert 1,0 angibt, dass blau vollständig vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ad826-118">A value of 0.0 indicates the complete absence of the blue component, while a value of 1.0 indicates that blue is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="ad826-119">**Eine**</span><span class="sxs-lookup"><span data-stu-id="ad826-119">**a**</span></span>
</dt> <dd>

<span data-ttu-id="ad826-120">Gleitkommawert, der die Alphakomponente einer Farbe angibt.</span><span class="sxs-lookup"><span data-stu-id="ad826-120">Floating-point value that specifies the alpha component of a color.</span></span> <span data-ttu-id="ad826-121">Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0.</span><span class="sxs-lookup"><span data-stu-id="ad826-121">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="ad826-122">Der Wert 0,0 gibt vollständig transparent an, während der Wert 1,0 für vollständig deckend steht.</span><span class="sxs-lookup"><span data-stu-id="ad826-122">A value of 0.0 indicates fully transparent, while a value of 1.0 indicates fully opaque.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ad826-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ad826-123">Remarks</span></span>

<span data-ttu-id="ad826-124">Sie können die Member dieser Struktur auf Werte außerhalb des Bereichs von 0 bis 1 festlegen, um einige ungewöhnliche Effekte zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="ad826-124">You can set the members of this structure to values outside the range of 0 through 1 to implement some unusual effects.</span></span> <span data-ttu-id="ad826-125">Werte größer als 1 erzeugen starke Lichtlichter, die dazu tendieren, eine Szene zu verwaschen.</span><span class="sxs-lookup"><span data-stu-id="ad826-125">Values greater than 1 produce strong lights that tend to wash out a scene.</span></span> <span data-ttu-id="ad826-126">Negative Werte erzeugen dunkle Lichtlichter, die tatsächlich Licht aus einer Szene entfernen.</span><span class="sxs-lookup"><span data-stu-id="ad826-126">Negative values produce dark lights that actually remove light from a scene.</span></span>

<span data-ttu-id="ad826-127">Der DXGItype.h-Headertyp definiert [**DXGI \_ RGBA**](dxgi-rgba.md) wie folgt als Alias von **D3DCOLORVALUE:**</span><span class="sxs-lookup"><span data-stu-id="ad826-127">The DXGItype.h header type-defines [**DXGI\_RGBA**](dxgi-rgba.md) as an alias of **D3DCOLORVALUE**, as follows:</span></span>


```
typedef D3DCOLORVALUE DXGI_RGBA;
```



<span data-ttu-id="ad826-128">Sie können D3DCOLORVALUE oder [**DXGI \_ RGBA**](dxgi-rgba.md) mit [**IDXGISwapChain1::SetBackgroundColor,**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor) [**IDXGISwapChain1::GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)und [**DXGI \_ ALPHA \_ MODE**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode)verwenden.</span><span class="sxs-lookup"><span data-stu-id="ad826-128">You can use D3DCOLORVALUE or [**DXGI\_RGBA**](dxgi-rgba.md) with [**IDXGISwapChain1::SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1::GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor), and [**DXGI\_ALPHA\_MODE**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).</span></span>

## <a name="requirements"></a><span data-ttu-id="ad826-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad826-129">Requirements</span></span>



| <span data-ttu-id="ad826-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad826-130">Requirement</span></span> | <span data-ttu-id="ad826-131">Wert</span><span class="sxs-lookup"><span data-stu-id="ad826-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ad826-132">Header</span><span class="sxs-lookup"><span data-stu-id="ad826-132">Header</span></span><br/> | <dl> <span data-ttu-id="ad826-133"><dt>Dxgitype.h</dt></span><span class="sxs-lookup"><span data-stu-id="ad826-133"><dt>Dxgitype.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad826-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ad826-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad826-135">DXGI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="ad826-135">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> <dt>

[<span data-ttu-id="ad826-136">**DXGI \_ RGBA**</span><span class="sxs-lookup"><span data-stu-id="ad826-136">**DXGI\_RGBA**</span></span>](dxgi-rgba.md)
</dt> </dl>

 

 




