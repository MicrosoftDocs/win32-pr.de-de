---
description: Löschen Sie einen Parameter Block.
ms.assetid: 5502dabc-1703-481b-a69d-f6bd8fd01d20
title: ID3DXEffect::D eleteparameterblock-Methode (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.DeleteParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 483b09ebf308b8cdfa14d714bc74786e5fcb1f83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351952"
---
# <a name="id3dxeffectdeleteparameterblock-method"></a><span data-ttu-id="e0ed0-103">ID3DXEffect::D eleteparameterblock-Methode</span><span class="sxs-lookup"><span data-stu-id="e0ed0-103">ID3DXEffect::DeleteParameterBlock method</span></span>

<span data-ttu-id="e0ed0-104">Löschen Sie einen Parameter Block.</span><span class="sxs-lookup"><span data-stu-id="e0ed0-104">Delete a parameter block.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0ed0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0ed0-105">Syntax</span></span>


```C++
HRESULT DeleteParameterBlock(
  [in] D3DXHANDLE  hParameterBlock
);
```



## <a name="parameters"></a><span data-ttu-id="e0ed0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0ed0-106">Parameters</span></span>

<dl> <dt>

 <span data-ttu-id="e0ed0-107">*hparameterblock* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0ed0-107">*hParameterBlock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0ed0-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="e0ed0-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="e0ed0-109">Ein Handle für den Parameter Block.</span><span class="sxs-lookup"><span data-stu-id="e0ed0-109">A handle to the parameter block.</span></span> <span data-ttu-id="e0ed0-110">Dies ist das Handle, das von [**ID3DXEffect:: endparameterblock**](id3dxeffect--endparameterblock.md)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e0ed0-110">This is the handle returned by [**ID3DXEffect::EndParameterBlock**](id3dxeffect--endparameterblock.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0ed0-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e0ed0-111">Return value</span></span>

<span data-ttu-id="e0ed0-112">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e0ed0-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e0ed0-113">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e0ed0-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e0ed0-114">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="e0ed0-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0ed0-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0ed0-115">Remarks</span></span>

<span data-ttu-id="e0ed0-116">Parameter Blöcke sind Blöcke von Effekt Zuständen.</span><span class="sxs-lookup"><span data-stu-id="e0ed0-116">Parameter blocks are blocks of effect states.</span></span> <span data-ttu-id="e0ed0-117">Verwenden Sie einen Parameter Block zum Aufzeichnen von Zustandsänderungen, sodass Sie später mit einem einzigen API-Befehl angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="e0ed0-117">Use a parameter block to record state changes so that they can be applied later on with a single API call.</span></span> <span data-ttu-id="e0ed0-118">Löschen Sie den Parameter Block, wenn er nicht mehr benötigt wird, um die Speicherauslastung zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="e0ed0-118">When no longer needed, delete the parameter block to reduce memory usage.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0ed0-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0ed0-119">Requirements</span></span>



| <span data-ttu-id="e0ed0-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0ed0-120">Requirement</span></span> | <span data-ttu-id="e0ed0-121">Wert</span><span class="sxs-lookup"><span data-stu-id="e0ed0-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0ed0-122">Header</span><span class="sxs-lookup"><span data-stu-id="e0ed0-122">Header</span></span><br/>  | <dl> <span data-ttu-id="e0ed0-123"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0ed0-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="e0ed0-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e0ed0-124">Library</span></span><br/> | <dl> <span data-ttu-id="e0ed0-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e0ed0-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e0ed0-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0ed0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0ed0-127">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="e0ed0-127">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="e0ed0-128">**ID3DXEffect:: beginparameterblock**</span><span class="sxs-lookup"><span data-stu-id="e0ed0-128">**ID3DXEffect::BeginParameterBlock**</span></span>](id3dxeffect--beginparameterblock.md)
</dt> <dt>

[<span data-ttu-id="e0ed0-129">**ID3DXEffect:: endparameterblock**</span><span class="sxs-lookup"><span data-stu-id="e0ed0-129">**ID3DXEffect::EndParameterBlock**</span></span>](id3dxeffect--endparameterblock.md)
</dt> </dl>

 

 




