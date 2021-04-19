---
description: Veraltet. Stellt einen Zeitpunkt dar, der normalerweise als Datum und Uhrzeit und als entsprechender Kalender ausgedrückt wird.
ms.assetid: a714ff32-2b1f-4256-931e-324d64daf2ac
title: Caldatetime-Struktur
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
ms.openlocfilehash: 5e3f0099a8e1dd7794b960af3d753085f2a32eaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363860"
---
# <a name="caldatetime-structure"></a>Caldatetime-Struktur

Veraltet. Stellt einen Zeitpunkt dar, der normalerweise als Datum und Uhrzeit und als entsprechender Kalender ausgedrückt wird.

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

**Calid**
</dt> <dd>

Der [Kalender Bezeichner](calendar-identifiers.md) für den Zeitpunkt des Zeitpunkts.

</dd> <dt>

**Thi**
</dt> <dd>

Die ERA-Informationen für den Zeitpunkt.

</dd> <dt>

**Jährigen**
</dt> <dd>

Das Jahr für den Zeitpunkt.

</dd> <dt>

**Ges**
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

**Geöffneten**
</dt> <dd>

Die Stunde für den Zeitpunkt.

</dd> <dt>

**Tiges**
</dt> <dd>

Die Minute für den Zeitpunkt.

</dd> <dt>

**Klässler**
</dt> <dd>

Die zweite für den Zeitpunkt.

</dd> <dt>

**Bewegt**
</dt> <dd>

Der Takt für den Zeitpunkt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Unterstützung für nationale Sprachunterstützung](national-language-support-structures.md)
</dt> </dl>

 

 




