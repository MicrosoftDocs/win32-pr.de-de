---
description: Starten Sie die Erfassung von Zustandsänderungen in einem Parameter Block.
ms.assetid: cdf6f572-1a21-4c1d-a113-13b48bacd060
title: 'ID3DXEffect:: beginparameterblock-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.BeginParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 60a43304c8e0e3d64ac6469c1c075c57b5411e3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050866"
---
# <a name="id3dxeffectbeginparameterblock-method"></a><span data-ttu-id="c13d3-103">ID3DXEffect:: beginparameterblock-Methode</span><span class="sxs-lookup"><span data-stu-id="c13d3-103">ID3DXEffect::BeginParameterBlock method</span></span>

<span data-ttu-id="c13d3-104">Starten Sie die Erfassung von Zustandsänderungen in einem Parameter Block.</span><span class="sxs-lookup"><span data-stu-id="c13d3-104">Start capturing state changes in a parameter block.</span></span>

## <a name="syntax"></a><span data-ttu-id="c13d3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c13d3-105">Syntax</span></span>


```C++
HRESULT BeginParameterBlock();
```



## <a name="parameters"></a><span data-ttu-id="c13d3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c13d3-106">Parameters</span></span>

<span data-ttu-id="c13d3-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c13d3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c13d3-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c13d3-108">Return value</span></span>

<span data-ttu-id="c13d3-109">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c13d3-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c13d3-110">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c13d3-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c13d3-111">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="c13d3-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="c13d3-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c13d3-112">Remarks</span></span>

<span data-ttu-id="c13d3-113">Statusänderungen des Erfassungs Effekts-Parameters, bis endparameterblock aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c13d3-113">Capture effect parameter state changes until EndParameterBlock is called.</span></span> <span data-ttu-id="c13d3-114">Effektparameter enthalten alle Zustandsänderungen außerhalb eines bestanden.</span><span class="sxs-lookup"><span data-stu-id="c13d3-114">Effect parameters include any state changes outside of a pass.</span></span> <span data-ttu-id="c13d3-115">Löschen Sie Parameter Blöcke, wenn Sie durch Aufrufen von deleteparameterblock nicht mehr benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="c13d3-115">Delete parameter blocks if they are no longer needed by calling DeleteParameterBlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="c13d3-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c13d3-116">Requirements</span></span>



| <span data-ttu-id="c13d3-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c13d3-117">Requirement</span></span> | <span data-ttu-id="c13d3-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c13d3-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c13d3-119">Header</span><span class="sxs-lookup"><span data-stu-id="c13d3-119">Header</span></span><br/>  | <dl> <span data-ttu-id="c13d3-120"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c13d3-120"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="c13d3-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c13d3-121">Library</span></span><br/> | <dl> <span data-ttu-id="c13d3-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c13d3-122"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c13d3-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c13d3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c13d3-124">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="c13d3-124">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="c13d3-125">**ID3DXEffect:: endparameterblock**</span><span class="sxs-lookup"><span data-stu-id="c13d3-125">**ID3DXEffect::EndParameterBlock**</span></span>](id3dxeffect--endparameterblock.md)
</dt> <dt>

[<span data-ttu-id="c13d3-126">**ID3DXEffect:: applyparameterblock**</span><span class="sxs-lookup"><span data-stu-id="c13d3-126">**ID3DXEffect::ApplyParameterBlock**</span></span>](id3dxeffect--applyparameterblock.md)
</dt> <dt>

[<span data-ttu-id="c13d3-127">**ID3DXEffect::D eleteparameterblock**</span><span class="sxs-lookup"><span data-stu-id="c13d3-127">**ID3DXEffect::DeleteParameterBlock**</span></span>](id3dxeffect--deleteparameterblock.md)
</dt> </dl>

 

 




