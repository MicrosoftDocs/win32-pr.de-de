---
title: D3DX11GetImageInfoFromMemory-Funktion (D3DX11tex. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Beachten Sie, dass Sie anstelle dieser Funktion die directxtex-Bibliothek GetMetadataFromXXXMemory (wobei xxx für WIC, DDS oder TGA verwendet wird) verwenden. Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele). Sie erhalten Informationen zu einem bereits in den Arbeitsspeicher geladenen Image.
ms.assetid: b13192fa-4235-4c38-ba46-e14ffab2f653
keywords:
- D3DX11GetImageInfoFromMemory-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11GetImageInfoFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85c5f1f04c9540614541b9f63b7833967d6ce959
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982324"
---
# <a name="d3dx11getimageinfofrommemory-function"></a><span data-ttu-id="49a83-106">D3DX11GetImageInfoFromMemory-Funktion</span><span class="sxs-lookup"><span data-stu-id="49a83-106">D3DX11GetImageInfoFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="49a83-107">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="49a83-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="49a83-108">Anstatt diese Funktion zu verwenden, empfiehlt es sich, die [directxtex](https://github.com/Microsoft/DirectXTex) -Bibliothek **GetMetadataFromXXXMemory** (wobei xxx für WIC, DDS oder TGA verwendet wird) zu verwenden. Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele).</span><span class="sxs-lookup"><span data-stu-id="49a83-108">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **GetMetadataFromXXXMemory** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>

 

<span data-ttu-id="49a83-109">Sie erhalten Informationen zu einem bereits in den Arbeitsspeicher geladenen Image.</span><span class="sxs-lookup"><span data-stu-id="49a83-109">Get information about an image already loaded into memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="49a83-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="49a83-110">Syntax</span></span>


```C++
HRESULT D3DX11GetImageInfoFromMemory(
  _In_  LPCVOID           pSrcData,
  _In_  SIZE_T            SrcDataSize,
  _In_  ID3DX11ThreadPump *pPump,
  _In_  D3DX11_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="49a83-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="49a83-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49a83-112">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="49a83-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49a83-113">Geben Sie Folgendes ein: **[ **lpcvoid**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="49a83-113">Type: **[**LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="49a83-114">Zeiger auf das Bild im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="49a83-114">Pointer to the image in memory.</span></span>

</dd> <dt>

<span data-ttu-id="49a83-115">*Srcdatasize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="49a83-115">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49a83-116">Typ: **[ **Größe \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="49a83-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="49a83-117">Größe des Bilds im Arbeitsspeicher in Bytes.</span><span class="sxs-lookup"><span data-stu-id="49a83-117">Size of the image in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="49a83-118">*ppump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="49a83-118">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49a83-119">Typ: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="49a83-119">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="49a83-120">Optionales threadpump, das verwendet werden kann, um die Informationen asynchron zu laden.</span><span class="sxs-lookup"><span data-stu-id="49a83-120">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="49a83-121">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="49a83-121">Can be **NULL**.</span></span> <span data-ttu-id="49a83-122">Siehe [**ID3DX11ThreadPump-Schnittstelle**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="49a83-122">See [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="49a83-123">*psrcinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="49a83-123">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49a83-124">Type: **[ **Bibliothek d3dx11 \_ Image \_ Info**](d3dx11-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="49a83-124">Type: **[**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)\***</span></span>

<span data-ttu-id="49a83-125">Informationen zum Image im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="49a83-125">Information about the image in memory.</span></span>

</dd> <dt>

<span data-ttu-id="49a83-126">*phresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="49a83-126">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="49a83-127">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="49a83-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="49a83-128">Ein Zeiger auf den Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="49a83-128">A pointer to the return value.</span></span> <span data-ttu-id="49a83-129">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="49a83-129">May be **NULL**.</span></span> <span data-ttu-id="49a83-130">Wenn *ppump* nicht **null** ist, muss *phresult* eine gültige Speicheradresse sein, bis die asynchrone Ausführung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="49a83-130">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49a83-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="49a83-131">Return value</span></span>

<span data-ttu-id="49a83-132">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="49a83-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="49a83-133">Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="49a83-133">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="49a83-134">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="49a83-134">Requirements</span></span>



| <span data-ttu-id="49a83-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="49a83-135">Requirement</span></span> | <span data-ttu-id="49a83-136">Wert</span><span class="sxs-lookup"><span data-stu-id="49a83-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="49a83-137">Header</span><span class="sxs-lookup"><span data-stu-id="49a83-137">Header</span></span><br/>  | <dl> <span data-ttu-id="49a83-138"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="49a83-138"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="49a83-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="49a83-139">Library</span></span><br/> | <dl> <span data-ttu-id="49a83-140"><dt>Bibliothek d3dx11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="49a83-140"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="49a83-141">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="49a83-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49a83-142">D3DX-Funktionen</span><span class="sxs-lookup"><span data-stu-id="49a83-142">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

