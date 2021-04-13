---
description: Zeichnen Sie ein Array von Sprites.
ms.assetid: 3fcc7705-0d59-450e-b137-c9cb7ec6b1ea
title: ID3DX10Sprite::D rawspritesimvermittler-Methode (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.DrawSpritesImmediate
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7fa4012f5f589c7bc0d1f789599da142194f6e08
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356117"
---
# <a name="id3dx10spritedrawspritesimmediate-method"></a><span data-ttu-id="e7c6c-103">ID3DX10Sprite::D rawspritesimvermittler-Methode</span><span class="sxs-lookup"><span data-stu-id="e7c6c-103">ID3DX10Sprite::DrawSpritesImmediate method</span></span>

<span data-ttu-id="e7c6c-104">Zeichnen Sie ein Array von Sprites.</span><span class="sxs-lookup"><span data-stu-id="e7c6c-104">Draw an array of sprites.</span></span> <span data-ttu-id="e7c6c-105">Dadurch werden die Sprites sofort zum Rendern an das Gerät gesendet. Dies unterscheidet sich von [**ID3DX10Sprite::D rawspritesbuffered**](id3dx10sprite-drawspritesbuffered.md) , das nur ein Array von Sprites zu einem Batch von Sprites hinzufügt, die gerendert werden, wenn [**ID3DX10Sprite:: Flush**](id3dx10sprite-flush.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e7c6c-105">This will immediately send the sprites to the device for rendering, which is different from [**ID3DX10Sprite::DrawSpritesBuffered**](id3dx10sprite-drawspritesbuffered.md) which only adds an array of sprites to a batch of sprites to be rendered when [**ID3DX10Sprite::Flush**](id3dx10sprite-flush.md) is called.</span></span> <span data-ttu-id="e7c6c-106">Diese Draw-Methode ist besonders nützlich, wenn eine große Anzahl von Sprites gezeichnet wird, die bereits auf der CPU sortiert wurden (oder nicht sortiert werden müssen), z. b. in einem Partikelsystem.</span><span class="sxs-lookup"><span data-stu-id="e7c6c-106">This draw method is most useful when drawing a large number of sprites that have already been sorted on the CPU (or do not need to be sorted), such as in a particle system.</span></span> <span data-ttu-id="e7c6c-107">Dies muss zwischen Aufrufen von [**ID3DX10Sprite:: begin**](id3dx10sprite-begin.md) und [**ID3DX10Sprite:: End**](id3dx10sprite-end.md)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e7c6c-107">This must be called in between calls to [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md) and [**ID3DX10Sprite::End**](id3dx10sprite-end.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e7c6c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7c6c-108">Syntax</span></span>


```C++
HRESULT DrawSpritesImmediate(
  [in] D3DX10_SPRITE *pSprites,
  [in] UINT          cSprites,
  [in] UINT          cbSprite,
  [in] UINT          flags
);
```



## <a name="parameters"></a><span data-ttu-id="e7c6c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7c6c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7c6c-110">*psprites* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7c6c-110">*pSprites* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7c6c-111">Typ: **[ **d3dx10 \_ Sprite**](d3dx10-sprite.md)\***</span><span class="sxs-lookup"><span data-stu-id="e7c6c-111">Type: **[**D3DX10\_SPRITE**](d3dx10-sprite.md)\***</span></span>

<span data-ttu-id="e7c6c-112">Das Array von Sprites, das gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e7c6c-112">The array of sprites to draw.</span></span> <span data-ttu-id="e7c6c-113">Siehe [**d3dx10 \_ Sprite**](d3dx10-sprite.md).</span><span class="sxs-lookup"><span data-stu-id="e7c6c-113">See [**D3DX10\_SPRITE**](d3dx10-sprite.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7c6c-114">*csprites* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7c6c-114">*cSprites* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7c6c-115">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e7c6c-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e7c6c-116">Die Anzahl der Sprites in psprites.</span><span class="sxs-lookup"><span data-stu-id="e7c6c-116">The number of sprites in pSprites.</span></span>

</dd> <dt>

<span data-ttu-id="e7c6c-117">*cbsprite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7c6c-117">*cbSprite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7c6c-118">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e7c6c-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e7c6c-119">Die Größe der Sprite-Struktur, die an psprites übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="e7c6c-119">The size of the sprite structure you are passing into pSprites.</span></span> <span data-ttu-id="e7c6c-120">Das übergeben von 0 entspricht der Übergabe von sizeof (d3dx10 \_ Sprite).</span><span class="sxs-lookup"><span data-stu-id="e7c6c-120">Passing in 0 is the equivalent of passing in sizeof(D3DX10\_SPRITE).</span></span>

</dd> <dt>

<span data-ttu-id="e7c6c-121">*Flags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7c6c-121">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7c6c-122">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e7c6c-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e7c6c-123">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="e7c6c-123">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7c6c-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e7c6c-124">Return value</span></span>

<span data-ttu-id="e7c6c-125">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e7c6c-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e7c6c-126">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e7c6c-126">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e7c6c-127">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="e7c6c-127">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7c6c-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7c6c-128">Requirements</span></span>



| <span data-ttu-id="e7c6c-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7c6c-129">Requirement</span></span> | <span data-ttu-id="e7c6c-130">Wert</span><span class="sxs-lookup"><span data-stu-id="e7c6c-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e7c6c-131">Header</span><span class="sxs-lookup"><span data-stu-id="e7c6c-131">Header</span></span><br/>  | <dl> <span data-ttu-id="e7c6c-132"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7c6c-132"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="e7c6c-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e7c6c-133">Library</span></span><br/> | <dl> <span data-ttu-id="e7c6c-134"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7c6c-134"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7c6c-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7c6c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7c6c-136">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="e7c6c-136">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="e7c6c-137">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="e7c6c-137">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
