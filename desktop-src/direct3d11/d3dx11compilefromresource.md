---
title: D3DX11CompileFromResource-Funktion (D3DX11async. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Beachten Sie, dass Sie anstelle dieser Funktion Ressourcen Funktionen verwenden und dann mithilfe des Befehlszeilen Compilers von Fxc.exe offline kompilieren oder eine der HLSL-Kompilierungs-APIs verwenden können, wie z. b. die D3DCompile-API. Kompilieren Sie einen Shader oder einen Effekt aus einer Ressource.
ms.assetid: ececa469-f5e3-4cb3-befe-0ed1a5a57671
keywords:
- D3DX11CompileFromResource-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CompileFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b26eeb825a1d3b6bcda9f77eae24c99c3cec168b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961686"
---
# <a name="d3dx11compilefromresource-function"></a><span data-ttu-id="65c2c-106">D3DX11CompileFromResource-Funktion</span><span class="sxs-lookup"><span data-stu-id="65c2c-106">D3DX11CompileFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="65c2c-107">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="65c2c-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="65c2c-108">Anstatt diese Funktion zu verwenden, empfiehlt es sich, [Ressourcen Funktionen](/windows/desktop/menurc/resources-functions)zu verwenden und dann mithilfe des Befehlszeilen Compilers von Fxc.exe offline zu kompilieren oder eine der HLSL-Kompilierungs-APIs wie die [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) -API zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="65c2c-108">Instead of using this function, we recommend that you use [resource functions](/windows/desktop/menurc/resources-functions), then compile offline by using the Fxc.exe command-line compiler or use one of the HLSL compile APIs, like the [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) API.</span></span>

 

<span data-ttu-id="65c2c-109">Kompilieren Sie einen Shader oder einen Effekt aus einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="65c2c-109">Compile a shader or an effect from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="65c2c-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="65c2c-110">Syntax</span></span>


```C++
HRESULT D3DX11CompileFromResource(
  _In_        HMODULE            hSrcModule,
  _In_        LPCTSTR            pSrcResource,
  _In_        LPCTSTR            pSrcFileName,
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



## <a name="parameters"></a><span data-ttu-id="65c2c-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="65c2c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65c2c-112">*hsrcmodule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65c2c-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65c2c-113">Typ: **[ **HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="65c2c-113">Type: **[**HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="65c2c-114">Handle für das Ressourcen Modul, das den Shader enthält.</span><span class="sxs-lookup"><span data-stu-id="65c2c-114">Handle to the resource module containing the shader.</span></span> <span data-ttu-id="65c2c-115">HMODULE kann mit der [GetModuleHandle-Funktion](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="65c2c-115">HMODULE can be obtained with [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="65c2c-116">*psrkresource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65c2c-116">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65c2c-117">Typ: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="65c2c-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="65c2c-118">Der Name der Ressource, die den Shader enthält.</span><span class="sxs-lookup"><span data-stu-id="65c2c-118">Name of the resource containing the shader.</span></span> <span data-ttu-id="65c2c-119">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="65c2c-119">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="65c2c-120">Andernfalls wird der Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="65c2c-120">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="65c2c-121">*psrcfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65c2c-121">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65c2c-122">Typ: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="65c2c-122">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="65c2c-123">Optional.</span><span class="sxs-lookup"><span data-stu-id="65c2c-123">Optional.</span></span> <span data-ttu-id="65c2c-124">Der Effekt Dateiname, der nur für Fehlermeldungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="65c2c-124">Effect file name, which is used for error messages only.</span></span> <span data-ttu-id="65c2c-125">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="65c2c-125">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="65c2c-126">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65c2c-126">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65c2c-127">Type: **Konstanten [**d3d10 \_ Shader- \_ Makro**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="65c2c-127">Type: **const [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="65c2c-128">Optional.</span><span class="sxs-lookup"><span data-stu-id="65c2c-128">Optional.</span></span> <span data-ttu-id="65c2c-129">Zeiger auf ein Array von Makro Definitionen (siehe [**d3d10 \_ Shader \_ Macro**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span><span class="sxs-lookup"><span data-stu-id="65c2c-129">Pointer to an array of macro definitions (see [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="65c2c-130">Die letzte Struktur im Array fungiert als Abschluss Zeichen und muss alle Elemente auf 0 (null) festlegen.</span><span class="sxs-lookup"><span data-stu-id="65c2c-130">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="65c2c-131">Wenn Sie nicht verwendet wird, legen Sie *pdefinitionen* auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="65c2c-131">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="65c2c-132">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65c2c-132">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65c2c-133">Typ: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="65c2c-133">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="65c2c-134">Optional.</span><span class="sxs-lookup"><span data-stu-id="65c2c-134">Optional.</span></span> <span data-ttu-id="65c2c-135">Zeiger auf eine-Schnittstelle zum Verarbeiten von Includedateien.</span><span class="sxs-lookup"><span data-stu-id="65c2c-135">Pointer to an interface for handling include files.</span></span> <span data-ttu-id="65c2c-136">Wenn dieser Wert auf **null** festgelegt wird, wird ein Kompilierungsfehler verursacht, wenn ein Shader eine include-Datei \#</span><span class="sxs-lookup"><span data-stu-id="65c2c-136">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="65c2c-137">*pfunctionname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65c2c-137">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65c2c-138">Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="65c2c-138">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="65c2c-139">Der Name der Shader-Einstiegspunkt Funktion, bei der die Shader-Ausführung beginnt.</span><span class="sxs-lookup"><span data-stu-id="65c2c-139">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="65c2c-140">Wenn Sie einen Effekt kompilieren,  ignoriert D3DX11CompileFromResource *pfunctionname*;. Es wird empfohlen, *pfunctionname* auf **null** festzulegen, da es eine gute Programmierpraxis ist, einen Zeiger Parameter auf **null** festzulegen, wenn die aufgerufene Funktion ihn nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="65c2c-140">When you compile an effect, **D3DX11CompileFromResource** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="65c2c-141">*pprofile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65c2c-141">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65c2c-142">Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="65c2c-142">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="65c2c-143">Eine Zeichenfolge, die das Shadermodell angibt. kann ein beliebiges Profil in Shader Model 2, Shader Model 3, Shader Model 4 oder Shader Model 5 sein.</span><span class="sxs-lookup"><span data-stu-id="65c2c-143">A string that specifies the shader model; can be any profile in shader model 2, shader model 3, shader model 4, or shader model 5.</span></span> <span data-ttu-id="65c2c-144">Das Profil kann auch für den Typ "Effect" (z \_ . b. FX 4 \_ 1) sein.</span><span class="sxs-lookup"><span data-stu-id="65c2c-144">The profile can also be for effect type (for example, fx\_4\_1).</span></span>

</dd> <dt>

<span data-ttu-id="65c2c-145">*Flags1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65c2c-145">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65c2c-146">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="65c2c-146">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="65c2c-147">Shader- [**Kompilierungs Flags**](/windows/desktop/direct3dhlsl/d3dcompile-constants).</span><span class="sxs-lookup"><span data-stu-id="65c2c-147">Shader [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-constants).</span></span>

</dd> <dt>

<span data-ttu-id="65c2c-148">*Flags2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65c2c-148">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65c2c-149">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="65c2c-149">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="65c2c-150">Effekt [**Kompilierungs Flags**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants).</span><span class="sxs-lookup"><span data-stu-id="65c2c-150">Effect [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants).</span></span> <span data-ttu-id="65c2c-151">Wenn Sie einen Shader und keine Effekt Datei kompilieren, ignoriert **D3DX11CompileFromResource** *Flags2*; Es wird empfohlen, *Flags2* auf NULL festzulegen, da es eine gute Programmierpraxis ist, einen Typ-Parameter auf 0 (null) festzulegen, wenn die aufgerufene Funktion ihn nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="65c2c-151">When you compile a shader and not an effect file, **D3DX11CompileFromResource** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="65c2c-152">*ppump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65c2c-152">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65c2c-153">Typ: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="65c2c-153">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="65c2c-154">Ein Zeiger auf eine Thread-Pump Schnittstelle (siehe [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="65c2c-154">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="65c2c-155">Verwenden Sie **null** , um anzugeben, dass diese Funktion erst zurückgegeben werden soll, wenn Sie abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="65c2c-155">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="65c2c-156">*ppshader* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="65c2c-156">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65c2c-157">Typ: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="65c2c-157">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="65c2c-158">Ein Zeiger auf den Arbeitsspeicher, der den kompilierten Shader sowie alle eingebetteten Debug-und Symbol Tabelleninformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="65c2c-158">A pointer to memory which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="65c2c-159">*pperrormsgs* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="65c2c-159">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65c2c-160">Typ: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="65c2c-160">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="65c2c-161">Ein Zeiger auf den Arbeitsspeicher, der eine Auflistung von Fehlern und Warnungen enthält, die während der Kompilierung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="65c2c-161">A pointer to memory which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="65c2c-162">Diese Fehler und Warnungen sind identisch mit der Debugausgabe eines Debuggers.</span><span class="sxs-lookup"><span data-stu-id="65c2c-162">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="65c2c-163">*phresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="65c2c-163">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65c2c-164">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="65c2c-164">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="65c2c-165">Ein Zeiger auf den Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="65c2c-165">A pointer to the return value.</span></span> <span data-ttu-id="65c2c-166">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="65c2c-166">May be **NULL**.</span></span> <span data-ttu-id="65c2c-167">Wenn *ppump* nicht **null** ist, muss *phresult* eine gültige Speicheradresse sein, bis die asynchrone Ausführung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="65c2c-167">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65c2c-168">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="65c2c-168">Return value</span></span>

<span data-ttu-id="65c2c-169">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="65c2c-169">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="65c2c-170">Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="65c2c-170">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

<span data-ttu-id="65c2c-171">**D3DX11CompileFromResource** gibt E \_ invalidArg zurück, wenn Sie einen Wert ungleich **null** für den Parameter " *phresult* " angeben, wenn Sie **null** für den *ppump* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="65c2c-171">**D3DX11CompileFromResource** returns E\_INVALIDARG if you supply non-**NULL** to the *pHResult* parameter when you supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="65c2c-172">Weitere Informationen zu dieser Situation finden Sie unter "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="65c2c-172">For more information about this situation, see Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="65c2c-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="65c2c-173">Remarks</span></span>

<span data-ttu-id="65c2c-174">Weitere Informationen zu **D3DX11CompileFromResource** finden Sie unter [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).</span><span class="sxs-lookup"><span data-stu-id="65c2c-174">For more information about **D3DX11CompileFromResource**, see [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).</span></span>

<span data-ttu-id="65c2c-175">Sie müssen **null** für den Parameter " *phresult* " angeben, wenn Sie auch **null** für den *ppump* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="65c2c-175">You must supply **NULL** to the *pHResult* parameter if you also supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="65c2c-176">Andernfalls können Sie später keinen Shader erstellen, indem Sie den kompilierten shadercode verwenden, den **D3DX11CompileFromResource** im Speicher zurückgibt, auf den der *ppshader* -Parameter verweist.</span><span class="sxs-lookup"><span data-stu-id="65c2c-176">Otherwise, you cannot subsequently create a shader by using the compiled shader code that **D3DX11CompileFromResource** returns in the memory that the *ppShader* parameter points to.</span></span> <span data-ttu-id="65c2c-177">Zum Erstellen eines Shaders aus dem eingehenden Shader-Code Rufen Sie eine der folgenden [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) -Schnittstellen Methoden auf:</span><span class="sxs-lookup"><span data-stu-id="65c2c-177">To create a shader from complied shader code, you call one of the following [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface methods:</span></span>

-   [<span data-ttu-id="65c2c-178">**"Kreatecomputeshader"**</span><span class="sxs-lookup"><span data-stu-id="65c2c-178">**CreateComputeShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader)
-   [<span data-ttu-id="65c2c-179">**"Kreatedomainshader"**</span><span class="sxs-lookup"><span data-stu-id="65c2c-179">**CreateDomainShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [<span data-ttu-id="65c2c-180">**"Kreategeometryshader"**</span><span class="sxs-lookup"><span data-stu-id="65c2c-180">**CreateGeometryShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [<span data-ttu-id="65c2c-181">**"Kreategeometryshaderwithstreamoutput"**</span><span class="sxs-lookup"><span data-stu-id="65c2c-181">**CreateGeometryShaderWithStreamOutput**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [<span data-ttu-id="65c2c-182">**"Kreatehullshader"**</span><span class="sxs-lookup"><span data-stu-id="65c2c-182">**CreateHullShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [<span data-ttu-id="65c2c-183">**"Kreatepixelshader"**</span><span class="sxs-lookup"><span data-stu-id="65c2c-183">**CreatePixelShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createpixelshader)
-   [<span data-ttu-id="65c2c-184">**"Kreatevertexshader"**</span><span class="sxs-lookup"><span data-stu-id="65c2c-184">**CreateVertexShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

<span data-ttu-id="65c2c-185">Wenn Sie einen Wert ungleich **null** *bei der Angabe* von **null** für *ppump* angeben, gibt **D3DX11CompileFromResource** den E \_ invalidArg-Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="65c2c-185">In addition, if you supply a non-**NULL** value to *pHResult* when you supply **NULL** to *pPump*, **D3DX11CompileFromResource** returns the E\_INVALIDARG error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="65c2c-186">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="65c2c-186">Requirements</span></span>



| <span data-ttu-id="65c2c-187">Anforderung</span><span class="sxs-lookup"><span data-stu-id="65c2c-187">Requirement</span></span> | <span data-ttu-id="65c2c-188">Wert</span><span class="sxs-lookup"><span data-stu-id="65c2c-188">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="65c2c-189">Header</span><span class="sxs-lookup"><span data-stu-id="65c2c-189">Header</span></span><br/>  | <dl> <span data-ttu-id="65c2c-190"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="65c2c-190"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="65c2c-191">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="65c2c-191">Library</span></span><br/> | <dl> <span data-ttu-id="65c2c-192"><dt>Bibliothek d3dx11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="65c2c-192"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="65c2c-193">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="65c2c-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65c2c-194">D3DX-Funktionen</span><span class="sxs-lookup"><span data-stu-id="65c2c-194">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

