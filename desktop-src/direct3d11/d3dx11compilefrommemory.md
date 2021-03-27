---
title: D3DX11CompileFromMemory-Funktion (D3DX11async. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Hinweis statt diese Funktion zu verwenden, wird empfohlen, die Offline Kompilierung mithilfe des Befehlszeilen Compilers Fxc.exe oder eine der HLSL-Kompilierungs-APIs wie die D3DCompile-API zu verwenden. Kompilieren Sie einen Shader oder einen Effekt, der in den Arbeitsspeicher geladen wird.
ms.assetid: 3396560f-f411-4c66-9f22-03c0050c74b0
keywords:
- D3DX11CompileFromMemory-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CompileFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e10590c3db458a23bf4d52b6507146884630087
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982359"
---
# <a name="d3dx11compilefrommemory-function"></a><span data-ttu-id="bec21-106">D3DX11CompileFromMemory-Funktion</span><span class="sxs-lookup"><span data-stu-id="bec21-106">D3DX11CompileFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="bec21-107">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bec21-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="bec21-108">Anstatt diese Funktion zu verwenden, wird empfohlen, dass Sie die Offline Kompilierung mithilfe des Befehlszeilen Compilers Fxc.exe oder eine der HLSL-Kompilierungs-APIs wie die [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) -API verwenden.</span><span class="sxs-lookup"><span data-stu-id="bec21-108">Instead of using this function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use one of the HLSL compile APIs, like the [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) API.</span></span>

 

<span data-ttu-id="bec21-109">Kompilieren Sie einen Shader oder einen Effekt, der in den Arbeitsspeicher geladen wird.</span><span class="sxs-lookup"><span data-stu-id="bec21-109">Compile a shader or an effect that is loaded in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="bec21-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="bec21-110">Syntax</span></span>


```C++
HRESULT D3DX11CompileFromMemory(
  _In_        LPCSTR             pSrcData,
  _In_        SIZE_T             SrcDataLen,
  _In_        LPCSTR             pFileName,
  _In_  const D3D10_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        LPCSTR             pFunctionName,
  _In_        LPCSTR             pProfile,
  _In_        UINT               Flags1,
  _In_        UINT               Flags2,
  _In_        ID3DX11ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShader,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="bec21-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="bec21-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bec21-112">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bec21-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bec21-113">Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bec21-113">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bec21-114">Zeiger auf den Shader im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="bec21-114">Pointer to the shader in memory.</span></span>

</dd> <dt>

<span data-ttu-id="bec21-115">*Srcdatalen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bec21-115">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bec21-116">Typ: **[ **Größe \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bec21-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bec21-117">Größe des Shaders im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="bec21-117">Size of the shader in memory.</span></span>

</dd> <dt>

<span data-ttu-id="bec21-118">*pfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bec21-118">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bec21-119">Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bec21-119">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bec21-120">Der Name der Datei, die den Shader-Code enthält.</span><span class="sxs-lookup"><span data-stu-id="bec21-120">The name of the file that contains the shader code.</span></span>

</dd> <dt>

<span data-ttu-id="bec21-121">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bec21-121">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bec21-122">Type: **Konstanten [**d3d10 \_ Shader- \_ Makro**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="bec21-122">Type: **const [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="bec21-123">Optional.</span><span class="sxs-lookup"><span data-stu-id="bec21-123">Optional.</span></span> <span data-ttu-id="bec21-124">Zeiger auf ein Array von Makro Definitionen (siehe [**d3d10 \_ Shader \_ Macro**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span><span class="sxs-lookup"><span data-stu-id="bec21-124">Pointer to an array of macro definitions (see [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="bec21-125">Die letzte Struktur im Array fungiert als Abschluss Zeichen und muss alle Elemente auf 0 (null) festlegen.</span><span class="sxs-lookup"><span data-stu-id="bec21-125">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="bec21-126">Wenn Sie nicht verwendet wird, legen Sie *pdefinitionen* auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="bec21-126">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bec21-127">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bec21-127">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bec21-128">Typ: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="bec21-128">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="bec21-129">Optional.</span><span class="sxs-lookup"><span data-stu-id="bec21-129">Optional.</span></span> <span data-ttu-id="bec21-130">Zeiger auf eine-Schnittstelle zum Verarbeiten von Includedateien.</span><span class="sxs-lookup"><span data-stu-id="bec21-130">Pointer to an interface for handling include files.</span></span> <span data-ttu-id="bec21-131">Wenn dieser Wert auf **null** festgelegt wird, wird ein Kompilierungsfehler verursacht, wenn ein Shader eine include-Datei \#</span><span class="sxs-lookup"><span data-stu-id="bec21-131">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="bec21-132">*pfunctionname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bec21-132">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bec21-133">Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bec21-133">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bec21-134">Der Name der Shader-Einstiegspunkt Funktion, bei der die Shader-Ausführung beginnt.</span><span class="sxs-lookup"><span data-stu-id="bec21-134">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="bec21-135">Wenn Sie einen Effekt kompilieren,  ignoriert D3DX11CompileFromMemory *pfunctionname*;. Es wird empfohlen, *pfunctionname* auf **null** festzulegen, da es eine gute Programmierpraxis ist, einen Zeiger Parameter auf **null** festzulegen, wenn die aufgerufene Funktion ihn nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="bec21-135">When you compile an effect, **D3DX11CompileFromMemory** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="bec21-136">*pprofile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bec21-136">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bec21-137">Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bec21-137">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bec21-138">Eine Zeichenfolge, die das Shadermodell angibt. kann ein beliebiges Profil in Shader Model 2, Shader Model 3, Shader Model 4 oder Shader Model 5 sein.</span><span class="sxs-lookup"><span data-stu-id="bec21-138">A string that specifies the shader model; can be any profile in shader model 2, shader model 3, shader model 4, or shader model 5.</span></span> <span data-ttu-id="bec21-139">Das Profil kann auch für den Typ "Effect" (z \_ . b. FX 4 \_ 1) sein.</span><span class="sxs-lookup"><span data-stu-id="bec21-139">The profile can also be for effect type (for example, fx\_4\_1).</span></span>

</dd> <dt>

<span data-ttu-id="bec21-140">*Flags1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bec21-140">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bec21-141">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bec21-141">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bec21-142">Shader- [**Kompilierungs Flags**](/windows/desktop/direct3dhlsl/d3dcompile-constants).</span><span class="sxs-lookup"><span data-stu-id="bec21-142">Shader [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-constants).</span></span>

</dd> <dt>

<span data-ttu-id="bec21-143">*Flags2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bec21-143">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bec21-144">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bec21-144">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bec21-145">Effekt [**Kompilierungs Flags**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants).</span><span class="sxs-lookup"><span data-stu-id="bec21-145">Effect [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants).</span></span> <span data-ttu-id="bec21-146">Wenn Sie einen Shader und keine Effekt Datei kompilieren, ignoriert **D3DX11CompileFromMemory** *Flags2*; Es wird empfohlen, *Flags2* auf NULL festzulegen, da es eine gute Programmierpraxis ist, einen Typ-Parameter auf 0 (null) festzulegen, wenn die aufgerufene Funktion ihn nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="bec21-146">When you compile a shader and not an effect file, **D3DX11CompileFromMemory** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="bec21-147">*ppump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bec21-147">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bec21-148">Typ: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="bec21-148">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="bec21-149">Ein Zeiger auf eine Thread-Pump Schnittstelle (siehe [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="bec21-149">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="bec21-150">Verwenden Sie **null** , um anzugeben, dass diese Funktion erst zurückgegeben werden soll, wenn Sie abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="bec21-150">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="bec21-151">*ppshader* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bec21-151">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bec21-152">Typ: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="bec21-152">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="bec21-153">Ein Zeiger auf den Arbeitsspeicher, der den kompilierten Shader sowie alle eingebetteten Debug-und Symbol Tabelleninformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="bec21-153">A pointer to memory which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="bec21-154">*pperrormsgs* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bec21-154">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bec21-155">Typ: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="bec21-155">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="bec21-156">Ein Zeiger auf den Arbeitsspeicher, der eine Auflistung von Fehlern und Warnungen enthält, die während der Kompilierung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="bec21-156">A pointer to memory which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="bec21-157">Diese Fehler und Warnungen sind identisch mit der Debugausgabe eines Debuggers.</span><span class="sxs-lookup"><span data-stu-id="bec21-157">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="bec21-158">*phresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bec21-158">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bec21-159">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="bec21-159">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="bec21-160">Ein Zeiger auf den Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="bec21-160">A pointer to the return value.</span></span> <span data-ttu-id="bec21-161">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="bec21-161">May be **NULL**.</span></span> <span data-ttu-id="bec21-162">Wenn *ppump* nicht **null** ist, muss *phresult* eine gültige Speicheradresse sein, bis die asynchrone Ausführung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="bec21-162">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bec21-163">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bec21-163">Return value</span></span>

<span data-ttu-id="bec21-164">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bec21-164">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bec21-165">Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="bec21-165">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

<span data-ttu-id="bec21-166">**D3DX11CompileFromMemory** gibt E \_ invalidArg zurück, wenn Sie einen Wert ungleich **null** für den Parameter " *phresult* " angeben, wenn Sie **null** für den *ppump* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="bec21-166">**D3DX11CompileFromMemory** returns E\_INVALIDARG if you supply non-**NULL** to the *pHResult* parameter when you supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="bec21-167">Weitere Informationen zu dieser Situation finden Sie unter "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="bec21-167">For more information about this situation, see Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="bec21-168">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bec21-168">Remarks</span></span>

<span data-ttu-id="bec21-169">Weitere Informationen zu **D3DX11CompileFromMemory** finden Sie unter [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).</span><span class="sxs-lookup"><span data-stu-id="bec21-169">For more information about **D3DX11CompileFromMemory**, see [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).</span></span>

<span data-ttu-id="bec21-170">Sie müssen **null** für den Parameter " *phresult* " angeben, wenn Sie auch **null** für den *ppump* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="bec21-170">You must supply **NULL** to the *pHResult* parameter if you also supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="bec21-171">Andernfalls können Sie später keinen Shader erstellen, indem Sie den kompilierten shadercode verwenden, den **D3DX11CompileFromMemory** im Speicher zurückgibt, auf den der *ppshader* -Parameter verweist.</span><span class="sxs-lookup"><span data-stu-id="bec21-171">Otherwise, you cannot subsequently create a shader by using the compiled shader code that **D3DX11CompileFromMemory** returns in the memory that the *ppShader* parameter points to.</span></span> <span data-ttu-id="bec21-172">Zum Erstellen eines Shaders aus dem eingehenden Shader-Code Rufen Sie eine der folgenden [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) -Schnittstellen Methoden auf:</span><span class="sxs-lookup"><span data-stu-id="bec21-172">To create a shader from complied shader code, you call one of the following [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface methods:</span></span>

-   [<span data-ttu-id="bec21-173">**"Kreatecomputeshader"**</span><span class="sxs-lookup"><span data-stu-id="bec21-173">**CreateComputeShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader)
-   [<span data-ttu-id="bec21-174">**"Kreatedomainshader"**</span><span class="sxs-lookup"><span data-stu-id="bec21-174">**CreateDomainShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [<span data-ttu-id="bec21-175">**"Kreategeometryshader"**</span><span class="sxs-lookup"><span data-stu-id="bec21-175">**CreateGeometryShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [<span data-ttu-id="bec21-176">**"Kreategeometryshaderwithstreamoutput"**</span><span class="sxs-lookup"><span data-stu-id="bec21-176">**CreateGeometryShaderWithStreamOutput**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [<span data-ttu-id="bec21-177">**"Kreatehullshader"**</span><span class="sxs-lookup"><span data-stu-id="bec21-177">**CreateHullShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [<span data-ttu-id="bec21-178">**"Kreatepixelshader"**</span><span class="sxs-lookup"><span data-stu-id="bec21-178">**CreatePixelShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createpixelshader)
-   [<span data-ttu-id="bec21-179">**"Kreatevertexshader"**</span><span class="sxs-lookup"><span data-stu-id="bec21-179">**CreateVertexShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

<span data-ttu-id="bec21-180">Wenn Sie einen Wert ungleich **null** *bei der Angabe* von **null** für *ppump* angeben, gibt **D3DX11CompileFromMemory** den E \_ invalidArg-Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="bec21-180">In addition, if you supply a non-**NULL** value to *pHResult* when you supply **NULL** to *pPump*, **D3DX11CompileFromMemory** returns the E\_INVALIDARG error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="bec21-181">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="bec21-181">Requirements</span></span>



| <span data-ttu-id="bec21-182">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bec21-182">Requirement</span></span> | <span data-ttu-id="bec21-183">Wert</span><span class="sxs-lookup"><span data-stu-id="bec21-183">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bec21-184">Header</span><span class="sxs-lookup"><span data-stu-id="bec21-184">Header</span></span><br/>  | <dl> <span data-ttu-id="bec21-185"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="bec21-185"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="bec21-186">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bec21-186">Library</span></span><br/> | <dl> <span data-ttu-id="bec21-187"><dt>Bibliothek d3dx11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bec21-187"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="bec21-188">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bec21-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bec21-189">D3DX-Funktionen</span><span class="sxs-lookup"><span data-stu-id="bec21-189">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

