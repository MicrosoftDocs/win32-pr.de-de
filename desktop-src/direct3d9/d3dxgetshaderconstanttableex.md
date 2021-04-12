---
description: Ruft die in einen Shader eingebettete Shader-Konstante Tabelle ab.
ms.assetid: f7e846e4-9cb4-4634-95e3-4b2a752978a8
title: D3DXGetShaderConstantTableEx-Funktion (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderConstantTableEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2107e7f30733c8f8a19e39e220c4c1d6cb174424
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219511"
---
# <a name="d3dxgetshaderconstanttableex-function"></a><span data-ttu-id="82a38-103">D3DXGetShaderConstantTableEx-Funktion</span><span class="sxs-lookup"><span data-stu-id="82a38-103">D3DXGetShaderConstantTableEx function</span></span>

<span data-ttu-id="82a38-104">Ruft die in einen Shader eingebettete Shader-Konstante Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="82a38-104">Gets the shader-constant table embedded inside a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="82a38-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="82a38-105">Syntax</span></span>


```C++
HRESULT D3DXGetShaderConstantTableEx(
  _In_  const DWORD               *pFunction,
  _In_        DWORD               Flags,
  _Out_       LPD3DXCONSTANTTABLE * ppConstantTable
);
```



## <a name="parameters"></a><span data-ttu-id="82a38-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="82a38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82a38-107">*pfunction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82a38-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82a38-108">Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="82a38-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="82a38-109">Ein Zeiger auf die Funktion DWORD-Stream.</span><span class="sxs-lookup"><span data-stu-id="82a38-109">Pointer to the function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="82a38-110">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="82a38-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82a38-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82a38-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="82a38-112">Verwenden Sie das D3DXCONSTTABLE \_ LARGEADDRESSAWARE-Flag, um auf bis zu 4 GB virtuellen Adressraum zuzugreifen (anstelle der Standardeinstellung von 2 GB).</span><span class="sxs-lookup"><span data-stu-id="82a38-112">Use the D3DXCONSTTABLE\_LARGEADDRESSAWARE flag to access up to 4 GB of virtual address space (instead of the default of 2 GB).</span></span> <span data-ttu-id="82a38-113">Wenn Sie den zusätzlichen virtuellen Adressraum nicht benötigen, verwenden Sie [**D3DXGetShaderConstantTable**](d3dxgetshaderconstanttable.md).</span><span class="sxs-lookup"><span data-stu-id="82a38-113">If you do not need the additional virtual address space, use [**D3DXGetShaderConstantTable**](d3dxgetshaderconstanttable.md).</span></span>

</dd> <dt>

 <span data-ttu-id="82a38-114">*ppconstanbar* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="82a38-114">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82a38-115">Typ: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="82a38-115">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="82a38-116">Gibt die Konstante Tabellen Schnittstelle (siehe [**ID3DXConstantTable**](id3dxconstanttable.md)) zurück, die die Konstante Tabelle verwaltet.</span><span class="sxs-lookup"><span data-stu-id="82a38-116">Returns the constant table interface (see [**ID3DXConstantTable**](id3dxconstanttable.md)) that manages the constant table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82a38-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="82a38-117">Return value</span></span>

<span data-ttu-id="82a38-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="82a38-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="82a38-119">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="82a38-119">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="82a38-120">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="82a38-120">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="82a38-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82a38-121">Remarks</span></span>

<span data-ttu-id="82a38-122">Eine Konstante Tabelle wird von [**D3DXCompileShader**](d3dxcompileshader.md) generiert und in den Shader-Text eingebettet.</span><span class="sxs-lookup"><span data-stu-id="82a38-122">A constant table is generated by [**D3DXCompileShader**](d3dxcompileshader.md) and embedded in the shader body.</span></span>

## <a name="requirements"></a><span data-ttu-id="82a38-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="82a38-123">Requirements</span></span>



| <span data-ttu-id="82a38-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="82a38-124">Requirement</span></span> | <span data-ttu-id="82a38-125">Wert</span><span class="sxs-lookup"><span data-stu-id="82a38-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="82a38-126">Header</span><span class="sxs-lookup"><span data-stu-id="82a38-126">Header</span></span><br/>  | <dl> <span data-ttu-id="82a38-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="82a38-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="82a38-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="82a38-128">Library</span></span><br/> | <dl> <span data-ttu-id="82a38-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="82a38-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="82a38-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82a38-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82a38-131">Shaderfunktionen</span><span class="sxs-lookup"><span data-stu-id="82a38-131">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
