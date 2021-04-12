---
description: Enthält Informationen über einen Prozessor.
ms.assetid: fa8c533c-3a54-4eb5-893f-649dfd8b4609
title: PROCESSOR_POWER_INFORMATION Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROCESSOR_POWER_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 500a346080d7bf0c44d392a63a71310db74225a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345488"
---
# <a name="processor_power_information-structure"></a>Struktur der Prozessor \_ Energie \_ Informationen

Enthält Informationen über einen Prozessor.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PROCESSOR_POWER_INFORMATION {
  ULONG Number;
  ULONG MaxMhz;
  ULONG CurrentMhz;
  ULONG MhzLimit;
  ULONG MaxIdleState;
  ULONG CurrentIdleState;
} PROCESSOR_POWER_INFORMATION, *PPROCESSOR_POWER_INFORMATION;
```



## <a name="members"></a>Member

<dl> <dt>

**Number**
</dt> <dd>

Die System Prozessornummer.

</dd> <dt>

**Maxmhz**
</dt> <dd>

Die maximale angegebene Taktfrequenz des System Prozessors in Megahertz.

</dd> <dt>

**Currentmhz**
</dt> <dd>

Die Prozessor Taktfrequenz in Megahertz. Diese Zahl entspricht der maximalen angegebenen Prozessor Taktfrequenz, multipliziert mit der aktuellen Prozessor Drosselung.

</dd> <dt>

**Mhzlimit**
</dt> <dd>

Der Grenzwert für die Prozessor Taktfrequenz in Megahertz. Diese Zahl entspricht der maximalen angegebenen Prozessor Taktfrequenz, multipliziert mit der aktuellen Prozessor-Grenzwert für die wärmedrosselung.

</dd> <dt>

**Maxidlestate**
</dt> <dd>

Der maximale Leerlauf Status dieses Prozessors.

</dd> <dt>

**"Ustidlestate"**
</dt> <dd>

Der aktuelle Leerlauf Status dieses Prozessors.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass diese Struktur Definition versehentlich aus "Winnt. h" weggelassen wurde. Dieser Fehler wird in Zukunft korrigiert. Fügen Sie in der Zwischenzeit die Struktur Definition, die in diesem Thema enthalten ist, in Ihren Quellcode ein, um die Anwendung zu kompilieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Callntpowerinformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation)
</dt> </dl>

 

 




