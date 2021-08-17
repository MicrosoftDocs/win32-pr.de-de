---
title: WINBIO_BDB_ANSI_381_HEADER -Struktur (Winbio \_ types.h)
description: Gibt Informationen zu einer Reihe von Fingerabdruck- oder Handflächenbeispielen an.
ms.assetid: 8b0caa50-9bba-45c4-b4bf-514540894793
keywords:
- WINBIO_BDB_ANSI_381_HEADER Struktur Windows Biometrieframework-API
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
ms.openlocfilehash: 3bc9eee5d3ca99799c76b849e7b990eee2b94c61309c4d729f736ad33a00eecc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911278"
---
# <a name="winbio_bdb_ansi_381_header-structure"></a>WINBIO \_ BDB \_ ANSI \_ 381 \_ HEADER-Struktur

Die **WINBIO \_ BDB \_ ANSI \_ 381 \_ HEADER-Struktur** gibt Informationen zu einer Reihe von Fingerabdruck- oder Handflächenbeispielen an.

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

**Recordlength**
</dt> <dd>

Die Größe dieser Struktur in Bytes plus die Größe aller [**WINBIO \_ BDB \_ ANSI \_ 381 \_ RECORD-Strukturen**](winbio-bdb-ansi-381-record.md) für die Fingerabdruck- oder Handflächenbeispiele, die von einem Endbenutzer erfasst wurden. Nur die niedrigen sechs Bytes sind gültig.

</dd> <dt>

**FormatIdentifier**
</dt> <dd>

Gibt das Format an. Derzeit muss dies 0x46495200.

</dd> <dt>

**VersionNumber**
</dt> <dd>

Gibt die Versionsnummer an. Derzeit muss dies 0x30313000, was intern 0.1.0.0 entspricht.

</dd> <dt>

**ProductId**
</dt> <dd>

Eine [**WINBIO \_ REGISTERED \_ FORMAT-Struktur,**](winbio-registered-format.md) die das registrierte Datenformat als Besitzer-Typ-Paar enthält.

</dd> <dt>

**CaptureDeviceId**
</dt> <dd>

Enthält die Einheiten-ID des Geräts, das zum Erfassen des Beispiels verwendet wird.

</dd> <dt>

**ImageAcquisitionLevel**
</dt> <dd>

Gibt die Auflösungsebene an, auf der das Beispiel erfasst wird.

</dd> <dt>

**HorizontalScanResolution**
</dt> <dd>

Gibt die horizontale Auflösung des Scans an.

</dd> <dt>

**VerticalScanResolution**
</dt> <dd>

Gibt die vertikale Auflösung des Scans an.

</dd> <dt>

**HorizontalImageResolution**
</dt> <dd>

Gibt die horizontale Auflösung des erfassten Fingerabdrucks oder Handflächenbilds an.

</dd> <dt>

**VerticalImageResolution**
</dt> <dd>

Gibt die vertikale Auflösung des erfassten Fingerabdrucks oder Handflächenbilds an.

</dd> <dt>

**ElementCount**
</dt> <dd>

Anzahl der Finger- oder Handflächendatensätze in dieser Struktur.

</dd> <dt>

**ScaleUnits**
</dt> <dd>

Enthält die Maßeinheit, 1 für Zoll und 2 für Zentimeter.

</dd> <dt>

**PixelDepth**
</dt> <dd>

Gibt die Anzahl der Bits in einem Pixel an. Dies kann 1 bis 16 Bits pro Pixel für Farbe sein.

</dd> <dt>

**ImageCompressionAlg**
</dt> <dd>

Gibt den Algorithmus an, der zum Komprimieren des Finger- oder Handflächenbilds verwendet wird.

</dd> <dt>

**Reserved**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (einschließlich Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Clientanwendungsstrukturen](client-application-structures.md)
</dt> </dl>

 

 





