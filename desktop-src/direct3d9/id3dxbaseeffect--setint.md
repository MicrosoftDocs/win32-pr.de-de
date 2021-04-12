---
description: Legt eine ganze Zahl fest.
ms.assetid: 1090d4a6-b4f5-4e15-a49f-e2724f1c3f95
title: 'ID3DXBaseEffect:: abtint-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetInt
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 3c27d66544d4064c8d6c682db168b57b88d213cd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354107"
---
# <a name="id3dxbaseeffectsetint-method"></a><span data-ttu-id="a6fe6-103">ID3DXBaseEffect:: abtint-Methode</span><span class="sxs-lookup"><span data-stu-id="a6fe6-103">ID3DXBaseEffect::SetInt method</span></span>

<span data-ttu-id="a6fe6-104">Legt eine ganze Zahl fest.</span><span class="sxs-lookup"><span data-stu-id="a6fe6-104">Sets an integer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6fe6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6fe6-105">Syntax</span></span>


```C++
HRESULT SetInt(
  [in] D3DXHANDLE hParameter,
  [in] INT        n
);
```



## <a name="parameters"></a><span data-ttu-id="a6fe6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6fe6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6fe6-107">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6fe6-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6fe6-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="a6fe6-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="a6fe6-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="a6fe6-109">Unique identifier.</span></span> <span data-ttu-id="a6fe6-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="a6fe6-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6fe6-111">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6fe6-111">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6fe6-112">Typ: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a6fe6-112">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a6fe6-113">Wert für ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="a6fe6-113">Integer value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6fe6-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a6fe6-114">Return value</span></span>

<span data-ttu-id="a6fe6-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a6fe6-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a6fe6-116">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a6fe6-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a6fe6-117">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="a6fe6-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6fe6-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6fe6-118">Requirements</span></span>



| <span data-ttu-id="a6fe6-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a6fe6-119">Requirement</span></span> | <span data-ttu-id="a6fe6-120">Wert</span><span class="sxs-lookup"><span data-stu-id="a6fe6-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6fe6-121">Header</span><span class="sxs-lookup"><span data-stu-id="a6fe6-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a6fe6-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6fe6-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="a6fe6-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a6fe6-123">Library</span></span><br/> | <dl> <span data-ttu-id="a6fe6-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a6fe6-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a6fe6-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6fe6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6fe6-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="a6fe6-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="a6fe6-127">**GetInt**</span><span class="sxs-lookup"><span data-stu-id="a6fe6-127">**GetInt**</span></span>](id3dxbaseeffect--getint.md)
</dt> </dl>

 

 
