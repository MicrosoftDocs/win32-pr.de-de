---
description: Die WIA \_ \_ -rohheaderstruktur definiert ein Bild im RAW-Datenformat eines Geräts und ermöglicht es Anwendungen, bei der Übertragung von Windows-Bild Käufen (WIA) das RAW-Format zu verwenden.
ms.assetid: c7b50816-d596-4c62-a00e-cd8d6e303e42
title: WIA_RAW_HEADER Struktur (wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_RAW_HEADER
api_type:
- HeaderDef
api_location:
- Wiadef.h
ms.openlocfilehash: 8da33f0b257168712f1b16fb7f940df5db862d3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357345"
---
# <a name="wia_raw_header-structure"></a><span data-ttu-id="a457d-103">WIA \_ - \_ rohheader Struktur</span><span class="sxs-lookup"><span data-stu-id="a457d-103">WIA\_RAW\_HEADER structure</span></span>

<span data-ttu-id="a457d-104">Die **WIA \_ - \_ rohheaderstruktur** definiert ein Bild im RAW-Datenformat eines Geräts und ermöglicht es Anwendungen, bei der Übertragung von Windows-Bild Käufen (WIA) das RAW-Format zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a457d-104">The **WIA\_RAW\_HEADER** structure defines an image in the RAW data format of a device and enables applications to use RAW format in Windows Image Acquisition (WIA) transfers.</span></span>

## <a name="syntax"></a><span data-ttu-id="a457d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a457d-105">Syntax</span></span>


```C++
typedef struct _WIA_RAW_HEADER {
  DWORD Tag;
  DWORD Version;
  DWORD HeaderSize;
  DWORD XRes;
  DWORD YRes;
  DWORD XExtent;
  DWORD YExtent;
  DWORD BytesPerLine;
  DWORD BitsPerPixel;
  DWORD ChannelsPerPixel;
  DWORD DataType;
  BYTE  BitsPerChannel[8];
  DWORD Compression;
  DWORD PhotometricInterp;
  DWORD LineOrder;
  DWORD RawDataOffset;
  DWORD RawDataSize;
  DWORD PaletteOffset;
  DWORD PaletteSize;
} WIA_RAW_HEADER;
```



## <a name="members"></a><span data-ttu-id="a457d-106">Member</span><span class="sxs-lookup"><span data-stu-id="a457d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a457d-107">**Tag**</span><span class="sxs-lookup"><span data-stu-id="a457d-107">**Tag**</span></span>
</dt> <dd>

<span data-ttu-id="a457d-108">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="a457d-108">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="a457d-109">Der Name des Formats.</span><span class="sxs-lookup"><span data-stu-id="a457d-109">The name of the format.</span></span> <span data-ttu-id="a457d-110">Dabei muss es sich um das Literale "wraw" (vier Einzel Byte-ASCII-Zeichen) handeln.</span><span class="sxs-lookup"><span data-stu-id="a457d-110">This must be the literal 'WRAW' (four single byte ASCII characters).</span></span>

</dd> <dt>

<span data-ttu-id="a457d-111">**Version**</span><span class="sxs-lookup"><span data-stu-id="a457d-111">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="a457d-112">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="a457d-112">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="a457d-113">Die Version des RAW-Formats.</span><span class="sxs-lookup"><span data-stu-id="a457d-113">The version of the RAW format.</span></span> <span data-ttu-id="a457d-114">Verwenden Sie immer 0x00010000 bis.</span><span class="sxs-lookup"><span data-stu-id="a457d-114">Always use 0x00010000.</span></span>

</dd> <dt>

<span data-ttu-id="a457d-115">**HeaderSize**</span><span class="sxs-lookup"><span data-stu-id="a457d-115">**HeaderSize**</span></span>
</dt> <dd>

<span data-ttu-id="a457d-116">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="a457d-116">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="a457d-117">Die Gesamtanzahl der gültigen Bytes in der Kopfzeile.</span><span class="sxs-lookup"><span data-stu-id="a457d-117">The total valid bytes in the header.</span></span>

</dd> <dt>

<span data-ttu-id="a457d-118">**Xres**</span><span class="sxs-lookup"><span data-stu-id="a457d-118">**XRes**</span></span>
</dt> <dd>

<span data-ttu-id="a457d-119">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="a457d-119">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="a457d-120">Die horizontale Auflösung als DPI-Wert.</span><span class="sxs-lookup"><span data-stu-id="a457d-120">The horizontal resolution in dots per inch.</span></span>

</dd> <dt>

<span data-ttu-id="a457d-121">**Yres**</span><span class="sxs-lookup"><span data-stu-id="a457d-121">**YRes**</span></span>
</dt> <dd>

<span data-ttu-id="a457d-122">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="a457d-122">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="a457d-123">Die vertikale Auflösung als DPI-Wert.</span><span class="sxs-lookup"><span data-stu-id="a457d-123">The vertical resolution in dots per inch.</span></span>

</dd> <dt>

<span data-ttu-id="a457d-124">**XBlock**</span><span class="sxs-lookup"><span data-stu-id="a457d-124">**XExtent**</span></span>
</dt> <dd>

<span data-ttu-id="a457d-125">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="a457d-125">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="a457d-126">Die Breite des Bilds in Pixel.</span><span class="sxs-lookup"><span data-stu-id="a457d-126">The width of the image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="a457d-127">**Yblock**</span><span class="sxs-lookup"><span data-stu-id="a457d-127">**YExtent**</span></span>
</dt> <dd>

<span data-ttu-id="a457d-128">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="a457d-128">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="a457d-129">Die Höhe des Bilds in Pixel.</span><span class="sxs-lookup"><span data-stu-id="a457d-129">The height of the image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="a457d-130">**Bytesperline**</span><span class="sxs-lookup"><span data-stu-id="a457d-130">**BytesPerLine**</span></span>
</dt> <dd>

<span data-ttu-id="a457d-131">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="a457d-131">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="a457d-132">Die Anzahl der Bytes in einer Zeile eines unkomprimierten Bilds.</span><span class="sxs-lookup"><span data-stu-id="a457d-132">The number of bytes in a line of an uncompressed image.</span></span> <span data-ttu-id="a457d-133">Verwenden Sie 0, wenn die Daten komprimiert werden, um zu signalisieren, dass die Anzahl der Bytes pro Zeile unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="a457d-133">Use 0 when the data is compressed to signal that the number of bytes per line is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="a457d-134">**Bitsper Pixel**</span><span class="sxs-lookup"><span data-stu-id="a457d-134">**BitsPerPixel**</span></span>
</dt> <dd>

<span data-ttu-id="a457d-135">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="a457d-135">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="a457d-136">Die Gesamtanzahl der Bits pro Pixel für alle Kanäle des Pixels.</span><span class="sxs-lookup"><span data-stu-id="a457d-136">The total number of bits per pixel for all the pixel's channels.</span></span>

</dd> <dt>

<span data-ttu-id="a457d-137">**Channelsperpixel**</span><span class="sxs-lookup"><span data-stu-id="a457d-137">**ChannelsPerPixel**</span></span>
</dt> <dd>

<span data-ttu-id="a457d-138">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="a457d-138">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="a457d-139">Die Anzahl der farbchannels in einem Pixel.</span><span class="sxs-lookup"><span data-stu-id="a457d-139">The number of color channels in a pixel.</span></span>

</dd> <dt>

<span data-ttu-id="a457d-140">**DataType**</span><span class="sxs-lookup"><span data-stu-id="a457d-140">**DataType**</span></span>
</dt> <dd>

<span data-ttu-id="a457d-141">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="a457d-141">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="a457d-142">Der WIA \_ IPA- \_ Datentyp des Bilds.</span><span class="sxs-lookup"><span data-stu-id="a457d-142">The WIA\_IPA\_DATATYPE of the image.</span></span> <span data-ttu-id="a457d-143">Da das WIA \_ IPA- \_ Format auf wiaimgfmt RAW festgelegt ist \_ , ist dies eine Liste zulässiger Werte, von denen die Anwendung auswählt.</span><span class="sxs-lookup"><span data-stu-id="a457d-143">Since WIA\_IPA\_FORMAT is set to WiaImgFmt\_RAW, this is a list of allowed values from which the application picks.</span></span>

</dd> <dt>

<span data-ttu-id="a457d-144">**Bitsperchannel \[ 8\]**</span><span class="sxs-lookup"><span data-stu-id="a457d-144">**BitsPerChannel\[8\]**</span></span>
</dt> <dd>

<span data-ttu-id="a457d-145">Type: **Byte**</span><span class="sxs-lookup"><span data-stu-id="a457d-145">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="a457d-146">Die Anzahl der Bits in einem Kanal bis maximal 8.</span><span class="sxs-lookup"><span data-stu-id="a457d-146">The number of bits in a channel, up to a maximum of 8.</span></span>

</dd> <dt>

<span data-ttu-id="a457d-147">**Komprimierung**</span><span class="sxs-lookup"><span data-stu-id="a457d-147">**Compression**</span></span>
</dt> <dd>

<span data-ttu-id="a457d-148">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="a457d-148">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="a457d-149">Ein WIA- \_ IPA- \_ Komprimierungs Wert, der den verwendeten Komprimierungstyp angibt, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a457d-149">A WIA\_IPA\_COMPRESSION value specifying the type of compression used, if any.</span></span>

</dd> <dt>

<span data-ttu-id="a457d-150">**Photomezcinterp**</span><span class="sxs-lookup"><span data-stu-id="a457d-150">**PhotometricInterp**</span></span>
</dt> <dd>

<span data-ttu-id="a457d-151">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="a457d-151">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="a457d-152">Ein WIA \_ IPA- \_ Wert für die photometrische \_ interp, der die photometrische Interpretation des Bilds angibt.</span><span class="sxs-lookup"><span data-stu-id="a457d-152">A WIA\_IPA\_PHOTOMETRIC\_INTERP value specifying the photometric interpretation of the image.</span></span>

</dd> <dt>

<span data-ttu-id="a457d-153">**Lineorder**</span><span class="sxs-lookup"><span data-stu-id="a457d-153">**LineOrder**</span></span>
</dt> <dd>

<span data-ttu-id="a457d-154">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="a457d-154">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="a457d-155">Ein Wert, der die Reihenfolge der Bildzeilen darstellt.</span><span class="sxs-lookup"><span data-stu-id="a457d-155">A value representing the image line order.</span></span> <span data-ttu-id="a457d-156">Dabei handelt es sich immer \_ um eine Zeile von \_ \_ oben \_ nach \_ unten oder eine \_ Zeilen \_ Reihenfolge \_ \_ von unten nach \_ oben.</span><span class="sxs-lookup"><span data-stu-id="a457d-156">This is always either WIA\_LINE\_ORDER\_TOP\_TO\_BOTTOM or WIA\_LINE\_ORDER\_BOTTOM\_TO\_TOP.</span></span>

</dd> <dt>

<span data-ttu-id="a457d-157">**Rawdataoffset**</span><span class="sxs-lookup"><span data-stu-id="a457d-157">**RawDataOffset**</span></span>
</dt> <dd>

<span data-ttu-id="a457d-158">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="a457d-158">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="a457d-159">Die Position der Rohbilddaten in Bytes, beginnend an der Position, an der die Kopfzeile endet, oder an der Position, an der die Palette endet.</span><span class="sxs-lookup"><span data-stu-id="a457d-159">The position of the raw image data in bytes, starting from position where the header ends or the position where the palette ends.</span></span>

</dd> <dt>

<span data-ttu-id="a457d-160">**Rawdatasize**</span><span class="sxs-lookup"><span data-stu-id="a457d-160">**RawDataSize**</span></span>
</dt> <dd>

<span data-ttu-id="a457d-161">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="a457d-161">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="a457d-162">Die Größe der Rohbilddaten in Bytes.</span><span class="sxs-lookup"><span data-stu-id="a457d-162">The size, in bytes, of the raw image data.</span></span>

</dd> <dt>

<span data-ttu-id="a457d-163">**Paletteoffset**</span><span class="sxs-lookup"><span data-stu-id="a457d-163">**PaletteOffset**</span></span>
</dt> <dd>

<span data-ttu-id="a457d-164">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="a457d-164">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="a457d-165">Die Position der Palette in Bytes, beginnend an der Position, an der die Kopfzeile endet, oder an der Position, an der die Daten enden.</span><span class="sxs-lookup"><span data-stu-id="a457d-165">The position of the palette in bytes, starting from the position where the header ends or the position where the data ends.</span></span> <span data-ttu-id="a457d-166">(Dieser Wert ist 0 (null), wenn keine Palette vorhanden ist.)</span><span class="sxs-lookup"><span data-stu-id="a457d-166">(This value is 0, if there is no palette.)</span></span>

</dd> <dt>

<span data-ttu-id="a457d-167">**Palettesize**</span><span class="sxs-lookup"><span data-stu-id="a457d-167">**PaletteSize**</span></span>
</dt> <dd>

<span data-ttu-id="a457d-168">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="a457d-168">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="a457d-169">Die Größe der Palettentabelle in Byte.</span><span class="sxs-lookup"><span data-stu-id="a457d-169">The size, in bytes, of the palette table.</span></span> <span data-ttu-id="a457d-170">(Dieser Wert ist 0, wenn keine Palette vorhanden ist.)</span><span class="sxs-lookup"><span data-stu-id="a457d-170">(This is 0, if there is no palette.)</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a457d-171">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a457d-171">Remarks</span></span>

<span data-ttu-id="a457d-172">Da es sich hierbei nicht um ein Dateiformat handelt, verwenden Sie eine leere Zeichenfolge für die WIA \_ IPA- \_ Datei \_ Erweiterungs Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a457d-172">Because this is not a file format, use an empty string for the WIA\_IPA\_FILE\_EXTENSION property.</span></span>

<span data-ttu-id="a457d-173">Die Palette und die Daten können in einer der beiden Reihenfolge stehen.</span><span class="sxs-lookup"><span data-stu-id="a457d-173">The palette and the data can come in either order.</span></span>

<span data-ttu-id="a457d-174">**Rawdatasize** enthält weder den Header noch die Palette.</span><span class="sxs-lookup"><span data-stu-id="a457d-174">**RawDataSize** does not include either the header or the palette.</span></span> <span data-ttu-id="a457d-175">Verwenden Sie dieses Feld, um zu überprüfen, ob die Übertragung des Abbilds erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="a457d-175">Use this field to verify that the transfer of the image has been successful.</span></span>

<span data-ttu-id="a457d-176">**Palettesize** ist bytes, nicht die Anzahl der Einträge in der Palette.</span><span class="sxs-lookup"><span data-stu-id="a457d-176">**PaletteSize** is bytes, not the number of entries in the palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="a457d-177">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a457d-177">Requirements</span></span>



| <span data-ttu-id="a457d-178">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a457d-178">Requirement</span></span> | <span data-ttu-id="a457d-179">Wert</span><span class="sxs-lookup"><span data-stu-id="a457d-179">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a457d-180">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a457d-180">Minimum supported client</span></span><br/> | <span data-ttu-id="a457d-181">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a457d-181">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a457d-182">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a457d-182">Minimum supported server</span></span><br/> | <span data-ttu-id="a457d-183">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a457d-183">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a457d-184">Header</span><span class="sxs-lookup"><span data-stu-id="a457d-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="a457d-185"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="a457d-185"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




