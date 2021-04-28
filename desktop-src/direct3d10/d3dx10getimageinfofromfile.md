---
description: 'D3DX10GetImageInfoFromFile-Funktion: Ruft Informationen zu einer bestimmten Bilddatei ab.'
ms.assetid: 59bdce45-82d9-42da-b847-a29ca71919b5
title: D3DX10GetImageInfoFromFile-Funktion (D3DX10Tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetImageInfoFromFile
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3e11c4cb52176b0a144e164501f8c70d1e3678c1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098332"
---
# <a name="d3dx10getimageinfofromfile-function"></a><span data-ttu-id="e8326-103">D3DX10GetImageInfoFromFile-Funktion</span><span class="sxs-lookup"><span data-stu-id="e8326-103">D3DX10GetImageInfoFromFile function</span></span>

<span data-ttu-id="e8326-104">Ruft Informationen zu einer bestimmten Bilddatei ab.</span><span class="sxs-lookup"><span data-stu-id="e8326-104">Retrieves information about a given image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8326-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8326-105">Syntax</span></span>


```C++
HRESULT D3DX10GetImageInfoFromFile(
  _In_  LPCTSTR           pSrcFile,
  _In_  ID3DX10ThreadPump *pPump,
  _In_  D3DX10_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="e8326-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8326-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8326-107">*pSrcFile* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e8326-107">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8326-108">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e8326-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e8326-109">Dateiname des Bilds, zu dem Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e8326-109">File name of image to retrieve information about.</span></span> <span data-ttu-id="e8326-110">Wenn UNICODE oder \_ UNICODE definiert ist, ist dieser Parametertyp LPCWSTR, andernfalls LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="e8326-110">If UNICODE or \_UNICODE are defined, this parameter type is LPCWSTR, otherwise, the type is LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="e8326-111">*pPump* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e8326-111">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8326-112">Typ: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="e8326-112">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="e8326-113">Optionale Threadpumpe, die zum asynchronen Laden der Informationen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e8326-113">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="e8326-114">Kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="e8326-114">Can be **NULL**.</span></span> <span data-ttu-id="e8326-115">Siehe [**ID3DX10ThreadPump.**](id3dx10threadpump.md)</span><span class="sxs-lookup"><span data-stu-id="e8326-115">See [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="e8326-116">*pSrcInfo* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e8326-116">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8326-117">Typ: **[ **D3DX10 \_ IMAGE \_ INFO**](d3dx10-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="e8326-117">Type: **[**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md)\***</span></span>

<span data-ttu-id="e8326-118">Zeiger auf eine D3DX10 \_ IMAGE \_ INFO-Struktur, die mit der Beschreibung der Daten in der Quelldatei gefüllt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8326-118">Pointer to a D3DX10\_IMAGE\_INFO structure to be filled with the description of the data in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="e8326-119">*pHResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e8326-119">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8326-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="e8326-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="e8326-121">Ein Zeiger auf den Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="e8326-121">A pointer to the return value.</span></span> <span data-ttu-id="e8326-122">Kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="e8326-122">May be **NULL**.</span></span> <span data-ttu-id="e8326-123">Wenn *pPump* nicht **NULL ist,** muss *pHResult* ein gültiger Speicherort sein, bis die asynchrone Ausführung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="e8326-123">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8326-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e8326-124">Return value</span></span>

<span data-ttu-id="e8326-125">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e8326-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e8326-126">Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e8326-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e8326-127">Wenn die Funktion fehlschlägt, kann der Rückgabewert wie folgt sein: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="e8326-127">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="e8326-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e8326-128">Remarks</span></span>

<span data-ttu-id="e8326-129">Diese Funktion unterstützt sowohl Unicode- als auch ANSI-Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="e8326-129">This function supports both Unicode and ANSI strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8326-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8326-130">Requirements</span></span>



| <span data-ttu-id="e8326-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8326-131">Requirement</span></span> | <span data-ttu-id="e8326-132">Wert</span><span class="sxs-lookup"><span data-stu-id="e8326-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8326-133">Header</span><span class="sxs-lookup"><span data-stu-id="e8326-133">Header</span></span><br/>  | <dl> <span data-ttu-id="e8326-134"><dt>D3DX10Tex.h</dt></span><span class="sxs-lookup"><span data-stu-id="e8326-134"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="e8326-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e8326-135">Library</span></span><br/> | <dl> <span data-ttu-id="e8326-136"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e8326-136"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e8326-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e8326-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8326-138">Texturfunktionen in D3DX 10</span><span class="sxs-lookup"><span data-stu-id="e8326-138">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
