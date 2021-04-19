---
description: Sie erhalten Informationen zu einem bereits in den Arbeitsspeicher geladenen Image.
ms.assetid: 6750116a-ad4f-4102-aba9-6ef32c367be4
title: D3DX10GetImageInfoFromMemory-Funktion (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetImageInfoFromMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 677ce6a2ac8e4e165ca0a2bbb64b6254870e4ed8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370429"
---
# <a name="d3dx10getimageinfofrommemory-function"></a><span data-ttu-id="adc10-103">D3DX10GetImageInfoFromMemory-Funktion</span><span class="sxs-lookup"><span data-stu-id="adc10-103">D3DX10GetImageInfoFromMemory function</span></span>

<span data-ttu-id="adc10-104">Sie erhalten Informationen zu einem bereits in den Arbeitsspeicher geladenen Image.</span><span class="sxs-lookup"><span data-stu-id="adc10-104">Get information about an image already loaded into memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="adc10-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="adc10-105">Syntax</span></span>


```C++
HRESULT D3DX10GetImageInfoFromMemory(
  _In_  LPCVOID           pSrcData,
  _In_  SIZE_T            SrcDataSize,
  _In_  ID3DX10ThreadPump *pPump,
  _In_  D3DX10_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="adc10-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="adc10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adc10-107">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="adc10-107">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adc10-108">Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="adc10-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="adc10-109">Zeiger auf das Bild im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="adc10-109">Pointer to the image in memory.</span></span>

</dd> <dt>

<span data-ttu-id="adc10-110">*Srcdatasize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="adc10-110">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adc10-111">Typ: **[ **Größe \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="adc10-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="adc10-112">Größe des Bilds im Arbeitsspeicher in Bytes.</span><span class="sxs-lookup"><span data-stu-id="adc10-112">Size of the image in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="adc10-113">*ppump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="adc10-113">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adc10-114">Typ: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="adc10-114">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="adc10-115">Optionales threadpump, das verwendet werden kann, um die Informationen asynchron zu laden.</span><span class="sxs-lookup"><span data-stu-id="adc10-115">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="adc10-116">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="adc10-116">Can be **NULL**.</span></span> <span data-ttu-id="adc10-117">Siehe [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="adc10-117">See [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="adc10-118">*psrcinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="adc10-118">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adc10-119">Type: **[ **d3dx10 \_ Image \_ Info**](d3dx10-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="adc10-119">Type: **[**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md)\***</span></span>

<span data-ttu-id="adc10-120">Informationen zum Image im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="adc10-120">Information about the image in memory.</span></span>

</dd> <dt>

<span data-ttu-id="adc10-121">*phresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="adc10-121">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="adc10-122">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="adc10-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="adc10-123">Ein Zeiger auf den Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="adc10-123">A pointer to the return value.</span></span> <span data-ttu-id="adc10-124">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="adc10-124">May be **NULL**.</span></span> <span data-ttu-id="adc10-125">Wenn *ppump* nicht **null** ist, muss *phresult* eine gültige Speicheradresse sein, bis die asynchrone Ausführung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="adc10-125">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adc10-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="adc10-126">Return value</span></span>

<span data-ttu-id="adc10-127">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="adc10-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="adc10-128">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="adc10-128">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="adc10-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="adc10-129">Requirements</span></span>



| <span data-ttu-id="adc10-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="adc10-130">Requirement</span></span> | <span data-ttu-id="adc10-131">Wert</span><span class="sxs-lookup"><span data-stu-id="adc10-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="adc10-132">Header</span><span class="sxs-lookup"><span data-stu-id="adc10-132">Header</span></span><br/>  | <dl> <span data-ttu-id="adc10-133"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="adc10-133"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="adc10-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="adc10-134">Library</span></span><br/> | <dl> <span data-ttu-id="adc10-135"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="adc10-135"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="adc10-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="adc10-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adc10-137">Textur Funktionen in D3DX 10</span><span class="sxs-lookup"><span data-stu-id="adc10-137">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
