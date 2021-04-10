---
description: Hinweis Wenn Sie diese Legacy Funktion nicht verwenden, empfiehlt es sich, die Offline Kompilierung mit dem Fxc.exe-Befehlszeilen Compiler oder der D3DCompile-API zu verwenden. Kompilieren Sie einen Shader oder einen Effekt, der in den Arbeitsspeicher geladen wird.
ms.assetid: c6458d82-a649-402c-8180-5b7320f9fdb0
title: D3DX10CompileFromMemory-Funktion (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CompileFromMemory
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: fbb4a716df4a893ea122e7badfd6faad536aacce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961725"
---
# <a name="d3dx10compilefrommemory-function"></a><span data-ttu-id="d264e-104">D3DX10CompileFromMemory-Funktion</span><span class="sxs-lookup"><span data-stu-id="d264e-104">D3DX10CompileFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="d264e-105">Anstatt diese Legacy Funktion zu verwenden, wird empfohlen, dass Sie die Offline Kompilierung mit dem Fxc.exe-Befehlszeilen Compiler oder der [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) -API verwenden.</span><span class="sxs-lookup"><span data-stu-id="d264e-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

<span data-ttu-id="d264e-106">Kompilieren Sie einen Shader oder einen Effekt, der in den Arbeitsspeicher geladen wird.</span><span class="sxs-lookup"><span data-stu-id="d264e-106">Compile a shader or an effect that is loaded in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="d264e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d264e-107">Syntax</span></span>


```C++
HRESULT D3DX10CompileFromMemory(
  _In_        LPCSTR             pSrcData,
  _In_        SIZE_T             SrcDataLen,
  _In_        LPCSTR             pFileName,
  _In_  const D3D10_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        LPCSTR             pFunctionName,
  _In_        LPCSTR             pProfile,
  _In_        UINT               Flags1,
  _In_        UINT               Flags2,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShader,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="d264e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d264e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d264e-109">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d264e-109">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d264e-110">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d264e-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d264e-111">Zeiger auf den Shader im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="d264e-111">Pointer to the shader in memory.</span></span>

</dd> <dt>

<span data-ttu-id="d264e-112">*Srcdatalen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d264e-112">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d264e-113">Typ: **[ **Größe \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d264e-113">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d264e-114">Größe des Shaders im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="d264e-114">Size of the shader in memory.</span></span>

</dd> <dt>

<span data-ttu-id="d264e-115">*pfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d264e-115">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d264e-116">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d264e-116">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d264e-117">Der Name der Datei, die den Shader-Code enthält.</span><span class="sxs-lookup"><span data-stu-id="d264e-117">The name of the file that contains the shader code.</span></span>

</dd> <dt>

<span data-ttu-id="d264e-118">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d264e-118">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d264e-119">Type: **Konstanten [**D3D \_ Shader- \_ Makro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="d264e-119">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="d264e-120">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="d264e-120">Optional.</span></span> <span data-ttu-id="d264e-121">Zeiger auf ein Array von Makro Definitionen (siehe [**D3D \_ Shader \_ Macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span><span class="sxs-lookup"><span data-stu-id="d264e-121">Pointer to an array of macro definitions (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="d264e-122">Die letzte Struktur im Array fungiert als Abschluss Zeichen und muss alle Elemente auf 0 (null) festlegen.</span><span class="sxs-lookup"><span data-stu-id="d264e-122">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="d264e-123">Wenn Sie nicht verwendet wird, legen Sie *pdefinitionen* auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="d264e-123">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d264e-124">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d264e-124">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d264e-125">Typ: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="d264e-125">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="d264e-126">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="d264e-126">Optional.</span></span> <span data-ttu-id="d264e-127">Zeiger auf eine [**ID3D10Include-Schnittstellen**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) Schnittstelle zur Behandlung von Includedateien.</span><span class="sxs-lookup"><span data-stu-id="d264e-127">Pointer to an [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) interface for handling include files.</span></span> <span data-ttu-id="d264e-128">Wenn dieser Wert auf **null** festgelegt wird, wird ein Kompilierungsfehler verursacht, wenn ein Shader eine include-Datei \#</span><span class="sxs-lookup"><span data-stu-id="d264e-128">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="d264e-129">*pfunctionname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d264e-129">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d264e-130">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d264e-130">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d264e-131">Der Name der Shader-Einstiegspunkt Funktion, bei der die Shader-Ausführung beginnt.</span><span class="sxs-lookup"><span data-stu-id="d264e-131">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="d264e-132">Wenn Sie einen Effekt kompilieren,  ignoriert D3DX10CompileFromMemory *pfunctionname*;. Es wird empfohlen, *pfunctionname* auf **null** festzulegen, da es eine gute Programmierpraxis ist, einen Zeiger Parameter auf **null** festzulegen, wenn die aufgerufene Funktion ihn nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d264e-132">When you compile an effect, **D3DX10CompileFromMemory** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="d264e-133">*pprofile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d264e-133">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d264e-134">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d264e-134">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d264e-135">Eine Zeichenfolge, die das Shadermodell angibt. kann ein beliebiges Profil in [Shader Model 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), [Shader Model 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md)oder [Shader Model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md)sein.</span><span class="sxs-lookup"><span data-stu-id="d264e-135">A string that specifies the shader model; can be any profile in [shader model 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), [shader model 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md), or [shader model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md).</span></span>

</dd> <dt>

<span data-ttu-id="d264e-136">*Flags1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d264e-136">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d264e-137">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d264e-137">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d264e-138">[Shader-Kompilierungs Flags](d3d10-shader.md).</span><span class="sxs-lookup"><span data-stu-id="d264e-138">[Shader compile flags](d3d10-shader.md).</span></span>

</dd> <dt>

<span data-ttu-id="d264e-139">*Flags2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d264e-139">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d264e-140">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d264e-140">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d264e-141">[Effekt Kompilierungs Flags](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d264e-141">[Effect compile flags](d3d10-graphics-reference-effect-constants.md).</span></span> <span data-ttu-id="d264e-142">Wenn Sie einen Shader und keine Effekt Datei kompilieren, ignoriert **D3DX10CompileFromMemory** *Flags2*; Es wird empfohlen, *Flags2* auf NULL festzulegen, da es eine gute Programmierpraxis ist, einen Typ-Parameter auf 0 (null) festzulegen, wenn die aufgerufene Funktion ihn nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d264e-142">When you compile a shader and not an effect file, **D3DX10CompileFromMemory** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="d264e-143">*ppump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d264e-143">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d264e-144">Typ: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="d264e-144">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="d264e-145">Ein Zeiger auf eine Thread-Pump Schnittstelle (siehe [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="d264e-145">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="d264e-146">Verwenden Sie **null** , um anzugeben, dass diese Funktion erst zurückgegeben werden soll, wenn Sie abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="d264e-146">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="d264e-147">*ppshader* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d264e-147">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d264e-148">Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="d264e-148">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="d264e-149">Ein Zeiger auf eine [**ID3D10Blob-Schnittstelle**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) , die den kompilierten Shader sowie alle eingebetteten Debug-und Symboltabellen Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="d264e-149">A pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="d264e-150">*pperrormsgs* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d264e-150">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d264e-151">Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="d264e-151">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="d264e-152">Ein Zeiger auf eine [**ID3D10Blob-Schnittstelle**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) , die eine Auflistung von Fehlern und Warnungen enthält, die während der Kompilierung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="d264e-152">A pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="d264e-153">Diese Fehler und Warnungen sind identisch mit der Debugausgabe eines Debuggers.</span><span class="sxs-lookup"><span data-stu-id="d264e-153">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="d264e-154">*phresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d264e-154">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d264e-155">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="d264e-155">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="d264e-156">Ein Zeiger auf den Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="d264e-156">A pointer to the return value.</span></span> <span data-ttu-id="d264e-157">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="d264e-157">May be **NULL**.</span></span> <span data-ttu-id="d264e-158">Wenn *ppump* nicht **null** ist, muss *phresult* eine gültige Speicheradresse sein, bis die asynchrone Ausführung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="d264e-158">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d264e-159">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d264e-159">Return value</span></span>

<span data-ttu-id="d264e-160">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d264e-160">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d264e-161">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="d264e-161">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d264e-162">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d264e-162">Requirements</span></span>



| <span data-ttu-id="d264e-163">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d264e-163">Requirement</span></span> | <span data-ttu-id="d264e-164">Wert</span><span class="sxs-lookup"><span data-stu-id="d264e-164">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d264e-165">Header</span><span class="sxs-lookup"><span data-stu-id="d264e-165">Header</span></span><br/> | <dl> <span data-ttu-id="d264e-166"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="d264e-166"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d264e-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d264e-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d264e-168">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="d264e-168">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
