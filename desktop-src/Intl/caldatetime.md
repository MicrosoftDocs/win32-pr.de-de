---
description: Veraltet. Stellt einen Zeitpunkt dar, der in der Regel als Datum und Uhrzeit und als entsprechender Kalender ausgedrückt wird.
ms.assetid: a714ff32-2b1f-4256-931e-324d64daf2ac
title: CALDATETIME-Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CALDATETIME
api_type:
- NA
api_location: ''
ms.openlocfilehash: 700e11f27b673d9ff706483cc4abcf2f06cd7d8bb779ef8eaf9b51a6d81b4068
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822830"
---
# <a name="caldatetime-structure"></a>CALDATETIME-Struktur

Veraltet. Stellt einen Zeitpunkt dar, der in der Regel als Datum und Uhrzeit und als entsprechender Kalender ausgedrückt wird.

## <a name="syntax"></a>Syntax


```C++
typedef struct _caldatetime {
  CALID CalId;
  UINT  Era;
  UINT  Year;
  UINT  Month;
  UINT  Day;
  UINT  DayOfWeek;
  UINT  Hour;
  UINT  Minute;
  UINT  Second;
  ULONG Tick;
} CALDATETIME, *LPCALDATETIME;
```



## <a name="members"></a>Member

<dl> <dt>

**CalId**
</dt> <dd>

Der [Kalenderbezeichner](calendar-identifiers.md) für den Zeitpunkt.

</dd> <dt>

**Ära**
</dt> <dd>

Die Informationen zum Zeitraum für den Zeitpunkt.

</dd> <dt>

**Jahr**
</dt> <dd>

Das Jahr für den Zeitpunkt.

</dd> <dt>

**Month (Monat)**
</dt> <dd>

Der Monat für den Zeitpunkt.

</dd> <dt>

**Day**
</dt> <dd>

Der Tag für den Zeitpunkt.

</dd> <dt>

**DayOfWeek**
</dt> <dd>

Der Wochentag für den Zeitpunkt.

</dd> <dt>

**Stunde**
</dt> <dd>

Die Stunde für den Zeitpunkt.

</dd> <dt>

**Minute**
</dt> <dd>

Die Minute für den Zeitpunkt.

</dd> <dt>

**Second**
</dt> <dd>

Die zweite für den Zeitpunkt.

</dd> <dt>

**Tick**
</dt> <dd>

Der Tick für den Zeitpunkt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Unterstützungsstrukturen für nationale Sprachen](national-language-support-structures.md)
</dt> </dl>

 

 




