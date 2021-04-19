---
description: Ruft einen Gleit Komma Wert ab.
ms.assetid: 239dd29c-092a-4b9f-ba24-eb6181e91461
title: 'ID3DXBaseEffect:: GetFloat-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFloat
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 51edaa1872223727abdc396766552720cd34d726
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370471"
---
# <a name="id3dxbaseeffectgetfloat-method"></a><span data-ttu-id="5dd52-103">ID3DXBaseEffect:: GetFloat-Methode</span><span class="sxs-lookup"><span data-stu-id="5dd52-103">ID3DXBaseEffect::GetFloat method</span></span>

<span data-ttu-id="5dd52-104">Ruft einen Gleit Komma Wert ab.</span><span class="sxs-lookup"><span data-stu-id="5dd52-104">Gets a floating point value.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dd52-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5dd52-105">Syntax</span></span>


```C++
HRESULT GetFloat(
  [in]  D3DXHANDLE hParameter,
  [out] FLOAT      *pf
);
```



## <a name="parameters"></a><span data-ttu-id="5dd52-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5dd52-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dd52-107">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5dd52-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5dd52-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="5dd52-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="5dd52-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="5dd52-109">Unique identifier.</span></span> <span data-ttu-id="5dd52-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="5dd52-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="5dd52-111">*PF* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5dd52-111">*pf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5dd52-112">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5dd52-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5dd52-113">Gibt einen Gleit Komma Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5dd52-113">Returns a floating point value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5dd52-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5dd52-114">Return value</span></span>

<span data-ttu-id="5dd52-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5dd52-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5dd52-116">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5dd52-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5dd52-117">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="5dd52-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="5dd52-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5dd52-118">Requirements</span></span>



| <span data-ttu-id="5dd52-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5dd52-119">Requirement</span></span> | <span data-ttu-id="5dd52-120">Wert</span><span class="sxs-lookup"><span data-stu-id="5dd52-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5dd52-121">Header</span><span class="sxs-lookup"><span data-stu-id="5dd52-121">Header</span></span><br/>  | <dl> <span data-ttu-id="5dd52-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="5dd52-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="5dd52-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5dd52-123">Library</span></span><br/> | <dl> <span data-ttu-id="5dd52-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5dd52-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5dd52-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5dd52-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dd52-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="5dd52-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="5dd52-127">**SetFloat**</span><span class="sxs-lookup"><span data-stu-id="5dd52-127">**SetFloat**</span></span>](id3dxbaseeffect--setfloat.md)
</dt> </dl>

 

 
