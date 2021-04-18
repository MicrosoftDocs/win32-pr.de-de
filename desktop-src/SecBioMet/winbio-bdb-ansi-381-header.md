---
title: WINBIO_BDB_ANSI_381_HEADER Struktur (winbio \_ types. h)
description: Gibt Informationen zu einer Reihe von Fingerabdruck-oder Palmen Beispielen an.
ms.assetid: 8b0caa50-9bba-45c4-b4bf-514540894793
keywords:
- WINBIO_BDB_ANSI_381_HEADER Struktur Windows-Biometrieframework-API
topic_type:
- apiref
api_name:
- WINBIO_BDB_ANSI_381_HEADER
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9da04643bbdff273a2594394011ba46c16bfa29d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345293"
---
# <a name="winbio_bdb_ansi_381_header-structure"></a>Winbio \_ BDB- \_ ANSI \_ 381- \_ Header Struktur

Die **Header Struktur von winbio \_ BDB \_ ANSI \_ 381 \_** gibt Informationen zu einer Reihe von Fingerabdruck-oder Palmen Beispielen an.

## <a name="syntax"></a>Syntax


```C++
typedef struct _WINBIO_BDB_ANSI_381_HEADER {
  ULONG64                  RecordLength;
  ULONG                    FormatIdentifier;
  ULONG                    VersionNumber;
  WINBIO_REGISTERED_FORMAT ProductId;
  USHORT                   CaptureDeviceId;
  USHORT                   ImageAcquisitionLevel;
  USHORT                   HorizontalScanResolution;
  USHORT                   VerticalScanResolution;
  USHORT                   HorizontalImageResolution;
  USHORT                   VerticalImageResolution;
  UCHAR                    ElementCount;
  UCHAR                    ScaleUnits;
  UCHAR                    PixelDepth;
  UCHAR                    ImageCompressionAlg;
  USHORT                   Reserved;
} WINBIO_BDB_ANSI_381_HEADER;
```



## <a name="members"></a>Member

<dl> <dt>

**RecordLength**
</dt> <dd>

Die Größe dieser Struktur in Bytes zuzüglich der Größe aller [**winbio \_ BDB- \_ ANSI \_ 381- \_ Daten Satz**](winbio-bdb-ansi-381-record.md) Strukturen für den Fingerabdruck oder die von einem Endbenutzer erfassten Palmen Beispiele. Nur die unteren sechs Bytes sind gültig.

</dd> <dt>

**Formatiertifier**
</dt> <dd>

Gibt das Format an. Derzeit muss dies 0x46495200 sein.

</dd> <dt>

**VersionNumber**
</dt> <dd>

Gibt die Versionsnummer an. Derzeit muss dies 0x30313000 sein, das intern 0.1.0.0 entspricht.

</dd> <dt>

**ProductId**
</dt> <dd>

Eine [**winbio- \_ registrierte \_ Format**](winbio-registered-format.md) Struktur, die das registrierte Datenformat als Besitzer-/typpaar enthält.

</dd> <dt>

**Capturede viceid**
</dt> <dd>

Enthält die Einheiten-ID des Geräts, das zum Erfassen des Beispiels verwendet wird.

</dd> <dt>

**Imageacquisitionlevel**
</dt> <dd>

Gibt die Auflösungsebene an, bei der das Beispiel aufgezeichnet wird.

</dd> <dt>

**Horizontalscanresolution**
</dt> <dd>

Gibt die horizontale Auflösung der Überprüfung an.

</dd> <dt>

**Verticalscanresolution**
</dt> <dd>

Gibt die vertikale Auflösung der Überprüfung an.

</dd> <dt>

**Horizontalimageresolution**
</dt> <dd>

Gibt die horizontale Auflösung des aufgezeichneten Finger Abbilds oder des Palm Bilds an.

</dd> <dt>

**Verticalimageresolution**
</dt> <dd>

Gibt die vertikale Auflösung des aufgezeichneten Finger Abbilds oder des Palm Bilds an.

</dd> <dt>

**Element count**
</dt> <dd>

Anzahl der Finger-oder Palmen Datensätze in dieser Struktur.

</dd> <dt>

**ScaleUnits**
</dt> <dd>

Enthält die Maßeinheit 1 für Zoll und 2 für Zentimeter.

</dd> <dt>

**Pixeltiefe**
</dt> <dd>

Gibt die Anzahl der Bits in einem Pixel an. Der Wert kann zwischen 1 und 16 Bits pro Pixel liegen.

</dd> <dt>

**Imagecompressionalg**
</dt> <dd>

Gibt den Algorithmus an, der zum Komprimieren des Fingers oder des Palmen Bilds verwendet wird.

</dd> <dt>

**Reserved**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types. h (Include winbio. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Client Anwendungs Strukturen](client-application-structures.md)
</dt> </dl>

 

 





