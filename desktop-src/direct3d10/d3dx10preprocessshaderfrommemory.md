---
description: Beachten Sie, dass Sie die D3DPreprocess-API verwenden, anstatt diese Legacy Funktion zu verwenden. Erstellen Sie einen Shader aus dem Arbeitsspeicher, ohne ihn zu kompilieren.
ms.assetid: 099bc010-1269-4833-8a96-a7c78ed48206
title: D3DX10PreprocessShaderFromMemory-Funktion (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10PreprocessShaderFromMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d1d06e46a5cd6b86420543b380f74273be032c17
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762222"
---
# <a name="d3dx10preprocessshaderfrommemory-function"></a><span data-ttu-id="97b1d-104">D3DX10PreprocessShaderFromMemory-Funktion</span><span class="sxs-lookup"><span data-stu-id="97b1d-104">D3DX10PreprocessShaderFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="97b1d-105">Anstatt diese Legacy Funktion zu verwenden, empfiehlt es sich, die [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) -API zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="97b1d-105">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

<span data-ttu-id="97b1d-106">Erstellen Sie einen Shader aus dem Arbeitsspeicher, ohne ihn zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="97b1d-106">Create a shader from memory without compiling it.</span></span>

## <a name="syntax"></a><span data-ttu-id="97b1d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="97b1d-107">Syntax</span></span>


```C++
HRESULT D3DX10PreprocessShaderFromMemory(
  _In_        LPCSTR             pSrcData,
  _In_        SIZE_T             SrcDataSize,
  _In_        LPCSTR             pFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="97b1d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="97b1d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97b1d-109">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97b1d-109">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97b1d-110">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97b1d-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="97b1d-111">Zeiger auf den Arbeitsspeicher, der den Shader enthält.</span><span class="sxs-lookup"><span data-stu-id="97b1d-111">Pointer to the memory containing the shader.</span></span>

</dd> <dt>

<span data-ttu-id="97b1d-112">*Srcdatasize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97b1d-112">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97b1d-113">Typ: **[ **Größe \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97b1d-113">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="97b1d-114">Größe des Shaders.</span><span class="sxs-lookup"><span data-stu-id="97b1d-114">Size of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="97b1d-115">*pfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97b1d-115">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97b1d-116">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97b1d-116">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="97b1d-117">Der Name des Shaders.</span><span class="sxs-lookup"><span data-stu-id="97b1d-117">Name of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="97b1d-118">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97b1d-118">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97b1d-119">Type: **Konstanten [**D3D \_ Shader- \_ Makro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="97b1d-119">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="97b1d-120">Ein mit Null endendes Array von Shader-Makros (siehe [**D3D \_ Shader \_ Macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); legen Sie diese Einstellung auf **null** fest, um keine Makros anzugeben.</span><span class="sxs-lookup"><span data-stu-id="97b1d-120">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="97b1d-121">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97b1d-121">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97b1d-122">Typ: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="97b1d-122">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="97b1d-123">Ein Zeiger auf eine include-Schnittstelle (siehe [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Legen Sie dies auf **null** fest, um anzugeben, dass keine Includedatei vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="97b1d-123">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="97b1d-124">*ppump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97b1d-124">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97b1d-125">Typ: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="97b1d-125">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="97b1d-126">Ein Zeiger auf eine Thread-Pump Schnittstelle (siehe [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="97b1d-126">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="97b1d-127">Verwenden Sie **null** , um anzugeben, dass diese Funktion erst zurückgegeben werden soll, wenn Sie abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="97b1d-127">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="97b1d-128">*ppshadertext* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="97b1d-128">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97b1d-129">Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="97b1d-129">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="97b1d-130">Ein Zeiger auf den Arbeitsspeicher (siehe [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)), der den nicht kompilierten Shader enthält.</span><span class="sxs-lookup"><span data-stu-id="97b1d-130">A pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains the uncompiled shader.</span></span>

</dd> <dt>

<span data-ttu-id="97b1d-131">*pperrormsgs* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="97b1d-131">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97b1d-132">Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="97b1d-132">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="97b1d-133">Die Adresse eines Zeigers auf den Speicher (siehe [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)), der Fehler bei der Fehler Erstellung enthält (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="97b1d-133">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect-creation errors, if any occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97b1d-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="97b1d-134">Return value</span></span>

<span data-ttu-id="97b1d-135">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="97b1d-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="97b1d-136">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="97b1d-136">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="97b1d-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97b1d-137">Requirements</span></span>



| <span data-ttu-id="97b1d-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97b1d-138">Requirement</span></span> | <span data-ttu-id="97b1d-139">Wert</span><span class="sxs-lookup"><span data-stu-id="97b1d-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="97b1d-140">Header</span><span class="sxs-lookup"><span data-stu-id="97b1d-140">Header</span></span><br/>  | <dl> <span data-ttu-id="97b1d-141"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="97b1d-141"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="97b1d-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="97b1d-142">Library</span></span><br/> | <dl> <span data-ttu-id="97b1d-143"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="97b1d-143"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97b1d-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97b1d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97b1d-145">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="97b1d-145">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
