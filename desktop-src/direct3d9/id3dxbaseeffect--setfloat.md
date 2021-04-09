---
description: Legt einen Gleit Komma Wert fest.
ms.assetid: f49fb4d2-6e3d-4452-8102-76200c55cf1f
title: 'ID3DXBaseEffect:: SetFloat-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetFloat
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: af955748fff66e67e0e2f5650b869a746168de54
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870079"
---
# <a name="id3dxbaseeffectsetfloat-method"></a><span data-ttu-id="f2c33-103">ID3DXBaseEffect:: SetFloat-Methode</span><span class="sxs-lookup"><span data-stu-id="f2c33-103">ID3DXBaseEffect::SetFloat method</span></span>

<span data-ttu-id="f2c33-104">Legt einen Gleit Komma Wert fest.</span><span class="sxs-lookup"><span data-stu-id="f2c33-104">Sets a floating point value.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2c33-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2c33-105">Syntax</span></span>


```C++
HRESULT SetFloat(
  [in] D3DXHANDLE hParameter,
  [in] FLOAT      f
);
```



## <a name="parameters"></a><span data-ttu-id="f2c33-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2c33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2c33-107">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2c33-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2c33-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="f2c33-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="f2c33-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="f2c33-109">Unique identifier.</span></span> <span data-ttu-id="f2c33-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="f2c33-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2c33-111">*f* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2c33-111">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2c33-112">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f2c33-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f2c33-113">Gleit Komma Wert.</span><span class="sxs-lookup"><span data-stu-id="f2c33-113">Floating point value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2c33-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f2c33-114">Return value</span></span>

<span data-ttu-id="f2c33-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f2c33-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f2c33-116">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f2c33-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f2c33-117">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="f2c33-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2c33-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2c33-118">Requirements</span></span>



| <span data-ttu-id="f2c33-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2c33-119">Requirement</span></span> | <span data-ttu-id="f2c33-120">Wert</span><span class="sxs-lookup"><span data-stu-id="f2c33-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2c33-121">Header</span><span class="sxs-lookup"><span data-stu-id="f2c33-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f2c33-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2c33-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="f2c33-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f2c33-123">Library</span></span><br/> | <dl> <span data-ttu-id="f2c33-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2c33-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f2c33-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2c33-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2c33-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="f2c33-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="f2c33-127">**GetFloat**</span><span class="sxs-lookup"><span data-stu-id="f2c33-127">**GetFloat**</span></span>](id3dxbaseeffect--getfloat.md)
</dt> </dl>

 

 
