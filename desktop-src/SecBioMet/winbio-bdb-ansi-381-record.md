---
title: WINBIO_BDB_ANSI_381_RECORD -Struktur (Winbio \_ types.h)
description: Enthält Informationen zu einem einzelnen Fingerabdruck- oder Handflächenbeispiel eines Endbenutzers.
ms.assetid: e0b32d05-3e96-4b42-9e18-57d10513f224
keywords:
- WINBIO_BDB_ANSI_381_RECORD Struktur Windows Biometrieframework-API
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
ms.openlocfilehash: 15e30cd66348245aa3090fb21188d7d1cea347c1b28ee51243d2effd9b52609f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119480340"
---
# <a name="winbio_bdb_ansi_381_record-structure"></a>WINBIO \_ BDB \_ ANSI \_ 381 \_ RECORD-Struktur

Die **WINBIO \_ BDB \_ ANSI \_ 381 \_ RECORD-Struktur** enthält Informationen zu einem einzelnen Fingerabdruck- oder Handflächenbeispiel eines Endbenutzers. Eine Auflistung dieser Strukturen ist in jeder [**WINBIO \_ BDB \_ ANSI \_ 381 \_ HEADER-Struktur**](winbio-bdb-ansi-381-header.md) enthalten.

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

**BlockLength**
</dt> <dd>

Enthält die Anzahl der Bytes in dieser Struktur plus die Anzahl der Bytes von Beispielbilddaten.

</dd> <dt>

**HorizontalLineLength**
</dt> <dd>

Gibt die Anzahl von Pixeln in einer horizontalen Linie des Beispiels an.

</dd> <dt>

**VerticalLineLength**
</dt> <dd>

Gibt die Anzahl der Pixel in einer vertikalen Linie des Beispiels an.

</dd> <dt>

**Position**
</dt> <dd>

Ein **WINBIO \_ BIOMETRIC \_ SUBTYPE-Wert,** der den Finger oder die Handfläche angibt, der bzw. die zum Generieren der biometrischen Stichprobe verwendet wird. Weitere Informationen finden Sie in den Hinweisen.

</dd> <dt>

**CountOfViews**
</dt> <dd>

Dies muss auf eins (1) festgelegt werden.

</dd> <dt>

**ViewNumber**
</dt> <dd>

Dies muss auf eins (1) festgelegt werden.

</dd> <dt>

**ImageQuality**
</dt> <dd>

Reserviert. Dieser muss 254 (0xFE) sein.

</dd> <dt>

**ImpressionType**
</dt> <dd>

Reserviert.

</dd> <dt>

**Reserved**
</dt> <dd>

Reserviert. Muss auf 0 (null) festgelegt werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das *Position-Element* gibt den Bereich der Hand oder Handfläche an, der bzw. die verwendet wird, um die biometrische Stichprobe zu machen. Das Windows Biometric Framework (WBF) unterstützt derzeit nur die Fingerabdruckerfassung und verwendet die folgenden Konstanten, um Positionsinformationen zu darstellen.

-   WINBIO \_ ANSI \_ 381 \_ POS \_ UNKNOWN
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ THUMB
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ INDEX \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ MIDDLE \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ RING \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ LITTLE \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LSFINGER \_
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ INDEX \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ \_ LENK-MITTELFINGER \_
-   WINBIO \_ ANSI \_ 381 \_ POS \_ \_ LN-RINGFINGER \_
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ LITTLE \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ FOUR \_ FINGERS
-   WINBIO \_ ANSI \_ 381 \_ POS \_ \_ 4 \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS ZWEI \_ \_ DAUMEN

> [!IMPORTANT]
>
> Versuchen Sie nicht, den für den Position-Wert angegebenen *Wert zu* überprüfen. Der Windows Biometriedienst überprüft den angegebenen Wert, bevor er an Ihre Implementierung übergeben wird. Wenn der Wert **WINBIO \_ SUBTYPE \_ NO \_ INFORMATION** oder **WINBIO \_ SUBTYPE \_ ANY ist,** überprüfen Sie gegebenenfalls.

 

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

 

 





