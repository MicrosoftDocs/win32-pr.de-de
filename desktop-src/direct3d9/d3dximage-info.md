---
description: 'D3DXIMAGE_INFO-Struktur: Gibt eine Beschreibung des ursprünglichen Inhalts einer Bilddatei zurück.'
ms.assetid: d6cbd5b7-642e-43ce-a2ed-11a400c5bdc1
title: D3DXIMAGE_INFO-Struktur (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIMAGE_INFO
api_type:
- HeaderDef
api_location:
- d3dx9tex.h
ms.openlocfilehash: be70cc88645e0aac6734907c6a97f2d4bb104c99
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090538"
---
# <a name="d3dximage_info-structure"></a><span data-ttu-id="4e0ac-103">D3DXIMAGE \_ INFO-Struktur</span><span class="sxs-lookup"><span data-stu-id="4e0ac-103">D3DXIMAGE\_INFO structure</span></span>

<span data-ttu-id="4e0ac-104">Gibt eine Beschreibung des ursprünglichen Inhalts einer Bilddatei zurück.</span><span class="sxs-lookup"><span data-stu-id="4e0ac-104">Returns a description of the original contents of an image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e0ac-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e0ac-105">Syntax</span></span>


```C++
typedef struct D3DXIMAGE_INFO {
  UINT                 Width;
  UINT                 Height;
  UINT                 Depth;
  UINT                 MipLevels;
  D3DFORMAT            Format;
  D3DRESOURCETYPE      ResourceType;
  D3DXIMAGE_FILEFORMAT ImageFileFormat;
} D3DXIMAGE_INFO, *LPD3DXIMAGE_INFO;
```



## <a name="members"></a><span data-ttu-id="4e0ac-106">Member</span><span class="sxs-lookup"><span data-stu-id="4e0ac-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4e0ac-107">**Width**</span><span class="sxs-lookup"><span data-stu-id="4e0ac-107">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="4e0ac-108">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e0ac-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4e0ac-109">Breite des ursprünglichen Bilds in Pixel.</span><span class="sxs-lookup"><span data-stu-id="4e0ac-109">Width of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="4e0ac-110">**Height**</span><span class="sxs-lookup"><span data-stu-id="4e0ac-110">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="4e0ac-111">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e0ac-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4e0ac-112">Höhe des ursprünglichen Bilds in Pixel.</span><span class="sxs-lookup"><span data-stu-id="4e0ac-112">Height of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="4e0ac-113">**Tiefe**</span><span class="sxs-lookup"><span data-stu-id="4e0ac-113">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="4e0ac-114">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e0ac-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4e0ac-115">Tiefe des ursprünglichen Bilds in Pixel.</span><span class="sxs-lookup"><span data-stu-id="4e0ac-115">Depth of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="4e0ac-116">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="4e0ac-116">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="4e0ac-117">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e0ac-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4e0ac-118">Anzahl der MIP-Ebenen im ursprünglichen Bild.</span><span class="sxs-lookup"><span data-stu-id="4e0ac-118">Number of mip levels in original image.</span></span>

</dd> <dt>

<span data-ttu-id="4e0ac-119">**Format**</span><span class="sxs-lookup"><span data-stu-id="4e0ac-119">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="4e0ac-120">Typ: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="4e0ac-120">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4e0ac-121">Ein Wert aus dem [D3DFORMAT-Enumerationstyp,](d3dformat.md) der die Daten im ursprünglichen Bild am genauesten beschreibt.</span><span class="sxs-lookup"><span data-stu-id="4e0ac-121">A value from the [D3DFORMAT](d3dformat.md) enumerated type that most closely describes the data in the original image.</span></span>

</dd> <dt>

<span data-ttu-id="4e0ac-122">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="4e0ac-122">**ResourceType**</span></span>
</dt> <dd>

<span data-ttu-id="4e0ac-123">Typ: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**</span><span class="sxs-lookup"><span data-stu-id="4e0ac-123">Type: **[**D3DRESOURCETYPE**](./d3dresourcetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4e0ac-124">Stellt den Typ der in der Datei gespeicherten Textur dar.</span><span class="sxs-lookup"><span data-stu-id="4e0ac-124">Represents the type of the texture stored in the file.</span></span> <span data-ttu-id="4e0ac-125">Dabei handelt es sich entweder um D3DRTYPE \_ TEXTURE, D3DRTYPE \_ VOLUMETEXTURE oder D3DRTYPE \_ CubeTexture.</span><span class="sxs-lookup"><span data-stu-id="4e0ac-125">It is either D3DRTYPE\_TEXTURE, D3DRTYPE\_VOLUMETEXTURE, or D3DRTYPE\_CubeTexture.</span></span>

</dd> <dt>

<span data-ttu-id="4e0ac-126">**ImageFileFormat**</span><span class="sxs-lookup"><span data-stu-id="4e0ac-126">**ImageFileFormat**</span></span>
</dt> <dd>

<span data-ttu-id="4e0ac-127">Typ: **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="4e0ac-127">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4e0ac-128">Stellt das Format der Bilddatei dar.</span><span class="sxs-lookup"><span data-stu-id="4e0ac-128">Represents the format of the image file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4e0ac-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e0ac-129">Requirements</span></span>



| <span data-ttu-id="4e0ac-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e0ac-130">Requirement</span></span> | <span data-ttu-id="4e0ac-131">Wert</span><span class="sxs-lookup"><span data-stu-id="4e0ac-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4e0ac-132">Header</span><span class="sxs-lookup"><span data-stu-id="4e0ac-132">Header</span></span><br/> | <dl> <span data-ttu-id="4e0ac-133"><dt>D3dx9tex.h</dt></span><span class="sxs-lookup"><span data-stu-id="4e0ac-133"><dt>D3dx9tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e0ac-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4e0ac-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e0ac-135">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="4e0ac-135">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
