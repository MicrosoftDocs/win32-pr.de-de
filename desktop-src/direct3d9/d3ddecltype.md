---
description: Definiert einen Scheitelpunkt Deklarations Datentyp.
ms.assetid: 993fc7e4-4752-4bce-82d0-0a034fdc69c0
title: D3DDECLTYPE-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3edb3f936772a7265c627f10eeb7aeb4f461701e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354377"
---
# <a name="d3ddecltype-enumeration"></a><span data-ttu-id="1db78-103">D3DDECLTYPE-Enumeration</span><span class="sxs-lookup"><span data-stu-id="1db78-103">D3DDECLTYPE enumeration</span></span>

<span data-ttu-id="1db78-104">Definiert einen Scheitelpunkt Deklarations Datentyp.</span><span class="sxs-lookup"><span data-stu-id="1db78-104">Defines a vertex declaration data type.</span></span>

## <a name="syntax"></a><span data-ttu-id="1db78-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1db78-105">Syntax</span></span>


```C++
typedef enum D3DDECLTYPE { 
  D3DDECLTYPE_FLOAT1     = 0,
  D3DDECLTYPE_FLOAT2     = 1,
  D3DDECLTYPE_FLOAT3     = 2,
  D3DDECLTYPE_FLOAT4     = 3,
  D3DDECLTYPE_D3DCOLOR   = 4,
  D3DDECLTYPE_UBYTE4     = 5,
  D3DDECLTYPE_SHORT2     = 6,
  D3DDECLTYPE_SHORT4     = 7,
  D3DDECLTYPE_UBYTE4N    = 8,
  D3DDECLTYPE_SHORT2N    = 9,
  D3DDECLTYPE_SHORT4N    = 10,
  D3DDECLTYPE_USHORT2N   = 11,
  D3DDECLTYPE_USHORT4N   = 12,
  D3DDECLTYPE_UDEC3      = 13,
  D3DDECLTYPE_DEC3N      = 14,
  D3DDECLTYPE_FLOAT16_2  = 15,
  D3DDECLTYPE_FLOAT16_4  = 16,
  D3DDECLTYPE_UNUSED     = 17
} D3DDECLTYPE, *LPD3DDECLTYPE;
```



## <a name="constants"></a><span data-ttu-id="1db78-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="1db78-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1db78-107"><span id="D3DDECLTYPE_FLOAT1"></span><span id="d3ddecltype_float1"></span>**D3DDECLTYPE \_ FLOAT1**</span><span class="sxs-lookup"><span data-stu-id="1db78-107"><span id="D3DDECLTYPE_FLOAT1"></span><span id="d3ddecltype_float1"></span>**D3DDECLTYPE\_FLOAT1**</span></span>
</dt> <dd>

<span data-ttu-id="1db78-108">Der float-Wert einer Komponente wurde auf (float, 0, 0, 1) erweitert.</span><span class="sxs-lookup"><span data-stu-id="1db78-108">One-component float expanded to (float, 0, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="1db78-109"><span id="D3DDECLTYPE_FLOAT2"></span><span id="d3ddecltype_float2"></span>**D3DDECLTYPE \_ FLOAT2**</span><span class="sxs-lookup"><span data-stu-id="1db78-109"><span id="D3DDECLTYPE_FLOAT2"></span><span id="d3ddecltype_float2"></span>**D3DDECLTYPE\_FLOAT2**</span></span>
</dt> <dd>

<span data-ttu-id="1db78-110">Der float-Wert für zwei Komponenten wurde auf (float, float, 0, 1) erweitert.</span><span class="sxs-lookup"><span data-stu-id="1db78-110">Two-component float expanded to (float, float, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="1db78-111"><span id="D3DDECLTYPE_FLOAT3"></span><span id="d3ddecltype_float3"></span>**D3DDECLTYPE \_ FLOAT3**</span><span class="sxs-lookup"><span data-stu-id="1db78-111"><span id="D3DDECLTYPE_FLOAT3"></span><span id="d3ddecltype_float3"></span>**D3DDECLTYPE\_FLOAT3**</span></span>
</dt> <dd>

<span data-ttu-id="1db78-112">Der float-Wert von drei Komponenten wurde auf (float, float, float, 1) erweitert.</span><span class="sxs-lookup"><span data-stu-id="1db78-112">Three-component float expanded to (float, float, float, 1).</span></span>

</dd> <dt>

<span data-ttu-id="1db78-113"><span id="D3DDECLTYPE_FLOAT4"></span><span id="d3ddecltype_float4"></span>**D3DDECLTYPE \_ float4**</span><span class="sxs-lookup"><span data-stu-id="1db78-113"><span id="D3DDECLTYPE_FLOAT4"></span><span id="d3ddecltype_float4"></span>**D3DDECLTYPE\_FLOAT4**</span></span>
</dt> <dd>

<span data-ttu-id="1db78-114">Der float-Wert von vier Komponenten wurde auf (float, float, float, float) erweitert.</span><span class="sxs-lookup"><span data-stu-id="1db78-114">Four-component float expanded to (float, float, float, float).</span></span>

</dd> <dt>

<span data-ttu-id="1db78-115"><span id="D3DDECLTYPE_D3DCOLOR"></span><span id="d3ddecltype_d3dcolor"></span>**D3DDECLTYPE \_ D3DCOLOR**</span><span class="sxs-lookup"><span data-stu-id="1db78-115"><span id="D3DDECLTYPE_D3DCOLOR"></span><span id="d3ddecltype_d3dcolor"></span>**D3DDECLTYPE\_D3DCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="1db78-116">Vier Komponenten, gepackte, nicht signierte bytes, die 0 bis 1 Bereich zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1db78-116">Four-component, packed, unsigned bytes mapped to 0 to 1 range.</span></span> <span data-ttu-id="1db78-117">Input ist ein [**D3DCOLOR**](d3dcolor.md) -Wert, der auf RGBA-Reihenfolge erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="1db78-117">Input is a [**D3DCOLOR**](d3dcolor.md) and is expanded to RGBA order.</span></span>

</dd> <dt>

<span data-ttu-id="1db78-118"><span id="D3DDECLTYPE_UBYTE4"></span><span id="d3ddecltype_ubyte4"></span>**D3DDECLTYPE \_ UBYTE4**</span><span class="sxs-lookup"><span data-stu-id="1db78-118"><span id="D3DDECLTYPE_UBYTE4"></span><span id="d3ddecltype_ubyte4"></span>**D3DDECLTYPE\_UBYTE4**</span></span>
</dt> <dd>

<span data-ttu-id="1db78-119">Ein Byte mit vier Komponenten, ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="1db78-119">Four-component, unsigned byte.</span></span>

</dd> <dt>

<span data-ttu-id="1db78-120"><span id="D3DDECLTYPE_SHORT2"></span><span id="d3ddecltype_short2"></span>**D3DDECLTYPE \_ SHORT2**</span><span class="sxs-lookup"><span data-stu-id="1db78-120"><span id="D3DDECLTYPE_SHORT2"></span><span id="d3ddecltype_short2"></span>**D3DDECLTYPE\_SHORT2**</span></span>
</dt> <dd>

<span data-ttu-id="1db78-121">Two-Component, signed Short erweitert auf (Wert, Wert, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="1db78-121">Two-component, signed short expanded to (value, value, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="1db78-122"><span id="D3DDECLTYPE_SHORT4"></span><span id="d3ddecltype_short4"></span>**D3DDECLTYPE \_ SHORT4**</span><span class="sxs-lookup"><span data-stu-id="1db78-122"><span id="D3DDECLTYPE_SHORT4"></span><span id="d3ddecltype_short4"></span>**D3DDECLTYPE\_SHORT4**</span></span>
</dt> <dd>

<span data-ttu-id="1db78-123">4-Component, signed Short erweitert auf (Wert, Wert, Wert, Wert).</span><span class="sxs-lookup"><span data-stu-id="1db78-123">Four-component, signed short expanded to (value, value, value, value).</span></span>

</dd> <dt>

<span data-ttu-id="1db78-124"><span id="D3DDECLTYPE_UBYTE4N"></span><span id="d3ddecltype_ubyte4n"></span>**D3DDECLTYPE \_ UBYTE4N**</span><span class="sxs-lookup"><span data-stu-id="1db78-124"><span id="D3DDECLTYPE_UBYTE4N"></span><span id="d3ddecltype_ubyte4n"></span>**D3DDECLTYPE\_UBYTE4N**</span></span>
</dt> <dd>

<span data-ttu-id="1db78-125">Ein 4-Byte-Byte, bei dem jedes Byte durch Dividieren durch 255.0 f normalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="1db78-125">Four-component byte with each byte normalized by dividing with 255.0f.</span></span>

</dd> <dt>

<span data-ttu-id="1db78-126"><span id="D3DDECLTYPE_SHORT2N"></span><span id="d3ddecltype_short2n"></span>**D3DDECLTYPE \_ SHORT2N**</span><span class="sxs-lookup"><span data-stu-id="1db78-126"><span id="D3DDECLTYPE_SHORT2N"></span><span id="d3ddecltype_short2n"></span>**D3DDECLTYPE\_SHORT2N**</span></span>
</dt> <dd>

<span data-ttu-id="1db78-127">Normalized, Two-Component, signed Short, erweitert auf (First Short/32767.0, Second Short/32767.0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="1db78-127">Normalized, two-component, signed short, expanded to (first short/32767.0, second short/32767.0, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="1db78-128"><span id="D3DDECLTYPE_SHORT4N"></span><span id="d3ddecltype_short4n"></span>**D3DDECLTYPE \_ SHORT4N**</span><span class="sxs-lookup"><span data-stu-id="1db78-128"><span id="D3DDECLTYPE_SHORT4N"></span><span id="d3ddecltype_short4n"></span>**D3DDECLTYPE\_SHORT4N**</span></span>
</dt> <dd>

<span data-ttu-id="1db78-129">Normalized, 4-Component, signed Short, erweitert auf (First Short/32767.0, Second Short/32767.0, dritte Short/32767.0, Fourth Short/32767.0).</span><span class="sxs-lookup"><span data-stu-id="1db78-129">Normalized, four-component, signed short, expanded to (first short/32767.0, second short/32767.0, third short/32767.0, fourth short/32767.0).</span></span>

</dd> <dt>

<span data-ttu-id="1db78-130"><span id="D3DDECLTYPE_USHORT2N"></span><span id="d3ddecltype_ushort2n"></span>**D3DDECLTYPE \_ USHORT2N**</span><span class="sxs-lookup"><span data-stu-id="1db78-130"><span id="D3DDECLTYPE_USHORT2N"></span><span id="d3ddecltype_ushort2n"></span>**D3DDECLTYPE\_USHORT2N**</span></span>
</dt> <dd>

<span data-ttu-id="1db78-131">Normalized, Two-Component, Ganzzahl ohne Vorzeichen Short, erweitert auf (First Short/65535.0, Short Short/65535.0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="1db78-131">Normalized, two-component, unsigned short, expanded to (first short/65535.0, short short/65535.0, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="1db78-132"><span id="D3DDECLTYPE_USHORT4N"></span><span id="d3ddecltype_ushort4n"></span>**D3DDECLTYPE \_ USHORT4N**</span><span class="sxs-lookup"><span data-stu-id="1db78-132"><span id="D3DDECLTYPE_USHORT4N"></span><span id="d3ddecltype_ushort4n"></span>**D3DDECLTYPE\_USHORT4N**</span></span>
</dt> <dd>

<span data-ttu-id="1db78-133">Normalized, 4-Component, Ganzzahl ohne Vorzeichen Short, erweitert auf (First Short/65535.0, Second Short/65535.0, dritte Short/65535.0, Fourth Short/65535.0).</span><span class="sxs-lookup"><span data-stu-id="1db78-133">Normalized, four-component, unsigned short, expanded to (first short/65535.0, second short/65535.0, third short/65535.0, fourth short/65535.0).</span></span>

</dd> <dt>

<span data-ttu-id="1db78-134"><span id="D3DDECLTYPE_UDEC3"></span><span id="d3ddecltype_udec3"></span>**D3DDECLTYPE \_ UDEC3**</span><span class="sxs-lookup"><span data-stu-id="1db78-134"><span id="D3DDECLTYPE_UDEC3"></span><span id="d3ddecltype_udec3"></span>**D3DDECLTYPE\_UDEC3**</span></span>
</dt> <dd>

<span data-ttu-id="1db78-135">Drei Komponenten, nicht signiertes, 10 10 10-Format, erweitert auf (Wert, Wert, Wert, 1).</span><span class="sxs-lookup"><span data-stu-id="1db78-135">Three-component, unsigned, 10 10 10 format expanded to (value, value, value, 1).</span></span>

</dd> <dt>

<span data-ttu-id="1db78-136"><span id="D3DDECLTYPE_DEC3N"></span><span id="d3ddecltype_dec3n"></span>**D3DDECLTYPE \_ DEC3N**</span><span class="sxs-lookup"><span data-stu-id="1db78-136"><span id="D3DDECLTYPE_DEC3N"></span><span id="d3ddecltype_dec3n"></span>**D3DDECLTYPE\_DEC3N**</span></span>
</dt> <dd>

<span data-ttu-id="1db78-137">Drei Komponenten, signiert, 10 10 10-Format normalisiert und erweitert auf (v \[ 0 \] /511,0, v \[ 1 \] /511,0, v \[ 2 \] /511,0, 1).</span><span class="sxs-lookup"><span data-stu-id="1db78-137">Three-component, signed, 10 10 10 format normalized and expanded to (v\[0\]/511.0, v\[1\]/511.0, v\[2\]/511.0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="1db78-138"><span id="D3DDECLTYPE_FLOAT16_2"></span><span id="d3ddecltype_float16_2"></span>**D3DDECLTYPE \_ FLOAT16 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="1db78-138"><span id="D3DDECLTYPE_FLOAT16_2"></span><span id="d3ddecltype_float16_2"></span>**D3DDECLTYPE\_FLOAT16\_2**</span></span>
</dt> <dd>

<span data-ttu-id="1db78-139">Zwei-Komponenten-16-Bit-Gleit Komma, erweitert auf (Wert, Wert, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="1db78-139">Two-component, 16-bit, floating point expanded to (value, value, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="1db78-140"><span id="D3DDECLTYPE_FLOAT16_4"></span><span id="d3ddecltype_float16_4"></span>**D3DDECLTYPE \_ FLOAT16 \_ 4**</span><span class="sxs-lookup"><span data-stu-id="1db78-140"><span id="D3DDECLTYPE_FLOAT16_4"></span><span id="d3ddecltype_float16_4"></span>**D3DDECLTYPE\_FLOAT16\_4**</span></span>
</dt> <dd>

<span data-ttu-id="1db78-141">Vier-Komponenten, 16-Bit-Gleit Komma, erweitert auf (Wert, Wert, Wert, Wert).</span><span class="sxs-lookup"><span data-stu-id="1db78-141">Four-component, 16-bit, floating point expanded to (value, value, value, value).</span></span>

</dd> <dt>

<span data-ttu-id="1db78-142"><span id="D3DDECLTYPE_UNUSED"></span><span id="d3ddecltype_unused"></span>**D3DDECLTYPE nicht \_ verwendet**</span><span class="sxs-lookup"><span data-stu-id="1db78-142"><span id="D3DDECLTYPE_UNUSED"></span><span id="d3ddecltype_unused"></span>**D3DDECLTYPE\_UNUSED**</span></span>
</dt> <dd>

<span data-ttu-id="1db78-143">Das typanfeld in der Deklaration wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1db78-143">Type field in the declaration is unused.</span></span> <span data-ttu-id="1db78-144">Dies ist für die Verwendung mit D3DDECLMETHOD \_ UV und D3DDECLMETHOD \_ lookuppresampling vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="1db78-144">This is designed for use with D3DDECLMETHOD\_UV and D3DDECLMETHOD\_LOOKUPPRESAMPLED.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1db78-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1db78-145">Remarks</span></span>

<span data-ttu-id="1db78-146">Vertex-Daten werden mit einem Array von [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) -Strukturen deklariert.</span><span class="sxs-lookup"><span data-stu-id="1db78-146">Vertex data is declared with an array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) structures.</span></span> <span data-ttu-id="1db78-147">Jedes Element im Array enthält einen Scheitelpunkt Deklarations Datentyp.</span><span class="sxs-lookup"><span data-stu-id="1db78-147">Each element in the array contains a vertex declaration data type.</span></span>

<span data-ttu-id="1db78-148">Verwenden Sie das DirectX Caps Viewer-Tool (DXCapsViewer.exe), um zu sehen, welche Typen auf Ihrem Gerät unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="1db78-148">Use the DirectX Caps Viewer Tool (DXCapsViewer.exe) to see which types are supported on your device.</span></span> <span data-ttu-id="1db78-149">Sie können dieses Tool aus dem DirectX SDK erhalten.</span><span class="sxs-lookup"><span data-stu-id="1db78-149">You can get this tool and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="1db78-150">Weitere Informationen zum DirectX SDK finden Sie unter [wo ist das DirectX SDK?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="1db78-150">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1db78-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1db78-151">Requirements</span></span>



| <span data-ttu-id="1db78-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1db78-152">Requirement</span></span> | <span data-ttu-id="1db78-153">Wert</span><span class="sxs-lookup"><span data-stu-id="1db78-153">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1db78-154">Header</span><span class="sxs-lookup"><span data-stu-id="1db78-154">Header</span></span><br/> | <dl> <span data-ttu-id="1db78-155"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="1db78-155"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1db78-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1db78-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1db78-157">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="1db78-157">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="1db78-158">**D3DDECLMETHOD**</span><span class="sxs-lookup"><span data-stu-id="1db78-158">**D3DDECLMETHOD**</span></span>](./d3ddeclmethod.md)
</dt> </dl>

 

 
