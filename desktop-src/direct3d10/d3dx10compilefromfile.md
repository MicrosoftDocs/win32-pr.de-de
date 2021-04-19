---
description: Hinweis Wenn Sie diese Legacy Funktion nicht verwenden, empfiehlt es sich, die Offline Kompilierung mit dem Fxc.exe-Befehlszeilen Compiler oder der D3DCompile-API zu verwenden. Kompilieren Sie einen Shader oder einen Effekt aus einer Datei.
ms.assetid: b0ca0b6a-3ff0-49ee-83de-14c4686a7104
title: D3DX10CompileFromFile-Funktion (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CompileFromFile
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 571f8123a9834c95ecca6043c3495fb18fbaca47
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106369324"
---
# <a name="d3dx10compilefromfile-function"></a><span data-ttu-id="43cce-104">D3DX10CompileFromFile-Funktion</span><span class="sxs-lookup"><span data-stu-id="43cce-104">D3DX10CompileFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="43cce-105">Anstatt diese Legacy Funktion zu verwenden, wird empfohlen, dass Sie die Offline Kompilierung mit dem Fxc.exe-Befehlszeilen Compiler oder der [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) -API verwenden.</span><span class="sxs-lookup"><span data-stu-id="43cce-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

<span data-ttu-id="43cce-106">Kompilieren Sie einen Shader oder einen Effekt aus einer Datei.</span><span class="sxs-lookup"><span data-stu-id="43cce-106">Compile a shader or an effect from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="43cce-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="43cce-107">Syntax</span></span>


```C++
HRESULT D3DX10CompileFromFile(
  _In_        LPCTSTR            pSrcFile,
  _In_  const D3D_SHADER_MACRO *pDefines,
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



## <a name="parameters"></a><span data-ttu-id="43cce-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="43cce-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43cce-109">*psrcfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43cce-109">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43cce-110">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43cce-110">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="43cce-111">Der Name der Datei, die den Shader-Code enthält.</span><span class="sxs-lookup"><span data-stu-id="43cce-111">The name of the file that contains the shader code.</span></span> <span data-ttu-id="43cce-112">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="43cce-112">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="43cce-113">Andernfalls wird der Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="43cce-113">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="43cce-114">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43cce-114">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43cce-115">Type: **Konstanten [**D3D \_ Shader- \_ Makro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="43cce-115">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="43cce-116">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="43cce-116">Optional.</span></span> <span data-ttu-id="43cce-117">Zeiger auf ein Array von Makro Definitionen (siehe [**D3D \_ Shader \_ Macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span><span class="sxs-lookup"><span data-stu-id="43cce-117">Pointer to an array of macro definitions (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="43cce-118">Die letzte Struktur im Array fungiert als Abschluss Zeichen und muss alle Elemente auf 0 (null) festlegen.</span><span class="sxs-lookup"><span data-stu-id="43cce-118">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="43cce-119">Wenn Sie nicht verwendet wird, legen Sie *pdefinitionen* auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="43cce-119">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="43cce-120">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43cce-120">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43cce-121">Typ: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="43cce-121">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="43cce-122">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="43cce-122">Optional.</span></span> <span data-ttu-id="43cce-123">Zeiger auf eine [**ID3D10Include-Schnittstellen**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) Schnittstelle zur Behandlung von Includedateien.</span><span class="sxs-lookup"><span data-stu-id="43cce-123">Pointer to an [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) interface for handling include files.</span></span> <span data-ttu-id="43cce-124">Wenn dieser Wert auf **null** festgelegt wird, wird ein Kompilierungsfehler verursacht, wenn ein Shader eine include-Datei \#</span><span class="sxs-lookup"><span data-stu-id="43cce-124">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="43cce-125">*pfunctionname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43cce-125">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43cce-126">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43cce-126">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="43cce-127">Der Name der Shader-Einstiegspunkt Funktion, bei der die Shader-Ausführung beginnt.</span><span class="sxs-lookup"><span data-stu-id="43cce-127">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="43cce-128">Wenn Sie einen Effekt kompilieren,  ignoriert D3DX10CompileFromFile *pfunctionname*;. Es wird empfohlen, *pfunctionname* auf **null** festzulegen, da es eine gute Programmierpraxis ist, einen Zeiger Parameter auf **null** festzulegen, wenn die aufgerufene Funktion ihn nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="43cce-128">When you compile an effect, **D3DX10CompileFromFile** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="43cce-129">*pprofile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43cce-129">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43cce-130">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43cce-130">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="43cce-131">Eine Zeichenfolge, die das Shadermodell angibt. kann ein beliebiges Profil in [Shader Model 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), [Shader Model 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md)oder [Shader Model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md)sein.</span><span class="sxs-lookup"><span data-stu-id="43cce-131">A string that specifies the shader model; can be any profile in [shader model 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), [shader model 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md), or [shader model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md).</span></span>

</dd> <dt>

<span data-ttu-id="43cce-132">*Flags1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43cce-132">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43cce-133">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43cce-133">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="43cce-134">[Shader-Kompilierungs Flags](d3d10-shader.md).</span><span class="sxs-lookup"><span data-stu-id="43cce-134">[Shader compile flags](d3d10-shader.md).</span></span>

</dd> <dt>

<span data-ttu-id="43cce-135">*Flags2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43cce-135">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43cce-136">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43cce-136">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="43cce-137">[Effekt Kompilierungs Flags](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="43cce-137">[Effect compile flags](d3d10-graphics-reference-effect-constants.md).</span></span> <span data-ttu-id="43cce-138">Wenn Sie einen Shader und keine Effekt Datei kompilieren, ignoriert **D3DX10CompileFromFile** *Flags2*; Es wird empfohlen, *Flags2* auf NULL festzulegen, da es eine gute Programmierpraxis ist, einen Typ-Parameter auf 0 (null) festzulegen, wenn die aufgerufene Funktion ihn nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="43cce-138">When you compile a shader and not an effect file, **D3DX10CompileFromFile** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="43cce-139">*ppump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43cce-139">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43cce-140">Typ: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="43cce-140">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="43cce-141">Ein Zeiger auf eine Thread-Pump Schnittstelle (siehe [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="43cce-141">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="43cce-142">Verwenden Sie **null** , um anzugeben, dass diese Funktion erst zurückgegeben werden soll, wenn Sie abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="43cce-142">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="43cce-143">*ppshader* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="43cce-143">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43cce-144">Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="43cce-144">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="43cce-145">Ein Zeiger auf eine [**ID3D10Blob-Schnittstelle**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) , die den kompilierten Shader sowie alle eingebetteten Debug-und Symboltabellen Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="43cce-145">A pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="43cce-146">*pperrormsgs* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="43cce-146">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43cce-147">Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="43cce-147">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="43cce-148">Ein Zeiger auf eine [**ID3D10Blob-Schnittstelle**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) , die eine Auflistung von Fehlern und Warnungen enthält, die während der Kompilierung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="43cce-148">A pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="43cce-149">Diese Fehler und Warnungen sind identisch mit der Debugausgabe eines Debuggers.</span><span class="sxs-lookup"><span data-stu-id="43cce-149">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="43cce-150">*phresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="43cce-150">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43cce-151">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="43cce-151">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="43cce-152">Ein Zeiger auf den Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="43cce-152">A pointer to the return value.</span></span> <span data-ttu-id="43cce-153">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="43cce-153">May be **NULL**.</span></span> <span data-ttu-id="43cce-154">Wenn *ppump* nicht **null** ist, muss *phresult* eine gültige Speicheradresse sein, bis die asynchrone Ausführung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="43cce-154">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43cce-155">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="43cce-155">Return value</span></span>

<span data-ttu-id="43cce-156">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="43cce-156">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="43cce-157">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="43cce-157">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="43cce-158">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43cce-158">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="43cce-159">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="43cce-159">Requirements</span></span>



| <span data-ttu-id="43cce-160">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43cce-160">Requirement</span></span> | <span data-ttu-id="43cce-161">Wert</span><span class="sxs-lookup"><span data-stu-id="43cce-161">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="43cce-162">Header</span><span class="sxs-lookup"><span data-stu-id="43cce-162">Header</span></span><br/> | <dl> <span data-ttu-id="43cce-163"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="43cce-163"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43cce-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43cce-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43cce-165">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="43cce-165">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
