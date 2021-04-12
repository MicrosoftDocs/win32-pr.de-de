---
description: Gibt eine Beschreibung des ursprünglichen Inhalts einer Bilddatei zurück.
ms.assetid: 40d89166-cc11-490d-867c-ae5db23a0784
title: D3DX10_IMAGE_INFO-Struktur (d3dx10. h)
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
ms.openlocfilehash: bf240296610c083e0d042d187ae29054461193a8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354437"
---
# <a name="d3dx10_image_info-structure"></a><span data-ttu-id="f24c3-103">D3dx10 \_ Image- \_ Informationsstruktur</span><span class="sxs-lookup"><span data-stu-id="f24c3-103">D3DX10\_IMAGE\_INFO structure</span></span>

<span data-ttu-id="f24c3-104">Gibt eine Beschreibung des ursprünglichen Inhalts einer Bilddatei zurück.</span><span class="sxs-lookup"><span data-stu-id="f24c3-104">Returns a description of the original contents of an image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="f24c3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f24c3-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="f24c3-106">Member</span><span class="sxs-lookup"><span data-stu-id="f24c3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f24c3-107">**Width**</span><span class="sxs-lookup"><span data-stu-id="f24c3-107">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="f24c3-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f24c3-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f24c3-109">Breite des ursprünglichen Bilds in Pixel.</span><span class="sxs-lookup"><span data-stu-id="f24c3-109">Width of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="f24c3-110">**Height**</span><span class="sxs-lookup"><span data-stu-id="f24c3-110">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="f24c3-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f24c3-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f24c3-112">Höhe des ursprünglichen Bilds in Pixel.</span><span class="sxs-lookup"><span data-stu-id="f24c3-112">Height of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="f24c3-113">**Tiefe**</span><span class="sxs-lookup"><span data-stu-id="f24c3-113">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="f24c3-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f24c3-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f24c3-115">Tiefe des ursprünglichen Bilds in Pixel.</span><span class="sxs-lookup"><span data-stu-id="f24c3-115">Depth of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="f24c3-116">**ArraySize**</span><span class="sxs-lookup"><span data-stu-id="f24c3-116">**ArraySize**</span></span>
</dt> <dd>

<span data-ttu-id="f24c3-117">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f24c3-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f24c3-118">Größe des Textur Arrays.</span><span class="sxs-lookup"><span data-stu-id="f24c3-118">Size of the texture array.</span></span> <span data-ttu-id="f24c3-119">*ArraySize* ist 1 für ein einzelnes Image.</span><span class="sxs-lookup"><span data-stu-id="f24c3-119">*ArraySize* will be 1 for a single image.</span></span>

</dd> <dt>

<span data-ttu-id="f24c3-120">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="f24c3-120">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="f24c3-121">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f24c3-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f24c3-122">Anzahl von MipMap-Ebenen im ursprünglichen Bild.</span><span class="sxs-lookup"><span data-stu-id="f24c3-122">Number of mipmap levels in original image.</span></span>

</dd> <dt>

<span data-ttu-id="f24c3-123">**Fehlflags**</span><span class="sxs-lookup"><span data-stu-id="f24c3-123">**MiscFlags**</span></span>
</dt> <dd>

<span data-ttu-id="f24c3-124">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f24c3-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f24c3-125">Verschiedene Ressourcen Eigenschaften (siehe [**d3d10 \_ Resource \_ misc- \_ Flag**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).</span><span class="sxs-lookup"><span data-stu-id="f24c3-125">Miscellaneous resource properties (see [**D3D10\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).</span></span>

</dd> <dt>

<span data-ttu-id="f24c3-126">**Format**</span><span class="sxs-lookup"><span data-stu-id="f24c3-126">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="f24c3-127">Typ: **[ **DXGI- \_ Format**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="f24c3-127">Type: **[**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

</dd> <dd>

<span data-ttu-id="f24c3-128">Ein Wert aus dem enumerierten [**DXGI- \_ Formattyp**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) , der die Daten im ursprünglichen Bild am ehesten beschreibt.</span><span class="sxs-lookup"><span data-stu-id="f24c3-128">A value from the [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) enumerated type that most closely describes the data in the original image.</span></span>

</dd> <dt>

<span data-ttu-id="f24c3-129">**Resourcedimension**</span><span class="sxs-lookup"><span data-stu-id="f24c3-129">**ResourceDimension**</span></span>
</dt> <dd>

<span data-ttu-id="f24c3-130">Type: **[ **d3d10- \_ Ressourcen \_ Dimension**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)**</span><span class="sxs-lookup"><span data-stu-id="f24c3-130">Type: **[**D3D10\_RESOURCE\_DIMENSION**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)**</span></span>

</dd> <dd>

<span data-ttu-id="f24c3-131">Stellt den Typ der Textur dar, die in der Datei gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="f24c3-131">Represents the type of the texture stored in the file.</span></span> <span data-ttu-id="f24c3-132">Siehe [**d3d10 \_ Resource- \_ Dimension**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension).</span><span class="sxs-lookup"><span data-stu-id="f24c3-132">See [**D3D10\_RESOURCE\_DIMENSION**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension).</span></span>

</dd> <dt>

<span data-ttu-id="f24c3-133">**Imagefileformat**</span><span class="sxs-lookup"><span data-stu-id="f24c3-133">**ImageFileFormat**</span></span>
</dt> <dd>

<span data-ttu-id="f24c3-134">Type: **[ **d3dx10 \_ Image \_ file \_ Format**](d3dx10-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="f24c3-134">Type: **[**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f24c3-135">Stellt das Format der Bilddatei dar.</span><span class="sxs-lookup"><span data-stu-id="f24c3-135">Represents the format of the image file.</span></span> <span data-ttu-id="f24c3-136">Siehe [**d3dx10 \_ Image \_ file \_ Format**](d3dx10-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="f24c3-136">See [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f24c3-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f24c3-137">Requirements</span></span>



| <span data-ttu-id="f24c3-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f24c3-138">Requirement</span></span> | <span data-ttu-id="f24c3-139">Wert</span><span class="sxs-lookup"><span data-stu-id="f24c3-139">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f24c3-140">Header</span><span class="sxs-lookup"><span data-stu-id="f24c3-140">Header</span></span><br/> | <dl> <span data-ttu-id="f24c3-141"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="f24c3-141"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f24c3-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f24c3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f24c3-143">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="f24c3-143">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
