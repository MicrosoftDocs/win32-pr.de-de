---
title: D3DX11CreateAsyncResourceLoader-Funktion (D3DX11async. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Siehe Hinweise. Erstellen Sie ein asynchrones Ressourcen Lade Modul.
ms.assetid: b49900a1-866d-4a4a-bf3a-2deb9ce4a208
keywords:
- D3DX11CreateAsyncResourceLoader-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncResourceLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc7dd914250f3d47b80643d88ef055681f2e8a9f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050900"
---
# <a name="d3dx11createasyncresourceloader-function"></a><span data-ttu-id="82d18-106">D3DX11CreateAsyncResourceLoader-Funktion</span><span class="sxs-lookup"><span data-stu-id="82d18-106">D3DX11CreateAsyncResourceLoader function</span></span>

> [!Note]  
> <span data-ttu-id="82d18-107">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="82d18-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="82d18-108">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="82d18-108">See Remarks.</span></span>

 

<span data-ttu-id="82d18-109">Erstellen Sie ein asynchrones Ressourcen Lade Modul.</span><span class="sxs-lookup"><span data-stu-id="82d18-109">Create an asynchronous-resource loader.</span></span>

## <a name="syntax"></a><span data-ttu-id="82d18-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="82d18-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncResourceLoader(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _Out_ ID3DX11DataLoader **ppDataLoader
);
```



## <a name="parameters"></a><span data-ttu-id="82d18-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="82d18-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82d18-112">*hsrcmodule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82d18-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82d18-113">Typ: **[ **HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="82d18-113">Type: **[**HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="82d18-114">Handle für das Ressourcen Modul.</span><span class="sxs-lookup"><span data-stu-id="82d18-114">Handle to the resource module.</span></span> <span data-ttu-id="82d18-115">Verwenden Sie die [GetModuleHandle-Funktion](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) , um das Handle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="82d18-115">Use [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) to get the handle.</span></span>

</dd> <dt>

<span data-ttu-id="82d18-116">*psrkresource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82d18-116">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82d18-117">Typ: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="82d18-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="82d18-118">Der Name der Ressource in hsrcmodule.</span><span class="sxs-lookup"><span data-stu-id="82d18-118">Name of the resource in hSrcModule.</span></span> <span data-ttu-id="82d18-119">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="82d18-119">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="82d18-120">Andernfalls wird der Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="82d18-120">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="82d18-121">*ppdataloader* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="82d18-121">*ppDataLoader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82d18-122">Typ: **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="82d18-122">Type: **[**ID3DX11DataLoader**](id3dx11dataloader.md)\*\***</span></span>

<span data-ttu-id="82d18-123">Die Adresse eines Zeigers auf den asynchronen Daten Lader (siehe [**ID3DX11DataLoader Interface**](id3dx11dataloader.md)).</span><span class="sxs-lookup"><span data-stu-id="82d18-123">The address of a pointer to the asynchronous-data loader (see [**ID3DX11DataLoader Interface**](id3dx11dataloader.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82d18-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="82d18-124">Return value</span></span>

<span data-ttu-id="82d18-125">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="82d18-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="82d18-126">Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="82d18-126">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="82d18-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82d18-127">Remarks</span></span>

<span data-ttu-id="82d18-128">Es gibt keine Implementierung des Async-Lade Moduls außerhalb von D3DX 10 und D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="82d18-128">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="82d18-129">Für Windows Store-Apps enthalten die DirectX-Beispiele (z. b. das [Direct3D-tutorialbeispiel](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) das **basicloader** -Modul, das das asynchrone Programmiermodell ([**asyncbase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))) Windows-Runtime verwendet.</span><span class="sxs-lookup"><span data-stu-id="82d18-129">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="82d18-130">Für Win32-Desktop-Apps können Sie den [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) verwenden, um etwas ähnliches wie das Windows-Runtime asynchrone Programmiermodell zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="82d18-130">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="82d18-131">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="82d18-131">Requirements</span></span>



| <span data-ttu-id="82d18-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="82d18-132">Requirement</span></span> | <span data-ttu-id="82d18-133">Wert</span><span class="sxs-lookup"><span data-stu-id="82d18-133">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="82d18-134">Header</span><span class="sxs-lookup"><span data-stu-id="82d18-134">Header</span></span><br/>  | <dl> <span data-ttu-id="82d18-135"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="82d18-135"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="82d18-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="82d18-136">Library</span></span><br/> | <dl> <span data-ttu-id="82d18-137"><dt>Bibliothek d3dx11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="82d18-137"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="82d18-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="82d18-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82d18-139">D3DX-Funktionen</span><span class="sxs-lookup"><span data-stu-id="82d18-139">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

