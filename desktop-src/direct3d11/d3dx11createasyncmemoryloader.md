---
title: D3DX11CreateAsyncMemoryLoader-Funktion (D3DX11async. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Siehe Hinweise. Erstellen Sie ein Lade Modul für asynchrone Speicher.
ms.assetid: 0bf1e6a2-a968-4644-a7b4-e847ed4f7450
keywords:
- D3DX11CreateAsyncMemoryLoader-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncMemoryLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d16c91b0537f79fb60a5b256789c13d664401ecc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996034"
---
# <a name="d3dx11createasyncmemoryloader-function"></a><span data-ttu-id="97601-106">D3DX11CreateAsyncMemoryLoader-Funktion</span><span class="sxs-lookup"><span data-stu-id="97601-106">D3DX11CreateAsyncMemoryLoader function</span></span>

> [!Note]  
> <span data-ttu-id="97601-107">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="97601-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="97601-108">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="97601-108">See Remarks.</span></span>

 

<span data-ttu-id="97601-109">Erstellen Sie ein Lade Modul für asynchrone Speicher.</span><span class="sxs-lookup"><span data-stu-id="97601-109">Create an asynchronous-memory loader.</span></span>

## <a name="syntax"></a><span data-ttu-id="97601-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="97601-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncMemoryLoader(
  _In_  LPCVOID           pData,
  _In_  SIZE_T            cbData,
  _Out_ ID3DX11DataLoader **ppDataLoader
);
```



## <a name="parameters"></a><span data-ttu-id="97601-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="97601-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97601-112">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97601-112">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97601-113">Geben Sie Folgendes ein: **[ **lpcvoid**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="97601-113">Type: **[**LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="97601-114">Zeiger auf die Daten.</span><span class="sxs-lookup"><span data-stu-id="97601-114">Pointer to the data.</span></span>

</dd> <dt>

<span data-ttu-id="97601-115">*cbData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97601-115">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97601-116">Typ: **[ **Größe \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="97601-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="97601-117">Größe der Daten.</span><span class="sxs-lookup"><span data-stu-id="97601-117">Size of the data.</span></span>

</dd> <dt>

<span data-ttu-id="97601-118">*ppdataloader* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="97601-118">*ppDataLoader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97601-119">Typ: **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="97601-119">Type: **[**ID3DX11DataLoader**](id3dx11dataloader.md)\*\***</span></span>

<span data-ttu-id="97601-120">Die Adresse eines Zeigers auf den asynchronen Daten Lader (siehe [**ID3DX11DataLoader Interface**](id3dx11dataloader.md)).</span><span class="sxs-lookup"><span data-stu-id="97601-120">The address of a pointer to the asynchronous-data loader (see [**ID3DX11DataLoader Interface**](id3dx11dataloader.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97601-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="97601-121">Return value</span></span>

<span data-ttu-id="97601-122">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="97601-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="97601-123">Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="97601-123">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="97601-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97601-124">Remarks</span></span>

<span data-ttu-id="97601-125">Es gibt keine Implementierung des Async-Lade Moduls außerhalb von D3DX 10 und D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="97601-125">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="97601-126">Für Windows Store-Apps enthalten die DirectX-Beispiele (z. b. das [Direct3D-tutorialbeispiel](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) das **basicloader** -Modul, das das asynchrone Programmiermodell ([**asyncbase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))) Windows-Runtime verwendet.</span><span class="sxs-lookup"><span data-stu-id="97601-126">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="97601-127">Für Win32-Desktop-Apps können Sie den [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) verwenden, um etwas ähnliches wie das Windows-Runtime asynchrone Programmiermodell zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="97601-127">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="97601-128">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="97601-128">Requirements</span></span>



| <span data-ttu-id="97601-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97601-129">Requirement</span></span> | <span data-ttu-id="97601-130">Wert</span><span class="sxs-lookup"><span data-stu-id="97601-130">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="97601-131">Header</span><span class="sxs-lookup"><span data-stu-id="97601-131">Header</span></span><br/>  | <dl> <span data-ttu-id="97601-132"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="97601-132"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="97601-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="97601-133">Library</span></span><br/> | <dl> <span data-ttu-id="97601-134"><dt>Bibliothek d3dx11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="97601-134"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="97601-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="97601-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97601-136">D3DX-Funktionen</span><span class="sxs-lookup"><span data-stu-id="97601-136">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

