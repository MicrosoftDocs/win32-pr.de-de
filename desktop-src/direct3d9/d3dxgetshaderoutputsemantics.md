---
description: Die Semantik für alle Shader-Ausgabe Elemente erhalten.
ms.assetid: 1a3cdd5d-0ea7-48ae-a3f1-030e95b03a42
title: D3DXGetShaderOutputSemantics-Funktion (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderOutputSemantics
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 264db967d2959c2f6e5096e0362e9db576ba9f94
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530902"
---
# <a name="d3dxgetshaderoutputsemantics-function"></a><span data-ttu-id="55a57-103">D3DXGetShaderOutputSemantics-Funktion</span><span class="sxs-lookup"><span data-stu-id="55a57-103">D3DXGetShaderOutputSemantics function</span></span>

<span data-ttu-id="55a57-104">Die Semantik für alle Shader-Ausgabe Elemente erhalten.</span><span class="sxs-lookup"><span data-stu-id="55a57-104">Get the semantics for all shader output elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="55a57-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="55a57-105">Syntax</span></span>


```C++
HRESULT D3DXGetShaderOutputSemantics(
  _In_  const DWORD        *pFunction,
  _In_        D3DXSEMANTIC *pSemantics,
  _Out_       UINT         *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="55a57-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="55a57-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55a57-107">*pfunction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55a57-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55a57-108">Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="55a57-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="55a57-109">Zeiger auf den DWORD-Datenstrom der Shader-Funktion.</span><span class="sxs-lookup"><span data-stu-id="55a57-109">Pointer to the shader function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="55a57-110">*psemantik* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55a57-110">*pSemantics* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55a57-111">Typ: **[ **D3DXSEMANTIC**](d3dxsemantic.md)\***</span><span class="sxs-lookup"><span data-stu-id="55a57-111">Type: **[**D3DXSEMANTIC**](d3dxsemantic.md)\***</span></span>

<span data-ttu-id="55a57-112">Zeiger auf ein Array von [**D3DXSEMANTIC**](d3dxsemantic.md) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="55a57-112">Pointer to an array of [**D3DXSEMANTIC**](d3dxsemantic.md) structures.</span></span> <span data-ttu-id="55a57-113">Die Funktion gibt dieses Array mit der Semantik für jedes Ausgabe Element aus, auf das vom Shader verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="55a57-113">The function will fill this array with the semantics for each output element referenced by the shader.</span></span> <span data-ttu-id="55a57-114">Es wird davon ausgegangen, dass in diesem Array mindestens MAXD3DDECLLENGTH Elemente enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="55a57-114">This array is assumed to contain at least MAXD3DDECLLENGTH elements.</span></span> <span data-ttu-id="55a57-115">Wenn Sie **D3DXGetShaderOutputSemantics** mit psemantics = **null** aufrufen, wird jedoch die Anzahl der für pcount benötigten Elemente zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="55a57-115">However, calling **D3DXGetShaderOutputSemantics** with pSemantics = **NULL** will return the number of elements needed for pCount.</span></span>

</dd> <dt>

<span data-ttu-id="55a57-116">*pcount* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="55a57-116">*pCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="55a57-117">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="55a57-117">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="55a57-118">Gibt die Anzahl der Elemente in psemantik zurück.</span><span class="sxs-lookup"><span data-stu-id="55a57-118">Returns the number of elements in pSemantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55a57-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="55a57-119">Return value</span></span>

<span data-ttu-id="55a57-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="55a57-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="55a57-121">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="55a57-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="55a57-122">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="55a57-122">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="55a57-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55a57-123">Requirements</span></span>



| <span data-ttu-id="55a57-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="55a57-124">Requirement</span></span> | <span data-ttu-id="55a57-125">Wert</span><span class="sxs-lookup"><span data-stu-id="55a57-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="55a57-126">Header</span><span class="sxs-lookup"><span data-stu-id="55a57-126">Header</span></span><br/>  | <dl> <span data-ttu-id="55a57-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="55a57-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="55a57-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="55a57-128">Library</span></span><br/> | <dl> <span data-ttu-id="55a57-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="55a57-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="55a57-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55a57-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55a57-131">Shaderfunktionen</span><span class="sxs-lookup"><span data-stu-id="55a57-131">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
