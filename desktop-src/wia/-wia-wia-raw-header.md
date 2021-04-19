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
# <a name="wia_raw_header-structure"></a>WIA \_ - \_ rohheader Struktur

Die **WIA \_ - \_ rohheaderstruktur** definiert ein Bild im RAW-Datenformat eines Geräts und ermöglicht es Anwendungen, bei der Übertragung von Windows-Bild Käufen (WIA) das RAW-Format zu verwenden.

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

Der Name des Formats. Dabei muss es sich um das Literale "wraw" (vier Einzel Byte-ASCII-Zeichen) handeln.

</dd> <dt>

**Version**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die Version des RAW-Formats. Verwenden Sie immer 0x00010000 bis.

</dd> <dt>

**HeaderSize**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die Gesamtanzahl der gültigen Bytes in der Kopfzeile.

</dd> <dt>

**Xres**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die horizontale Auflösung als DPI-Wert.

</dd> <dt>

**Yres**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die vertikale Auflösung als DPI-Wert.

</dd> <dt>

**XBlock**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die Breite des Bilds in Pixel.

</dd> <dt>

**Yblock**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die Höhe des Bilds in Pixel.

</dd> <dt>

**Bytesperline**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die Anzahl der Bytes in einer Zeile eines unkomprimierten Bilds. Verwenden Sie 0, wenn die Daten komprimiert werden, um zu signalisieren, dass die Anzahl der Bytes pro Zeile unbekannt ist.

</dd> <dt>

**Bitsper Pixel**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die Gesamtanzahl der Bits pro Pixel für alle Kanäle des Pixels.

</dd> <dt>

**Channelsperpixel**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die Anzahl der farbchannels in einem Pixel.

</dd> <dt>

**DataType**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Der WIA \_ IPA- \_ Datentyp des Bilds. Da das WIA \_ IPA- \_ Format auf wiaimgfmt RAW festgelegt ist \_ , ist dies eine Liste zulässiger Werte, von denen die Anwendung auswählt.

</dd> <dt>

**Bitsperchannel \[ 8\]**
</dt> <dd>

Type: **Byte**

</dd> <dd>

Die Anzahl der Bits in einem Kanal bis maximal 8.

</dd> <dt>

**Komprimierung**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Ein WIA- \_ IPA- \_ Komprimierungs Wert, der den verwendeten Komprimierungstyp angibt, sofern vorhanden.

</dd> <dt>

**Photomezcinterp**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Ein WIA \_ IPA- \_ Wert für die photometrische \_ interp, der die photometrische Interpretation des Bilds angibt.

</dd> <dt>

**Lineorder**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Ein Wert, der die Reihenfolge der Bildzeilen darstellt. Dabei handelt es sich immer \_ um eine Zeile von \_ \_ oben \_ nach \_ unten oder eine \_ Zeilen \_ Reihenfolge \_ \_ von unten nach \_ oben.

</dd> <dt>

**Rawdataoffset**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die Position der Rohbilddaten in Bytes, beginnend an der Position, an der die Kopfzeile endet, oder an der Position, an der die Palette endet.

</dd> <dt>

**Rawdatasize**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die Größe der Rohbilddaten in Bytes.

</dd> <dt>

**Paletteoffset**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die Position der Palette in Bytes, beginnend an der Position, an der die Kopfzeile endet, oder an der Position, an der die Daten enden. (Dieser Wert ist 0 (null), wenn keine Palette vorhanden ist.)

</dd> <dt>

**Palettesize**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die Größe der Palettentabelle in Byte. (Dieser Wert ist 0, wenn keine Palette vorhanden ist.)

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Da es sich hierbei nicht um ein Dateiformat handelt, verwenden Sie eine leere Zeichenfolge für die WIA \_ IPA- \_ Datei \_ Erweiterungs Eigenschaft.

Die Palette und die Daten können in einer der beiden Reihenfolge stehen.

**Rawdatasize** enthält weder den Header noch die Palette. Verwenden Sie dieses Feld, um zu überprüfen, ob die Übertragung des Abbilds erfolgreich war.

**Palettesize** ist bytes, nicht die Anzahl der Einträge in der Palette.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 




