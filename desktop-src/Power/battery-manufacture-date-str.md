---
description: Enthält das Herstellungsdatum einer Akkukapazität.
ms.assetid: 0cda66fc-bf4a-4a38-b43c-6eecde46c414
title: BATTERY_MANUFACTURE_DATE -Struktur (Poclass.h)
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
ms.openlocfilehash: 30a70fed151304d189fa91b20106e1154ca0e9f4ea5225c52bf1023dbd218346
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032970"
---
# <a name="battery_manufacture_date-structure"></a>BATTERY \_ MANUFACTURE \_ DATE-Struktur

Enthält das Herstellungsdatum einer Akkukapazität. Diese Struktur wird von der [**BATTERY \_ QUERY \_ INFORMATION-Struktur verwendet,**](battery-query-information-str.md) wenn die BatteryManufactureDate-Informationsebene angefordert wird.

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

Der Tag des Herstellungsmonats im Bereich von 1 bis 31. Trotz des Datentyps ist dies kein ASCII-codierter Wert. Es handelt sich um ein Byte ohne Vorzeichen.

</dd> <dt>

**Month (Monat)**
</dt> <dd>

Der Herstellungsmonat im Bereich von 1 (Januar) bis 12 (Dezember). Trotz des Datentyps ist dies kein ASCII-codierter Wert. Es handelt sich um ein Byte ohne Vorzeichen.

</dd> <dt>

**Jahr**
</dt> <dd>

Das Herstellungsjahr. Dies liegt in der Regel im Bereich von 1900 bis 2100.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das Datum wird im gregorianischen oder im Westkalenderformat codiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                                                                                                                                                                                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                                                                                                                                                                                |
| Header<br/>                   | <dl> <dt>Poclass.h;</dt> <dt>Batclass.h auf Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003</dt> und Windows XP </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_ \_ AKKUABFRAGEINFORMATIONEN**](battery-query-information-str.md)
</dt> <dt>

[**IOCTL \_ BATTERY \_ QUERY \_ INFORMATION**](ioctl-battery-query-information.md)
</dt> </dl>

 

 




