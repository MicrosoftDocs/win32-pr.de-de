---
description: 'D3DXGetShaderConstantTableEx-Funktion: Ruft die in einen Shader eingebettete Shaderkonstante-Tabelle ab.'
ms.assetid: f7e846e4-9cb4-4634-95e3-4b2a752978a8
title: D3DXGetShaderConstantTableEx-Funktion (D3DX9Shader.h)
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
ms.openlocfilehash: 2cac525f6f6fc4f4e3b6e5900aa9b655e7c7f60d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114429"
---
# <a name="d3dxgetshaderconstanttableex-function"></a><span data-ttu-id="0ad46-103">D3DXGetShaderConstantTableEx-Funktion</span><span class="sxs-lookup"><span data-stu-id="0ad46-103">D3DXGetShaderConstantTableEx function</span></span>

<span data-ttu-id="0ad46-104">Ruft die shaderkonstierte Tabelle ab, die in einen Shader eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="0ad46-104">Gets the shader-constant table embedded inside a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ad46-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ad46-105">Syntax</span></span>


```C++
HRESULT D3DXGetShaderConstantTableEx(
  _In_  const DWORD               *pFunction,
  _In_        DWORD               Flags,
  _Out_       LPD3DXCONSTANTTABLE * ppConstantTable
);
```



## <a name="parameters"></a><span data-ttu-id="0ad46-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ad46-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ad46-107">*pFunction* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="0ad46-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ad46-108">Typ: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="0ad46-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0ad46-109">Zeiger auf den DWORD-Datenstrom der Funktion.</span><span class="sxs-lookup"><span data-stu-id="0ad46-109">Pointer to the function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="0ad46-110">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="0ad46-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ad46-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0ad46-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0ad46-112">Verwenden Sie das D3DXCONSTTABLE LARGEADDRESSAWARE-Flag für den Zugriff auf bis zu 4 GB virtuellen Adressraum (anstelle des Standardwerts \_ von 2 GB).</span><span class="sxs-lookup"><span data-stu-id="0ad46-112">Use the D3DXCONSTTABLE\_LARGEADDRESSAWARE flag to access up to 4 GB of virtual address space (instead of the default of 2 GB).</span></span> <span data-ttu-id="0ad46-113">Wenn Sie den zusätzlichen virtuellen Adressraum nicht benötigen, verwenden Sie [**D3DXGetShaderConstantTable.**](d3dxgetshaderconstanttable.md)</span><span class="sxs-lookup"><span data-stu-id="0ad46-113">If you do not need the additional virtual address space, use [**D3DXGetShaderConstantTable**](d3dxgetshaderconstanttable.md).</span></span>

</dd> <dt>

 <span data-ttu-id="0ad46-114">*ppConstantTable* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0ad46-114">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ad46-115">Typ: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="0ad46-115">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="0ad46-116">Gibt die konstante Tabellenschnittstelle (siehe [**ID3DXConstantTable)**](id3dxconstanttable.md)zurück, die die Konstantentabelle verwaltet.</span><span class="sxs-lookup"><span data-stu-id="0ad46-116">Returns the constant table interface (see [**ID3DXConstantTable**](id3dxconstanttable.md)) that manages the constant table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ad46-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0ad46-117">Return value</span></span>

<span data-ttu-id="0ad46-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0ad46-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0ad46-119">Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0ad46-119">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0ad46-120">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="0ad46-120">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ad46-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ad46-121">Remarks</span></span>

<span data-ttu-id="0ad46-122">Eine Konstantentabelle wird von [**D3DXCompileShader**](d3dxcompileshader.md) generiert und in den Shader-Text eingebettet.</span><span class="sxs-lookup"><span data-stu-id="0ad46-122">A constant table is generated by [**D3DXCompileShader**](d3dxcompileshader.md) and embedded in the shader body.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ad46-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ad46-123">Requirements</span></span>



| <span data-ttu-id="0ad46-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ad46-124">Requirement</span></span> | <span data-ttu-id="0ad46-125">Wert</span><span class="sxs-lookup"><span data-stu-id="0ad46-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ad46-126">Header</span><span class="sxs-lookup"><span data-stu-id="0ad46-126">Header</span></span><br/>  | <dl> <span data-ttu-id="0ad46-127"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="0ad46-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="0ad46-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0ad46-128">Library</span></span><br/> | <dl> <span data-ttu-id="0ad46-129"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="0ad46-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0ad46-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0ad46-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ad46-131">Shaderfunktionen</span><span class="sxs-lookup"><span data-stu-id="0ad46-131">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
