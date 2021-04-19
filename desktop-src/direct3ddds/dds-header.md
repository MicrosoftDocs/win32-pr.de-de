---
title: DDS_HEADER-Struktur (DDS. h)
description: Beschreibt einen DDS-Dateiheader.
ms.assetid: 7f8bde30-0ff9-4bb9-b444-5c875e6a0865
keywords:
- DDS_HEADER Struktur-DDS
topic_type:
- apiref
api_name:
- DDS_HEADER
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d70fa0c4b05b6655ce0329cc73651ea21d4d808
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355165"
---
# <a name="dds_header-structure"></a><span data-ttu-id="4b99a-104">DDS- \_ Header Struktur</span><span class="sxs-lookup"><span data-stu-id="4b99a-104">DDS\_HEADER structure</span></span>

<span data-ttu-id="4b99a-105">Beschreibt einen DDS-Dateiheader.</span><span class="sxs-lookup"><span data-stu-id="4b99a-105">Describes a DDS file header.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b99a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b99a-106">Syntax</span></span>


```C++
typedef struct {
  DWORD           dwSize;
  DWORD           dwFlags;
  DWORD           dwHeight;
  DWORD           dwWidth;
  DWORD           dwPitchOrLinearSize;
  DWORD           dwDepth;
  DWORD           dwMipMapCount;
  DWORD           dwReserved1[11];
  DDS_PIXELFORMAT ddspf;
  DWORD           dwCaps;
  DWORD           dwCaps2;
  DWORD           dwCaps3;
  DWORD           dwCaps4;
  DWORD           dwReserved2;
} DDS_HEADER;
```



## <a name="members"></a><span data-ttu-id="4b99a-107">Member</span><span class="sxs-lookup"><span data-stu-id="4b99a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="4b99a-108">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="4b99a-108">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="4b99a-109">Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4b99a-109">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4b99a-110">Größe der Struktur.</span><span class="sxs-lookup"><span data-stu-id="4b99a-110">Size of structure.</span></span> <span data-ttu-id="4b99a-111">Dieser Member muss auf 124 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4b99a-111">This member must be set to 124.</span></span>

</dd> <dt>

<span data-ttu-id="4b99a-112">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="4b99a-112">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="4b99a-113">Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4b99a-113">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4b99a-114">Flags, die angeben, welche Member gültige Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="4b99a-114">Flags to indicate which members contain valid data.</span></span>



| <span data-ttu-id="4b99a-115">Flag</span><span class="sxs-lookup"><span data-stu-id="4b99a-115">Flag</span></span>              | <span data-ttu-id="4b99a-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4b99a-116">Description</span></span>                                                  | <span data-ttu-id="4b99a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="4b99a-117">Value</span></span>    |
|-------------------|--------------------------------------------------------------|----------|
| <span data-ttu-id="4b99a-118">ddsd- \_ Caps</span><span class="sxs-lookup"><span data-stu-id="4b99a-118">DDSD\_CAPS</span></span>        | <span data-ttu-id="4b99a-119">In jeder DDS-Datei erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4b99a-119">Required in every .dds file.</span></span>                                 | <span data-ttu-id="4b99a-120">0x1</span><span class="sxs-lookup"><span data-stu-id="4b99a-120">0x1</span></span>      |
| <span data-ttu-id="4b99a-121">ddsd- \_ Höhe</span><span class="sxs-lookup"><span data-stu-id="4b99a-121">DDSD\_HEIGHT</span></span>      | <span data-ttu-id="4b99a-122">In jeder DDS-Datei erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4b99a-122">Required in every .dds file.</span></span>                                 | <span data-ttu-id="4b99a-123">0x2</span><span class="sxs-lookup"><span data-stu-id="4b99a-123">0x2</span></span>      |
| <span data-ttu-id="4b99a-124">ddsd- \_ Breite</span><span class="sxs-lookup"><span data-stu-id="4b99a-124">DDSD\_WIDTH</span></span>       | <span data-ttu-id="4b99a-125">In jeder DDS-Datei erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4b99a-125">Required in every .dds file.</span></span>                                 | <span data-ttu-id="4b99a-126">0x4</span><span class="sxs-lookup"><span data-stu-id="4b99a-126">0x4</span></span>      |
| <span data-ttu-id="4b99a-127">ddsd- \_ Tonhöhe</span><span class="sxs-lookup"><span data-stu-id="4b99a-127">DDSD\_PITCH</span></span>       | <span data-ttu-id="4b99a-128">Erforderlich, wenn für eine nicht komprimierte Textur eine Tonhöhe bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="4b99a-128">Required when pitch is provided for an uncompressed texture.</span></span> | <span data-ttu-id="4b99a-129">0x8</span><span class="sxs-lookup"><span data-stu-id="4b99a-129">0x8</span></span>      |
| <span data-ttu-id="4b99a-130">ddsd- \_ Pixel Format</span><span class="sxs-lookup"><span data-stu-id="4b99a-130">DDSD\_PIXELFORMAT</span></span> | <span data-ttu-id="4b99a-131">In jeder DDS-Datei erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4b99a-131">Required in every .dds file.</span></span>                                 | <span data-ttu-id="4b99a-132">0x1000</span><span class="sxs-lookup"><span data-stu-id="4b99a-132">0x1000</span></span>   |
| <span data-ttu-id="4b99a-133">ddsd \_ mipmapcount</span><span class="sxs-lookup"><span data-stu-id="4b99a-133">DDSD\_MIPMAPCOUNT</span></span> | <span data-ttu-id="4b99a-134">Erforderlich in einer Mipmapping-Textur.</span><span class="sxs-lookup"><span data-stu-id="4b99a-134">Required in a mipmapped texture.</span></span>                             | <span data-ttu-id="4b99a-135">0x20000</span><span class="sxs-lookup"><span data-stu-id="4b99a-135">0x20000</span></span>  |
| <span data-ttu-id="4b99a-136">ddsd \_ linearsize</span><span class="sxs-lookup"><span data-stu-id="4b99a-136">DDSD\_LINEARSIZE</span></span>  | <span data-ttu-id="4b99a-137">Erforderlich, wenn für eine komprimierte Textur eine Tonhöhe bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="4b99a-137">Required when pitch is provided for a compressed texture.</span></span>    | <span data-ttu-id="4b99a-138">0x80000</span><span class="sxs-lookup"><span data-stu-id="4b99a-138">0x80000</span></span>  |
| <span data-ttu-id="4b99a-139">ddsd- \_ Tiefe</span><span class="sxs-lookup"><span data-stu-id="4b99a-139">DDSD\_DEPTH</span></span>       | <span data-ttu-id="4b99a-140">In einer tiefen Textur erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4b99a-140">Required in a depth texture.</span></span>                                 | <span data-ttu-id="4b99a-141">0x800000</span><span class="sxs-lookup"><span data-stu-id="4b99a-141">0x800000</span></span> |



 

> [!Note]  
> <span data-ttu-id="4b99a-142">Wenn Sie DDS-Dateien schreiben, sollten Sie die ddsd \_ Caps-und ddsd- \_ Pixel Formatflags festlegen. für mipzugeordnete Texturen sollten Sie auch das ddsd- \_ Flag "mipmapcount" festlegen.</span><span class="sxs-lookup"><span data-stu-id="4b99a-142">When you write .dds files, you should set the DDSD\_CAPS and DDSD\_PIXELFORMAT flags, and for mipmapped textures you should also set the DDSD\_MIPMAPCOUNT flag.</span></span> <span data-ttu-id="4b99a-143">Wenn Sie jedoch eine DDS-Datei lesen, sollten Sie sich nicht darauf verlassen, dass die \_ Flags ddsd Caps, ddsd \_ Pixel Format und ddsd \_ mipmapcount festgelegt werden, da einige Writer einer solchen Datei diese Flags möglicherweise nicht festlegen.</span><span class="sxs-lookup"><span data-stu-id="4b99a-143">However, when you read a .dds file, you should not rely on the DDSD\_CAPS, DDSD\_PIXELFORMAT, and DDSD\_MIPMAPCOUNT flags being set because some writers of such a file might not set these flags.</span></span>

 

<span data-ttu-id="4b99a-144">Das \_ \_ \_ in DDS. h definierte DDS-Header Kennzeichen-Textur Kennzeichen ist eine bitweise OR-Kombination aus den ddsd- \_ Caps-, ddsd \_ height-, ddsd \_ Width-und ddsd \_ Pixel Format-Flags.</span><span class="sxs-lookup"><span data-stu-id="4b99a-144">The DDS\_HEADER\_FLAGS\_TEXTURE flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSD\_CAPS, DDSD\_HEIGHT, DDSD\_WIDTH, and DDSD\_PIXELFORMAT flags.</span></span>

<span data-ttu-id="4b99a-145">Das MipMap-Flag für DDS- \_ Header \_ \_ , das in DDS. h definiert ist, entspricht dem ddsd \_ mipmapcount-Flag.</span><span class="sxs-lookup"><span data-stu-id="4b99a-145">The DDS\_HEADER\_FLAGS\_MIPMAP flag, which is defined in Dds.h, is equal to the DDSD\_MIPMAPCOUNT flag.</span></span>

<span data-ttu-id="4b99a-146">Das \_ \_ \_ in DDS. h definierte DDS-Header Kennzeichen-volumenflag ist gleich dem ddsd- \_ tiefen Flag.</span><span class="sxs-lookup"><span data-stu-id="4b99a-146">The DDS\_HEADER\_FLAGS\_VOLUME flag, which is defined in Dds.h, is equal to the DDSD\_DEPTH flag.</span></span>

<span data-ttu-id="4b99a-147">Das \_ \_ \_ in DDS. h definierte DDS-Header Kennzeichen-pitchflag ist gleich dem ddsd- \_ pitchflag.</span><span class="sxs-lookup"><span data-stu-id="4b99a-147">The DDS\_HEADER\_FLAGS\_PITCH flag, which is defined in Dds.h, is equal to the DDSD\_PITCH flag.</span></span>

<span data-ttu-id="4b99a-148">Das \_ \_ \_ in DDS. h definierte DDS-Header Kennzeichen linearsize-Flag ist gleich dem ddsd \_ linearsize-Flag.</span><span class="sxs-lookup"><span data-stu-id="4b99a-148">The DDS\_HEADER\_FLAGS\_LINEARSIZE flag, which is defined in Dds.h, is equal to the DDSD\_LINEARSIZE flag.</span></span>

</dd> <dt>

<span data-ttu-id="4b99a-149">**dwheight**</span><span class="sxs-lookup"><span data-stu-id="4b99a-149">**dwHeight**</span></span>
</dt> <dd>

<span data-ttu-id="4b99a-150">Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4b99a-150">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4b99a-151">Oberflächen Höhe (in Pixel).</span><span class="sxs-lookup"><span data-stu-id="4b99a-151">Surface height (in pixels).</span></span>

</dd> <dt>

<span data-ttu-id="4b99a-152">**dwwidth**</span><span class="sxs-lookup"><span data-stu-id="4b99a-152">**dwWidth**</span></span>
</dt> <dd>

<span data-ttu-id="4b99a-153">Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4b99a-153">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4b99a-154">Die Oberflächen Breite (in Pixel).</span><span class="sxs-lookup"><span data-stu-id="4b99a-154">Surface width (in pixels).</span></span>

</dd> <dt>

<span data-ttu-id="4b99a-155">**dwpitchorlinearsize**</span><span class="sxs-lookup"><span data-stu-id="4b99a-155">**dwPitchOrLinearSize**</span></span>
</dt> <dd>

<span data-ttu-id="4b99a-156">Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4b99a-156">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4b99a-157">Die Größe und die Anzahl der Bytes pro Scan Zeile in einer unkomprimierten Textur. die Gesamtanzahl der Bytes in der Textur der obersten Ebene für eine komprimierte Textur.</span><span class="sxs-lookup"><span data-stu-id="4b99a-157">The pitch or number of bytes per scan line in an uncompressed texture; the total number of bytes in the top level texture for a compressed texture.</span></span> <span data-ttu-id="4b99a-158">Weitere Informationen zum Berechnen der Tonhöhe finden Sie im Abschnitt DDS-Datei Layout des [Programmier Handbuchs für DDS](dx-graphics-dds-pguide.md).</span><span class="sxs-lookup"><span data-stu-id="4b99a-158">For information about how to compute the pitch, see the DDS File Layout section of the [Programming Guide for DDS](dx-graphics-dds-pguide.md).</span></span>

</dd> <dt>

<span data-ttu-id="4b99a-159">**dwtiefe**</span><span class="sxs-lookup"><span data-stu-id="4b99a-159">**dwDepth**</span></span>
</dt> <dd>

<span data-ttu-id="4b99a-160">Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4b99a-160">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4b99a-161">Die Tiefe einer volumetextur (in Pixel), andernfalls nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4b99a-161">Depth of a volume texture (in pixels), otherwise unused.</span></span>

</dd> <dt>

<span data-ttu-id="4b99a-162">**dwmipmapcount**</span><span class="sxs-lookup"><span data-stu-id="4b99a-162">**dwMipMapCount**</span></span>
</dt> <dd>

<span data-ttu-id="4b99a-163">Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4b99a-163">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4b99a-164">Anzahl von MipMap-Ebenen, andernfalls nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4b99a-164">Number of mipmap levels, otherwise unused.</span></span>

</dd> <dt>

<span data-ttu-id="4b99a-165">**dwReserved1 \[ 11\]**</span><span class="sxs-lookup"><span data-stu-id="4b99a-165">**dwReserved1\[11\]**</span></span>
</dt> <dd>

<span data-ttu-id="4b99a-166">Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4b99a-166">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4b99a-167">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4b99a-167">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="4b99a-168">**ddspf**</span><span class="sxs-lookup"><span data-stu-id="4b99a-168">**ddspf**</span></span>
</dt> <dd>

<span data-ttu-id="4b99a-169">Typ: **[ **DDS \_ Pixel Format**](dds-pixelformat.md)**</span><span class="sxs-lookup"><span data-stu-id="4b99a-169">Type: **[**DDS\_PIXELFORMAT**](dds-pixelformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4b99a-170">Das Pixel Format (siehe [**DDS \_ Pixel Format**](dds-pixelformat.md)).</span><span class="sxs-lookup"><span data-stu-id="4b99a-170">The pixel format (see [**DDS\_PIXELFORMAT**](dds-pixelformat.md)).</span></span>

</dd> <dt>

<span data-ttu-id="4b99a-171">**dwcaps**</span><span class="sxs-lookup"><span data-stu-id="4b99a-171">**dwCaps**</span></span>
</dt> <dd>

<span data-ttu-id="4b99a-172">Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4b99a-172">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4b99a-173">Gibt die Komplexität der gespeicherten Oberflächen an.</span><span class="sxs-lookup"><span data-stu-id="4b99a-173">Specifies the complexity of the surfaces stored.</span></span>



| <span data-ttu-id="4b99a-174">Flag</span><span class="sxs-lookup"><span data-stu-id="4b99a-174">Flag</span></span>             | <span data-ttu-id="4b99a-175">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4b99a-175">Description</span></span>                                                                                                                              | <span data-ttu-id="4b99a-176">Wert</span><span class="sxs-lookup"><span data-stu-id="4b99a-176">Value</span></span>    |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------|----------|
| <span data-ttu-id="4b99a-177">DDSCAPS \_ Komplex</span><span class="sxs-lookup"><span data-stu-id="4b99a-177">DDSCAPS\_COMPLEX</span></span> | <span data-ttu-id="4b99a-178">Optionale muss für jede Datei verwendet werden, die mehr als eine Oberfläche (eine MipMap, eine kubische Umgebungs Zuordnung oder eine mipzugeordnete volumetextur) enthält.</span><span class="sxs-lookup"><span data-stu-id="4b99a-178">Optional; must be used on any file that contains more than one surface (a mipmap, a cubic environment map, or mipmapped volume texture).</span></span> | <span data-ttu-id="4b99a-179">0x8</span><span class="sxs-lookup"><span data-stu-id="4b99a-179">0x8</span></span>      |
| <span data-ttu-id="4b99a-180">DDSCAPS- \_ MipMap</span><span class="sxs-lookup"><span data-stu-id="4b99a-180">DDSCAPS\_MIPMAP</span></span>  | <span data-ttu-id="4b99a-181">Optionale sollte für eine MipMap verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4b99a-181">Optional; should be used for a mipmap.</span></span>                                                                                                   | <span data-ttu-id="4b99a-182">0x400000</span><span class="sxs-lookup"><span data-stu-id="4b99a-182">0x400000</span></span> |
| <span data-ttu-id="4b99a-183">DDSCAPS- \_ Textur</span><span class="sxs-lookup"><span data-stu-id="4b99a-183">DDSCAPS\_TEXTURE</span></span> | <span data-ttu-id="4b99a-184">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="4b99a-184">Required</span></span>                                                                                                                                 | <span data-ttu-id="4b99a-185">0x1000</span><span class="sxs-lookup"><span data-stu-id="4b99a-185">0x1000</span></span>   |



 

> [!Note]  
> <span data-ttu-id="4b99a-186">Wenn Sie DDS-Dateien schreiben, sollten Sie das DDSCAPS \_ -Textur Kennzeichen festlegen, und für mehrere Oberflächen sollten Sie auch das komplexe DDSCAPS- \_ Flag festlegen.</span><span class="sxs-lookup"><span data-stu-id="4b99a-186">When you write .dds files, you should set the DDSCAPS\_TEXTURE flag, and for multiple surfaces you should also set the DDSCAPS\_COMPLEX flag.</span></span> <span data-ttu-id="4b99a-187">Wenn Sie jedoch eine DDS-Datei lesen, sollten Sie sich nicht darauf verlassen, dass die komplexen DDSCAPS \_ -Textur-und DDSCAPS- \_ Flags festgelegt werden, da einige Writer einer solchen Datei diese Flags möglicherweise nicht festlegen.</span><span class="sxs-lookup"><span data-stu-id="4b99a-187">However, when you read a .dds file, you should not rely on the DDSCAPS\_TEXTURE and DDSCAPS\_COMPLEX flags being set because some writers of such a file might not set these flags.</span></span>

 

<span data-ttu-id="4b99a-188">Das in " \_ \_ \_ DDS. h" definierte Flag "Mipmap" der DDS-oberflächenflags ist eine bitweise OR-Kombination aus den komplexen DDSCAPS- \_ und DDSCAPS- \_ MipMap-Flags.</span><span class="sxs-lookup"><span data-stu-id="4b99a-188">The DDS\_SURFACE\_FLAGS\_MIPMAP flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS\_COMPLEX and DDSCAPS\_MIPMAP flags.</span></span>

<span data-ttu-id="4b99a-189">Das Textur Kennzeichen der DDS- \_ Surface- \_ Flags \_ , das in DDS. h definiert ist, entspricht dem DDSCAPS- \_ Textur Kennzeichen.</span><span class="sxs-lookup"><span data-stu-id="4b99a-189">The DDS\_SURFACE\_FLAGS\_TEXTURE flag, which is defined in Dds.h, is equal to the DDSCAPS\_TEXTURE flag.</span></span>

<span data-ttu-id="4b99a-190">Das cubemap-Flag der DDS- \_ Surface- \_ Flags \_ , das in DDS. h definiert ist, entspricht dem komplexen DDSCAPS- \_ Flag.</span><span class="sxs-lookup"><span data-stu-id="4b99a-190">The DDS\_SURFACE\_FLAGS\_CUBEMAP flag, which is defined in Dds.h, is equal to the DDSCAPS\_COMPLEX flag.</span></span>

</dd> <dt>

<span data-ttu-id="4b99a-191">**dwCaps2**</span><span class="sxs-lookup"><span data-stu-id="4b99a-191">**dwCaps2**</span></span>
</dt> <dd>

<span data-ttu-id="4b99a-192">Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4b99a-192">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4b99a-193">Weitere Details zu den gespeicherten Oberflächen.</span><span class="sxs-lookup"><span data-stu-id="4b99a-193">Additional detail about the surfaces stored.</span></span>



| <span data-ttu-id="4b99a-194">Flag</span><span class="sxs-lookup"><span data-stu-id="4b99a-194">Flag</span></span>                         | <span data-ttu-id="4b99a-195">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4b99a-195">Description</span></span>                                            | <span data-ttu-id="4b99a-196">Wert</span><span class="sxs-lookup"><span data-stu-id="4b99a-196">Value</span></span>    |
|------------------------------|--------------------------------------------------------|----------|
| <span data-ttu-id="4b99a-197">DDSCAPS2 \_ cubemap</span><span class="sxs-lookup"><span data-stu-id="4b99a-197">DDSCAPS2\_CUBEMAP</span></span>            | <span data-ttu-id="4b99a-198">Erforderlich für eine cubemap.</span><span class="sxs-lookup"><span data-stu-id="4b99a-198">Required for a cube map.</span></span>                               | <span data-ttu-id="4b99a-199">0x200</span><span class="sxs-lookup"><span data-stu-id="4b99a-199">0x200</span></span>    |
| <span data-ttu-id="4b99a-200">DDSCAPS2 \_ cubemap \_ positivex</span><span class="sxs-lookup"><span data-stu-id="4b99a-200">DDSCAPS2\_CUBEMAP\_POSITIVEX</span></span> | <span data-ttu-id="4b99a-201">Erforderlich, wenn diese Oberflächen in einer cubemap gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="4b99a-201">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="4b99a-202">0x400</span><span class="sxs-lookup"><span data-stu-id="4b99a-202">0x400</span></span>    |
| <span data-ttu-id="4b99a-203">DDSCAPS2 \_ cubemap \_ negativex</span><span class="sxs-lookup"><span data-stu-id="4b99a-203">DDSCAPS2\_CUBEMAP\_NEGATIVEX</span></span> | <span data-ttu-id="4b99a-204">Erforderlich, wenn diese Oberflächen in einer cubemap gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="4b99a-204">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="4b99a-205">0x800</span><span class="sxs-lookup"><span data-stu-id="4b99a-205">0x800</span></span>    |
| <span data-ttu-id="4b99a-206">DDSCAPS2 \_ cubemap \_ positivey</span><span class="sxs-lookup"><span data-stu-id="4b99a-206">DDSCAPS2\_CUBEMAP\_POSITIVEY</span></span> | <span data-ttu-id="4b99a-207">Erforderlich, wenn diese Oberflächen in einer cubemap gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="4b99a-207">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="4b99a-208">0x1000</span><span class="sxs-lookup"><span data-stu-id="4b99a-208">0x1000</span></span>   |
| <span data-ttu-id="4b99a-209">DDSCAPS2 \_ cubemap \_ negativey</span><span class="sxs-lookup"><span data-stu-id="4b99a-209">DDSCAPS2\_CUBEMAP\_NEGATIVEY</span></span> | <span data-ttu-id="4b99a-210">Erforderlich, wenn diese Oberflächen in einer cubemap gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="4b99a-210">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="4b99a-211">0x2000</span><span class="sxs-lookup"><span data-stu-id="4b99a-211">0x2000</span></span>   |
| <span data-ttu-id="4b99a-212">DDSCAPS2 \_ cubemap \_ positivez</span><span class="sxs-lookup"><span data-stu-id="4b99a-212">DDSCAPS2\_CUBEMAP\_POSITIVEZ</span></span> | <span data-ttu-id="4b99a-213">Erforderlich, wenn diese Oberflächen in einer cubemap gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="4b99a-213">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="4b99a-214">0x4000</span><span class="sxs-lookup"><span data-stu-id="4b99a-214">0x4000</span></span>   |
| <span data-ttu-id="4b99a-215">DDSCAPS2 \_ cubemap \_ negativez</span><span class="sxs-lookup"><span data-stu-id="4b99a-215">DDSCAPS2\_CUBEMAP\_NEGATIVEZ</span></span> | <span data-ttu-id="4b99a-216">Erforderlich, wenn diese Oberflächen in einer cubemap gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="4b99a-216">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="4b99a-217">0x8000</span><span class="sxs-lookup"><span data-stu-id="4b99a-217">0x8000</span></span>   |
| <span data-ttu-id="4b99a-218">DDSCAPS2- \_ Volume</span><span class="sxs-lookup"><span data-stu-id="4b99a-218">DDSCAPS2\_VOLUME</span></span>             | <span data-ttu-id="4b99a-219">Erforderlich für eine volumetextur.</span><span class="sxs-lookup"><span data-stu-id="4b99a-219">Required for a volume texture.</span></span>                         | <span data-ttu-id="4b99a-220">0x200000</span><span class="sxs-lookup"><span data-stu-id="4b99a-220">0x200000</span></span> |



 

<span data-ttu-id="4b99a-221">Das \_ \_ in DDS. h definierte DDS-cubemap positivex-Flag ist eine bitweise OR-Kombination der DDSCAPS2 \_ cubemap-und DDSCAPS2 \_ cubemap \_ positivex-Flags.</span><span class="sxs-lookup"><span data-stu-id="4b99a-221">The DDS\_CUBEMAP\_POSITIVEX flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_POSITIVEX flags.</span></span>

<span data-ttu-id="4b99a-222">Das DDS \_ cubemap \_ negativex-Flag, das in DDS. h definiert ist, ist eine bitweise OR-Kombination der DDSCAPS2 \_ cubemap-und DDSCAPS2 \_ cubemap \_ negativex-Flags.</span><span class="sxs-lookup"><span data-stu-id="4b99a-222">The DDS\_CUBEMAP\_NEGATIVEX flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_NEGATIVEX flags.</span></span>

<span data-ttu-id="4b99a-223">Das \_ \_ in DDS. h definierte Flag "DDS cubemap positivey" ist eine bitweise OR-Kombination aus den DDSCAPS2 \_ cubemap-und DDSCAPS2 \_ cubemap- \_ Flags.</span><span class="sxs-lookup"><span data-stu-id="4b99a-223">The DDS\_CUBEMAP\_POSITIVEY flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_POSITIVEY flags.</span></span>

<span data-ttu-id="4b99a-224">Das DDS \_ -cubemap \_ -negativey-Flag, das in DDS. h definiert ist, ist eine bitweise OR-Kombination der DDSCAPS2 \_ cubemap-und DDSCAPS2 \_ cubemap \_ negativey-Flags.</span><span class="sxs-lookup"><span data-stu-id="4b99a-224">The DDS\_CUBEMAP\_NEGATIVEY flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_NEGATIVEY flags.</span></span>

<span data-ttu-id="4b99a-225">Das \_ \_ in DDS. h definierte DDS-cubemap-Element, das in DDS. h definiert ist, ist eine bitweise OR-Kombination aus den DDSCAPS2 \_ cubemap-und DDSCAPS2 \_ cubemap \_ positivez-Flags.</span><span class="sxs-lookup"><span data-stu-id="4b99a-225">The DDS\_CUBEMAP\_POSITIVEZ flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_POSITIVEZ flags.</span></span>

<span data-ttu-id="4b99a-226">Das DDS \_ -cubemap \_ negativez-Flag, das in DDS. h definiert ist, ist eine bitweise OR-Kombination der DDSCAPS2 \_ cubemap-und DDSCAPS2 \_ cubemap \_ negativez-Flags.</span><span class="sxs-lookup"><span data-stu-id="4b99a-226">The DDS\_CUBEMAP\_NEGATIVEZ flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_NEGATIVEZ flags.</span></span>

<span data-ttu-id="4b99a-227">Das Flag für die DDS- \_ cubemap \_ allgesichter, die in DDS. h definiert ist, ist eine bitweise OR-Kombination der DDS- \_ cubemap \_ positivex, DDS \_ cubemap \_ negativex, DDS \_ cubemap \_ positivvey, DDS \_ cubemap \_ negativey, DDS \_ cubemap \_ positivvez und DDSCAPS2 \_ cubemap \_ negativez Flags.</span><span class="sxs-lookup"><span data-stu-id="4b99a-227">The DDS\_CUBEMAP\_ALLFACES flag, which is defined in Dds.h, is a bitwise-OR combination of the DDS\_CUBEMAP\_POSITIVEX, DDS\_CUBEMAP\_NEGATIVEX, DDS\_CUBEMAP\_POSITIVEY, DDS\_CUBEMAP\_NEGATIVEY, DDS\_CUBEMAP\_POSITIVEZ, and DDSCAPS2\_CUBEMAP\_NEGATIVEZ flags.</span></span>

<span data-ttu-id="4b99a-228">Das \_ \_ in DDS. h definierte Flag für das DDS-Flags-Volume ist gleich dem DDSCAPS2- \_ volumenflag.</span><span class="sxs-lookup"><span data-stu-id="4b99a-228">The DDS\_FLAGS\_VOLUME flag, which is defined in Dds.h, is equal to the DDSCAPS2\_VOLUME flag.</span></span>

> [!Note]  
> <span data-ttu-id="4b99a-229">Obwohl Direct3D 9 partielle Cubemaps, Direct3D 10, 10,1 und 11 unterstützt, müssen Sie alle sechs Cube-Map-Gesichter definieren (d. h., Sie müssen DDS \_ cubemap \_ allgesichter festlegen).</span><span class="sxs-lookup"><span data-stu-id="4b99a-229">Although Direct3D 9 supports partial cube-maps, Direct3D 10, 10.1, and 11 require that you define all six cube-map faces (that is, you must set DDS\_CUBEMAP\_ALLFACES).</span></span>

 

</dd> <dt>

<span data-ttu-id="4b99a-230">**dwCaps3**</span><span class="sxs-lookup"><span data-stu-id="4b99a-230">**dwCaps3**</span></span>
</dt> <dd>

<span data-ttu-id="4b99a-231">Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4b99a-231">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4b99a-232">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4b99a-232">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="4b99a-233">**dwCaps4**</span><span class="sxs-lookup"><span data-stu-id="4b99a-233">**dwCaps4**</span></span>
</dt> <dd>

<span data-ttu-id="4b99a-234">Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4b99a-234">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4b99a-235">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4b99a-235">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="4b99a-236">**dwReserved2**</span><span class="sxs-lookup"><span data-stu-id="4b99a-236">**dwReserved2**</span></span>
</dt> <dd>

<span data-ttu-id="4b99a-237">Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4b99a-237">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4b99a-238">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4b99a-238">Unused.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4b99a-239">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4b99a-239">Remarks</span></span>

<span data-ttu-id="4b99a-240">Einschließen von Flags in **dwFlags** für die Member der Struktur, die gültige Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="4b99a-240">Include flags in **dwFlags** for the members of the structure that contain valid data.</span></span>

<span data-ttu-id="4b99a-241">Verwenden Sie diese Struktur in Kombination mit einem [**DDS- \_ Header \_ DXT10**](dds-header-dxt10.md) , um ein Ressourcen Array in einer DDS-Datei zu speichern.</span><span class="sxs-lookup"><span data-stu-id="4b99a-241">Use this structure in combination with a [**DDS\_HEADER\_DXT10**](dds-header-dxt10.md) to store a resource array in a DDS file.</span></span> <span data-ttu-id="4b99a-242">Weitere Informationen finden Sie unter [Textur Arrays](dx-graphics-dds-pguide.md).</span><span class="sxs-lookup"><span data-stu-id="4b99a-242">For more information, see [texture arrays](dx-graphics-dds-pguide.md).</span></span>

<span data-ttu-id="4b99a-243">**DDS \_ Der Header** ist mit der DirectDraw DDSURFACEDESC2-Struktur ohne DirectDraw-Abhängigkeiten identisch.</span><span class="sxs-lookup"><span data-stu-id="4b99a-243">**DDS\_HEADER** is identical to the DirectDraw DDSURFACEDESC2 structure without DirectDraw dependencies.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b99a-244">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b99a-244">Requirements</span></span>



| <span data-ttu-id="4b99a-245">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4b99a-245">Requirement</span></span> | <span data-ttu-id="4b99a-246">Wert</span><span class="sxs-lookup"><span data-stu-id="4b99a-246">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4b99a-247">Header</span><span class="sxs-lookup"><span data-stu-id="4b99a-247">Header</span></span><br/> | <dl> <span data-ttu-id="4b99a-248"><dt>DDS. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b99a-248"><dt>Dds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b99a-249">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b99a-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b99a-250">Verweis für DDS</span><span class="sxs-lookup"><span data-stu-id="4b99a-250">Reference for DDS</span></span>](dx-graphics-dds-reference.md)
</dt> </dl>

 

