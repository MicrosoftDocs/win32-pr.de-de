---
description: Ruft den literalstatus eines Parameters ab. Ein literalparameter weist einen Wert auf, der sich während der Lebensdauer eines Effekts nicht ändert.
ms.assetid: 417abbee-5193-462e-b0d1-b4928ad0a041
title: 'ID3DXEffectCompiler:: getliteralmethode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.GetLiteral
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c16e3798ab66a34e12812a3560572c45b9206b30
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364352"
---
# <a name="id3dxeffectcompilergetliteral-method"></a><span data-ttu-id="2e61b-104">ID3DXEffectCompiler:: getliteralmethode</span><span class="sxs-lookup"><span data-stu-id="2e61b-104">ID3DXEffectCompiler::GetLiteral method</span></span>

<span data-ttu-id="2e61b-105">Ruft den literalstatus eines Parameters ab.</span><span class="sxs-lookup"><span data-stu-id="2e61b-105">Gets a literal status of a parameter.</span></span> <span data-ttu-id="2e61b-106">Ein literalparameter weist einen Wert auf, der sich während der Lebensdauer eines Effekts nicht ändert.</span><span class="sxs-lookup"><span data-stu-id="2e61b-106">A literal parameter has a value that doesn't change during the lifetime of an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e61b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e61b-107">Syntax</span></span>


```C++
HRESULT GetLiteral(
  [in]  D3DXHANDLE hParameter,
  [out] BOOL       *pLiteral
);
```



## <a name="parameters"></a><span data-ttu-id="2e61b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e61b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e61b-109">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e61b-109">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e61b-110">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2e61b-110">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2e61b-111">Eindeutiger Bezeichner für einen Parameter.</span><span class="sxs-lookup"><span data-stu-id="2e61b-111">Unique identifier to a parameter.</span></span> <span data-ttu-id="2e61b-112">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="2e61b-112">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e61b-113">*pliteral* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2e61b-113">*pLiteral* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e61b-114">Typ: **[ **bool**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2e61b-114">Type: **[**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2e61b-115">Gibt true zurück, wenn der-Parameter ein Literalwert ist, andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="2e61b-115">Returns True if the parameter is a literal, and False otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e61b-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2e61b-116">Return value</span></span>

<span data-ttu-id="2e61b-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2e61b-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2e61b-118">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2e61b-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2e61b-119">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="2e61b-119">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e61b-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e61b-120">Remarks</span></span>

<span data-ttu-id="2e61b-121">Diese Methoden ändern nur, ob der Parameter ein Literalwert ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="2e61b-121">This methods only changes whether the parameter is a literal or not.</span></span> <span data-ttu-id="2e61b-122">Um den Wert eines Parameters zu ändern, verwenden Sie eine Methode wie [**ID3DXBaseEffect:: SetBool**](id3dxbaseeffect--setbool.md) oder [**ID3DXBaseEffect:: SetValue**](id3dxbaseeffect--setvalue.md).</span><span class="sxs-lookup"><span data-stu-id="2e61b-122">To change the value of a parameter, use a method like [**ID3DXBaseEffect::SetBool**](id3dxbaseeffect--setbool.md) or [**ID3DXBaseEffect::SetValue**](id3dxbaseeffect--setvalue.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2e61b-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e61b-123">Requirements</span></span>



| <span data-ttu-id="2e61b-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e61b-124">Requirement</span></span> | <span data-ttu-id="2e61b-125">Wert</span><span class="sxs-lookup"><span data-stu-id="2e61b-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e61b-126">Header</span><span class="sxs-lookup"><span data-stu-id="2e61b-126">Header</span></span><br/>  | <dl> <span data-ttu-id="2e61b-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e61b-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="2e61b-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2e61b-128">Library</span></span><br/> | <dl> <span data-ttu-id="2e61b-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e61b-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2e61b-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e61b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e61b-131">ID3DXEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="2e61b-131">ID3DXEffectCompiler</span></span>](id3dxeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="2e61b-132">Verwendungen und Literale (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2e61b-132">Usages and Literals (Direct3D 9)</span></span>](usages-and-literals.md)
</dt> <dt>

[<span data-ttu-id="2e61b-133">**ID3DXEffectCompiler:: setliteral**</span><span class="sxs-lookup"><span data-stu-id="2e61b-133">**ID3DXEffectCompiler::SetLiteral**</span></span>](id3dxeffectcompiler--setliteral.md)
</dt> </dl>

 

 
