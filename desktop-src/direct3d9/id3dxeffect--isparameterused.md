---
description: Bestimmt, ob ein Parameter von der Technik verwendet wird.
ms.assetid: ac50c0d3-93d9-4477-a854-d0b53df28c90
title: 'ID3DXEffect:: isparameterused-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.IsParameterUsed
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6cbe4783a9ad5b618f05941eae08af4c15be0512
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132301"
---
# <a name="id3dxeffectisparameterused-method"></a><span data-ttu-id="da1d4-103">ID3DXEffect:: isparameterused-Methode</span><span class="sxs-lookup"><span data-stu-id="da1d4-103">ID3DXEffect::IsParameterUsed method</span></span>

<span data-ttu-id="da1d4-104">Bestimmt, ob ein Parameter von der Technik verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="da1d4-104">Determines if a parameter is used by the technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="da1d4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="da1d4-105">Syntax</span></span>


```C++
BOOL IsParameterUsed(
  [in] D3DXHANDLE hParameter,
  [in] D3DXHANDLE hTechnique
);
```



## <a name="parameters"></a><span data-ttu-id="da1d4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="da1d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da1d4-107">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da1d4-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da1d4-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="da1d4-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="da1d4-109">Eindeutiger Bezeichner für den Parameter.</span><span class="sxs-lookup"><span data-stu-id="da1d4-109">Unique identifier for the parameter.</span></span> <span data-ttu-id="da1d4-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="da1d4-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="da1d4-111">*htechnik* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da1d4-111">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da1d4-112">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="da1d4-112">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="da1d4-113">Eindeutiger Bezeichner für die Technik.</span><span class="sxs-lookup"><span data-stu-id="da1d4-113">Unique identifier for the technique.</span></span> <span data-ttu-id="da1d4-114">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="da1d4-114">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da1d4-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="da1d4-115">Return value</span></span>

<span data-ttu-id="da1d4-116">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="da1d4-116">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="da1d4-117">Gibt **true** zurück, wenn der-Parameter verwendet wird, und gibt **false** zurück, wenn der-Parameter nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="da1d4-117">Returns **TRUE** if the parameter is being used and returns **FALSE** if the parameter is not being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="da1d4-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da1d4-118">Requirements</span></span>



| <span data-ttu-id="da1d4-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da1d4-119">Requirement</span></span> | <span data-ttu-id="da1d4-120">Wert</span><span class="sxs-lookup"><span data-stu-id="da1d4-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="da1d4-121">Header</span><span class="sxs-lookup"><span data-stu-id="da1d4-121">Header</span></span><br/>  | <dl> <span data-ttu-id="da1d4-122"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="da1d4-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="da1d4-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="da1d4-123">Library</span></span><br/> | <dl> <span data-ttu-id="da1d4-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="da1d4-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="da1d4-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da1d4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da1d4-126">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="da1d4-126">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
