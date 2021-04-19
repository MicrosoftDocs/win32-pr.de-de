---
description: Disassembliert einen Shader.
ms.assetid: 30159223-8f88-4929-8ef1-7a6acc13f485
title: D3DXDisassembleShader-Funktion (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDisassembleShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6192b77c190ed73dc6e5038c9119152836eca375
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353362"
---
# <a name="d3dxdisassembleshader-function"></a><span data-ttu-id="e5e7d-103">D3DXDisassembleShader-Funktion</span><span class="sxs-lookup"><span data-stu-id="e5e7d-103">D3DXDisassembleShader function</span></span>

<span data-ttu-id="e5e7d-104">Disassembliert einen Shader.</span><span class="sxs-lookup"><span data-stu-id="e5e7d-104">Disassemble a shader.</span></span>

> [!Note]  
> <span data-ttu-id="e5e7d-105">Anstatt diese Legacy Funktion zu verwenden, empfiehlt es sich, die [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) -API zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="e5e7d-105">Instead of using this legacy function, we recommend that you use the [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e5e7d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5e7d-106">Syntax</span></span>


```C++
HRESULT D3DXDisassembleShader(
  _In_  const DWORD        *pShader,
  _In_        BOOL         EnableColorCode,
  _In_        LPCSTR       pComments,
  _Out_       LPD3DXBUFFER *ppDisassembly
);
```



## <a name="parameters"></a><span data-ttu-id="e5e7d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5e7d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5e7d-108">*pshader* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e5e7d-108">*pShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5e7d-109">Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="e5e7d-109">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e5e7d-110">Zeiger auf einen Arbeitsspeicher Puffer, der die Shader-Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="e5e7d-110">Pointer to a memory buffer that contains the shader data.</span></span>

</dd> <dt>

<span data-ttu-id="e5e7d-111">*Enablecolorcode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e5e7d-111">*EnableColorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5e7d-112">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5e7d-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e5e7d-113">Aktivieren Sie Farbcode, um die Disassembly leichter lesbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="e5e7d-113">Enable color code to make it easier to read the disassembly.</span></span>

</dd> <dt>

<span data-ttu-id="e5e7d-114">*pcomments* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e5e7d-114">*pComments* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5e7d-115">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5e7d-115">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e5e7d-116">Eine optionale, auf NULL endenden Kommentar Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="e5e7d-116">An optional NULL-terminated comment string.</span></span> <span data-ttu-id="e5e7d-117">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="e5e7d-117">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e5e7d-118">*ppdisassembly* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e5e7d-118">*ppDisassembly* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5e7d-119">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="e5e7d-119">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="e5e7d-120">Gibt einen Puffer zurück, der den disassemblierten Shader enthält.</span><span class="sxs-lookup"><span data-stu-id="e5e7d-120">Returns a buffer containing the disassembled shader.</span></span> <span data-ttu-id="e5e7d-121">Siehe [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="e5e7d-121">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5e7d-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e5e7d-122">Return value</span></span>

<span data-ttu-id="e5e7d-123">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e5e7d-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e5e7d-124">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e5e7d-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e5e7d-125">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="e5e7d-125">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5e7d-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e5e7d-126">Requirements</span></span>



| <span data-ttu-id="e5e7d-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e5e7d-127">Requirement</span></span> | <span data-ttu-id="e5e7d-128">Wert</span><span class="sxs-lookup"><span data-stu-id="e5e7d-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5e7d-129">Header</span><span class="sxs-lookup"><span data-stu-id="e5e7d-129">Header</span></span><br/>  | <dl> <span data-ttu-id="e5e7d-130"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5e7d-130"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="e5e7d-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e5e7d-131">Library</span></span><br/> | <dl> <span data-ttu-id="e5e7d-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5e7d-132"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e5e7d-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e5e7d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5e7d-134">Shaderfunktionen</span><span class="sxs-lookup"><span data-stu-id="e5e7d-134">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
