---
title: D3DX11CreateShaderResourceViewFromResource-Funktion (D3DX11tex. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Beachten Sie, dass Sie anstelle der Verwendung dieser Funktion Ressourcen Funktionen verwenden, dann diese directxtk-Bibliothek (Runtime), den Befehl "kreatexxxtexturefrommemory" (wobei xxx DDS oder WIC ist) directxtex Library (Tools), loadfromxxxmemory (hierbei ist xxx WIC, DDS oder TGA). Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele), dann erstellt "anateshaderresourceview" eine Shader-Ressourcen Ansicht aus einer Ressource.
ms.assetid: 64620e6d-fc0d-4411-8744-d9d8ffe6ccb8
keywords:
- D3DX11CreateShaderResourceViewFromResource-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateShaderResourceViewFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb374bd569cb58451461a7fe269c58c200895b7a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996004"
---
# <a name="d3dx11createshaderresourceviewfromresource-function"></a><span data-ttu-id="3b730-105">D3DX11CreateShaderResourceViewFromResource-Funktion</span><span class="sxs-lookup"><span data-stu-id="3b730-105">D3DX11CreateShaderResourceViewFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="3b730-106">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3b730-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="3b730-107">Anstatt diese Funktion zu verwenden, empfiehlt es sich, [Ressourcen Funktionen](/windows/desktop/menurc/resources-functions)zu verwenden, die dann folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="3b730-107">Instead of using this function, we recommend that you use [resource functions](/windows/desktop/menurc/resources-functions), then these:</span></span>
>
> -   <span data-ttu-id="3b730-108">[Directxtk](https://github.com/Microsoft/DirectXTK) - **Bibliothek (Runtime), "** ", "", "", "", "", "", "".</span><span class="sxs-lookup"><span data-stu-id="3b730-108">[DirectXTK](https://github.com/Microsoft/DirectXTK) library (runtime), **CreateXXXTextureFromMemory** (where XXX is DDS or WIC)</span></span>
> -   <span data-ttu-id="3b730-109">[Directxtex](https://github.com/Microsoft/DirectXTex) -Bibliothek (Tools), **loadfromxxxmemory** (hierbei ist xxx WIC, DDS oder TGA). Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele) und dann " **kreateshaderresourceview** "</span><span class="sxs-lookup"><span data-stu-id="3b730-109">[DirectXTex](https://github.com/Microsoft/DirectXTex) library (tools), **LoadFromXXXMemory** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then **CreateShaderResourceView**</span></span>

 

<span data-ttu-id="3b730-110">Erstellen Sie eine Shader-Ressourcen Ansicht aus einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="3b730-110">Create a shader-resource view from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b730-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b730-111">Syntax</span></span>


```C++
HRESULT D3DX11CreateShaderResourceViewFromResource(
  _In_  ID3D11Device             *pDevice,
  _In_  HMODULE                  hSrcModule,
  _In_  LPCTSTR                  pSrcResource,
  _In_  D3DX11_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX11ThreadPump        *pPump,
  _Out_ ID3D11ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="3b730-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b730-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b730-113">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3b730-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b730-114">Typ: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="3b730-114">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="3b730-115">Ein Zeiger auf das Gerät (siehe [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)), von dem die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3b730-115">A pointer to the device (see [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="3b730-116">*hsrcmodule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3b730-116">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b730-117">Typ: **[ **HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3b730-117">Type: **[**HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3b730-118">Handle für das Ressourcen Modul, das die Shader-Ressourcen Ansicht enthält.</span><span class="sxs-lookup"><span data-stu-id="3b730-118">Handle to the resource module containing the shader-resource view.</span></span> <span data-ttu-id="3b730-119">HMODULE kann mit der [GetModuleHandle-Funktion](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="3b730-119">HMODULE can be obtained with [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="3b730-120">*psrkresource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3b730-120">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b730-121">Typ: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3b730-121">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3b730-122">Name der Shader-Ressourcen Ansicht in hsrcmodule.</span><span class="sxs-lookup"><span data-stu-id="3b730-122">Name of the shader resource view in hSrcModule.</span></span> <span data-ttu-id="3b730-123">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="3b730-123">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="3b730-124">Andernfalls wird der Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="3b730-124">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="3b730-125">*ploadinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3b730-125">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b730-126">Type: **[ **Bibliothek d3dx11 \_ Image \_ Load \_ Info**](d3dx11-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="3b730-126">Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***</span></span>

<span data-ttu-id="3b730-127">Optional.</span><span class="sxs-lookup"><span data-stu-id="3b730-127">Optional.</span></span> <span data-ttu-id="3b730-128">Gibt die Merkmale einer Textur an (siehe [**Bibliothek d3dx11 \_ Image \_ Load \_ Info**](d3dx11-image-load-info.md)), wenn der Datenprozessor erstellt wird. Legen Sie diese Einstellung auf **null** fest, um die Merkmale einer Textur beim Laden der Textur zu lesen.</span><span class="sxs-lookup"><span data-stu-id="3b730-128">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="3b730-129">*ppump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3b730-129">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b730-130">Typ: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="3b730-130">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="3b730-131">Ein Zeiger auf eine Thread-Pump Schnittstelle (siehe [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="3b730-131">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="3b730-132">Wenn **null** angegeben wird, verhält sich diese Funktion synchron und wird erst nach Abschluss des Vorgangs zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3b730-132">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="3b730-133">*ppshaderresourceview* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3b730-133">*ppShaderResourceView* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b730-134">Typ: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="3b730-134">Type: **[**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span></span>

<span data-ttu-id="3b730-135">Adresse eines Zeigers auf die Shader-Ressourcen Ansicht (siehe [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)).</span><span class="sxs-lookup"><span data-stu-id="3b730-135">Address of a pointer to the shader-resource view (see [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)).</span></span>

</dd> <dt>

<span data-ttu-id="3b730-136">*phresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3b730-136">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b730-137">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="3b730-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="3b730-138">Ein Zeiger auf den Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="3b730-138">A pointer to the return value.</span></span> <span data-ttu-id="3b730-139">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="3b730-139">May be **NULL**.</span></span> <span data-ttu-id="3b730-140">Wenn *ppump* nicht **null** ist, muss *phresult* eine gültige Speicheradresse sein, bis die asynchrone Ausführung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="3b730-140">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b730-141">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3b730-141">Return value</span></span>

<span data-ttu-id="3b730-142">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3b730-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3b730-143">Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="3b730-143">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3b730-144">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="3b730-144">Requirements</span></span>



| <span data-ttu-id="3b730-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3b730-145">Requirement</span></span> | <span data-ttu-id="3b730-146">Wert</span><span class="sxs-lookup"><span data-stu-id="3b730-146">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b730-147">Header</span><span class="sxs-lookup"><span data-stu-id="3b730-147">Header</span></span><br/>  | <dl> <span data-ttu-id="3b730-148"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b730-148"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="3b730-149">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3b730-149">Library</span></span><br/> | <dl> <span data-ttu-id="3b730-150"><dt>Bibliothek d3dx11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b730-150"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="3b730-151">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3b730-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b730-152">D3DX-Funktionen</span><span class="sxs-lookup"><span data-stu-id="3b730-152">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

