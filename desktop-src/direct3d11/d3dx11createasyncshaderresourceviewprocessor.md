---
title: D3DX11CreateAsyncShaderResourceViewProcessor-Funktion (D3DX11async. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird.
ms.assetid: bd9349af-f433-47f9-b443-3049c32fc286
keywords:
- D3DX11CreateAsyncShaderResourceViewProcessor-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncShaderResourceViewProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3164aac5ddaec3d61108a2cf129b76991b8f76a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996022"
---
# <a name="d3dx11createasyncshaderresourceviewprocessor-function"></a><span data-ttu-id="25fc8-104">D3DX11CreateAsyncShaderResourceViewProcessor-Funktion</span><span class="sxs-lookup"><span data-stu-id="25fc8-104">D3DX11CreateAsyncShaderResourceViewProcessor function</span></span>

> [!Note]  
> <span data-ttu-id="25fc8-105">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="25fc8-105">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="25fc8-106">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="25fc8-106">See Remarks.</span></span>

 

<span data-ttu-id="25fc8-107">Erstellen Sie einen Datenprozessor, der eine Ressource lädt, und erstellen Sie dann eine Shader-Ressourcen Ansicht dafür.</span><span class="sxs-lookup"><span data-stu-id="25fc8-107">Create a data processor that will load a resource and then create a shader-resource view for it.</span></span> <span data-ttu-id="25fc8-108">Datenprozessoren sind eine Komponente der Funktion zum asynchronen Laden von Daten in Bibliothek d3dx11, die [**Thread-Pumpen**](id3dx11threadpump.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="25fc8-108">Data processors are a component of the asynchronous data loading feature in D3DX11 that uses [**thread pumps**](id3dx11threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="25fc8-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="25fc8-109">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncShaderResourceViewProcessor(
  _In_  ID3D11Device           *pDevice,
  _In_  D3DX11_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX11DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="25fc8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="25fc8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25fc8-111">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25fc8-111">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25fc8-112">Typ: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="25fc8-112">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="25fc8-113">Zeiger auf das Direct3D-Gerät (siehe [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)), das verwendet wird, um eine Ressource und eine Shader-Ressourcen Ansicht für diese Ressource zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="25fc8-113">Pointer to the Direct3D device (see [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) that will be used to create a resource and a shader-resource view for that resource.</span></span>

</dd> <dt>

<span data-ttu-id="25fc8-114">*ploadinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25fc8-114">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25fc8-115">Type: **[ **Bibliothek d3dx11 \_ Image \_ Load \_ Info**](d3dx11-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="25fc8-115">Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***</span></span>

<span data-ttu-id="25fc8-116">Optional.</span><span class="sxs-lookup"><span data-stu-id="25fc8-116">Optional.</span></span> <span data-ttu-id="25fc8-117">Gibt die Merkmale einer Textur an (siehe [**Bibliothek d3dx11 \_ Image \_ Load \_ Info**](d3dx11-image-load-info.md)), wenn der Datenprozessor erstellt wird. Legen Sie diese Einstellung auf **null** fest, um die Merkmale einer Textur beim Laden der Textur zu lesen.</span><span class="sxs-lookup"><span data-stu-id="25fc8-117">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="25fc8-118">*ppdataprocessor* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="25fc8-118">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25fc8-119">Typ: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="25fc8-119">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span></span>

<span data-ttu-id="25fc8-120">Adresse eines Zeigers auf einen Puffer, der den erstellten Datenprozessor enthält (siehe [**ID3DX11DataProcessor-Schnittstelle**](id3dx11dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="25fc8-120">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX11DataProcessor Interface**](id3dx11dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25fc8-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="25fc8-121">Return value</span></span>

<span data-ttu-id="25fc8-122">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="25fc8-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="25fc8-123">Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="25fc8-123">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="25fc8-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="25fc8-124">Remarks</span></span>

<span data-ttu-id="25fc8-125">Es gibt keine Implementierung des Async-Lade Moduls außerhalb von D3DX 10 und D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="25fc8-125">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="25fc8-126">Für Windows Store-Apps enthalten die DirectX-Beispiele (z. b. das [Direct3D-tutorialbeispiel](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) das **basicloader** -Modul, das das asynchrone Programmiermodell ([**asyncbase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))) Windows-Runtime verwendet.</span><span class="sxs-lookup"><span data-stu-id="25fc8-126">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="25fc8-127">Für Win32-Desktop-Apps können Sie den [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) verwenden, um etwas ähnliches wie das Windows-Runtime asynchrone Programmiermodell zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="25fc8-127">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="25fc8-128">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="25fc8-128">Requirements</span></span>



| <span data-ttu-id="25fc8-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="25fc8-129">Requirement</span></span> | <span data-ttu-id="25fc8-130">Wert</span><span class="sxs-lookup"><span data-stu-id="25fc8-130">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="25fc8-131">Header</span><span class="sxs-lookup"><span data-stu-id="25fc8-131">Header</span></span><br/>  | <dl> <span data-ttu-id="25fc8-132"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="25fc8-132"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="25fc8-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="25fc8-133">Library</span></span><br/> | <dl> <span data-ttu-id="25fc8-134"><dt>Bibliothek d3dx11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="25fc8-134"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="25fc8-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="25fc8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25fc8-136">D3DX-Funktionen</span><span class="sxs-lookup"><span data-stu-id="25fc8-136">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

