---
description: Wenden Sie die Werte in einem Zustands Block auf den Systemstatus aktueller Effekt an.
ms.assetid: f228e2a2-64fa-4354-9f49-42d1d3b12d50
title: 'ID3DXEffect:: applyparameterblock-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.ApplyParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 12af672b929822180c4dba681ca333692a9174ec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357237"
---
# <a name="id3dxeffectapplyparameterblock-method"></a><span data-ttu-id="854d4-103">ID3DXEffect:: applyparameterblock-Methode</span><span class="sxs-lookup"><span data-stu-id="854d4-103">ID3DXEffect::ApplyParameterBlock method</span></span>

<span data-ttu-id="854d4-104">Wenden Sie die Werte in einem Zustands Block auf den Systemstatus aktueller Effekt an.</span><span class="sxs-lookup"><span data-stu-id="854d4-104">Apply the values in a state block to the current effect system state.</span></span>

## <a name="syntax"></a><span data-ttu-id="854d4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="854d4-105">Syntax</span></span>


```C++
HRESULT ApplyParameterBlock(
  [in] D3DXHANDLE  hParameterBlock
);
```



## <a name="parameters"></a><span data-ttu-id="854d4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="854d4-106">Parameters</span></span>

<dl> <dt>

 <span data-ttu-id="854d4-107">*hparameterblock* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="854d4-107">*hParameterBlock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="854d4-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="854d4-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="854d4-109">Ein Handle für den Parameter Block.</span><span class="sxs-lookup"><span data-stu-id="854d4-109">A handle to the parameter block.</span></span> <span data-ttu-id="854d4-110">Dies ist das Handle, das von [**ID3DXEffect:: endparameterblock**](id3dxeffect--endparameterblock.md)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="854d4-110">This is the handle returned by [**ID3DXEffect::EndParameterBlock**](id3dxeffect--endparameterblock.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="854d4-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="854d4-111">Return value</span></span>

<span data-ttu-id="854d4-112">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="854d4-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="854d4-113">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="854d4-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="854d4-114">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="854d4-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="854d4-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="854d4-115">Remarks</span></span>

<span data-ttu-id="854d4-116">Erfassungs Effekt-Parameter Zustandsänderungen in einem Parameter Block durch Aufrufen von beginparameterblock; beendet die Erfassung von Zustandsänderungen, indem endparameterblock aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="854d4-116">Capture effect parameter state changes in a parameter block by calling BeginParameterBlock; stop capturing state changes by calling EndParameterBlock.</span></span> <span data-ttu-id="854d4-117">Diese Zustandsänderungen beinhalten alle Auswirkung-Parameteränderungen, die in einer Technik auftreten (einschließlich der außerhalb eines bestanden).</span><span class="sxs-lookup"><span data-stu-id="854d4-117">These state changes include any effect parameter changes that occur inside of a technique (including those outside of a pass).</span></span> <span data-ttu-id="854d4-118">Wenn Sie mit dem Parameter Block abgeschlossen haben, können Sie deleteparameterblock aufrufen, um Arbeitsspeicher wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="854d4-118">Once you are done with the parameter block, call DeleteParameterBlock to recover memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="854d4-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="854d4-119">Requirements</span></span>



| <span data-ttu-id="854d4-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="854d4-120">Requirement</span></span> | <span data-ttu-id="854d4-121">Wert</span><span class="sxs-lookup"><span data-stu-id="854d4-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="854d4-122">Header</span><span class="sxs-lookup"><span data-stu-id="854d4-122">Header</span></span><br/>  | <dl> <span data-ttu-id="854d4-123"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="854d4-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="854d4-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="854d4-124">Library</span></span><br/> | <dl> <span data-ttu-id="854d4-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="854d4-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="854d4-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="854d4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="854d4-127">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="854d4-127">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="854d4-128">**ID3DXEffect:: beginparameterblock**</span><span class="sxs-lookup"><span data-stu-id="854d4-128">**ID3DXEffect::BeginParameterBlock**</span></span>](id3dxeffect--beginparameterblock.md)
</dt> <dt>

[<span data-ttu-id="854d4-129">**ID3DXEffect:: endparameterblock**</span><span class="sxs-lookup"><span data-stu-id="854d4-129">**ID3DXEffect::EndParameterBlock**</span></span>](id3dxeffect--endparameterblock.md)
</dt> <dt>

[<span data-ttu-id="854d4-130">**ID3DXEffect::D eleteparameterblock**</span><span class="sxs-lookup"><span data-stu-id="854d4-130">**ID3DXEffect::DeleteParameterBlock**</span></span>](id3dxeffect--deleteparameterblock.md)
</dt> </dl>

 

 




