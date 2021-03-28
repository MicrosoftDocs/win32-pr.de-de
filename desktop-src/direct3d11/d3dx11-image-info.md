---
title: D3DX11_IMAGE_INFO-Struktur (D3DX11tex. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Stellen Sie optional Informationen für Textur Lade-APIs bereit, um zu steuern, wie Texturen geladen werden. | D3DX11_IMAGE_INFO-Struktur (D3DX11tex. h)
ms.assetid: 981f4f1d-7609-416a-8f92-c7223d8b2773
keywords:
- D3DX11_IMAGE_INFO Struktur Direct3D 11
- LPD3DX11_IMAGE_INFO Struktur Zeiger Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_IMAGE_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 927967f8e76d0147ccc264bcbdd773191a170ae7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982557"
---
# <a name="d3dx11_image_info-structure"></a><span data-ttu-id="2fdb8-107">Bibliothek d3dx11 \_ Image- \_ Informationsstruktur</span><span class="sxs-lookup"><span data-stu-id="2fdb8-107">D3DX11\_IMAGE\_INFO structure</span></span>

> [!Note]  
> <span data-ttu-id="2fdb8-108">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2fdb8-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="2fdb8-109">Stellen Sie optional Informationen für Textur Lade-APIs bereit, um zu steuern, wie Texturen geladen werden.</span><span class="sxs-lookup"><span data-stu-id="2fdb8-109">Optionally provide information to texture loader APIs to control how textures get loaded.</span></span> <span data-ttu-id="2fdb8-110">Der Wert Bibliothek d3dx11 \_ Default für einen dieser Parameter bewirkt, dass D3DX automatisch den Wert aus der Quelldatei verwendet.</span><span class="sxs-lookup"><span data-stu-id="2fdb8-110">A value of D3DX11\_DEFAULT for any of these parameters will cause D3DX to automatically use the value from the source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fdb8-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="2fdb8-111">Syntax</span></span>


```C++
typedef struct D3DX11_IMAGE_INFO {
  UINT                     Width;
  UINT                     Height;
  UINT                     Depth;
  UINT                     ArraySize;
  UINT                     MipLevels;
  UINT                     MiscFlags;
  DXGI_FORMAT              Format;
  D3D11_RESOURCE_DIMENSION ResourceDimension;
  D3DX11_IMAGE_FILE_FORMAT ImageFileFormat;
} D3DX11_IMAGE_INFO, *LPD3DX11_IMAGE_INFO;
```



## <a name="members"></a><span data-ttu-id="2fdb8-112">Member</span><span class="sxs-lookup"><span data-stu-id="2fdb8-112">Members</span></span>

<dl> <dt>

<span data-ttu-id="2fdb8-113">**Width**</span><span class="sxs-lookup"><span data-stu-id="2fdb8-113">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="2fdb8-114">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2fdb8-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="2fdb8-115">Die Ziel Breite der Textur.</span><span class="sxs-lookup"><span data-stu-id="2fdb8-115">The target width of the texture.</span></span> <span data-ttu-id="2fdb8-116">Wenn die tatsächliche Breite der Textur größer oder kleiner als dieser Wert ist, wird die Textur zentral hoch-oder herunterskaliert, um dieser Ziel Breite gerecht zu werden.</span><span class="sxs-lookup"><span data-stu-id="2fdb8-116">If the actual width of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target width.</span></span>

</dd> <dt>

<span data-ttu-id="2fdb8-117">**Height**</span><span class="sxs-lookup"><span data-stu-id="2fdb8-117">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="2fdb8-118">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2fdb8-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="2fdb8-119">Die Zielhöhe der Textur.</span><span class="sxs-lookup"><span data-stu-id="2fdb8-119">The target height of the texture.</span></span> <span data-ttu-id="2fdb8-120">Wenn die tatsächliche Höhe der Textur größer oder kleiner als dieser Wert ist, wird die Textur zentral hoch-oder herunterskaliert, um an diese Zielhöhe angepasst zu werden.</span><span class="sxs-lookup"><span data-stu-id="2fdb8-120">If the actual height of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target height.</span></span>

</dd> <dt>

<span data-ttu-id="2fdb8-121">**Tiefe**</span><span class="sxs-lookup"><span data-stu-id="2fdb8-121">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="2fdb8-122">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2fdb8-122">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="2fdb8-123">Die Tiefe der Textur.</span><span class="sxs-lookup"><span data-stu-id="2fdb8-123">The depth of the texture.</span></span> <span data-ttu-id="2fdb8-124">Dies gilt nur für Volumentexturen.</span><span class="sxs-lookup"><span data-stu-id="2fdb8-124">This only applies to volume textures.</span></span>

</dd> <dt>

<span data-ttu-id="2fdb8-125">**ArraySize**</span><span class="sxs-lookup"><span data-stu-id="2fdb8-125">**ArraySize**</span></span>
</dt> <dd>

<span data-ttu-id="2fdb8-126">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2fdb8-126">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="2fdb8-127">Die Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="2fdb8-127">The number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="2fdb8-128">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="2fdb8-128">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="2fdb8-129">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2fdb8-129">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="2fdb8-130">Die maximale Anzahl von MipMap-Ebenen in der Textur.</span><span class="sxs-lookup"><span data-stu-id="2fdb8-130">The maximum number of mipmap levels in the texture.</span></span> <span data-ttu-id="2fdb8-131">Weitere Informationen finden Sie in den Hinweisen unter [**D3D11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv).</span><span class="sxs-lookup"><span data-stu-id="2fdb8-131">See the remarks in [**D3D11\_TEX1D\_SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv).</span></span> <span data-ttu-id="2fdb8-132">Die Verwendung von 0 oder Bibliothek d3dx11 \_ default bewirkt, dass eine vollständige MipMap-Kette erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="2fdb8-132">Using 0 or D3DX11\_DEFAULT will cause a full mipmap chain to be created.</span></span>

</dd> <dt>

<span data-ttu-id="2fdb8-133">**Fehlflags**</span><span class="sxs-lookup"><span data-stu-id="2fdb8-133">**MiscFlags**</span></span>
</dt> <dd>

<span data-ttu-id="2fdb8-134">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2fdb8-134">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="2fdb8-135">Verschiedene Ressourcen Eigenschaften, die mit [**dem \_ Flag "D3D11 Resource \_ misc \_ Flag**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) " angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2fdb8-135">Miscellaneous resource properties specified with a [**D3D11\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) flag.</span></span>

</dd> <dt>

<span data-ttu-id="2fdb8-136">**Format**</span><span class="sxs-lookup"><span data-stu-id="2fdb8-136">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="2fdb8-137">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="2fdb8-137">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

</dd> <dd>

<span data-ttu-id="2fdb8-138">Eine [**DXGI- \_ formatenumeration**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) , die das Format angibt, in dem sich die Textur befindet, nachdem Sie geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="2fdb8-138">A [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) enumeration specifying the format the texture will be in after it is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="2fdb8-139">**Resourcedimension**</span><span class="sxs-lookup"><span data-stu-id="2fdb8-139">**ResourceDimension**</span></span>
</dt> <dd>

<span data-ttu-id="2fdb8-140">Type: **[ **D3D11- \_ Ressourcen \_ Dimension**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension)**</span><span class="sxs-lookup"><span data-stu-id="2fdb8-140">Type: **[**D3D11\_RESOURCE\_DIMENSION**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension)**</span></span>

</dd> <dd>

<span data-ttu-id="2fdb8-141">Ein [**D3D11- \_ Ressourcen \_ Dimensions**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension) Wert, der den Typ der Ressource identifiziert.</span><span class="sxs-lookup"><span data-stu-id="2fdb8-141">A [**D3D11\_RESOURCE\_DIMENSION**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension) value, which identifies the type of resource.</span></span>

</dd> <dt>

<span data-ttu-id="2fdb8-142">**Imagefileformat**</span><span class="sxs-lookup"><span data-stu-id="2fdb8-142">**ImageFileFormat**</span></span>
</dt> <dd>

<span data-ttu-id="2fdb8-143">Type: **[ **Bibliothek d3dx11 \_ Image \_ file \_ Format**](d3dx11-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="2fdb8-143">Type: **[**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2fdb8-144">Ein [**Bibliothek d3dx11 \_ Image \_ file \_ Format**](d3dx11-image-file-format.md) -Wert, der das Bildformat angibt.</span><span class="sxs-lookup"><span data-stu-id="2fdb8-144">A [**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md) value, which identifies the image format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2fdb8-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2fdb8-145">Remarks</span></span>

<span data-ttu-id="2fdb8-146">Diese Struktur wird von Methoden wie z. b. [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md)oder [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="2fdb8-146">This structure is used by methods such as: [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md), or [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2fdb8-147">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="2fdb8-147">Requirements</span></span>



| <span data-ttu-id="2fdb8-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2fdb8-148">Requirement</span></span> | <span data-ttu-id="2fdb8-149">Wert</span><span class="sxs-lookup"><span data-stu-id="2fdb8-149">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2fdb8-150">Header</span><span class="sxs-lookup"><span data-stu-id="2fdb8-150">Header</span></span><br/> | <dl> <span data-ttu-id="2fdb8-151"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fdb8-151"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fdb8-152">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2fdb8-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fdb8-153">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="2fdb8-153">D3DX Structures</span></span>](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

