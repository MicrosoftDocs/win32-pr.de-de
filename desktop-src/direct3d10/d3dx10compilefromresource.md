---
description: Hinweis Wenn Sie diese Legacy Funktion nicht verwenden, empfiehlt es sich, die Offline Kompilierung mit dem Fxc.exe-Befehlszeilen Compiler oder der D3DCompile-API zu verwenden. Kompilieren Sie einen Shader oder einen Effekt aus einer Ressource.
ms.assetid: d291e47d-e04f-4e2d-9d05-9aef8e4fcf7e
title: D3DX10CompileFromResource-Funktion (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CompileFromResource
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 6b698700804ca767c953343e6d5a5e540ca77555
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355170"
---
# <a name="d3dx10compilefromresource-function"></a><span data-ttu-id="a6f7d-104">D3DX10CompileFromResource-Funktion</span><span class="sxs-lookup"><span data-stu-id="a6f7d-104">D3DX10CompileFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="a6f7d-105">Anstatt diese Legacy Funktion zu verwenden, wird empfohlen, dass Sie die Offline Kompilierung mit dem Fxc.exe-Befehlszeilen Compiler oder der [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) -API verwenden.</span><span class="sxs-lookup"><span data-stu-id="a6f7d-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

<span data-ttu-id="a6f7d-106">Kompilieren Sie einen Shader oder einen Effekt aus einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="a6f7d-106">Compile a shader or an effect from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6f7d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6f7d-107">Syntax</span></span>


```C++
HRESULT D3DX10CompileFromResource(
  _In_        HMODULE            hSrcModule,
  _In_        LPCTSTR            pSrcResource,
  _In_        LPCTSTR            pSrcFileName,
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



## <a name="parameters"></a><span data-ttu-id="a6f7d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6f7d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6f7d-109">*hsrcmodule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6f7d-109">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6f7d-110">Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a6f7d-110">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a6f7d-111">Handle für das Ressourcen Modul, das den Shader enthält.</span><span class="sxs-lookup"><span data-stu-id="a6f7d-111">Handle to the resource module containing the shader.</span></span> <span data-ttu-id="a6f7d-112">HMODULE kann mit der [GetModuleHandle-Funktion](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a6f7d-112">HMODULE can be obtained with [GetModuleHandle Function](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="a6f7d-113">*psrkresource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6f7d-113">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6f7d-114">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a6f7d-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a6f7d-115">Der Name der Ressource, die den Shader enthält.</span><span class="sxs-lookup"><span data-stu-id="a6f7d-115">Name of the resource containing the shader.</span></span> <span data-ttu-id="a6f7d-116">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="a6f7d-116">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="a6f7d-117">Andernfalls wird der Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="a6f7d-117">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="a6f7d-118">*psrcfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6f7d-118">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6f7d-119">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a6f7d-119">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a6f7d-120">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="a6f7d-120">Optional.</span></span> <span data-ttu-id="a6f7d-121">Der Effekt Dateiname, der nur für Fehlermeldungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a6f7d-121">Effect file name, which is used for error messages only.</span></span> <span data-ttu-id="a6f7d-122">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="a6f7d-122">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a6f7d-123">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6f7d-123">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6f7d-124">Type: **Konstanten [**D3D \_ Shader- \_ Makro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="a6f7d-124">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="a6f7d-125">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="a6f7d-125">Optional.</span></span> <span data-ttu-id="a6f7d-126">Zeiger auf ein Array von Makro Definitionen (siehe [**D3D \_ Shader \_ Macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span><span class="sxs-lookup"><span data-stu-id="a6f7d-126">Pointer to an array of macro definitions (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="a6f7d-127">Die letzte Struktur im Array fungiert als Abschluss Zeichen und muss alle Elemente auf 0 (null) festlegen.</span><span class="sxs-lookup"><span data-stu-id="a6f7d-127">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="a6f7d-128">Wenn Sie nicht verwendet wird, legen Sie *pdefinitionen* auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="a6f7d-128">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a6f7d-129">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6f7d-129">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6f7d-130">Typ: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="a6f7d-130">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="a6f7d-131">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="a6f7d-131">Optional.</span></span> <span data-ttu-id="a6f7d-132">Zeiger auf eine [**ID3D10Include-Schnittstellen**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) Schnittstelle zur Behandlung von Includedateien.</span><span class="sxs-lookup"><span data-stu-id="a6f7d-132">Pointer to an [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) interface for handling include files.</span></span> <span data-ttu-id="a6f7d-133">Wenn dieser Wert auf **null** festgelegt wird, wird ein Kompilierungsfehler verursacht, wenn ein Shader eine include-Datei \#</span><span class="sxs-lookup"><span data-stu-id="a6f7d-133">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="a6f7d-134">*pfunctionname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6f7d-134">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6f7d-135">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a6f7d-135">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a6f7d-136">Der Name der Shader-Einstiegspunkt Funktion, bei der die Shader-Ausführung beginnt.</span><span class="sxs-lookup"><span data-stu-id="a6f7d-136">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="a6f7d-137">Wenn Sie einen Effekt kompilieren,  ignoriert D3DX10CompileFromResource *pfunctionname*;. Es wird empfohlen, *pfunctionname* auf **null** festzulegen, da es eine gute Programmierpraxis ist, einen Zeiger Parameter auf **null** festzulegen, wenn die aufgerufene Funktion ihn nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a6f7d-137">When you compile an effect, **D3DX10CompileFromResource** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="a6f7d-138">*pprofile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6f7d-138">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6f7d-139">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a6f7d-139">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a6f7d-140">Eine Zeichenfolge, die das Shadermodell angibt. kann ein beliebiges Profil in [Shader Model 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), [Shader Model 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md)oder [Shader Model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md)sein.</span><span class="sxs-lookup"><span data-stu-id="a6f7d-140">A string that specifies the shader model; can be any profile in [shader model 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), [shader model 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md), or [shader model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6f7d-141">*Flags1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6f7d-141">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6f7d-142">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a6f7d-142">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a6f7d-143">[Shader-Kompilierungs Flags](d3d10-shader.md).</span><span class="sxs-lookup"><span data-stu-id="a6f7d-143">[Shader compile flags](d3d10-shader.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6f7d-144">*Flags2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6f7d-144">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6f7d-145">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a6f7d-145">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a6f7d-146">[Effekt Kompilierungs Flags](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a6f7d-146">[Effect compile flags](d3d10-graphics-reference-effect-constants.md).</span></span> <span data-ttu-id="a6f7d-147">Wenn Sie einen Shader und keine Effekt Datei kompilieren, ignoriert **D3DX10CompileFromResource** *Flags2*; Es wird empfohlen, *Flags2* auf NULL festzulegen, da es eine gute Programmierpraxis ist, einen Typ-Parameter auf 0 (null) festzulegen, wenn die aufgerufene Funktion ihn nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a6f7d-147">When you compile a shader and not an effect file, **D3DX10CompileFromResource** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="a6f7d-148">*ppump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6f7d-148">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6f7d-149">Typ: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="a6f7d-149">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="a6f7d-150">Ein Zeiger auf eine Thread-Pump Schnittstelle (siehe [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="a6f7d-150">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="a6f7d-151">Verwenden Sie **null** , um anzugeben, dass diese Funktion erst zurückgegeben werden soll, wenn Sie abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="a6f7d-151">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="a6f7d-152">*ppshader* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a6f7d-152">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6f7d-153">Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="a6f7d-153">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="a6f7d-154">Ein Zeiger auf eine [**ID3D10Blob-Schnittstelle**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) , die den kompilierten Shader sowie alle eingebetteten Debug-und Symboltabellen Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="a6f7d-154">A pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="a6f7d-155">*pperrormsgs* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a6f7d-155">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6f7d-156">Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="a6f7d-156">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="a6f7d-157">Ein Zeiger auf eine [**ID3D10Blob-Schnittstelle**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) , die eine Auflistung von Fehlern und Warnungen enthält, die während der Kompilierung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="a6f7d-157">A pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="a6f7d-158">Diese Fehler und Warnungen sind identisch mit der Debugausgabe eines Debuggers.</span><span class="sxs-lookup"><span data-stu-id="a6f7d-158">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="a6f7d-159">*phresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a6f7d-159">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6f7d-160">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="a6f7d-160">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="a6f7d-161">Ein Zeiger auf den Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="a6f7d-161">A pointer to the return value.</span></span> <span data-ttu-id="a6f7d-162">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="a6f7d-162">May be **NULL**.</span></span> <span data-ttu-id="a6f7d-163">Wenn *ppump* nicht **null** ist, muss *phresult* eine gültige Speicheradresse sein, bis die asynchrone Ausführung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="a6f7d-163">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6f7d-164">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a6f7d-164">Return value</span></span>

<span data-ttu-id="a6f7d-165">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a6f7d-165">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a6f7d-166">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="a6f7d-166">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a6f7d-167">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6f7d-167">Requirements</span></span>



| <span data-ttu-id="a6f7d-168">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a6f7d-168">Requirement</span></span> | <span data-ttu-id="a6f7d-169">Wert</span><span class="sxs-lookup"><span data-stu-id="a6f7d-169">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6f7d-170">Header</span><span class="sxs-lookup"><span data-stu-id="a6f7d-170">Header</span></span><br/> | <dl> <span data-ttu-id="a6f7d-171"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6f7d-171"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6f7d-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6f7d-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6f7d-173">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="a6f7d-173">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
