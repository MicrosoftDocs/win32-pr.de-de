---
description: 'DXGI_RGBA Struktur: Stellt einen Farbwert mit Alpha dar, der zur Transparenz verwendet wird.'
ms.assetid: 5F9DDDC1-644E-4DA2-8E3D-F157789809E7
title: DXGI_RGBA -Struktur (DXGItype.h)
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
ms.openlocfilehash: b0447d6470401d4136fbfd36f6d9c089e331b14b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114268"
---
# <a name="dxgi_rgba-structure"></a><span data-ttu-id="97433-103">DXGI \_ RGBA-Struktur</span><span class="sxs-lookup"><span data-stu-id="97433-103">DXGI\_RGBA structure</span></span>

<span data-ttu-id="97433-104">Stellt einen Farbwert mit Alpha dar, der zur Transparenz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="97433-104">Represents a color value with alpha, which is used for transparency.</span></span>

## <a name="syntax"></a><span data-ttu-id="97433-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="97433-105">Syntax</span></span>


```C++
typedef struct _DXGI_RGBA {
  float r;
  float g;
  float b;
  float a;
} DXGI_RGBA;
```



## <a name="members"></a><span data-ttu-id="97433-106">Member</span><span class="sxs-lookup"><span data-stu-id="97433-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="97433-107">**r**</span><span class="sxs-lookup"><span data-stu-id="97433-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="97433-108">Gleitkommawert, der die rote Komponente einer Farbe angibt.</span><span class="sxs-lookup"><span data-stu-id="97433-108">Floating-point value that specifies the red component of a color.</span></span> <span data-ttu-id="97433-109">Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0.</span><span class="sxs-lookup"><span data-stu-id="97433-109">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="97433-110">Der Wert 0,0 gibt das vollständige Fehlen der roten Komponente an, während der Wert 1,0 angibt, dass Rot vollständig vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="97433-110">A value of 0.0 indicates the complete absence of the red component, while a value of 1.0 indicates that red is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="97433-111">**g**</span><span class="sxs-lookup"><span data-stu-id="97433-111">**g**</span></span>
</dt> <dd>

<span data-ttu-id="97433-112">Gleitkommawert, der die grüne Komponente einer Farbe angibt.</span><span class="sxs-lookup"><span data-stu-id="97433-112">Floating-point value that specifies the green component of a color.</span></span> <span data-ttu-id="97433-113">Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0.</span><span class="sxs-lookup"><span data-stu-id="97433-113">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="97433-114">Der Wert 0,0 gibt das vollständige Fehlen der grünen Komponente an, während der Wert 1,0 angibt, dass grün vollständig vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="97433-114">A value of 0.0 indicates the complete absence of the green component, while a value of 1.0 indicates that green is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="97433-115">**b**</span><span class="sxs-lookup"><span data-stu-id="97433-115">**b**</span></span>
</dt> <dd>

<span data-ttu-id="97433-116">Gleitkommawert, der die blaue Komponente einer Farbe angibt.</span><span class="sxs-lookup"><span data-stu-id="97433-116">Floating-point value that specifies the blue component of a color.</span></span> <span data-ttu-id="97433-117">Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0.</span><span class="sxs-lookup"><span data-stu-id="97433-117">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="97433-118">Der Wert 0,0 gibt das vollständige Fehlen der blauen Komponente an, während der Wert 1,0 angibt, dass blau vollständig vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="97433-118">A value of 0.0 indicates the complete absence of the blue component, while a value of 1.0 indicates that blue is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="97433-119">**Eine**</span><span class="sxs-lookup"><span data-stu-id="97433-119">**a**</span></span>
</dt> <dd>

<span data-ttu-id="97433-120">Gleitkommawert, der die Alphakomponente einer Farbe angibt.</span><span class="sxs-lookup"><span data-stu-id="97433-120">Floating-point value that specifies the alpha component of a color.</span></span> <span data-ttu-id="97433-121">Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0.</span><span class="sxs-lookup"><span data-stu-id="97433-121">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="97433-122">Der Wert 0,0 gibt vollständig transparent an, während der Wert 1,0 für vollständig deckend steht.</span><span class="sxs-lookup"><span data-stu-id="97433-122">A value of 0.0 indicates fully transparent, while a value of 1.0 indicates fully opaque.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="97433-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97433-123">Remarks</span></span>

<span data-ttu-id="97433-124">Sie können die Member dieser Struktur auf Werte außerhalb des Bereichs von 0 bis 1 festlegen, um einige ungewöhnliche Effekte zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="97433-124">You can set the members of this structure to values outside the range of 0 through 1 to implement some unusual effects.</span></span> <span data-ttu-id="97433-125">Werte größer als 1 erzeugen starke Lichtlichter, die dazu tendieren, eine Szene zu verwaschen.</span><span class="sxs-lookup"><span data-stu-id="97433-125">Values greater than 1 produce strong lights that tend to wash out a scene.</span></span> <span data-ttu-id="97433-126">Negative Werte erzeugen dunkle Lichtlichter, die tatsächlich Licht aus einer Szene entfernen.</span><span class="sxs-lookup"><span data-stu-id="97433-126">Negative values produce dark lights that actually remove light from a scene.</span></span>

<span data-ttu-id="97433-127">Der DXGItype.h-Headertyp definiert **DXGI \_ RGBA** wie folgt als Alias von [**D3DCOLORVALUE:**](d3dcolorvalue.md)</span><span class="sxs-lookup"><span data-stu-id="97433-127">The DXGItype.h header type-defines **DXGI\_RGBA** as an alias of [**D3DCOLORVALUE**](d3dcolorvalue.md), as follows:</span></span>


```
typedef D3DCOLORVALUE DXGI_RGBA;
```



<span data-ttu-id="97433-128">Sie können **DXGI \_ RGBA** mit [**IDXGISwapChain1::SetBackgroundColor,**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor) [**IDXGISwapChain1::GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)und [**DXGI \_ ALPHA \_ MODE**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode)verwenden.</span><span class="sxs-lookup"><span data-stu-id="97433-128">You can use **DXGI\_RGBA** with [**IDXGISwapChain1::SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1::GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor), and [**DXGI\_ALPHA\_MODE**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).</span></span>

## <a name="requirements"></a><span data-ttu-id="97433-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97433-129">Requirements</span></span>



| <span data-ttu-id="97433-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97433-130">Requirement</span></span> | <span data-ttu-id="97433-131">Wert</span><span class="sxs-lookup"><span data-stu-id="97433-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97433-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="97433-132">Minimum supported client</span></span><br/> | <span data-ttu-id="97433-133">Windows 8 und Plattformupdate für Windows \[ 7-Desktop-Apps \| UWP-Apps\]</span><span class="sxs-lookup"><span data-stu-id="97433-133">Windows 8 and Platform Update for Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="97433-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="97433-134">Minimum supported server</span></span><br/> | <span data-ttu-id="97433-135">Windows Server 2012 und Plattformupdate für Windows Server 2008 \[ R2-Desktop-Apps \| UWP-Apps\]</span><span class="sxs-lookup"><span data-stu-id="97433-135">Windows Server 2012 and Platform Update for Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="97433-136">Header</span><span class="sxs-lookup"><span data-stu-id="97433-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="97433-137"><dt>DXGItype.h</dt></span><span class="sxs-lookup"><span data-stu-id="97433-137"><dt>DXGItype.h</dt></span></span> </dl>                      |



## <a name="see-also"></a><span data-ttu-id="97433-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="97433-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97433-139">DXGI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="97433-139">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> <dt>

[<span data-ttu-id="97433-140">**D3DCOLORVALUE**</span><span class="sxs-lookup"><span data-stu-id="97433-140">**D3DCOLORVALUE**</span></span>](d3dcolorvalue.md)
</dt> <dt>

[<span data-ttu-id="97433-141">**D3DCOLORVALUE (in Direct3D 9)**</span><span class="sxs-lookup"><span data-stu-id="97433-141">**D3DCOLORVALUE (in Direct3D 9)**</span></span>](../direct3d9/d3dcolorvalue.md)
</dt> </dl>

 

 
