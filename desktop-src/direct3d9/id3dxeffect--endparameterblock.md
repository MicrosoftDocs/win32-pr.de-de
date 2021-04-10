---
description: Beendet die Erfassung von Effekt-Parameter Zustandsänderungen.
ms.assetid: b6ca2917-2df0-4f3a-9ee3-23e9d2501ff4
title: 'ID3DXEffect:: endparameterblock-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.EndParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 3359e3b923d05e003ffbda18791e497d18ba627e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961622"
---
# <a name="id3dxeffectendparameterblock-method"></a><span data-ttu-id="dc48f-103">ID3DXEffect:: endparameterblock-Methode</span><span class="sxs-lookup"><span data-stu-id="dc48f-103">ID3DXEffect::EndParameterBlock method</span></span>

<span data-ttu-id="dc48f-104">Beendet die Erfassung von Effekt-Parameter Zustandsänderungen.</span><span class="sxs-lookup"><span data-stu-id="dc48f-104">Stop capturing effect parameter state changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc48f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc48f-105">Syntax</span></span>


```C++
D3DXHANDLE EndParameterBlock();
```



## <a name="parameters"></a><span data-ttu-id="dc48f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc48f-106">Parameters</span></span>

<span data-ttu-id="dc48f-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="dc48f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dc48f-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dc48f-108">Return value</span></span>

<span data-ttu-id="dc48f-109">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="dc48f-109">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="dc48f-110">Gibt ein Handle für den Parameter Status Block zurück.</span><span class="sxs-lookup"><span data-stu-id="dc48f-110">Returns a handle to the parameter state block.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc48f-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dc48f-111">Remarks</span></span>

<span data-ttu-id="dc48f-112">Alle Effektparameter, die den Zustand ändern (nach dem Aufrufen von beginparameterblock und vor dem Aufrufen von endparameterblock), werden in einem Effektparameter-Zustands Block gespeichert.</span><span class="sxs-lookup"><span data-stu-id="dc48f-112">All effect parameters that change state (after calling BeginParameterBlock and before calling EndParameterBlock) will be saved in an effect parameter state block.</span></span> <span data-ttu-id="dc48f-113">Verwenden Sie applyparameterblock, um diesen Block von Zustandsänderungen auf das Effektsystem anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="dc48f-113">Use ApplyParameterBlock to apply this block of state changes to the effect system.</span></span> <span data-ttu-id="dc48f-114">Wenn Sie mit einem Zustands Block fertig sind, verwenden Sie deleteparameterblock, um den Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="dc48f-114">Once you are finished with a state block use DeleteParameterBlock to free the memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc48f-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc48f-115">Requirements</span></span>



| <span data-ttu-id="dc48f-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc48f-116">Requirement</span></span> | <span data-ttu-id="dc48f-117">Wert</span><span class="sxs-lookup"><span data-stu-id="dc48f-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc48f-118">Header</span><span class="sxs-lookup"><span data-stu-id="dc48f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="dc48f-119"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc48f-119"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="dc48f-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dc48f-120">Library</span></span><br/> | <dl> <span data-ttu-id="dc48f-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dc48f-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="dc48f-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc48f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc48f-123">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="dc48f-123">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="dc48f-124">**ID3DXEffect:: beginparameterblock**</span><span class="sxs-lookup"><span data-stu-id="dc48f-124">**ID3DXEffect::BeginParameterBlock**</span></span>](id3dxeffect--beginparameterblock.md)
</dt> <dt>

[<span data-ttu-id="dc48f-125">**ID3DXEffect:: applyparameterblock**</span><span class="sxs-lookup"><span data-stu-id="dc48f-125">**ID3DXEffect::ApplyParameterBlock**</span></span>](id3dxeffect--applyparameterblock.md)
</dt> <dt>

[<span data-ttu-id="dc48f-126">**ID3DXEffect::D eleteparameterblock**</span><span class="sxs-lookup"><span data-stu-id="dc48f-126">**ID3DXEffect::DeleteParameterBlock**</span></span>](id3dxeffect--deleteparameterblock.md)
</dt> </dl>

 

 




