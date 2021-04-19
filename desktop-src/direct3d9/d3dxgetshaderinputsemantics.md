---
description: Ruft die Semantik für die shadereingaben ab. Verwenden Sie diese Methode, um das Format der Eingabe Vertex zu bestimmen.
ms.assetid: e94b2b14-3830-4a13-8c23-7841a56d6730
title: D3DXGetShaderInputSemantics-Funktion (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderInputSemantics
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2032f241d6ca5c22506c0875a21f9d5b431920df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355186"
---
# <a name="d3dxgetshaderinputsemantics-function"></a><span data-ttu-id="cdcb9-104">D3DXGetShaderInputSemantics-Funktion</span><span class="sxs-lookup"><span data-stu-id="cdcb9-104">D3DXGetShaderInputSemantics function</span></span>

<span data-ttu-id="cdcb9-105">Ruft die Semantik für die shadereingaben ab.</span><span class="sxs-lookup"><span data-stu-id="cdcb9-105">Gets the semantics for the shader inputs.</span></span> <span data-ttu-id="cdcb9-106">Verwenden Sie diese Methode, um das Format der Eingabe Vertex zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="cdcb9-106">Use this method to determine the input vertex format.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdcb9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cdcb9-107">Syntax</span></span>


```C++
HRESULT D3DXGetShaderInputSemantics(
  _In_  const DWORD        *pFunction,
  _In_        D3DXSEMANTIC *pSemantics,
  _Out_       UINT         *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="cdcb9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cdcb9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdcb9-109">*pfunction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdcb9-109">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdcb9-110">Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="cdcb9-110">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cdcb9-111">Zeiger auf den DWORD-Datenstrom der Shader-Funktion.</span><span class="sxs-lookup"><span data-stu-id="cdcb9-111">Pointer to the shader function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="cdcb9-112">*psemantik* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdcb9-112">*pSemantics* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdcb9-113">Typ: **[ **D3DXSEMANTIC**](d3dxsemantic.md)\***</span><span class="sxs-lookup"><span data-stu-id="cdcb9-113">Type: **[**D3DXSEMANTIC**](d3dxsemantic.md)\***</span></span>

<span data-ttu-id="cdcb9-114">Zeiger auf ein Array von [**D3DXSEMANTIC**](d3dxsemantic.md) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="cdcb9-114">Pointer to an array of [**D3DXSEMANTIC**](d3dxsemantic.md) structures.</span></span> <span data-ttu-id="cdcb9-115">Die Funktion gibt dieses Array mit der Semantik für jedes Eingabe Element aus, auf das vom Shader verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="cdcb9-115">The function will fill this array with the semantics for each input element referenced by the shader.</span></span> <span data-ttu-id="cdcb9-116">Es wird davon ausgegangen, dass in diesem Array mindestens MAXD3DDECLLENGTH Elemente enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="cdcb9-116">This array is assumed to contain at least MAXD3DDECLLENGTH elements.</span></span> <span data-ttu-id="cdcb9-117">Wenn Sie **D3DXGetShaderInputSemantics** mit psemantics = **null** aufrufen, wird jedoch die Anzahl der für pcount benötigten Elemente zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cdcb9-117">However, calling **D3DXGetShaderInputSemantics** with pSemantics = **NULL** will return the number of elements needed for pCount.</span></span>

</dd> <dt>

<span data-ttu-id="cdcb9-118">*pcount* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cdcb9-118">*pCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cdcb9-119">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="cdcb9-119">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cdcb9-120">Gibt die Anzahl der Elemente in psemantik zurück.</span><span class="sxs-lookup"><span data-stu-id="cdcb9-120">Returns the number of elements in pSemantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdcb9-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cdcb9-121">Return value</span></span>

<span data-ttu-id="cdcb9-122">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cdcb9-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cdcb9-123">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cdcb9-123">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cdcb9-124">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="cdcb9-124">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdcb9-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cdcb9-125">Remarks</span></span>

<span data-ttu-id="cdcb9-126">Verwenden Sie **D3DXGetShaderInputSemantics** , um eine Liste der vom Shader benötigten Eingabe Semantik zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="cdcb9-126">Use **D3DXGetShaderInputSemantics** to return a list of input semantics required by the shader.</span></span> <span data-ttu-id="cdcb9-127">Auf diese Weise können Sie herausfinden, was das Eingabe Vertex-Format für einen HLSL-Shader (High-Level Shader Language) ist.</span><span class="sxs-lookup"><span data-stu-id="cdcb9-127">This is the way to find out what the input vertex format is for a high-level shader language (HLSL) shader.</span></span> <span data-ttu-id="cdcb9-128">Wenn der Shader zusätzliche Eingaben hat, die ihre Scheitelpunkt Deklaration fehlt, können Sie einen zusätzlichen vertexstream mit einem Sprung von 0 erstellen, der die fehlenden Komponenten mit den Standardwerten aufweist.</span><span class="sxs-lookup"><span data-stu-id="cdcb9-128">If the shader has additional inputs that your vertex declaration is missing, you could create an extra vertex stream that has a stride of 0 that has the missing components with default values.</span></span> <span data-ttu-id="cdcb9-129">Diese Technik könnte beispielsweise verwendet werden, um Standard Scheitelpunkt Farben für Modelle bereitzustellen, die diese nicht angeben.</span><span class="sxs-lookup"><span data-stu-id="cdcb9-129">For instance, this technique could be used to provide default vertex color for models that do not specify it.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdcb9-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cdcb9-130">Requirements</span></span>



| <span data-ttu-id="cdcb9-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cdcb9-131">Requirement</span></span> | <span data-ttu-id="cdcb9-132">Wert</span><span class="sxs-lookup"><span data-stu-id="cdcb9-132">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdcb9-133">Header</span><span class="sxs-lookup"><span data-stu-id="cdcb9-133">Header</span></span><br/>  | <dl> <span data-ttu-id="cdcb9-134"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdcb9-134"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="cdcb9-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cdcb9-135">Library</span></span><br/> | <dl> <span data-ttu-id="cdcb9-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cdcb9-136"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="cdcb9-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cdcb9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdcb9-138">Shaderfunktionen</span><span class="sxs-lookup"><span data-stu-id="cdcb9-138">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
