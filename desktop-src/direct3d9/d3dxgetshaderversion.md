---
description: Gibt die Shader-Version des kompilierten Shaders zurück.
ms.assetid: 6cc6c654-e8d1-4225-b5d0-6bc2434a16bd
title: D3DXGetShaderVersion-Funktion (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderVersion
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2c4a65db8706f6d8648096cf0822654e562687a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132337"
---
# <a name="d3dxgetshaderversion-function"></a><span data-ttu-id="3312d-103">D3DXGetShaderVersion-Funktion</span><span class="sxs-lookup"><span data-stu-id="3312d-103">D3DXGetShaderVersion function</span></span>

<span data-ttu-id="3312d-104">Gibt die Shader-Version des kompilierten Shaders zurück.</span><span class="sxs-lookup"><span data-stu-id="3312d-104">Returns the shader version of the compiled shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="3312d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3312d-105">Syntax</span></span>


```C++
DWORD D3DXGetShaderVersion(
  _In_ const DWORD *pFunction
);
```



## <a name="parameters"></a><span data-ttu-id="3312d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3312d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3312d-107">*pfunction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3312d-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3312d-108">Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="3312d-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3312d-109">Ein Zeiger auf die Funktion DWORD-Stream.</span><span class="sxs-lookup"><span data-stu-id="3312d-109">Pointer to the function DWORD stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3312d-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3312d-110">Return value</span></span>

<span data-ttu-id="3312d-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3312d-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3312d-112">Gibt die Shader-Version des angegebenen Shaders zurück, oder 0 (null), wenn die Shader-Funktion **null** ist.</span><span class="sxs-lookup"><span data-stu-id="3312d-112">Returns the shader version of the given shader, or zero if the shader function is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3312d-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3312d-113">Requirements</span></span>



| <span data-ttu-id="3312d-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3312d-114">Requirement</span></span> | <span data-ttu-id="3312d-115">Wert</span><span class="sxs-lookup"><span data-stu-id="3312d-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3312d-116">Header</span><span class="sxs-lookup"><span data-stu-id="3312d-116">Header</span></span><br/>  | <dl> <span data-ttu-id="3312d-117"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="3312d-117"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="3312d-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3312d-118">Library</span></span><br/> | <dl> <span data-ttu-id="3312d-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3312d-119"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="3312d-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3312d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3312d-121">Shaderfunktionen</span><span class="sxs-lookup"><span data-stu-id="3312d-121">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
