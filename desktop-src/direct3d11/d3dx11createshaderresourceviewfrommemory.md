---
title: D3DX11CreateShaderResourceViewFromMemory-Funktion (D3DX11tex. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Beachten Sie anstelle dieser Funktion, dass Sie diese directxtk-Bibliothek (Runtime), den "anatexxxtexturefrommemory" (wobei xxx DDS oder WIC ist) directxtex Library (Tools), loadfromxxxmemory (wobei xxx für WIC, DDS oder TGA verwendet wird) verwenden. Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele), dann erstellt "anateshaderresourceview" eine Shader-Ressourcen Ansicht aus einer Datei im Arbeitsspeicher.
ms.assetid: fd75b187-2c9c-403c-8327-c312c4cda238
keywords:
- D3DX11CreateShaderResourceViewFromMemory-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateShaderResourceViewFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c0730fafdeb85cc22944f282eaaf556a1cdb12d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996009"
---
# <a name="d3dx11createshaderresourceviewfrommemory-function"></a><span data-ttu-id="057ed-105">D3DX11CreateShaderResourceViewFromMemory-Funktion</span><span class="sxs-lookup"><span data-stu-id="057ed-105">D3DX11CreateShaderResourceViewFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="057ed-106">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="057ed-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="057ed-107">Anstatt diese Funktion zu verwenden, empfiehlt es sich, diese zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="057ed-107">Instead of using this function, we recommend that you use these:</span></span>
>
> -   <span data-ttu-id="057ed-108">[Directxtk](https://github.com/Microsoft/DirectXTK) - **Bibliothek (Runtime), "** ", "", "", "", "", "", "".</span><span class="sxs-lookup"><span data-stu-id="057ed-108">[DirectXTK](https://github.com/Microsoft/DirectXTK) library (runtime), **CreateXXXTextureFromMemory** (where XXX is DDS or WIC)</span></span>
> -   <span data-ttu-id="057ed-109">[Directxtex](https://github.com/Microsoft/DirectXTex) -Bibliothek (Tools), **loadfromxxxmemory** (hierbei ist xxx WIC, DDS oder TGA). Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele) und dann " **kreateshaderresourceview** "</span><span class="sxs-lookup"><span data-stu-id="057ed-109">[DirectXTex](https://github.com/Microsoft/DirectXTex) library (tools), **LoadFromXXXMemory** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then **CreateShaderResourceView**</span></span>

 

<span data-ttu-id="057ed-110">Erstellen Sie eine Shader-Ressourcen Ansicht aus einer Datei im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="057ed-110">Create a shader-resource view from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="057ed-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="057ed-111">Syntax</span></span>


```C++
HRESULT D3DX11CreateShaderResourceViewFromMemory(
  _In_  ID3D11Device             *pDevice,
  _In_  LPCVOID                  pSrcData,
  _In_  SIZE_T                   SrcDataSize,
  _In_  D3DX11_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX11ThreadPump        *pPump,
  _Out_ ID3D11ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="057ed-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="057ed-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="057ed-113">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="057ed-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="057ed-114">Typ: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="057ed-114">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="057ed-115">Ein Zeiger auf das Gerät (siehe [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)), von dem die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="057ed-115">A pointer to the device (see [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="057ed-116">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="057ed-116">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="057ed-117">Geben Sie Folgendes ein: **[ **lpcvoid**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="057ed-117">Type: **[**LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="057ed-118">Ein Zeiger auf die Datei im Arbeitsspeicher, die die Shader-Ressourcen Ansicht enthält.</span><span class="sxs-lookup"><span data-stu-id="057ed-118">Pointer to the file in memory that contains the shader-resource view.</span></span>

</dd> <dt>

<span data-ttu-id="057ed-119">*Srcdatasize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="057ed-119">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="057ed-120">Typ: **[ **Größe \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="057ed-120">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="057ed-121">Größe der Datei im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="057ed-121">Size of the file in memory.</span></span>

</dd> <dt>

<span data-ttu-id="057ed-122">*ploadinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="057ed-122">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="057ed-123">Type: **[ **Bibliothek d3dx11 \_ Image \_ Load \_ Info**](d3dx11-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="057ed-123">Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***</span></span>

<span data-ttu-id="057ed-124">Optional.</span><span class="sxs-lookup"><span data-stu-id="057ed-124">Optional.</span></span> <span data-ttu-id="057ed-125">Gibt die Merkmale einer Textur an (siehe [**Bibliothek d3dx11 \_ Image \_ Load \_ Info**](d3dx11-image-load-info.md)), wenn der Datenprozessor erstellt wird. Legen Sie diese Einstellung auf **null** fest, um die Merkmale einer Textur beim Laden der Textur zu lesen.</span><span class="sxs-lookup"><span data-stu-id="057ed-125">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="057ed-126">*ppump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="057ed-126">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="057ed-127">Typ: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="057ed-127">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="057ed-128">Ein Zeiger auf eine Thread-Pump Schnittstelle (siehe [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="057ed-128">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="057ed-129">Wenn **null** angegeben wird, verhält sich diese Funktion synchron und wird erst nach Abschluss des Vorgangs zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="057ed-129">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="057ed-130">*ppshaderresourceview* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="057ed-130">*ppShaderResourceView* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="057ed-131">Typ: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="057ed-131">Type: **[**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span></span>

<span data-ttu-id="057ed-132">Adresse eines Zeigers auf die neu erstellte Shader-Ressourcen Ansicht.</span><span class="sxs-lookup"><span data-stu-id="057ed-132">Address of a pointer to the newly created shader resource view.</span></span> <span data-ttu-id="057ed-133">Siehe [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="057ed-133">See [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span></span>

</dd> <dt>

<span data-ttu-id="057ed-134">*phresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="057ed-134">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="057ed-135">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="057ed-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="057ed-136">Ein Zeiger auf den Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="057ed-136">A pointer to the return value.</span></span> <span data-ttu-id="057ed-137">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="057ed-137">May be **NULL**.</span></span> <span data-ttu-id="057ed-138">Wenn *ppump* nicht **null** ist, muss *phresult* eine gültige Speicheradresse sein, bis die asynchrone Ausführung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="057ed-138">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="057ed-139">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="057ed-139">Return value</span></span>

<span data-ttu-id="057ed-140">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="057ed-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="057ed-141">Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="057ed-141">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="057ed-142">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="057ed-142">Requirements</span></span>



| <span data-ttu-id="057ed-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="057ed-143">Requirement</span></span> | <span data-ttu-id="057ed-144">Wert</span><span class="sxs-lookup"><span data-stu-id="057ed-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="057ed-145">Header</span><span class="sxs-lookup"><span data-stu-id="057ed-145">Header</span></span><br/>  | <dl> <span data-ttu-id="057ed-146"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="057ed-146"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="057ed-147">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="057ed-147">Library</span></span><br/> | <dl> <span data-ttu-id="057ed-148"><dt>Bibliothek d3dx11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="057ed-148"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="057ed-149">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="057ed-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="057ed-150">D3DX-Funktionen</span><span class="sxs-lookup"><span data-stu-id="057ed-150">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

