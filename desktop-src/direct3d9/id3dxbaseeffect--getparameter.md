---
description: Ruft das Handle eines Parameters der obersten Ebene oder eines Strukturmember-Parameters ab.
ms.assetid: 940f1bfd-ce62-4c86-88cc-787e62cf6a93
title: 'ID3DXBaseEffect:: GetParameter-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameter
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b7c96c371b36b8dcfc2e3e64a95798347ca3a6ea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050936"
---
# <a name="id3dxbaseeffectgetparameter-method"></a><span data-ttu-id="dfdee-103">ID3DXBaseEffect:: GetParameter-Methode</span><span class="sxs-lookup"><span data-stu-id="dfdee-103">ID3DXBaseEffect::GetParameter method</span></span>

<span data-ttu-id="dfdee-104">Ruft das Handle eines Parameters der obersten Ebene oder eines Strukturmember-Parameters ab.</span><span class="sxs-lookup"><span data-stu-id="dfdee-104">Gets the handle of a top-level parameter or a structure member parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfdee-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dfdee-105">Syntax</span></span>


```C++
D3DXHANDLE GetParameter(
  [in] D3DXHANDLE hParameter,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="dfdee-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dfdee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfdee-107">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfdee-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfdee-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="dfdee-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="dfdee-109">Handle des-Parameters oder **null** für Parameter der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="dfdee-109">Handle of the parameter, or **NULL** for top-level parameters.</span></span> <span data-ttu-id="dfdee-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="dfdee-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfdee-111">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfdee-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfdee-112">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dfdee-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dfdee-113">Parameterindex.</span><span class="sxs-lookup"><span data-stu-id="dfdee-113">Parameter index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfdee-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dfdee-114">Return value</span></span>

<span data-ttu-id="dfdee-115">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="dfdee-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="dfdee-116">Gibt das Handle des angegebenen Parameters oder **null** zurück, wenn der Index ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="dfdee-116">Returns the handle of the specified parameter, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="dfdee-117">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="dfdee-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dfdee-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dfdee-118">Requirements</span></span>



| <span data-ttu-id="dfdee-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dfdee-119">Requirement</span></span> | <span data-ttu-id="dfdee-120">Wert</span><span class="sxs-lookup"><span data-stu-id="dfdee-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfdee-121">Header</span><span class="sxs-lookup"><span data-stu-id="dfdee-121">Header</span></span><br/>  | <dl> <span data-ttu-id="dfdee-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfdee-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="dfdee-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dfdee-123">Library</span></span><br/> | <dl> <span data-ttu-id="dfdee-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dfdee-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="dfdee-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dfdee-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfdee-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="dfdee-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
