---
description: Das Handle eines Array Element-Parameters erhalten.
ms.assetid: fe8edbc5-dc1d-4386-8149-489541d55bde
title: 'ID3DXBaseEffect:: getparameterelement-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterElement
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5130ccf57634f9b1a569a1dd70833fe2014e1a74
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355876"
---
# <a name="id3dxbaseeffectgetparameterelement-method"></a><span data-ttu-id="912cb-103">ID3DXBaseEffect:: getparameterelement-Methode</span><span class="sxs-lookup"><span data-stu-id="912cb-103">ID3DXBaseEffect::GetParameterElement method</span></span>

<span data-ttu-id="912cb-104">Das Handle eines Array Element-Parameters erhalten.</span><span class="sxs-lookup"><span data-stu-id="912cb-104">Get the handle of an array element parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="912cb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="912cb-105">Syntax</span></span>


```C++
D3DXHANDLE GetParameterElement(
  [in] D3DXHANDLE hParameter,
  [in] UINT       ElementIndex
);
```



## <a name="parameters"></a><span data-ttu-id="912cb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="912cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="912cb-107">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="912cb-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="912cb-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="912cb-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="912cb-109">Handle des Arrays.</span><span class="sxs-lookup"><span data-stu-id="912cb-109">Handle of the array.</span></span> <span data-ttu-id="912cb-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="912cb-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="912cb-111">*Element Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="912cb-111">*ElementIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="912cb-112">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="912cb-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="912cb-113">Array Element Index.</span><span class="sxs-lookup"><span data-stu-id="912cb-113">Array element index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="912cb-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="912cb-114">Return value</span></span>

<span data-ttu-id="912cb-115">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="912cb-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="912cb-116">Gibt das Handle des angegebenen Parameters zurück, oder **null** , wenn hparameter oder Elementindex ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="912cb-116">Returns the handle of the specified parameter, or **NULL** if either hParameter or ElementIndex is invalid.</span></span> <span data-ttu-id="912cb-117">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="912cb-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="912cb-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="912cb-118">Remarks</span></span>

<span data-ttu-id="912cb-119">Diese Methode wird verwendet, um ein Element eines Parameters zu erhalten, bei dem es sich um ein Array handelt.</span><span class="sxs-lookup"><span data-stu-id="912cb-119">This method is used to get an element of a parameter that is an array.</span></span>

## <a name="requirements"></a><span data-ttu-id="912cb-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="912cb-120">Requirements</span></span>



| <span data-ttu-id="912cb-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="912cb-121">Requirement</span></span> | <span data-ttu-id="912cb-122">Wert</span><span class="sxs-lookup"><span data-stu-id="912cb-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="912cb-123">Header</span><span class="sxs-lookup"><span data-stu-id="912cb-123">Header</span></span><br/>  | <dl> <span data-ttu-id="912cb-124"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="912cb-124"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="912cb-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="912cb-125">Library</span></span><br/> | <dl> <span data-ttu-id="912cb-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="912cb-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="912cb-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="912cb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="912cb-128">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="912cb-128">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
