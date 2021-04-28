---
description: 'D3DXGetImageInfoFromFile-Funktion: Ruft Informationen zu einer bestimmten Bilddatei ab.'
ms.assetid: 2e9d7073-4136-4fb7-8749-810aee000433
title: D3DXGetImageInfoFromFile-Funktion (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetImageInfoFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bb03b6482d140a3b78e43d8b99c60499ae6c8b16
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114493"
---
# <a name="d3dxgetimageinfofromfile-function"></a><span data-ttu-id="d8046-103">D3DXGetImageInfoFromFile-Funktion</span><span class="sxs-lookup"><span data-stu-id="d8046-103">D3DXGetImageInfoFromFile function</span></span>

<span data-ttu-id="d8046-104">Ruft Informationen zu einer bestimmten Bilddatei ab.</span><span class="sxs-lookup"><span data-stu-id="d8046-104">Retrieves information about a given image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8046-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8046-105">Syntax</span></span>


```C++
HRESULT D3DXGetImageInfoFromFile(
  _In_ LPCSTR         pSrcFile,
  _In_ D3DXIMAGE_INFO *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="d8046-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8046-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8046-107">*pSrcFile* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d8046-107">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8046-108">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d8046-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d8046-109">Dateiname des Bilds, zu dem Informationen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d8046-109">File name of image to retrieve information about.</span></span> <span data-ttu-id="d8046-110">Wenn UNICODE oder UNICODE definiert sind, ist dieser \_ Parametertyp LPCWSTR, andernfalls ist der Typ LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="d8046-110">If UNICODE or \_UNICODE are defined, this parameter type is LPCWSTR, otherwise, the type is LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="d8046-111">*pSrcInfo* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d8046-111">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8046-112">Typ: **[ **D3DXIMAGE \_ INFO**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="d8046-112">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="d8046-113">Zeiger auf eine [**D3DXIMAGE \_ INFO-Struktur,**](d3dximage-info.md) die mit der Beschreibung der Daten in der Quelldatei gefüllt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d8046-113">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with the description of the data in the source file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8046-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d8046-114">Return value</span></span>

<span data-ttu-id="d8046-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d8046-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d8046-116">Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d8046-116">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d8046-117">Wenn die Funktion fehlschlägt, kann der Rückgabewert wie folgt sein: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="d8046-117">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="d8046-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d8046-118">Remarks</span></span>

<span data-ttu-id="d8046-119">Diese Funktion unterstützt sowohl Unicode- als auch ANSI-Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="d8046-119">This function supports both Unicode and ANSI strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8046-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d8046-120">Requirements</span></span>



| <span data-ttu-id="d8046-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d8046-121">Requirement</span></span> | <span data-ttu-id="d8046-122">Wert</span><span class="sxs-lookup"><span data-stu-id="d8046-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d8046-123">Header</span><span class="sxs-lookup"><span data-stu-id="d8046-123">Header</span></span><br/>  | <dl> <span data-ttu-id="d8046-124"><dt>D3dx9tex.h</dt></span><span class="sxs-lookup"><span data-stu-id="d8046-124"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="d8046-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d8046-125">Library</span></span><br/> | <dl> <span data-ttu-id="d8046-126"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8046-126"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="d8046-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d8046-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8046-128">Texturfunktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="d8046-128">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="d8046-129">**D3DXGetImageInfoFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="d8046-129">**D3DXGetImageInfoFromFileInMemory**</span></span>](d3dxgetimageinfofromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="d8046-130">**D3DXGetImageInfoFromResource**</span><span class="sxs-lookup"><span data-stu-id="d8046-130">**D3DXGetImageInfoFromResource**</span></span>](d3dxgetimageinfofromresource.md)
</dt> </dl>

 

 
