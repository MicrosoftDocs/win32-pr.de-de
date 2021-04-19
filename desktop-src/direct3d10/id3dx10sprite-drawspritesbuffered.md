---
description: Fügen Sie dem Batch von Sprites, die gerendert werden sollen, ein Array von Sprites hinzu.
ms.assetid: e6a9f806-7244-4139-b47e-c46dfab38a31
title: ID3DX10Sprite::D rawspritesbuffered-Methode (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.DrawSpritesBuffered
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 72893f6a8c3cf82c67f014b4bdbb9a92453de319
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364015"
---
# <a name="id3dx10spritedrawspritesbuffered-method"></a><span data-ttu-id="c04bb-103">ID3DX10Sprite::D rawspritesbuffered-Methode</span><span class="sxs-lookup"><span data-stu-id="c04bb-103">ID3DX10Sprite::DrawSpritesBuffered method</span></span>

<span data-ttu-id="c04bb-104">Fügen Sie dem Batch von Sprites, die gerendert werden sollen, ein Array von Sprites hinzu.</span><span class="sxs-lookup"><span data-stu-id="c04bb-104">Add an array of sprites to the batch of sprites to be rendered.</span></span> <span data-ttu-id="c04bb-105">Dies muss zwischen Aufrufen von [**ID3DX10Sprite:: begin**](id3dx10sprite-begin.md) und [**ID3DX10Sprite:: End**](id3dx10sprite-end.md)aufgerufen werden, und [**ID3DX10Sprite:: Flush**](id3dx10sprite-flush.md) muss vor Ende aufgerufen werden, um alle Batch Sprites zum Rendering an das Gerät zu senden.</span><span class="sxs-lookup"><span data-stu-id="c04bb-105">This must be called in between calls to [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md) and [**ID3DX10Sprite::End**](id3dx10sprite-end.md), and [**ID3DX10Sprite::Flush**](id3dx10sprite-flush.md) must be called before End to send all of the batched sprites to the device for rendering.</span></span> <span data-ttu-id="c04bb-106">Diese Draw-Methode ist besonders nützlich, wenn Sie eine kleine Anzahl von Sprites zeichnen möchten, die Sie in einem großen Batch, wie z. b. Schriftarten, gepuffert werden</span><span class="sxs-lookup"><span data-stu-id="c04bb-106">This draw method is most useful when drawing a small number of sprites that you want buffered into a large batch, such as fonts.</span></span>

## <a name="syntax"></a><span data-ttu-id="c04bb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c04bb-107">Syntax</span></span>


```C++
HRESULT DrawSpritesBuffered(
  [in] D3DX10_SPRITE *pSprites,
  [in] UINT          cSprites
);
```



## <a name="parameters"></a><span data-ttu-id="c04bb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c04bb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c04bb-109">*psprites* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c04bb-109">*pSprites* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c04bb-110">Typ: **[ **d3dx10 \_ Sprite**](d3dx10-sprite.md)\***</span><span class="sxs-lookup"><span data-stu-id="c04bb-110">Type: **[**D3DX10\_SPRITE**](d3dx10-sprite.md)\***</span></span>

<span data-ttu-id="c04bb-111">Das Array von Sprites, das gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c04bb-111">The array of sprites to draw.</span></span> <span data-ttu-id="c04bb-112">Siehe [**d3dx10 \_ Sprite**](d3dx10-sprite.md).</span><span class="sxs-lookup"><span data-stu-id="c04bb-112">See [**D3DX10\_SPRITE**](d3dx10-sprite.md).</span></span>

</dd> <dt>

<span data-ttu-id="c04bb-113">*csprites* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c04bb-113">*cSprites* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c04bb-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c04bb-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c04bb-115">Die Anzahl der Sprites in psprites.</span><span class="sxs-lookup"><span data-stu-id="c04bb-115">The number of sprites in pSprites.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c04bb-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c04bb-116">Return value</span></span>

<span data-ttu-id="c04bb-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c04bb-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c04bb-118">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c04bb-118">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c04bb-119">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="c04bb-119">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="c04bb-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c04bb-120">Requirements</span></span>



| <span data-ttu-id="c04bb-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c04bb-121">Requirement</span></span> | <span data-ttu-id="c04bb-122">Wert</span><span class="sxs-lookup"><span data-stu-id="c04bb-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c04bb-123">Header</span><span class="sxs-lookup"><span data-stu-id="c04bb-123">Header</span></span><br/>  | <dl> <span data-ttu-id="c04bb-124"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="c04bb-124"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="c04bb-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c04bb-125">Library</span></span><br/> | <dl> <span data-ttu-id="c04bb-126"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c04bb-126"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c04bb-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c04bb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c04bb-128">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="c04bb-128">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="c04bb-129">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="c04bb-129">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
