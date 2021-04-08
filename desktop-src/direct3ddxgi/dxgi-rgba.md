---
description: Stellt einen Farbwert mit Alpha dar, der für Transparenz verwendet wird.
ms.assetid: 5F9DDDC1-644E-4DA2-8E3D-F157789809E7
title: DXGI_RGBA-Struktur (dxgitype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_RGBA
api_type:
- HeaderDef
api_location:
- DXGItype.h
ms.openlocfilehash: 77b526e916d43868304c6c01a7dbbe8ebbb5692b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746768"
---
# <a name="dxgi_rgba-structure"></a><span data-ttu-id="64e1e-103">DXGI- \_ RGBA-Struktur</span><span class="sxs-lookup"><span data-stu-id="64e1e-103">DXGI\_RGBA structure</span></span>

<span data-ttu-id="64e1e-104">Stellt einen Farbwert mit Alpha dar, der für Transparenz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="64e1e-104">Represents a color value with alpha, which is used for transparency.</span></span>

## <a name="syntax"></a><span data-ttu-id="64e1e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="64e1e-105">Syntax</span></span>


```C++
typedef struct _DXGI_RGBA {
  float r;
  float g;
  float b;
  float a;
} DXGI_RGBA;
```



## <a name="members"></a><span data-ttu-id="64e1e-106">Member</span><span class="sxs-lookup"><span data-stu-id="64e1e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="64e1e-107">**r**</span><span class="sxs-lookup"><span data-stu-id="64e1e-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="64e1e-108">Ein Gleit Komma Wert, der die rote Komponente einer Farbe angibt.</span><span class="sxs-lookup"><span data-stu-id="64e1e-108">Floating-point value that specifies the red component of a color.</span></span> <span data-ttu-id="64e1e-109">Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0.</span><span class="sxs-lookup"><span data-stu-id="64e1e-109">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="64e1e-110">Der Wert 0,0 gibt das vollständige Fehlen der roten Komponente an, während der Wert 1,0 angibt, dass Rot vollständig vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="64e1e-110">A value of 0.0 indicates the complete absence of the red component, while a value of 1.0 indicates that red is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="64e1e-111">**g**</span><span class="sxs-lookup"><span data-stu-id="64e1e-111">**g**</span></span>
</dt> <dd>

<span data-ttu-id="64e1e-112">Ein Gleit Komma Wert, der die grüne Komponente einer Farbe angibt.</span><span class="sxs-lookup"><span data-stu-id="64e1e-112">Floating-point value that specifies the green component of a color.</span></span> <span data-ttu-id="64e1e-113">Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0.</span><span class="sxs-lookup"><span data-stu-id="64e1e-113">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="64e1e-114">Der Wert 0,0 gibt das vollständige Fehlen der grünen Komponente an, während der Wert 1,0 angibt, dass grün vollständig vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="64e1e-114">A value of 0.0 indicates the complete absence of the green component, while a value of 1.0 indicates that green is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="64e1e-115">**b**</span><span class="sxs-lookup"><span data-stu-id="64e1e-115">**b**</span></span>
</dt> <dd>

<span data-ttu-id="64e1e-116">Ein Gleit Komma Wert, der die blaue Komponente einer Farbe angibt.</span><span class="sxs-lookup"><span data-stu-id="64e1e-116">Floating-point value that specifies the blue component of a color.</span></span> <span data-ttu-id="64e1e-117">Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0.</span><span class="sxs-lookup"><span data-stu-id="64e1e-117">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="64e1e-118">Der Wert 0,0 gibt das vollständige Fehlen der blauen Komponente an, während der Wert 1,0 angibt, dass Blue vollständig vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="64e1e-118">A value of 0.0 indicates the complete absence of the blue component, while a value of 1.0 indicates that blue is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="64e1e-119">**ein**</span><span class="sxs-lookup"><span data-stu-id="64e1e-119">**a**</span></span>
</dt> <dd>

<span data-ttu-id="64e1e-120">Ein Gleit Komma Wert, der die Alpha Komponente einer Farbe angibt.</span><span class="sxs-lookup"><span data-stu-id="64e1e-120">Floating-point value that specifies the alpha component of a color.</span></span> <span data-ttu-id="64e1e-121">Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0.</span><span class="sxs-lookup"><span data-stu-id="64e1e-121">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="64e1e-122">Der Wert 0,0 gibt vollständig transparent an, während der Wert 1,0 vollständig deckend angibt.</span><span class="sxs-lookup"><span data-stu-id="64e1e-122">A value of 0.0 indicates fully transparent, while a value of 1.0 indicates fully opaque.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="64e1e-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64e1e-123">Remarks</span></span>

<span data-ttu-id="64e1e-124">Sie können die Member dieser Struktur auf Werte außerhalb des Bereichs von 0 bis 1 festlegen, um ungewöhnliche Effekte zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="64e1e-124">You can set the members of this structure to values outside the range of 0 through 1 to implement some unusual effects.</span></span> <span data-ttu-id="64e1e-125">Werte, die größer als 1 sind, führen zu starken Lichtern, die tendenziell eine Szene auslagern.</span><span class="sxs-lookup"><span data-stu-id="64e1e-125">Values greater than 1 produce strong lights that tend to wash out a scene.</span></span> <span data-ttu-id="64e1e-126">Durch negative Werte werden dunkle Lichter erzeugt, die das Licht aus einer Szene entfernen.</span><span class="sxs-lookup"><span data-stu-id="64e1e-126">Negative values produce dark lights that actually remove light from a scene.</span></span>

<span data-ttu-id="64e1e-127">Der dxgitype. h-Headertyp: definiert **DXGI \_ RGBA** als Alias von [**D3DCOLORVALUE**](d3dcolorvalue.md)wie folgt:</span><span class="sxs-lookup"><span data-stu-id="64e1e-127">The DXGItype.h header type-defines **DXGI\_RGBA** as an alias of [**D3DCOLORVALUE**](d3dcolorvalue.md), as follows:</span></span>


```
typedef D3DCOLORVALUE DXGI_RGBA;
```



<span data-ttu-id="64e1e-128">Sie können **DXGI \_ RGBA** mit [**IDXGISwapChain1:: SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1:: getbackgroundcolor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)und dem [**DXGI \_ alpha- \_ Modus**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode)verwenden.</span><span class="sxs-lookup"><span data-stu-id="64e1e-128">You can use **DXGI\_RGBA** with [**IDXGISwapChain1::SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1::GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor), and [**DXGI\_ALPHA\_MODE**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).</span></span>

## <a name="requirements"></a><span data-ttu-id="64e1e-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64e1e-129">Requirements</span></span>



| <span data-ttu-id="64e1e-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64e1e-130">Requirement</span></span> | <span data-ttu-id="64e1e-131">Wert</span><span class="sxs-lookup"><span data-stu-id="64e1e-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64e1e-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="64e1e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="64e1e-133">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="64e1e-133">Windows 8 and Platform Update for Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="64e1e-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="64e1e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="64e1e-135">Windows Server 2012 und Platt Form Update für Windows Server 2008 R2 \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="64e1e-135">Windows Server 2012 and Platform Update for Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="64e1e-136">Header</span><span class="sxs-lookup"><span data-stu-id="64e1e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="64e1e-137"><dt>Dxgitype. h</dt></span><span class="sxs-lookup"><span data-stu-id="64e1e-137"><dt>DXGItype.h</dt></span></span> </dl>                      |



## <a name="see-also"></a><span data-ttu-id="64e1e-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64e1e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64e1e-139">DXGI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="64e1e-139">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> <dt>

[<span data-ttu-id="64e1e-140">**D3DCOLORVALUE**</span><span class="sxs-lookup"><span data-stu-id="64e1e-140">**D3DCOLORVALUE**</span></span>](d3dcolorvalue.md)
</dt> <dt>

[<span data-ttu-id="64e1e-141">**D3DCOLORVALUE (in Direct3D 9)**</span><span class="sxs-lookup"><span data-stu-id="64e1e-141">**D3DCOLORVALUE (in Direct3D 9)**</span></span>](../direct3d9/d3dcolorvalue.md)
</dt> </dl>

 

 
