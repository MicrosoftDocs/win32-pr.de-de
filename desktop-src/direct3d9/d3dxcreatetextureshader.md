---
description: Erstellt ein Textur-Shader-Objekt aus dem kompilierten Shader.
ms.assetid: 3e8017f7-fe6b-4f4e-a80e-b16b16c0b348
title: D3DXCreateTextureShader-Funktion (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c32715f1b939d30acb53b1cbe07e081d43d21823
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354906"
---
# <a name="d3dxcreatetextureshader-function"></a><span data-ttu-id="3873d-103">D3DXCreateTextureShader-Funktion</span><span class="sxs-lookup"><span data-stu-id="3873d-103">D3DXCreateTextureShader function</span></span>

<span data-ttu-id="3873d-104">Erstellt ein Textur-Shader-Objekt aus dem kompilierten Shader.</span><span class="sxs-lookup"><span data-stu-id="3873d-104">Creates a texture shader object from the compiled shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="3873d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3873d-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureShader(
  _In_  const DWORD               *pFunction,
  _Out_       LPD3DXTEXTURESHADER *ppTextureShader
);
```



## <a name="parameters"></a><span data-ttu-id="3873d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3873d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3873d-107">*pfunction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3873d-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3873d-108">Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="3873d-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3873d-109">Ein Zeiger auf die Funktion DWORD-Stream.</span><span class="sxs-lookup"><span data-stu-id="3873d-109">Pointer to the function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="3873d-110">*pptextureshader* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3873d-110">*ppTextureShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3873d-111">Typ: **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)\***</span><span class="sxs-lookup"><span data-stu-id="3873d-111">Type: **[**LPD3DXTEXTURESHADER**](id3dxtextureshader.md)\***</span></span>

<span data-ttu-id="3873d-112">Gibt ein [**ID3DXTextureShader**](id3dxtextureshader.md) -Objekt zurück, das verwendet werden kann, um den Inhalt einer Textur mithilfe der [**D3DXFillTextureTX**](d3dxfilltexturetx.md) -Funktionen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="3873d-112">Returns an [**ID3DXTextureShader**](id3dxtextureshader.md) object which can be used to procedurally fill the contents of a texture using the [**D3DXFillTextureTX**](d3dxfilltexturetx.md) functions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3873d-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3873d-113">Return value</span></span>

<span data-ttu-id="3873d-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3873d-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3873d-115">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3873d-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3873d-116">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="3873d-116">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="3873d-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3873d-117">Requirements</span></span>



| <span data-ttu-id="3873d-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3873d-118">Requirement</span></span> | <span data-ttu-id="3873d-119">Wert</span><span class="sxs-lookup"><span data-stu-id="3873d-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3873d-120">Header</span><span class="sxs-lookup"><span data-stu-id="3873d-120">Header</span></span><br/>  | <dl> <span data-ttu-id="3873d-121"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="3873d-121"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="3873d-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3873d-122">Library</span></span><br/> | <dl> <span data-ttu-id="3873d-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3873d-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="3873d-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3873d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3873d-125">Shaderfunktionen</span><span class="sxs-lookup"><span data-stu-id="3873d-125">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
