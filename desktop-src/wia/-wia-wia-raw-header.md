---
description: Die WIA \_ RAW \_ HEADER-Struktur definiert ein Bild im RAW-Datenformat eines Geräts und ermöglicht Anwendungen die Verwendung des RAW-Formats in Windows Wia-Übertragungen (Image Acquisition).
ms.assetid: c7b50816-d596-4c62-a00e-cd8d6e303e42
title: WIA_RAW_HEADER-Struktur (Wiadef.h)
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
ms.openlocfilehash: 2b4e89f47737788fa9ebf238f06f6420eafbc31d7b27ab7933372d0716fb6588
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812950"
---
# <a name="wia_raw_header-structure"></a>WIA \_ RAW \_ HEADER-Struktur

Die **WIA \_ RAW \_ HEADER-Struktur** definiert ein Bild im RAW-Datenformat eines Geräts und ermöglicht Anwendungen die Verwendung des RAW-Formats in Windows Übertragungen der Bilderfassung (WIA).

## <a name="syntax"></a>Syntax


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



## <a name="members"></a>Member

<dl> <dt>

**Tag**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Der Name des Formats. Dies muss das Literal "WRAW" (vier EINZELNE BYTE-ASCII-Zeichen) sein.

</dd> <dt>

**Version**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die Version des RAW-Formats. Verwenden Sie immer 0x00010000.

</dd> <dt>

**HeaderSize**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die insgesamt gültigen Bytes im Header.

</dd> <dt>

**XRes**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die horizontale Auflösung als DPI-Wert.

</dd> <dt>

**YRes**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die vertikale Auflösung als DPI-Wert.

</dd> <dt>

**XExtent**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die Breite des Bilds in Pixel.

</dd> <dt>

**YExtent**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die Höhe des Bilds in Pixel.

</dd> <dt>

**BytesPerLine**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die Anzahl der Bytes in einer Zeile eines nicht komprimierten Bilds. Verwenden Sie 0, wenn die Daten komprimiert werden, um zu signalisieren, dass die Anzahl der Bytes pro Zeile unbekannt ist.

</dd> <dt>

**BitsPerPixel**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die Gesamtanzahl von Bits pro Pixel für alle Kanäle des Pixels.

</dd> <dt>

**ChannelsPerPixel**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die Anzahl der Farbkanäle in einem Pixel.

</dd> <dt>

**DataType**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Der WIA \_ \_ IPA-DATENTYP des Bilds. Da WIA \_ IPA \_ FORMAT auf WiaImgFmt RAW festgelegt \_ ist, ist dies eine Liste der zulässigen Werte, aus denen die Anwendung wählt.

</dd> <dt>

**BitsPerChannel \[ 8\]**
</dt> <dd>

Typ: **BYTE**

</dd> <dd>

Die Anzahl der Bits in einem Kanal, bis zu einem Maximum von 8.

</dd> <dt>

**Komprimierung**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Ein WIA \_ IPA \_ COMPRESSION-Wert, der ggf. den Typ der verwendeten Komprimierung angibt.

</dd> <dt>

**PhotometricInterp**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Ein WIA \_ IPA \_ PHOTOMETRIC \_ INTERP-Wert, der die fotometrische Interpretation des Bilds angibt.

</dd> <dt>

**LineOrder**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Ein -Wert, der die Bildzeilenreihenfolge darstellt. Dies ist immer ENTWEDER WIA \_ LINE ORDER TOP TO BOTTOM oder \_ \_ \_ \_ WIA LINE ORDER BOTTOM \_ TO \_ \_ \_ \_ TOP.

</dd> <dt>

**RawDataOffset**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die Position der Rohbilddaten in Bytes, beginnend an der Position, an der der Header endet, oder an der Position, an der die Palette endet.

</dd> <dt>

**RawDataSize**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die Größe der Rohdaten des Bilds in Bytes.

</dd> <dt>

**PaletteOffset**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die Position der Palette in Bytes, beginnend mit der Position, an der der Header endet, oder der Position, an der die Daten enden. (Dieser Wert ist 0, wenn keine Palette vorhanden ist.)

</dd> <dt>

**PaletteSize**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die Größe der Palettentabelle in Bytes. (Dies ist 0, wenn keine Palette vorhanden ist.)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Da dies kein Dateiformat ist, verwenden Sie eine leere Zeichenfolge für die WIA \_ IPA \_ FILE \_ EXTENSION-Eigenschaft.

Die Palette und die Daten können in beiden Reihenfolgen angezeigt werden.

**RawDataSize** enthält weder den Header noch die Palette. Verwenden Sie dieses Feld, um zu überprüfen, ob die Übertragung des Images erfolgreich war.

**PaletteSize** ist Bytes, nicht die Anzahl der Einträge in der Palette.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wiadef.h</dt> </dl> |



 

 




