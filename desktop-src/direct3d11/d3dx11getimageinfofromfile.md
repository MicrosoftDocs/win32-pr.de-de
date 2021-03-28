---
title: D3DX11GetImageInfoFromFile-Funktion (D3DX11tex. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Beachten Sie, dass Sie anstelle dieser Funktion die directxtex-Bibliothek GetMetadataFromXXXFile (wobei xxx für WIC, DDS oder TGA verwendet wird) verwenden. Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele). Ruft Informationen zu einer angegebenen Bilddatei ab.
ms.assetid: 57768604-3672-49a0-8120-f09240b8fc98
keywords:
- D3DX11GetImageInfoFromFile-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11GetImageInfoFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8448d31a3f4fdb14855ea2c9456da87f9df1de4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050898"
---
# <a name="d3dx11getimageinfofromfile-function"></a><span data-ttu-id="99f70-106">D3DX11GetImageInfoFromFile-Funktion</span><span class="sxs-lookup"><span data-stu-id="99f70-106">D3DX11GetImageInfoFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="99f70-107">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="99f70-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="99f70-108">Anstatt diese Funktion zu verwenden, empfiehlt es sich, die [directxtex](https://github.com/Microsoft/DirectXTex) -Bibliothek **GetMetadataFromXXXFile** (wobei xxx für WIC, DDS oder TGA verwendet wird) zu verwenden. Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele).</span><span class="sxs-lookup"><span data-stu-id="99f70-108">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **GetMetadataFromXXXFile** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>

 

<span data-ttu-id="99f70-109">Ruft Informationen zu einer angegebenen Bilddatei ab.</span><span class="sxs-lookup"><span data-stu-id="99f70-109">Retrieves information about a given image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="99f70-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="99f70-110">Syntax</span></span>


```C++
HRESULT D3DX11GetImageInfoFromFile(
  _In_  LPCTSTR           pSrcFile,
  _In_  ID3DX11ThreadPump *pPump,
  _In_  D3DX11_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="99f70-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="99f70-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99f70-112">*psrcfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99f70-112">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99f70-113">Typ: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="99f70-113">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="99f70-114">Dateiname des Bilds, über das Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="99f70-114">File name of image to retrieve information about.</span></span> <span data-ttu-id="99f70-115">Wenn Unicode oder \_ Unicode definiert ist, ist dieser Parametertyp LPCWSTR; andernfalls lautet der Typ LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="99f70-115">If UNICODE or \_UNICODE are defined, this parameter type is LPCWSTR, otherwise, the type is LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="99f70-116">*ppump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99f70-116">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99f70-117">Typ: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="99f70-117">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="99f70-118">Optionales threadpump, das verwendet werden kann, um die Informationen asynchron zu laden.</span><span class="sxs-lookup"><span data-stu-id="99f70-118">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="99f70-119">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="99f70-119">Can be **NULL**.</span></span> <span data-ttu-id="99f70-120">Siehe [**ID3DX11ThreadPump-Schnittstelle**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="99f70-120">See [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="99f70-121">*psrcinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99f70-121">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99f70-122">Type: **[ **Bibliothek d3dx11 \_ Image \_ Info**](d3dx11-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="99f70-122">Type: **[**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)\***</span></span>

<span data-ttu-id="99f70-123">Zeiger auf eine [**Bibliothek d3dx11- \_ Bild \_ Info**](d3dx11-image-info.md) , die mit der Beschreibung der Daten in der Quelldatei aufgefüllt werden soll.</span><span class="sxs-lookup"><span data-stu-id="99f70-123">Pointer to a [**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md) to be filled with the description of the data in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="99f70-124">*phresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="99f70-124">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99f70-125">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="99f70-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="99f70-126">Ein Zeiger auf den Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="99f70-126">A pointer to the return value.</span></span> <span data-ttu-id="99f70-127">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="99f70-127">May be **NULL**.</span></span> <span data-ttu-id="99f70-128">Wenn *ppump* nicht **null** ist, muss *phresult* eine gültige Speicheradresse sein, bis die asynchrone Ausführung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="99f70-128">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99f70-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="99f70-129">Return value</span></span>

<span data-ttu-id="99f70-130">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="99f70-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="99f70-131">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="99f70-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="99f70-132">Wenn die Funktion fehlschlägt, kann der Rückgabewert wie folgt lauten: D3DERR \_ invalidcall</span><span class="sxs-lookup"><span data-stu-id="99f70-132">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="99f70-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="99f70-133">Remarks</span></span>

<span data-ttu-id="99f70-134">Diese Funktion unterstützt sowohl Unicode-als auch ANSI-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="99f70-134">This function supports both Unicode and ANSI strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="99f70-135">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="99f70-135">Requirements</span></span>



| <span data-ttu-id="99f70-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="99f70-136">Requirement</span></span> | <span data-ttu-id="99f70-137">Wert</span><span class="sxs-lookup"><span data-stu-id="99f70-137">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="99f70-138">Header</span><span class="sxs-lookup"><span data-stu-id="99f70-138">Header</span></span><br/>  | <dl> <span data-ttu-id="99f70-139"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="99f70-139"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="99f70-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="99f70-140">Library</span></span><br/> | <dl> <span data-ttu-id="99f70-141"><dt>Bibliothek d3dx11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99f70-141"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="99f70-142">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="99f70-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99f70-143">D3DX-Funktionen</span><span class="sxs-lookup"><span data-stu-id="99f70-143">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

