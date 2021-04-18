---
title: D3DX11CreateAsyncFileLoader-Funktion (D3DX11async. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Siehe Hinweise. Erstellen Sie ein asynchrones Datei Lade Modul.
ms.assetid: ee24ac00-3636-4900-9b8a-27778c9a2152
keywords:
- D3DX11CreateAsyncFileLoader-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncFileLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5637b2eddb035d937315582188295d93d9fd0e9b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996045"
---
# <a name="d3dx11createasyncfileloader-function"></a><span data-ttu-id="09ca8-106">D3DX11CreateAsyncFileLoader-Funktion</span><span class="sxs-lookup"><span data-stu-id="09ca8-106">D3DX11CreateAsyncFileLoader function</span></span>

> [!Note]  
> <span data-ttu-id="09ca8-107">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="09ca8-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="09ca8-108">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="09ca8-108">See Remarks.</span></span>

 

<span data-ttu-id="09ca8-109">Erstellen Sie ein asynchrones Datei Lade Modul.</span><span class="sxs-lookup"><span data-stu-id="09ca8-109">Create an asynchronous-file loader.</span></span>

## <a name="syntax"></a><span data-ttu-id="09ca8-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="09ca8-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncFileLoader(
  _In_  LPCTSTR           pFileName,
  _Out_ ID3DX11DataLoader **ppDataLoader
);
```



## <a name="parameters"></a><span data-ttu-id="09ca8-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="09ca8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09ca8-112">*pfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="09ca8-112">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09ca8-113">Typ: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="09ca8-113">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="09ca8-114">Der Name der zu ladenden Datei.</span><span class="sxs-lookup"><span data-stu-id="09ca8-114">The name of the file to load.</span></span> <span data-ttu-id="09ca8-115">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="09ca8-115">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="09ca8-116">Andernfalls wird der Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="09ca8-116">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="09ca8-117">*ppdataloader* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="09ca8-117">*ppDataLoader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09ca8-118">Typ: **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="09ca8-118">Type: **[**ID3DX11DataLoader**](id3dx11dataloader.md)\*\***</span></span>

<span data-ttu-id="09ca8-119">Adresse eines Zeigers auf den asynchronen Daten Lader (siehe [**ID3DX11DataLoader Interface**](id3dx11dataloader.md)).</span><span class="sxs-lookup"><span data-stu-id="09ca8-119">Address of a pointer to the asynchronous-data loader (see [**ID3DX11DataLoader Interface**](id3dx11dataloader.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09ca8-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="09ca8-120">Return value</span></span>

<span data-ttu-id="09ca8-121">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="09ca8-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="09ca8-122">Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="09ca8-122">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="09ca8-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="09ca8-123">Remarks</span></span>

<span data-ttu-id="09ca8-124">Es gibt keine Implementierung des Async-Lade Moduls außerhalb von D3DX 10 und D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="09ca8-124">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="09ca8-125">Für Windows Store-Apps enthalten die DirectX-Beispiele (z. b. das [Direct3D-tutorialbeispiel](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) das **basicloader** -Modul, das das asynchrone Programmiermodell ([**asyncbase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))) Windows-Runtime verwendet.</span><span class="sxs-lookup"><span data-stu-id="09ca8-125">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="09ca8-126">Für Win32-Desktop-Apps können Sie den [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) verwenden, um etwas ähnliches wie das Windows-Runtime asynchrone Programmiermodell zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="09ca8-126">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="09ca8-127">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="09ca8-127">Requirements</span></span>



| <span data-ttu-id="09ca8-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="09ca8-128">Requirement</span></span> | <span data-ttu-id="09ca8-129">Wert</span><span class="sxs-lookup"><span data-stu-id="09ca8-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="09ca8-130">Header</span><span class="sxs-lookup"><span data-stu-id="09ca8-130">Header</span></span><br/>  | <dl> <span data-ttu-id="09ca8-131"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="09ca8-131"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="09ca8-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="09ca8-132">Library</span></span><br/> | <dl> <span data-ttu-id="09ca8-133"><dt>Bibliothek d3dx11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="09ca8-133"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="09ca8-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="09ca8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09ca8-135">D3DX-Funktionen</span><span class="sxs-lookup"><span data-stu-id="09ca8-135">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

