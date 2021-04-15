---
description: Beachten Sie, dass Sie die D3DPreprocess-API verwenden, anstatt diese Legacy Funktion zu verwenden. Erstellen Sie einen Shader aus einer Ressource, ohne ihn zu kompilieren.
ms.assetid: ca93e208-7627-4bf5-ab83-d4e906e149eb
title: D3DX10PreprocessShaderFromResource-Funktion (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10PreprocessShaderFromResource
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 81a9f272cb0769d4313a4375f98bdc25b9e403e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394270"
---
# <a name="d3dx10preprocessshaderfromresource-function"></a><span data-ttu-id="dc0bc-104">D3DX10PreprocessShaderFromResource-Funktion</span><span class="sxs-lookup"><span data-stu-id="dc0bc-104">D3DX10PreprocessShaderFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="dc0bc-105">Anstatt diese Legacy Funktion zu verwenden, empfiehlt es sich, die [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) -API zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="dc0bc-105">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

<span data-ttu-id="dc0bc-106">Erstellen Sie einen Shader aus einer Ressource, ohne ihn zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="dc0bc-106">Create a shader from a resource without compiling it.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc0bc-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc0bc-107">Syntax</span></span>


```C++
HRESULT D3DX10PreprocessShaderFromResource(
  _In_        HMODULE            hModule,
  _In_        LPCTSTR            pResourceName,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="dc0bc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc0bc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc0bc-109">*HMODULE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc0bc-109">*hModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc0bc-110">Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dc0bc-110">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dc0bc-111">Handle für das Ressourcen Modul, das den Shader enthält.</span><span class="sxs-lookup"><span data-stu-id="dc0bc-111">Handle to the resource module containing the shader.</span></span> <span data-ttu-id="dc0bc-112">HMODULE kann mit der [GetModuleHandle-Funktion](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="dc0bc-112">HMODULE can be obtained with [GetModuleHandle Function](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="dc0bc-113">*presourcename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc0bc-113">*pResourceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc0bc-114">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dc0bc-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dc0bc-115">Der Name der Ressource in Side HMODULE, die den Shader enthält.</span><span class="sxs-lookup"><span data-stu-id="dc0bc-115">The name of the resource in side hModule containing the shader.</span></span> <span data-ttu-id="dc0bc-116">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="dc0bc-116">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="dc0bc-117">Andernfalls wird der Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="dc0bc-117">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="dc0bc-118">*psrcfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc0bc-118">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc0bc-119">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dc0bc-119">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dc0bc-120">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="dc0bc-120">Optional.</span></span> <span data-ttu-id="dc0bc-121">Der Effekt Dateiname, der nur für Fehlermeldungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dc0bc-121">Effect file name, which is used for error messages only.</span></span> <span data-ttu-id="dc0bc-122">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="dc0bc-122">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="dc0bc-123">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc0bc-123">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc0bc-124">Type: **Konstanten [**D3D \_ Shader- \_ Makro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="dc0bc-124">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="dc0bc-125">Ein mit Null endendes Array von Shader-Makros (siehe [**D3D \_ Shader \_ Macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); legen Sie diese Einstellung auf **null** fest, um keine Makros anzugeben.</span><span class="sxs-lookup"><span data-stu-id="dc0bc-125">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="dc0bc-126">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc0bc-126">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc0bc-127">Typ: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="dc0bc-127">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="dc0bc-128">Ein Zeiger auf eine include-Schnittstelle (siehe [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Legen Sie dies auf **null** fest, um anzugeben, dass keine Includedatei vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="dc0bc-128">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="dc0bc-129">*ppump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc0bc-129">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc0bc-130">Typ: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="dc0bc-130">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="dc0bc-131">Ein Zeiger auf eine Thread-Pump Schnittstelle (siehe [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="dc0bc-131">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="dc0bc-132">Verwenden Sie **null** , um anzugeben, dass diese Funktion erst zurückgegeben werden soll, wenn Sie abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="dc0bc-132">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="dc0bc-133">*ppshadertext* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dc0bc-133">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc0bc-134">Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="dc0bc-134">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="dc0bc-135">Ein Zeiger auf den Arbeitsspeicher (siehe [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)), der den nicht kompilierten Shader enthält.</span><span class="sxs-lookup"><span data-stu-id="dc0bc-135">A pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains the uncompiled shader.</span></span>

</dd> <dt>

<span data-ttu-id="dc0bc-136">*pperrormsgs* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dc0bc-136">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc0bc-137">Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="dc0bc-137">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="dc0bc-138">Die Adresse eines Zeigers auf den Speicher (siehe [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)), der Fehler bei der Fehler Erstellung enthält (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="dc0bc-138">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect-creation errors, if any occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc0bc-139">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dc0bc-139">Return value</span></span>

<span data-ttu-id="dc0bc-140">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dc0bc-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dc0bc-141">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="dc0bc-141">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dc0bc-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc0bc-142">Requirements</span></span>



| <span data-ttu-id="dc0bc-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc0bc-143">Requirement</span></span> | <span data-ttu-id="dc0bc-144">Wert</span><span class="sxs-lookup"><span data-stu-id="dc0bc-144">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dc0bc-145">Header</span><span class="sxs-lookup"><span data-stu-id="dc0bc-145">Header</span></span><br/>  | <dl> <span data-ttu-id="dc0bc-146"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc0bc-146"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="dc0bc-147">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dc0bc-147">Library</span></span><br/> | <dl> <span data-ttu-id="dc0bc-148"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dc0bc-148"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc0bc-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc0bc-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc0bc-150">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="dc0bc-150">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
