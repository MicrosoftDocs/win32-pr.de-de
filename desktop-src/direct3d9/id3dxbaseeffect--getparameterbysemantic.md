---
description: Ruft das Handle eines Parameters der obersten Ebene oder eines Strukturmember-Parameters ab, indem seine Semantik mit einer Suche ohne Berücksichtigung der Groß-/Kleinschreibung gesucht wird
ms.assetid: 3de3791a-fe09-4a39-bd6f-0e20a641dd32
title: 'ID3DXBaseEffect:: getparameterbysemantic-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterBySemantic
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c70d30d68d73d6c4dd33d483747be4293a255693
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355877"
---
# <a name="id3dxbaseeffectgetparameterbysemantic-method"></a><span data-ttu-id="33a56-103">ID3DXBaseEffect:: getparameterbysemantic-Methode</span><span class="sxs-lookup"><span data-stu-id="33a56-103">ID3DXBaseEffect::GetParameterBySemantic method</span></span>

<span data-ttu-id="33a56-104">Ruft das Handle eines Parameters der obersten Ebene oder eines Strukturmember-Parameters ab, indem seine Semantik mit einer Suche ohne Berücksichtigung der Groß-/Kleinschreibung gesucht wird</span><span class="sxs-lookup"><span data-stu-id="33a56-104">Gets the handle of a top-level parameter or a structure member parameter by looking up its semantic with a case-insensitive search.</span></span>

## <a name="syntax"></a><span data-ttu-id="33a56-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="33a56-105">Syntax</span></span>


```C++
D3DXHANDLE GetParameterBySemantic(
  [in] D3DXHANDLE hParameter,
  [in] LPCSTR     pSemantic
);
```



## <a name="parameters"></a><span data-ttu-id="33a56-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="33a56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33a56-107">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="33a56-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33a56-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="33a56-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="33a56-109">Handle des-Parameters oder **null** für Parameter der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="33a56-109">Handle of the parameter, or **NULL** for top-level parameters.</span></span> <span data-ttu-id="33a56-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="33a56-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="33a56-111">*psemantic* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="33a56-111">*pSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33a56-112">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33a56-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="33a56-113">Zeichenfolge, die den semantischen Namen enthält.</span><span class="sxs-lookup"><span data-stu-id="33a56-113">String containing the semantic name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33a56-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="33a56-114">Return value</span></span>

<span data-ttu-id="33a56-115">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="33a56-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="33a56-116">Gibt das Handle des ersten Parameters zurück, der der angegebenen Semantik entspricht, oder **null** , wenn die Semantik nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="33a56-116">Returns the handle of the first parameter that matches the specified semantic, or **NULL** if the semantic was not found.</span></span> <span data-ttu-id="33a56-117">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="33a56-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="33a56-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33a56-118">Requirements</span></span>



| <span data-ttu-id="33a56-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33a56-119">Requirement</span></span> | <span data-ttu-id="33a56-120">Wert</span><span class="sxs-lookup"><span data-stu-id="33a56-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="33a56-121">Header</span><span class="sxs-lookup"><span data-stu-id="33a56-121">Header</span></span><br/>  | <dl> <span data-ttu-id="33a56-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="33a56-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="33a56-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="33a56-123">Library</span></span><br/> | <dl> <span data-ttu-id="33a56-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="33a56-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="33a56-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33a56-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33a56-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="33a56-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
