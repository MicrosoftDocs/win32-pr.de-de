---
description: Ruft eine Pass Beschreibung ab.
ms.assetid: 44c65a82-bcf4-49f5-9312-8320e133bb2f
title: 'ID3DXBaseEffect:: getpassdesc-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPassDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 15a997470fddf5056b7191fcc3226ad210724041
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363185"
---
# <a name="id3dxbaseeffectgetpassdesc-method"></a><span data-ttu-id="20291-103">ID3DXBaseEffect:: getpassdesc-Methode</span><span class="sxs-lookup"><span data-stu-id="20291-103">ID3DXBaseEffect::GetPassDesc method</span></span>

<span data-ttu-id="20291-104">Ruft eine Pass Beschreibung ab.</span><span class="sxs-lookup"><span data-stu-id="20291-104">Gets a pass description.</span></span>

## <a name="syntax"></a><span data-ttu-id="20291-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="20291-105">Syntax</span></span>


```C++
HRESULT GetPassDesc(
  [in]  D3DXHANDLE    hPass,
  [out] D3DXPASS_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="20291-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="20291-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20291-107">*hpass* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="20291-107">*hPass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20291-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="20291-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="20291-109">Pass-handle.</span><span class="sxs-lookup"><span data-stu-id="20291-109">Pass handle.</span></span> <span data-ttu-id="20291-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="20291-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="20291-111">*PDE SC* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="20291-111">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20291-112">Typ: **[ **D3DXPASS \_ DESC**](d3dxpass-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="20291-112">Type: **[**D3DXPASS\_DESC**](d3dxpass-desc.md)\***</span></span>

<span data-ttu-id="20291-113">Gibt eine Beschreibung des angegebenen Pass zurück.</span><span class="sxs-lookup"><span data-stu-id="20291-113">Returns a description of the specified pass.</span></span> <span data-ttu-id="20291-114">Weitere Informationen finden Sie unter [**D3DXPASS \_**](d3dxpass-desc.md).</span><span class="sxs-lookup"><span data-stu-id="20291-114">See [**D3DXPASS\_DESC**](d3dxpass-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20291-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="20291-115">Return value</span></span>

<span data-ttu-id="20291-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="20291-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="20291-117">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="20291-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="20291-118">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="20291-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="20291-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="20291-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="20291-120">Wenn ein Effekt mit [D3DXFX \_ Not \_ cloneable](d3dxfx.md)erstellt wird, gibt diese Methode **null** -Zeiger (in [**D3DXPASS \_ DESC**](d3dxpass-desc.md)) an die Shader-Funktionen zurück.</span><span class="sxs-lookup"><span data-stu-id="20291-120">If an effect is created with [D3DXFX\_NOT\_CLONEABLE](d3dxfx.md), this method will return **NULL** pointers (in [**D3DXPASS\_DESC**](d3dxpass-desc.md)) to the shader functions.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="20291-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="20291-121">Requirements</span></span>



| <span data-ttu-id="20291-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="20291-122">Requirement</span></span> | <span data-ttu-id="20291-123">Wert</span><span class="sxs-lookup"><span data-stu-id="20291-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="20291-124">Header</span><span class="sxs-lookup"><span data-stu-id="20291-124">Header</span></span><br/>  | <dl> <span data-ttu-id="20291-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="20291-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="20291-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="20291-126">Library</span></span><br/> | <dl> <span data-ttu-id="20291-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20291-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="20291-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20291-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20291-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="20291-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 




