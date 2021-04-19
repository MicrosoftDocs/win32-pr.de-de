---
description: Ruft Informationen zu einer angegebenen Bilddatei ab.
ms.assetid: 59bdce45-82d9-42da-b847-a29ca71919b5
title: D3DX10GetImageInfoFromFile-Funktion (D3DX10Tex. h)
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
ms.openlocfilehash: 836d2e18b5c1c48bbe64d0026e97f8ebc5a066ba
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370395"
---
# <a name="d3dx10getimageinfofromfile-function"></a><span data-ttu-id="2c2d2-103">D3DX10GetImageInfoFromFile-Funktion</span><span class="sxs-lookup"><span data-stu-id="2c2d2-103">D3DX10GetImageInfoFromFile function</span></span>

<span data-ttu-id="2c2d2-104">Ruft Informationen zu einer angegebenen Bilddatei ab.</span><span class="sxs-lookup"><span data-stu-id="2c2d2-104">Retrieves information about a given image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c2d2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c2d2-105">Syntax</span></span>


```C++
HRESULT D3DX10GetImageInfoFromFile(
  _In_  LPCTSTR           pSrcFile,
  _In_  ID3DX10ThreadPump *pPump,
  _In_  D3DX10_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="2c2d2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c2d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c2d2-107">*psrcfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c2d2-107">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c2d2-108">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2c2d2-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2c2d2-109">Dateiname des Bilds, über das Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2c2d2-109">File name of image to retrieve information about.</span></span> <span data-ttu-id="2c2d2-110">Wenn Unicode oder \_ Unicode definiert ist, ist dieser Parametertyp LPCWSTR; andernfalls lautet der Typ LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="2c2d2-110">If UNICODE or \_UNICODE are defined, this parameter type is LPCWSTR, otherwise, the type is LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="2c2d2-111">*ppump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c2d2-111">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c2d2-112">Typ: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="2c2d2-112">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="2c2d2-113">Optionales threadpump, das verwendet werden kann, um die Informationen asynchron zu laden.</span><span class="sxs-lookup"><span data-stu-id="2c2d2-113">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="2c2d2-114">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="2c2d2-114">Can be **NULL**.</span></span> <span data-ttu-id="2c2d2-115">Siehe [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="2c2d2-115">See [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c2d2-116">*psrcinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c2d2-116">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c2d2-117">Type: **[ **d3dx10 \_ Image \_ Info**](d3dx10-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="2c2d2-117">Type: **[**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md)\***</span></span>

<span data-ttu-id="2c2d2-118">Zeiger auf eine d3dx10 \_ Image \_ Info-Struktur, die mit der Beschreibung der Daten in der Quelldatei aufgefüllt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2c2d2-118">Pointer to a D3DX10\_IMAGE\_INFO structure to be filled with the description of the data in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="2c2d2-119">*phresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2c2d2-119">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2c2d2-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="2c2d2-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="2c2d2-121">Ein Zeiger auf den Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="2c2d2-121">A pointer to the return value.</span></span> <span data-ttu-id="2c2d2-122">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="2c2d2-122">May be **NULL**.</span></span> <span data-ttu-id="2c2d2-123">Wenn *ppump* nicht **null** ist, muss *phresult* eine gültige Speicheradresse sein, bis die asynchrone Ausführung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="2c2d2-123">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c2d2-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2c2d2-124">Return value</span></span>

<span data-ttu-id="2c2d2-125">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2c2d2-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2c2d2-126">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2c2d2-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2c2d2-127">Wenn die Funktion fehlschlägt, kann der Rückgabewert wie folgt lauten: D3DERR \_ invalidcall</span><span class="sxs-lookup"><span data-stu-id="2c2d2-127">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="2c2d2-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2c2d2-128">Remarks</span></span>

<span data-ttu-id="2c2d2-129">Diese Funktion unterstützt sowohl Unicode-als auch ANSI-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="2c2d2-129">This function supports both Unicode and ANSI strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c2d2-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c2d2-130">Requirements</span></span>



| <span data-ttu-id="2c2d2-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c2d2-131">Requirement</span></span> | <span data-ttu-id="2c2d2-132">Wert</span><span class="sxs-lookup"><span data-stu-id="2c2d2-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c2d2-133">Header</span><span class="sxs-lookup"><span data-stu-id="2c2d2-133">Header</span></span><br/>  | <dl> <span data-ttu-id="2c2d2-134"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c2d2-134"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="2c2d2-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2c2d2-135">Library</span></span><br/> | <dl> <span data-ttu-id="2c2d2-136"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2c2d2-136"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2c2d2-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c2d2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c2d2-138">Textur Funktionen in D3DX 10</span><span class="sxs-lookup"><span data-stu-id="2c2d2-138">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
