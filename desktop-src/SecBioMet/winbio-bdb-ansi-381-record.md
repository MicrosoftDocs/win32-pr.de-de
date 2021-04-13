---
title: WINBIO_BDB_ANSI_381_RECORD Struktur (winbio \_ types. h)
description: Enthält Informationen zu einem einzelnen Fingerabdruck oder einem Palmen Beispiel von einem Endbenutzer.
ms.assetid: e0b32d05-3e96-4b42-9e18-57d10513f224
keywords:
- WINBIO_BDB_ANSI_381_RECORD Struktur Windows-Biometrieframework-API
topic_type:
- apiref
api_name:
- WINBIO_BDB_ANSI_381_RECORD
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f30af31d88349dbe02066f231cdff21293aebe90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391570"
---
# <a name="winbio_bdb_ansi_381_record-structure"></a>Struktur von winbio \_ BDB \_ ANSI \_ 381- \_ Datensätzen

Die Struktur von **winbio \_ BDB \_ ANSI \_ 381 \_** -Datensätzen enthält Informationen zu einem einzelnen Fingerabdruck oder einem Palmen Beispiel von einem Endbenutzer. Eine Auflistung dieser Strukturen ist in jeder [**winbio \_ BDB- \_ ANSI \_ 381- \_ Header**](winbio-bdb-ansi-381-header.md) Struktur enthalten.

## <a name="syntax"></a>Syntax


```C++
typedef struct _WINBIO_BDB_ANSI_381_RECORD {
  ULONG                    BlockLength;
  USHORT                   HorizontalLineLength;
  USHORT                   VerticalLineLength;
  WINBIO_BIOMETRIC_SUBTYPE Position;
  UCHAR                    CountOfViews;
  UCHAR                    ViewNumber;
  UCHAR                    ImageQuality;
  UCHAR                    ImpressionType;
  UCHAR                    Reserved;
} WINBIO_BDB_ANSI_381_RECORD;
```



## <a name="members"></a>Member

<dl> <dt>

**Blocklength**
</dt> <dd>

Enthält die Anzahl der Bytes in dieser Struktur zuzüglich der Anzahl von Bytes von Beispiel Bilddaten.

</dd> <dt>

**Horizontallinelength**
</dt> <dd>

Gibt die Anzahl der Pixel in einer horizontalen Zeile des Beispiels an.

</dd> <dt>

**Verticallinelength**
</dt> <dd>

Gibt die Anzahl der Pixel in einer vertikalen Zeile des Beispiels an.

</dd> <dt>

**Position**
</dt> <dd>

Ein Wert des **Typs "winbio \_ biometrische \_ SubType** ", der den Finger oder die Palme angibt, mit dem das biometrische Beispiel generiert wird. Weitere Informationen finden Sie in den Hinweisen.

</dd> <dt>

**Ansichts Ansichten**
</dt> <dd>

Diese muss auf 1 festgelegt werden.

</dd> <dt>

**Viewnumber**
</dt> <dd>

Diese muss auf 1 festgelegt werden.

</dd> <dt>

**ImageQuality**
</dt> <dd>

Reserviert. Dies muss 254 (0xFE) sein.

</dd> <dt>

**Impressiontype**
</dt> <dd>

Reserviert.

</dd> <dt>

**Reserved**
</dt> <dd>

Reserviert. Muss auf 0 (null) festgelegt werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der *Positions* Member gibt den Bereich der Hand oder der Palme an, der zum Erstellen des biometrischen Beispiels verwendet wird. Der Windows-Biometrieframework (WBF) unterstützt derzeit nur die Fingerabdruck Erfassung und verwendet die folgenden Konstanten, um Positionsinformationen darzustellen.

-   Winbio \_ ANSI \_ 381 Torys \_ \_ unbekannt
-   Winbio \_ ANSI \_ 381 \_ POS, \_ RH \_ Thumb
-   Winbio \_ ANSI \_ 381 POS-Zeige- \_ \_ \_ \_ Finger
-   Winbio \_ ANSI \_ 381 \_ Torpo- \_ \_ \_ Mittelfinger
-   Winbio \_ ANSI \_ 381 \_ POS, \_ RH- \_ Klingel \_ Finger
-   Winbio \_ ANSI \_ 381 Torys \_ \_ RH \_ Little \_ Finger
-   Winbio \_ ANSI \_ 381 \_ POS \_ LH \_ Thumb
-   Winbio \_ ANSI \_ 381 Torys \_ \_ LH \_ Index \_ Finger
-   Winbio \_ ANSI \_ 381 \_ POS \_ - \_ Mittel \_ Fingerabdruck
-   Winbio \_ ANSI \_ 381 Torys LH- \_ \_ \_ Klingel \_ Finger
-   Winbio \_ ANSI \_ 381 Torys \_ \_ LH \_ wenig \_ Finger
-   Winbio \_ ANSI 381 Torys mit \_ \_ \_ \_ vier \_ Fingern
-   Winbio \_ ANSI 381 Torys mit \_ \_ \_ \_ vier \_ Fingern
-   Winbio \_ ANSI \_ 381 \_ POS \_ zwei \_ Daumen

> [!IMPORTANT]
>
> Versuchen Sie nicht, den für den *Positions* Wert angegebenen Wert zu überprüfen. Der Windows-Biometrie-Dienst überprüft den angegebenen Wert vor der Übergabe an Ihre Implementierung. Wenn der Wert " **winbio \_ SubType \_ No \_ Information** " oder " **winbio \_ SubType \_ any**" lautet, überprüfen Sie ggf. ggf.

 

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

 

 





