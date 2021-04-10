---
description: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um eine Transformation festzulegen.
ms.assetid: 5d886554-ddb6-4b8a-a7fd-453e94b9516f
title: 'ID3DXEffectStateManager:: setTransform-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetTransform
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b19a060cfeb09d5d1a92e5e7a1a1f25b58e64f4d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961664"
---
# <a name="id3dxeffectstatemanagersettransform-method"></a><span data-ttu-id="c4fa5-103">ID3DXEffectStateManager:: setTransform-Methode</span><span class="sxs-lookup"><span data-stu-id="c4fa5-103">ID3DXEffectStateManager::SetTransform method</span></span>

<span data-ttu-id="c4fa5-104">Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um eine Transformation festzulegen.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-104">A callback function that must be implemented by a user to set a transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4fa5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4fa5-105">Syntax</span></span>


```C++
HRESULT SetTransform(
  [in]       D3DTRANSFORMSTATETYPE State,
  [in] const D3DMATRIX             *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="c4fa5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4fa5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4fa5-107">*Status* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4fa5-107">*State* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4fa5-108">Typ: **[ **D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md)**</span><span class="sxs-lookup"><span data-stu-id="c4fa5-108">Type: **[**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md)**</span></span>

<span data-ttu-id="c4fa5-109">Der Typ der Transformation, auf die die Matrix angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-109">The type of transform to apply the matrix to.</span></span> <span data-ttu-id="c4fa5-110">Siehe [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md).</span><span class="sxs-lookup"><span data-stu-id="c4fa5-110">See [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4fa5-111">*pmatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4fa5-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4fa5-112">Typ: **Konstanten [**D3DMATRIX**](d3dmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c4fa5-112">Type: **const [**D3DMATRIX**](d3dmatrix.md)\***</span></span>

<span data-ttu-id="c4fa5-113">Eine Transformationsmatrix.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-113">A transformation matrix.</span></span> <span data-ttu-id="c4fa5-114">Siehe [**D3DMATRIX**](d3dmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="c4fa5-114">See [**D3DMATRIX**](d3dmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4fa5-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c4fa5-115">Return value</span></span>

<span data-ttu-id="c4fa5-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c4fa5-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c4fa5-117">Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-117">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="c4fa5-118">Wenn der Rückruf beim Festlegen des Geräte Zustands fehlschlägt, wird eine der folgenden Aktionen ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="c4fa5-118">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="c4fa5-119">Der Effekt schlägt während [**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md)fehl.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-119">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="c4fa5-120">Der dynamische Effekt Zustands Aufrufe (z. b. [**IDirect3DDevice9:: setTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)) schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-120">The dynamic effect state call (such as [**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4fa5-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c4fa5-121">Requirements</span></span>



| <span data-ttu-id="c4fa5-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c4fa5-122">Requirement</span></span> | <span data-ttu-id="c4fa5-123">Wert</span><span class="sxs-lookup"><span data-stu-id="c4fa5-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4fa5-124">Header</span><span class="sxs-lookup"><span data-stu-id="c4fa5-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c4fa5-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4fa5-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="c4fa5-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c4fa5-126">Library</span></span><br/> | <dl> <span data-ttu-id="c4fa5-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4fa5-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c4fa5-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4fa5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4fa5-129">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="c4fa5-129">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
