---
description: Ruft Informationen zu einer angegebenen Bilddatei ab.
ms.assetid: 2e9d7073-4136-4fb7-8749-810aee000433
title: D3DXGetImageInfoFromFile-Funktion (D3dx9tex. h)
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
ms.openlocfilehash: ff5d540871482b2628fd48deb382121591a9594f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361205"
---
# <a name="d3dxgetimageinfofromfile-function"></a><span data-ttu-id="8a0d6-103">D3DXGetImageInfoFromFile-Funktion</span><span class="sxs-lookup"><span data-stu-id="8a0d6-103">D3DXGetImageInfoFromFile function</span></span>

<span data-ttu-id="8a0d6-104">Ruft Informationen zu einer angegebenen Bilddatei ab.</span><span class="sxs-lookup"><span data-stu-id="8a0d6-104">Retrieves information about a given image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a0d6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a0d6-105">Syntax</span></span>


```C++
HRESULT D3DXGetImageInfoFromFile(
  _In_ LPCSTR         pSrcFile,
  _In_ D3DXIMAGE_INFO *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="8a0d6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a0d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a0d6-107">*psrcfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a0d6-107">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a0d6-108">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8a0d6-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8a0d6-109">Dateiname des Bilds, über das Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8a0d6-109">File name of image to retrieve information about.</span></span> <span data-ttu-id="8a0d6-110">Wenn Unicode oder \_ Unicode definiert ist, ist dieser Parametertyp LPCWSTR; andernfalls lautet der Typ LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="8a0d6-110">If UNICODE or \_UNICODE are defined, this parameter type is LPCWSTR, otherwise, the type is LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="8a0d6-111">*psrcinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a0d6-111">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a0d6-112">Type: **[ **D3DXIMAGE \_ Info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="8a0d6-112">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="8a0d6-113">Zeiger auf eine [**D3DXIMAGE \_ Info**](d3dximage-info.md) -Struktur, die mit der Beschreibung der Daten in der Quelldatei aufgefüllt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8a0d6-113">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with the description of the data in the source file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a0d6-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8a0d6-114">Return value</span></span>

<span data-ttu-id="8a0d6-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8a0d6-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8a0d6-116">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8a0d6-116">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8a0d6-117">Wenn die Funktion fehlschlägt, kann der Rückgabewert wie folgt lauten: D3DERR \_ invalidcall</span><span class="sxs-lookup"><span data-stu-id="8a0d6-117">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="8a0d6-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8a0d6-118">Remarks</span></span>

<span data-ttu-id="8a0d6-119">Diese Funktion unterstützt sowohl Unicode-als auch ANSI-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="8a0d6-119">This function supports both Unicode and ANSI strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a0d6-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8a0d6-120">Requirements</span></span>



| <span data-ttu-id="8a0d6-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8a0d6-121">Requirement</span></span> | <span data-ttu-id="8a0d6-122">Wert</span><span class="sxs-lookup"><span data-stu-id="8a0d6-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8a0d6-123">Header</span><span class="sxs-lookup"><span data-stu-id="8a0d6-123">Header</span></span><br/>  | <dl> <span data-ttu-id="8a0d6-124"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a0d6-124"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="8a0d6-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8a0d6-125">Library</span></span><br/> | <dl> <span data-ttu-id="8a0d6-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a0d6-126"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="8a0d6-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a0d6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a0d6-128">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="8a0d6-128">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="8a0d6-129">**D3DXGetImageInfoFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="8a0d6-129">**D3DXGetImageInfoFromFileInMemory**</span></span>](d3dxgetimageinfofromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="8a0d6-130">**D3DXGetImageInfoFromResource**</span><span class="sxs-lookup"><span data-stu-id="8a0d6-130">**D3DXGetImageInfoFromResource**</span></span>](d3dxgetimageinfofromresource.md)
</dt> </dl>

 

 
