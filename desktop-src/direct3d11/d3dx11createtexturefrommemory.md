---
title: D3DX11CreateTextureFromMemory-Funktion (Bibliothek d3dx11. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Beachten Sie anstelle dieser Funktion, dass Sie diese directxtk-Bibliothek (Runtime), den "anatexxxtexturefrommemory" (wobei xxx DDS oder WIC ist) directxtex Library (Tools), loadfromxxxmemory (wobei xxx für WIC, DDS oder TGA verwendet wird) verwenden. Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele), dann erstellt "kreatetexture" eine Textur Ressource aus einer Datei, die sich im Systemspeicher befindet.
ms.assetid: 1b07653e-8dc8-40b2-b591-bd25a54cfaa2
keywords:
- D3DX11CreateTextureFromMemory-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateTextureFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99987e882430da7f5e884f1b22e890947f7105e3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961682"
---
# <a name="d3dx11createtexturefrommemory-function"></a><span data-ttu-id="917f5-105">D3DX11CreateTextureFromMemory-Funktion</span><span class="sxs-lookup"><span data-stu-id="917f5-105">D3DX11CreateTextureFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="917f5-106">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="917f5-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="917f5-107">Anstatt diese Funktion zu verwenden, empfiehlt es sich, diese zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="917f5-107">Instead of using this function, we recommend that you use these:</span></span>
>
> -   <span data-ttu-id="917f5-108">[Directxtk](https://github.com/Microsoft/DirectXTK) - **Bibliothek (Runtime), "** ", "", "", "", "", "", "".</span><span class="sxs-lookup"><span data-stu-id="917f5-108">[DirectXTK](https://github.com/Microsoft/DirectXTK) library (runtime), **CreateXXXTextureFromMemory** (where XXX is DDS or WIC)</span></span>
> -   <span data-ttu-id="917f5-109">[Directxtex](https://github.com/Microsoft/DirectXTex) -Bibliothek (Tools), **loadfromxxxmemory** (hierbei ist xxx WIC, DDS oder TGA). Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele) und dann " **kreatetexture** "</span><span class="sxs-lookup"><span data-stu-id="917f5-109">[DirectXTex](https://github.com/Microsoft/DirectXTex) library (tools), **LoadFromXXXMemory** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then **CreateTexture**</span></span>

 

<span data-ttu-id="917f5-110">Erstellen Sie eine Textur Ressource aus einer Datei, die sich im Systemspeicher befindet.</span><span class="sxs-lookup"><span data-stu-id="917f5-110">Create a texture resource from a file residing in system memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="917f5-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="917f5-111">Syntax</span></span>


```C++
HRESULT D3DX11CreateTextureFromMemory(
  _In_  ID3D11Device           *pDevice,
  _In_  LPCVOID                pSrcData,
  _In_  SIZE_T                 SrcDataSize,
  _In_  D3DX11_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX11ThreadPump      *pPump,
  _Out_ ID3D11Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="917f5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="917f5-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="917f5-113">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="917f5-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="917f5-114">Typ: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="917f5-114">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="917f5-115">Ein Zeiger auf das Gerät (siehe [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)), von dem die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="917f5-115">A pointer to the device (see [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="917f5-116">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="917f5-116">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="917f5-117">Geben Sie Folgendes ein: **[ **lpcvoid**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="917f5-117">Type: **[**LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="917f5-118">Zeiger auf die Ressource im Systemspeicher.</span><span class="sxs-lookup"><span data-stu-id="917f5-118">Pointer to the resource in system memory.</span></span>

</dd> <dt>

<span data-ttu-id="917f5-119">*Srcdatasize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="917f5-119">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="917f5-120">Typ: **[ **Größe \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="917f5-120">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="917f5-121">Größe der Ressource im Systemspeicher.</span><span class="sxs-lookup"><span data-stu-id="917f5-121">Size of the resource in system memory.</span></span>

</dd> <dt>

<span data-ttu-id="917f5-122">*ploadinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="917f5-122">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="917f5-123">Type: **[ **Bibliothek d3dx11 \_ Image \_ Load \_ Info**](d3dx11-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="917f5-123">Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***</span></span>

<span data-ttu-id="917f5-124">Optional.</span><span class="sxs-lookup"><span data-stu-id="917f5-124">Optional.</span></span> <span data-ttu-id="917f5-125">Gibt die Merkmale einer Textur an (siehe [**Bibliothek d3dx11 \_ Image \_ Load \_ Info**](d3dx11-image-load-info.md)), wenn der Datenprozessor erstellt wird. Legen Sie diese Einstellung auf **null** fest, um die Merkmale einer Textur beim Laden der Textur zu lesen.</span><span class="sxs-lookup"><span data-stu-id="917f5-125">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="917f5-126">*ppump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="917f5-126">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="917f5-127">Typ: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="917f5-127">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="917f5-128">Ein Zeiger auf eine Thread-Pump Schnittstelle (siehe [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="917f5-128">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="917f5-129">Wenn **null** angegeben wird, verhält sich diese Funktion synchron und wird erst nach Abschluss des Vorgangs zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="917f5-129">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="917f5-130">*pptexture* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="917f5-130">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="917f5-131">Typ: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\*\***</span><span class="sxs-lookup"><span data-stu-id="917f5-131">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\*\***</span></span>

<span data-ttu-id="917f5-132">Adresse eines Zeigers auf die erstellte Ressource.</span><span class="sxs-lookup"><span data-stu-id="917f5-132">Address of a pointer to the created resource.</span></span> <span data-ttu-id="917f5-133">Siehe [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span><span class="sxs-lookup"><span data-stu-id="917f5-133">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> <dt>

<span data-ttu-id="917f5-134">*phresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="917f5-134">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="917f5-135">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="917f5-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="917f5-136">Ein Zeiger auf den Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="917f5-136">A pointer to the return value.</span></span> <span data-ttu-id="917f5-137">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="917f5-137">May be **NULL**.</span></span> <span data-ttu-id="917f5-138">Wenn *ppump* nicht **null** ist, muss *phresult* eine gültige Speicheradresse sein, bis die asynchrone Ausführung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="917f5-138">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="917f5-139">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="917f5-139">Return value</span></span>

<span data-ttu-id="917f5-140">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="917f5-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="917f5-141">Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="917f5-141">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="917f5-142">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="917f5-142">Requirements</span></span>



| <span data-ttu-id="917f5-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="917f5-143">Requirement</span></span> | <span data-ttu-id="917f5-144">Wert</span><span class="sxs-lookup"><span data-stu-id="917f5-144">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="917f5-145">Header</span><span class="sxs-lookup"><span data-stu-id="917f5-145">Header</span></span><br/>  | <dl> <span data-ttu-id="917f5-146"><dt>Bibliothek d3dx11. h</dt></span><span class="sxs-lookup"><span data-stu-id="917f5-146"><dt>D3DX11.h</dt></span></span> </dl>   |
| <span data-ttu-id="917f5-147">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="917f5-147">Library</span></span><br/> | <dl> <span data-ttu-id="917f5-148"><dt>Bibliothek d3dx11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="917f5-148"><dt>D3DX11.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="917f5-149">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="917f5-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="917f5-150">D3DX-Funktionen</span><span class="sxs-lookup"><span data-stu-id="917f5-150">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

