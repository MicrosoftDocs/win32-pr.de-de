---
description: 'D3DX10_IMAGE_INFO struktur: Gibt eine Beschreibung des ursprünglichen Inhalts einer Bilddatei zurück.'
ms.assetid: 40d89166-cc11-490d-867c-ae5db23a0784
title: D3DX10_IMAGE_INFO -Struktur (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_IMAGE_INFO
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 228ddf777217e9e61369b0a7fc3b3eb1ca012b1d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105478"
---
# <a name="d3dx10_image_info-structure"></a><span data-ttu-id="12839-103">D3DX10 \_ IMAGE \_ INFO-Struktur</span><span class="sxs-lookup"><span data-stu-id="12839-103">D3DX10\_IMAGE\_INFO structure</span></span>

<span data-ttu-id="12839-104">Gibt eine Beschreibung des ursprünglichen Inhalts einer Bilddatei zurück.</span><span class="sxs-lookup"><span data-stu-id="12839-104">Returns a description of the original contents of an image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="12839-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="12839-105">Syntax</span></span>


```C++
typedef struct D3DX10_IMAGE_INFO {
  UINT                     Width;
  UINT                     Height;
  UINT                     Depth;
  UINT                     ArraySize;
  UINT                     MipLevels;
  UINT                     MiscFlags;
  DXGI_FORMAT              Format;
  D3D10_RESOURCE_DIMENSION ResourceDimension;
  D3DX10_IMAGE_FILE_FORMAT ImageFileFormat;
} D3DX10_IMAGE_INFO, *LPD3DX10_IMAGE_INFO;
```



## <a name="members"></a><span data-ttu-id="12839-106">Member</span><span class="sxs-lookup"><span data-stu-id="12839-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="12839-107">**Width**</span><span class="sxs-lookup"><span data-stu-id="12839-107">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="12839-108">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="12839-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="12839-109">Breite des ursprünglichen Bilds in Pixel.</span><span class="sxs-lookup"><span data-stu-id="12839-109">Width of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="12839-110">**Height**</span><span class="sxs-lookup"><span data-stu-id="12839-110">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="12839-111">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="12839-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="12839-112">Höhe des ursprünglichen Bilds in Pixel.</span><span class="sxs-lookup"><span data-stu-id="12839-112">Height of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="12839-113">**Tiefe**</span><span class="sxs-lookup"><span data-stu-id="12839-113">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="12839-114">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="12839-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="12839-115">Tiefe des ursprünglichen Bilds in Pixel.</span><span class="sxs-lookup"><span data-stu-id="12839-115">Depth of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="12839-116">**ArraySize**</span><span class="sxs-lookup"><span data-stu-id="12839-116">**ArraySize**</span></span>
</dt> <dd>

<span data-ttu-id="12839-117">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="12839-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="12839-118">Größe des Texturarrays.</span><span class="sxs-lookup"><span data-stu-id="12839-118">Size of the texture array.</span></span> <span data-ttu-id="12839-119">*ArraySize ist* für ein einzelnes Bild 1.</span><span class="sxs-lookup"><span data-stu-id="12839-119">*ArraySize* will be 1 for a single image.</span></span>

</dd> <dt>

<span data-ttu-id="12839-120">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="12839-120">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="12839-121">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="12839-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="12839-122">Anzahl der Mipmapebenen im originalen Bild.</span><span class="sxs-lookup"><span data-stu-id="12839-122">Number of mipmap levels in original image.</span></span>

</dd> <dt>

<span data-ttu-id="12839-123">**MiscFlags**</span><span class="sxs-lookup"><span data-stu-id="12839-123">**MiscFlags**</span></span>
</dt> <dd>

<span data-ttu-id="12839-124">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="12839-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="12839-125">Verschiedene Ressourceneigenschaften (siehe [**D3D10 \_ RESOURCE \_ MISC \_ FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).</span><span class="sxs-lookup"><span data-stu-id="12839-125">Miscellaneous resource properties (see [**D3D10\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).</span></span>

</dd> <dt>

<span data-ttu-id="12839-126">**Format**</span><span class="sxs-lookup"><span data-stu-id="12839-126">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="12839-127">Typ: **[ **DXGI \_ FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="12839-127">Type: **[**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

</dd> <dd>

<span data-ttu-id="12839-128">Ein Wert aus dem enumerierten [**DXGI \_ FORMAT-Typ,**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) der die Daten im ursprünglichen Bild am genauesten beschreibt.</span><span class="sxs-lookup"><span data-stu-id="12839-128">A value from the [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) enumerated type that most closely describes the data in the original image.</span></span>

</dd> <dt>

<span data-ttu-id="12839-129">**ResourceDimension**</span><span class="sxs-lookup"><span data-stu-id="12839-129">**ResourceDimension**</span></span>
</dt> <dd>

<span data-ttu-id="12839-130">Typ: **[ **D3D10 \_ RESOURCE \_ DIMENSION**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)**</span><span class="sxs-lookup"><span data-stu-id="12839-130">Type: **[**D3D10\_RESOURCE\_DIMENSION**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)**</span></span>

</dd> <dd>

<span data-ttu-id="12839-131">Stellt den Typ der in der Datei gespeicherten Textur dar.</span><span class="sxs-lookup"><span data-stu-id="12839-131">Represents the type of the texture stored in the file.</span></span> <span data-ttu-id="12839-132">Weitere Informationen finden Sie unter [**D3D10 \_ RESOURCE \_ DIMENSION**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension).</span><span class="sxs-lookup"><span data-stu-id="12839-132">See [**D3D10\_RESOURCE\_DIMENSION**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension).</span></span>

</dd> <dt>

<span data-ttu-id="12839-133">**ImageFileFormat**</span><span class="sxs-lookup"><span data-stu-id="12839-133">**ImageFileFormat**</span></span>
</dt> <dd>

<span data-ttu-id="12839-134">Typ: **[ **D3DX10 \_ IMAGE \_ FILE \_ FORMAT**](d3dx10-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="12839-134">Type: **[**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md)**</span></span>

</dd> <dd>

<span data-ttu-id="12839-135">Stellt das Format der Bilddatei dar.</span><span class="sxs-lookup"><span data-stu-id="12839-135">Represents the format of the image file.</span></span> <span data-ttu-id="12839-136">Weitere Informationen finden Sie unter [**D3DX10 \_ IMAGE \_ FILE \_ FORMAT**](d3dx10-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="12839-136">See [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="12839-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="12839-137">Requirements</span></span>



| <span data-ttu-id="12839-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="12839-138">Requirement</span></span> | <span data-ttu-id="12839-139">Wert</span><span class="sxs-lookup"><span data-stu-id="12839-139">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="12839-140">Header</span><span class="sxs-lookup"><span data-stu-id="12839-140">Header</span></span><br/> | <dl> <span data-ttu-id="12839-141"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="12839-141"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12839-142">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="12839-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12839-143">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="12839-143">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
