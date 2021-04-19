---
description: Ruft eine Zeichenfolge ab.
ms.assetid: 49388582-a110-4aa2-90ab-2282b59da951
title: 'ID3DXBaseEffect:: GetString-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetString
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 74c82bb80603dc4519e717d86297f6529ad36193
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350732"
---
# <a name="id3dxbaseeffectgetstring-method"></a><span data-ttu-id="879b2-103">ID3DXBaseEffect:: GetString-Methode</span><span class="sxs-lookup"><span data-stu-id="879b2-103">ID3DXBaseEffect::GetString method</span></span>

<span data-ttu-id="879b2-104">Ruft eine Zeichenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="879b2-104">Gets a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="879b2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="879b2-105">Syntax</span></span>


```C++
HRESULT GetString(
  [in]  D3DXHANDLE hParameter,
  [out] LPCSTR     *ppString
);
```



## <a name="parameters"></a><span data-ttu-id="879b2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="879b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="879b2-107">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="879b2-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="879b2-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="879b2-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="879b2-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="879b2-109">Unique identifier.</span></span> <span data-ttu-id="879b2-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="879b2-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="879b2-111">*ppString* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="879b2-111">*ppString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="879b2-112">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="879b2-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="879b2-113">Gibt eine durch hparameter identifizierte Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="879b2-113">Returns a string identified by hParameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="879b2-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="879b2-114">Return value</span></span>

<span data-ttu-id="879b2-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="879b2-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="879b2-116">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="879b2-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="879b2-117">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="879b2-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="879b2-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="879b2-118">Requirements</span></span>



| <span data-ttu-id="879b2-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="879b2-119">Requirement</span></span> | <span data-ttu-id="879b2-120">Wert</span><span class="sxs-lookup"><span data-stu-id="879b2-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="879b2-121">Header</span><span class="sxs-lookup"><span data-stu-id="879b2-121">Header</span></span><br/>  | <dl> <span data-ttu-id="879b2-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="879b2-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="879b2-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="879b2-123">Library</span></span><br/> | <dl> <span data-ttu-id="879b2-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="879b2-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="879b2-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="879b2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="879b2-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="879b2-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="879b2-127">**SetString**</span><span class="sxs-lookup"><span data-stu-id="879b2-127">**SetString**</span></span>](id3dxbaseeffect--setstring.md)
</dt> </dl>

 

 
