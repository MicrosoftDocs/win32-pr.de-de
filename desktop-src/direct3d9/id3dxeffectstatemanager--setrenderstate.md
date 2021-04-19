---
description: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um den gerengerzustand festzulegen.
ms.assetid: a5a27e30-c141-44a4-b8d4-38c1d6076b2a
title: 'ID3DXEffectStateManager:: strenderstate-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetRenderState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 111ab8ff379d5b095500101674fc45b6a2b31bc1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355028"
---
# <a name="id3dxeffectstatemanagersetrenderstate-method"></a><span data-ttu-id="0508b-103">ID3DXEffectStateManager:: strenderstate-Methode</span><span class="sxs-lookup"><span data-stu-id="0508b-103">ID3DXEffectStateManager::SetRenderState method</span></span>

<span data-ttu-id="0508b-104">Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um den gerengerzustand festzulegen.</span><span class="sxs-lookup"><span data-stu-id="0508b-104">A callback function that must be implemented by a user to set render state.</span></span>

## <a name="syntax"></a><span data-ttu-id="0508b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0508b-105">Syntax</span></span>


```C++
HRESULT SetRenderState(
  [in] D3DRENDERSTATETYPE State,
  [in] DWORD              Value
);
```



## <a name="parameters"></a><span data-ttu-id="0508b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0508b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0508b-107">*Status* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0508b-107">*State* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0508b-108">Typ: **[ **D3DRENDERSTATETYPE**](./d3drenderstatetype.md)**</span><span class="sxs-lookup"><span data-stu-id="0508b-108">Type: **[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)**</span></span>

<span data-ttu-id="0508b-109">Der festzulegende Rendering-Zustand.</span><span class="sxs-lookup"><span data-stu-id="0508b-109">The render state to set.</span></span> [<span data-ttu-id="0508b-110">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="0508b-110">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)

</dd> <dt>

<span data-ttu-id="0508b-111">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0508b-111">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0508b-112">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0508b-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0508b-113">Der Wert des Rendering-Zustands.</span><span class="sxs-lookup"><span data-stu-id="0508b-113">The render state value.</span></span> <span data-ttu-id="0508b-114">Siehe [Effekt Zustände (Direct3D 9)](effect-states.md).</span><span class="sxs-lookup"><span data-stu-id="0508b-114">See [Effect States (Direct3D 9)](effect-states.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0508b-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0508b-115">Return value</span></span>

<span data-ttu-id="0508b-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0508b-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0508b-117">Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="0508b-117">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="0508b-118">Wenn der Rückruf beim Festlegen des Geräte Zustands fehlschlägt, wird eine der folgenden Aktionen ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="0508b-118">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="0508b-119">Der Effekt schlägt während [**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md)fehl.</span><span class="sxs-lookup"><span data-stu-id="0508b-119">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="0508b-120">Der Status des dynamischen Effekts (z. b. [**IDirect3DDevice9:: strenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)) schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="0508b-120">The dynamic effect state call (such as [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="0508b-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0508b-121">Requirements</span></span>



| <span data-ttu-id="0508b-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0508b-122">Requirement</span></span> | <span data-ttu-id="0508b-123">Wert</span><span class="sxs-lookup"><span data-stu-id="0508b-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0508b-124">Header</span><span class="sxs-lookup"><span data-stu-id="0508b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0508b-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0508b-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="0508b-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0508b-126">Library</span></span><br/> | <dl> <span data-ttu-id="0508b-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0508b-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0508b-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0508b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0508b-129">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="0508b-129">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
