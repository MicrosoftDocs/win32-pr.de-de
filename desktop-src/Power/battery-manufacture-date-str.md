---
description: Enthält das Erstellungstag eines Akkus.
ms.assetid: 0cda66fc-bf4a-4a38-b43c-6eecde46c414
title: BATTERY_MANUFACTURE_DATE-Struktur (poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_MANUFACTURE_DATE
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: cdd3f067bc3ed2e3339710e0a5bd48c8f42e6525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362223"
---
# <a name="battery_manufacture_date-structure"></a>\_ \_ Datums Struktur der Akku Fertigung

Enthält das Erstellungstag eines Akkus. Diese Struktur wird von der Struktur der [**Akku \_ Abfrage \_ Informationen**](battery-query-information-str.md) verwendet, wenn die Informationen auf der Ebene "batterymanufacturedate" angefordert werden.

## <a name="syntax"></a>Syntax


```C++
typedef struct _BATTERY_MANUFACTURE_DATE {
  UCHAR  Day;
  UCHAR  Month;
  USHORT Year;
} BATTERY_MANUFACTURE_DATE, *PBATTERY_MANUFACTURE_DATE;
```



## <a name="members"></a>Member

<dl> <dt>

**Day**
</dt> <dd>

Der Tag des Herstellungs Monats im Bereich von 1 bis 31. Trotz des-Datentyps ist dies kein ASCII-codierter Wert. Dabei handelt es sich um ein Byte ohne Vorzeichen.

</dd> <dt>

**Ges**
</dt> <dd>

Der Monat der Fertigung im Bereich von 1 (Januar) bis 12 (Dezember). Trotz des-Datentyps ist dies kein ASCII-codierter Wert. Dabei handelt es sich um ein Byte ohne Vorzeichen.

</dd> <dt>

**Jährigen**
</dt> <dd>

Das Jahr der Fertigung. Dies liegt in der Regel im Bereich von 1900-2100.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das Datum wird im gregorianischen oder westlichen Kalender Format codiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                                                                                                                                                                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                                                                                                                                                                                |
| Header<br/>                   | <dl> <dt>Poclass. h; </dt> <dt>Batclass. h unter Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Akku \_ Abfrage \_ Informationen**](battery-query-information-str.md)
</dt> <dt>

[**IOCTL- \_ Akku \_ Abfrage \_ Informationen**](ioctl-battery-query-information.md)
</dt> </dl>

 

 




