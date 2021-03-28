---
title: D3DX11CreateAsyncTextureProcessor-Funktion (D3DX11tex. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Siehe Hinweise. Erstellen Sie einen Datenprozessor, der mit einem threadpump verwendet werden soll. | D3DX11CreateAsyncTextureProcessor-Funktion (D3DX11tex. h)
ms.assetid: 4f23d265-b326-4449-b7ca-dd0596511b35
keywords:
- D3DX11CreateAsyncTextureProcessor-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncTextureProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 612be6da4dce05ccae368edc4effea83a823dcff
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996016"
---
# <a name="d3dx11createasynctextureprocessor-function"></a><span data-ttu-id="faf8a-107">D3DX11CreateAsyncTextureProcessor-Funktion</span><span class="sxs-lookup"><span data-stu-id="faf8a-107">D3DX11CreateAsyncTextureProcessor function</span></span>

> [!Note]  
> <span data-ttu-id="faf8a-108">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="faf8a-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="faf8a-109">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="faf8a-109">See Remarks.</span></span>

 

<span data-ttu-id="faf8a-110">Erstellen Sie einen Datenprozessor, der mit einem [**threadpump**](id3dx11threadpump.md)verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="faf8a-110">Create a data processor to be used with a [**thread pump**](id3dx11threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="faf8a-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="faf8a-111">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncTextureProcessor(
  _In_  ID3D11Device           *pDevice,
  _In_  D3DX11_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX11DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="faf8a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="faf8a-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="faf8a-113">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="faf8a-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="faf8a-114">Typ: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="faf8a-114">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="faf8a-115">Ein Zeiger auf den devive (siehe [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)).</span><span class="sxs-lookup"><span data-stu-id="faf8a-115">A pointer to the devive (see [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)).</span></span>

</dd> <dt>

<span data-ttu-id="faf8a-116">*ploadinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="faf8a-116">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="faf8a-117">Type: **[ **Bibliothek d3dx11 \_ Image \_ Load \_ Info**](d3dx11-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="faf8a-117">Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***</span></span>

<span data-ttu-id="faf8a-118">Optional.</span><span class="sxs-lookup"><span data-stu-id="faf8a-118">Optional.</span></span> <span data-ttu-id="faf8a-119">Gibt die Merkmale einer Textur an (siehe [**Bibliothek d3dx11 \_ Image \_ Load \_ Info**](d3dx11-image-load-info.md)), wenn der Datenprozessor erstellt wird. Legen Sie diese Einstellung auf **null** fest, um die Merkmale einer Textur beim Laden der Textur zu lesen.</span><span class="sxs-lookup"><span data-stu-id="faf8a-119">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="faf8a-120">*ppdataprocessor* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="faf8a-120">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="faf8a-121">Typ: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="faf8a-121">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span></span>

<span data-ttu-id="faf8a-122">Adresse eines Zeigers auf einen Puffer, der den erstellten Datenprozessor enthält (siehe [**ID3DX11DataProcessor-Schnittstelle**](id3dx11dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="faf8a-122">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX11DataProcessor Interface**](id3dx11dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="faf8a-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="faf8a-123">Return value</span></span>

<span data-ttu-id="faf8a-124">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="faf8a-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="faf8a-125">Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="faf8a-125">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="faf8a-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="faf8a-126">Remarks</span></span>

<span data-ttu-id="faf8a-127">Diese API erstellt eine Datenprozessor Schnittstelle und lädt die Textur. [**D3DX11CreateAsyncTextureInfoProcessor**](d3dx11createasynctextureinfoprocessor.md) erstellt die Datenprozessor Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="faf8a-127">This API does creates a data-processor interface and loads the texture; [**D3DX11CreateAsyncTextureInfoProcessor**](d3dx11createasynctextureinfoprocessor.md) creates the data-processor interface.</span></span>

<span data-ttu-id="faf8a-128">Es gibt keine Implementierung des Async-Lade Moduls außerhalb von D3DX 10 und D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="faf8a-128">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="faf8a-129">Für Windows Store-Apps enthalten die DirectX-Beispiele (z. b. das [Direct3D-tutorialbeispiel](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) das **basicloader** -Modul, das das asynchrone Programmiermodell ([**asyncbase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))) Windows-Runtime verwendet.</span><span class="sxs-lookup"><span data-stu-id="faf8a-129">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="faf8a-130">Für Win32-Desktop-Apps können Sie den [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) verwenden, um etwas ähnliches wie das Windows-Runtime asynchrone Programmiermodell zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="faf8a-130">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="faf8a-131">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="faf8a-131">Requirements</span></span>



| <span data-ttu-id="faf8a-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="faf8a-132">Requirement</span></span> | <span data-ttu-id="faf8a-133">Wert</span><span class="sxs-lookup"><span data-stu-id="faf8a-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="faf8a-134">Header</span><span class="sxs-lookup"><span data-stu-id="faf8a-134">Header</span></span><br/>  | <dl> <span data-ttu-id="faf8a-135"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="faf8a-135"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="faf8a-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="faf8a-136">Library</span></span><br/> | <dl> <span data-ttu-id="faf8a-137"><dt>Bibliothek d3dx11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="faf8a-137"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="faf8a-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="faf8a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faf8a-139">D3DX-Funktionen</span><span class="sxs-lookup"><span data-stu-id="faf8a-139">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

