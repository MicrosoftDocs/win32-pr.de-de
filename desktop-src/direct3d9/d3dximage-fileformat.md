---
description: Beschreibt die unterstützten Bild Dateiformate. Beschreibungen dieser Formate finden Sie unter "Hinweise".
ms.assetid: 245a0052-f156-44ad-ab46-3677a818167e
title: D3DXIMAGE_FILEFORMAT-Enumeration (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIMAGE_FILEFORMAT
api_type:
- HeaderDef
api_location:
- d3dx9tex.h
ms.openlocfilehash: 3b1195e7503ff32e92cdbafde941b811dcf86427
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354827"
---
# <a name="d3dximage_fileformat-enumeration"></a><span data-ttu-id="0db1f-104">D3DXIMAGE \_ FileFormat-Enumeration</span><span class="sxs-lookup"><span data-stu-id="0db1f-104">D3DXIMAGE\_FILEFORMAT enumeration</span></span>

<span data-ttu-id="0db1f-105">Beschreibt die unterstützten Bild Dateiformate.</span><span class="sxs-lookup"><span data-stu-id="0db1f-105">Describes the supported image file formats.</span></span> <span data-ttu-id="0db1f-106">Beschreibungen dieser Formate finden Sie unter "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="0db1f-106">See Remarks for descriptions of these formats.</span></span>

## <a name="syntax"></a><span data-ttu-id="0db1f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0db1f-107">Syntax</span></span>


```C++
typedef enum D3DXIMAGE_FILEFORMAT { 
  D3DXIFF_BMP          = 0,
  D3DXIFF_JPG          = 1,
  D3DXIFF_TGA          = 2,
  D3DXIFF_PNG          = 3,
  D3DXIFF_DDS          = 4,
  D3DXIFF_PPM          = 5,
  D3DXIFF_DIB          = 6,
  D3DXIFF_HDR          = 7,
  D3DXIFF_PFM          = 8,
  D3DXIFF_FORCE_DWORD  = 0x7fffffff
} D3DXIMAGE_FILEFORMAT, *LPD3DXIMAGE_FILEFORMAT;
```



## <a name="constants"></a><span data-ttu-id="0db1f-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="0db1f-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0db1f-109"><span id="D3DXIFF_BMP"></span><span id="d3dxiff_bmp"></span>**D3DXIFF \_ BMP**</span><span class="sxs-lookup"><span data-stu-id="0db1f-109"><span id="D3DXIFF_BMP"></span><span id="d3dxiff_bmp"></span>**D3DXIFF\_BMP**</span></span>
</dt> <dd>

<span data-ttu-id="0db1f-110">Windows-Bitmap-Dateiformat (BMP).</span><span class="sxs-lookup"><span data-stu-id="0db1f-110">Windows bitmap (BMP) file format.</span></span>

</dd> <dt>

<span data-ttu-id="0db1f-111"><span id="D3DXIFF_JPG"></span><span id="d3dxiff_jpg"></span>**D3DXIFF \_ JPG**</span><span class="sxs-lookup"><span data-stu-id="0db1f-111"><span id="D3DXIFF_JPG"></span><span id="d3dxiff_jpg"></span>**D3DXIFF\_JPG**</span></span>
</dt> <dd>

<span data-ttu-id="0db1f-112">Komprimiertes Dateiformat für eine gemeinsame Photographics Experts Group (JPEG).</span><span class="sxs-lookup"><span data-stu-id="0db1f-112">Joint Photographics Experts Group (JPEG) compressed file format.</span></span>

</dd> <dt>

<span data-ttu-id="0db1f-113"><span id="D3DXIFF_TGA"></span><span id="d3dxiff_tga"></span>**D3DXIFF- \_ TGA**</span><span class="sxs-lookup"><span data-stu-id="0db1f-113"><span id="D3DXIFF_TGA"></span><span id="d3dxiff_tga"></span>**D3DXIFF\_TGA**</span></span>
</dt> <dd>

<span data-ttu-id="0db1f-114">Bild Dateiformat Truevision (Targa, TGA).</span><span class="sxs-lookup"><span data-stu-id="0db1f-114">Truevision (Targa, or TGA) image file format.</span></span>

</dd> <dt>

<span data-ttu-id="0db1f-115"><span id="D3DXIFF_PNG"></span><span id="d3dxiff_png"></span>**D3DXIFF \_ PNG**</span><span class="sxs-lookup"><span data-stu-id="0db1f-115"><span id="D3DXIFF_PNG"></span><span id="d3dxiff_png"></span>**D3DXIFF\_PNG**</span></span>
</dt> <dd>

<span data-ttu-id="0db1f-116">Das Dateiformat Portable Network Graphics (PNG).</span><span class="sxs-lookup"><span data-stu-id="0db1f-116">Portable Network Graphics (PNG) file format.</span></span>

</dd> <dt>

<span data-ttu-id="0db1f-117"><span id="D3DXIFF_DDS"></span><span id="d3dxiff_dds"></span>**D3DXIFF- \_ DDS**</span><span class="sxs-lookup"><span data-stu-id="0db1f-117"><span id="D3DXIFF_DDS"></span><span id="d3dxiff_dds"></span>**D3DXIFF\_DDS**</span></span>
</dt> <dd>

<span data-ttu-id="0db1f-118">Das DDS-Dateiformat (DirectDraw Surface).</span><span class="sxs-lookup"><span data-stu-id="0db1f-118">DirectDraw surface (DDS) file format.</span></span>

</dd> <dt>

<span data-ttu-id="0db1f-119"><span id="D3DXIFF_PPM"></span><span id="d3dxiff_ppm"></span>**D3DXIFF \_ ppm**</span><span class="sxs-lookup"><span data-stu-id="0db1f-119"><span id="D3DXIFF_PPM"></span><span id="d3dxiff_ppm"></span>**D3DXIFF\_PPM**</span></span>
</dt> <dd>

<span data-ttu-id="0db1f-120">Dateiformat für Portable pixmap (ppm).</span><span class="sxs-lookup"><span data-stu-id="0db1f-120">Portable pixmap (PPM) file format.</span></span>

</dd> <dt>

<span data-ttu-id="0db1f-121"><span id="D3DXIFF_DIB"></span><span id="d3dxiff_dib"></span>**D3DXIFF \_ DIB**</span><span class="sxs-lookup"><span data-stu-id="0db1f-121"><span id="D3DXIFF_DIB"></span><span id="d3dxiff_dib"></span>**D3DXIFF\_DIB**</span></span>
</dt> <dd>

<span data-ttu-id="0db1f-122">Windows-DIB-Dateiformat (geräteunabhängige Bitmap).</span><span class="sxs-lookup"><span data-stu-id="0db1f-122">Windows device-independent bitmap (DIB) file format.</span></span>

</dd> <dt>

<span data-ttu-id="0db1f-123"><span id="D3DXIFF_HDR"></span><span id="d3dxiff_hdr"></span>**D3DXIFF \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="0db1f-123"><span id="D3DXIFF_HDR"></span><span id="d3dxiff_hdr"></span>**D3DXIFF\_HDR**</span></span>
</dt> <dd>

<span data-ttu-id="0db1f-124">Das HDR-Dateiformat (High Dynamic Range).</span><span class="sxs-lookup"><span data-stu-id="0db1f-124">High dynamic range (HDR) file format.</span></span>

</dd> <dt>

<span data-ttu-id="0db1f-125"><span id="D3DXIFF_PFM"></span><span id="d3dxiff_pfm"></span>**D3DXIFF \_ PFM**</span><span class="sxs-lookup"><span data-stu-id="0db1f-125"><span id="D3DXIFF_PFM"></span><span id="d3dxiff_pfm"></span>**D3DXIFF\_PFM**</span></span>
</dt> <dd>

<span data-ttu-id="0db1f-126">Portable float-Kartendatei Format.</span><span class="sxs-lookup"><span data-stu-id="0db1f-126">Portable float map file format.</span></span>

</dd> <dt>

<span data-ttu-id="0db1f-127"><span id="D3DXIFF_FORCE_DWORD"></span><span id="d3dxiff_force_dword"></span>**D3DXIFF \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="0db1f-127"><span id="D3DXIFF_FORCE_DWORD"></span><span id="d3dxiff_force_dword"></span>**D3DXIFF\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="0db1f-128">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="0db1f-128">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="0db1f-129">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="0db1f-129">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="0db1f-130">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0db1f-130">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0db1f-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0db1f-131">Remarks</span></span>

<span data-ttu-id="0db1f-132">Funktionen, die mit D3DXLoadxxx beginnen, unterstützen alle aufgeführten Formate.</span><span class="sxs-lookup"><span data-stu-id="0db1f-132">Functions that begin with D3DXLoadxxx support all of the formats listed.</span></span> <span data-ttu-id="0db1f-133">Funktionen, die mit D3DXSavexxx beginnen, unterstützen alle aufgeführten Formate, ausgenommen die Formate Truevision (. TGA) und Portable pixmap (. ppm).</span><span class="sxs-lookup"><span data-stu-id="0db1f-133">Functions that begin with D3DXSavexxx support all of the formats listed except the Truevision (.tga) and portable pixmap (.ppm) formats.</span></span>

<span data-ttu-id="0db1f-134">In der folgenden Tabelle sind die verfügbaren Eingabe-und Ausgabeformate aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="0db1f-134">The following table lists the available input and output formats.</span></span>



| <span data-ttu-id="0db1f-135">Dateierweiterung</span><span class="sxs-lookup"><span data-stu-id="0db1f-135">File Extension</span></span> | <span data-ttu-id="0db1f-136">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0db1f-136">Description</span></span>                                                                                                                                                                                                                                                                                                                                        |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0db1f-137">BMP</span><span class="sxs-lookup"><span data-stu-id="0db1f-137">.bmp</span></span>           | <span data-ttu-id="0db1f-138">Windows-Bitmap-Format.</span><span class="sxs-lookup"><span data-stu-id="0db1f-138">Windows bitmap format.</span></span> <span data-ttu-id="0db1f-139">Enthält einen Header, der die Auflösung des Geräts, auf dem das Rechteck von Pixeln erstellt wurde, die Abmessungen des Rechtecks, die Größe des Bits-Arrays, eine logische Palette und ein Array von Bits beschreibt, das die Beziehung zwischen Pixeln im bitzugeordneten Bild und Einträgen in der logischen Palette definiert.</span><span class="sxs-lookup"><span data-stu-id="0db1f-139">Contains a header that describes the resolution of the device on which the rectangle of pixels was created, the dimensions of the rectangle, the size of the array of bits, a logical palette, and an array of bits that defines the relationship between pixels in the bitmapped image and entries in the logical palette.</span></span> |
| <span data-ttu-id="0db1f-140">.dds</span><span class="sxs-lookup"><span data-stu-id="0db1f-140">.dds</span></span>           | <span data-ttu-id="0db1f-141">Format der DirectDraw-Oberflächen Datei.</span><span class="sxs-lookup"><span data-stu-id="0db1f-141">DirectDraw Surface file format.</span></span> <span data-ttu-id="0db1f-142">Speichert Texturen, volumetexturen und kubische Umgebungs Zuordnungen mit oder ohne MipMap-Ebenen und mit oder ohne Pixel Komprimierung.</span><span class="sxs-lookup"><span data-stu-id="0db1f-142">Stores textures, volume textures, and cubic environment maps, with or without mipmap levels, and with or without pixel compression.</span></span> <span data-ttu-id="0db1f-143">Siehe [DDS](../direct3ddds/dx-graphics-dds.md).</span><span class="sxs-lookup"><span data-stu-id="0db1f-143">See [DDS](../direct3ddds/dx-graphics-dds.md).</span></span>                                                                                                                                       |
| <span data-ttu-id="0db1f-144">DIB</span><span class="sxs-lookup"><span data-stu-id="0db1f-144">.dib</span></span>           | <span data-ttu-id="0db1f-145">Windows DIB.</span><span class="sxs-lookup"><span data-stu-id="0db1f-145">Windows DIB.</span></span> <span data-ttu-id="0db1f-146">Enthält ein Array von Bits in Kombination mit Strukturen, die die Breite und Höhe des bitzugeordneten Bilds, das Farb Format des Geräts, auf dem das Image erstellt wurde, und die Auflösung des Geräts angeben, das zum Erstellen des Bilds verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="0db1f-146">Contains an array of bits combined with structures that specify width and height of the bitmapped image, color format of the device where the image was created, and resolution of the device used to create that image.</span></span>                                                                                                              |
| <span data-ttu-id="0db1f-147">. HDR</span><span class="sxs-lookup"><span data-stu-id="0db1f-147">.hdr</span></span>           | <span data-ttu-id="0db1f-148">HDR-Format.</span><span class="sxs-lookup"><span data-stu-id="0db1f-148">HDR format.</span></span> <span data-ttu-id="0db1f-149">Codiert jedes Pixel als RGBE-32-Bit-Farbe mit 8 Bits der Mantisse für Rot, grün und blau und einem freigegebenen 8-Bit-Exponenten.</span><span class="sxs-lookup"><span data-stu-id="0db1f-149">Encodes each pixel as an RGBE 32-bit color, with 8 bits of mantissa for red, green, and blue, and a shared 8-bit exponent.</span></span> <span data-ttu-id="0db1f-150">Jeder Kanal wird separat mit der Lauf Zeit Codierung (Run-Length Encoding, RLE) komprimiert.</span><span class="sxs-lookup"><span data-stu-id="0db1f-150">Each channel is separately compressed with run-length encoding (RLE).</span></span>                                                                                                                                       |
| <span data-ttu-id="0db1f-151">.jpg</span><span class="sxs-lookup"><span data-stu-id="0db1f-151">.jpg</span></span>           | <span data-ttu-id="0db1f-152">JPEG-Standard.</span><span class="sxs-lookup"><span data-stu-id="0db1f-152">JPEG standard.</span></span> <span data-ttu-id="0db1f-153">Gibt die Variablen Komprimierung von 24-Bit-RGB-Farb-und 8-Bit-Bilddokument Dateien mit Graustufen Tagged Image File Format (TIFF) an.</span><span class="sxs-lookup"><span data-stu-id="0db1f-153">Specifies variable compression of 24-bit RGB color and 8-bit gray-scale Tagged Image File Format (TIFF) image document files.</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="0db1f-154">. PFM</span><span class="sxs-lookup"><span data-stu-id="0db1f-154">.pfm</span></span>           | <span data-ttu-id="0db1f-155">Portable float-Kartenformat.</span><span class="sxs-lookup"><span data-stu-id="0db1f-155">Portable float map format.</span></span> <span data-ttu-id="0db1f-156">Ein unformatierte Gleit Komma Bildformat ohne Komprimierung.</span><span class="sxs-lookup"><span data-stu-id="0db1f-156">A raw floating point image format, without any compression.</span></span> <span data-ttu-id="0db1f-157">Der Dateiheader gibt Bildbreite, Höhe, monochrome oder Farbe und die Reihenfolge des Computers an.</span><span class="sxs-lookup"><span data-stu-id="0db1f-157">The file header specifies image width, height, monochrome or color, and machine word order.</span></span> <span data-ttu-id="0db1f-158">Pixel Daten werden als 32-Bit-Gleit Komma Werte mit drei Werten pro Pixel für Farbe und einem Wert pro Pixel für monochrome gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0db1f-158">Pixel data is stored as 32-bit floating point values, with 3 values per pixel for color, and one value per pixel for monochrome.</span></span>                                |
| <span data-ttu-id="0db1f-159">.png</span><span class="sxs-lookup"><span data-stu-id="0db1f-159">.png</span></span>           | <span data-ttu-id="0db1f-160">PNG-Format.</span><span class="sxs-lookup"><span data-stu-id="0db1f-160">PNG format.</span></span> <span data-ttu-id="0db1f-161">Ein nicht proprietäres Bitmap-Format, das die Verlust lose Komprimierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="0db1f-161">A non-proprietary bitmap format using lossless compression.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="0db1f-162">. ppm</span><span class="sxs-lookup"><span data-stu-id="0db1f-162">.ppm</span></span>           | <span data-ttu-id="0db1f-163">Portables Pixmap-Format.</span><span class="sxs-lookup"><span data-stu-id="0db1f-163">Portable Pixmap format.</span></span> <span data-ttu-id="0db1f-164">Ein Binär-oder ASCII-Dateiformat für Farbbilder, das Bild Höhe und-Breite sowie den Wert der maximalen Farbkomponente enthält.</span><span class="sxs-lookup"><span data-stu-id="0db1f-164">A binary or ASCII file format for color images that includes image height and width and the maximum color component value.</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="0db1f-165">.tga</span><span class="sxs-lookup"><span data-stu-id="0db1f-165">.tga</span></span>           | <span data-ttu-id="0db1f-166">Format für das Targa-oder Truevision-Grafik Adapter.</span><span class="sxs-lookup"><span data-stu-id="0db1f-166">Targa or Truevision Graphics Adapter format.</span></span> <span data-ttu-id="0db1f-167">Unterstützt Tiefen von 8, 15, 16, 24 und 32 Bits, einschließlich der 8-Bit-Grau Skala, und enthält optionale Farb Palettendaten, Bild (x, y) Ursprungs-und Größendaten sowie Pixeldaten.</span><span class="sxs-lookup"><span data-stu-id="0db1f-167">Supports depths of 8, 15, 16, 24, and 32 bits, including 8-bit gray scale, and contains optional color palette data, image (x, y) origin and size data, and pixel data.</span></span>                                                                                                                               |



 

<span data-ttu-id="0db1f-168">Weitere Informationen zu einigen dieser Formate finden Sie unter [Typen von Bitmaps](../gdiplus/-gdiplus-types-of-bitmaps-about.md) .</span><span class="sxs-lookup"><span data-stu-id="0db1f-168">See [Types of Bitmaps](../gdiplus/-gdiplus-types-of-bitmaps-about.md) for more information on some of these formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="0db1f-169">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0db1f-169">Requirements</span></span>



| <span data-ttu-id="0db1f-170">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0db1f-170">Requirement</span></span> | <span data-ttu-id="0db1f-171">Wert</span><span class="sxs-lookup"><span data-stu-id="0db1f-171">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0db1f-172">Header</span><span class="sxs-lookup"><span data-stu-id="0db1f-172">Header</span></span><br/> | <dl> <span data-ttu-id="0db1f-173"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="0db1f-173"><dt>D3dx9tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0db1f-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0db1f-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0db1f-175">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="0db1f-175">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
