---
description: Gibt die Größe des Shader-Bytecodes in Bytes zurück.
ms.assetid: 7dd091f7-fda9-49e1-982d-2eb57d9ecb23
title: D3DXGetShaderSize-Funktion (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3017c5a5371e99bcf9e1d69827de0227d929f33a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367366"
---
# <a name="d3dxgetshadersize-function"></a><span data-ttu-id="276f1-103">D3DXGetShaderSize-Funktion</span><span class="sxs-lookup"><span data-stu-id="276f1-103">D3DXGetShaderSize function</span></span>

<span data-ttu-id="276f1-104">Gibt die Größe des Shader-Bytecodes in Bytes zurück.</span><span class="sxs-lookup"><span data-stu-id="276f1-104">Returns the size of the shader byte code, in bytes.</span></span>

## <a name="syntax"></a><span data-ttu-id="276f1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="276f1-105">Syntax</span></span>


```C++
UINT D3DXGetShaderSize(
  _In_ const DWORD *pFunction
);
```



## <a name="parameters"></a><span data-ttu-id="276f1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="276f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="276f1-107">*pfunction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="276f1-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="276f1-108">Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="276f1-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="276f1-109">Ein Zeiger auf die Funktion DWORD-Stream.</span><span class="sxs-lookup"><span data-stu-id="276f1-109">Pointer to the function DWORD stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="276f1-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="276f1-110">Return value</span></span>

<span data-ttu-id="276f1-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="276f1-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="276f1-112">Gibt die Größe des Shader-Bytecodes in Bytes zurück.</span><span class="sxs-lookup"><span data-stu-id="276f1-112">Returns the size of the shader byte code, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="276f1-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="276f1-113">Requirements</span></span>



| <span data-ttu-id="276f1-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="276f1-114">Requirement</span></span> | <span data-ttu-id="276f1-115">Wert</span><span class="sxs-lookup"><span data-stu-id="276f1-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="276f1-116">Header</span><span class="sxs-lookup"><span data-stu-id="276f1-116">Header</span></span><br/>  | <dl> <span data-ttu-id="276f1-117"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="276f1-117"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="276f1-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="276f1-118">Library</span></span><br/> | <dl> <span data-ttu-id="276f1-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="276f1-119"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="276f1-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="276f1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="276f1-121">Shaderfunktionen</span><span class="sxs-lookup"><span data-stu-id="276f1-121">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
