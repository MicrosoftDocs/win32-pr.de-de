---
description: Holen Sie sich die in einem Shader referenzierten samplernamen.
ms.assetid: fe769917-daac-43b8-bf63-fb337915ff53
title: D3DXGetShaderSamplers-Funktion (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderSamplers
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2135ba36f238188c6e7817001ba89bb47e3b9998
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365311"
---
# <a name="d3dxgetshadersamplers-function"></a><span data-ttu-id="54b17-103">D3DXGetShaderSamplers-Funktion</span><span class="sxs-lookup"><span data-stu-id="54b17-103">D3DXGetShaderSamplers function</span></span>

<span data-ttu-id="54b17-104">Holen Sie sich die in einem Shader referenzierten samplernamen.</span><span class="sxs-lookup"><span data-stu-id="54b17-104">Get the sampler names referenced in a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="54b17-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="54b17-105">Syntax</span></span>


```C++
HRESULT D3DXGetShaderSamplers(
  _In_    const DWORD  *pFunction,
  _Inout_       LPCSTR *pSamplers,
  _Out_         UINT   *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="54b17-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="54b17-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54b17-107">*pfunction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54b17-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54b17-108">Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="54b17-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="54b17-109">Zeiger auf den DWORD-Datenstrom der Shader-Funktion.</span><span class="sxs-lookup"><span data-stu-id="54b17-109">Pointer to the shader function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="54b17-110">*psamplers* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="54b17-110">*pSamplers* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="54b17-111">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="54b17-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="54b17-112">Zeiger auf ein Array von lpcstrins.</span><span class="sxs-lookup"><span data-stu-id="54b17-112">Pointer to an array of LPCSTRs.</span></span> <span data-ttu-id="54b17-113">Die-Funktion wird dieses Array mit Zeigern auf die in *pfunction* enthaltenen samplnamen ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="54b17-113">The function will fill this array with pointers to the sampler names contained within *pFunction*.</span></span> <span data-ttu-id="54b17-114">Die maximale Array Größe ist die maximale Anzahl von samplerregistern (16 für vs \_ 3 \_ 0 und PS \_ 3 \_ 0).</span><span class="sxs-lookup"><span data-stu-id="54b17-114">The maximum array size is the maximum number of sampler registers (16 for vs\_3\_0 and ps\_3\_0).</span></span>

<span data-ttu-id="54b17-115">Um die Anzahl der verwendeten Samplern zu ermitteln, überprüfen Sie *pcount* nach dem Aufruf von **D3DXGetShaderSamplers** mit psamplers = **null**.</span><span class="sxs-lookup"><span data-stu-id="54b17-115">To find the number of samplers used, check *pCount* after calling **D3DXGetShaderSamplers** with pSamplers = **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="54b17-116">*pcount* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="54b17-116">*pCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54b17-117">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="54b17-117">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="54b17-118">Gibt die Anzahl der Samplern zurück, auf die vom Shader verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="54b17-118">Returns the number of samplers referenced by the shader.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54b17-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="54b17-119">Return value</span></span>

<span data-ttu-id="54b17-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="54b17-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="54b17-121">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="54b17-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="54b17-122">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="54b17-122">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="54b17-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54b17-123">Requirements</span></span>



| <span data-ttu-id="54b17-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54b17-124">Requirement</span></span> | <span data-ttu-id="54b17-125">Wert</span><span class="sxs-lookup"><span data-stu-id="54b17-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="54b17-126">Header</span><span class="sxs-lookup"><span data-stu-id="54b17-126">Header</span></span><br/>  | <dl> <span data-ttu-id="54b17-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="54b17-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="54b17-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="54b17-128">Library</span></span><br/> | <dl> <span data-ttu-id="54b17-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54b17-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="54b17-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54b17-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54b17-131">Shaderfunktionen</span><span class="sxs-lookup"><span data-stu-id="54b17-131">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
