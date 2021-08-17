---
description: Enthält Informationen zu einem Prozessor.
ms.assetid: fa8c533c-3a54-4eb5-893f-649dfd8b4609
title: PROCESSOR_POWER_INFORMATION-Struktur
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
ms.openlocfilehash: 3bdb6a3bb8ae5b768c42609817c76934c203989ba6dea665fc6cc0a6896659de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143333"
---
# <a name="processor_power_information-structure"></a>STRUKTUR DER \_ \_ PROZESSORLEISTUNGSINFORMATIONEN

Enthält Informationen zu einem Prozessor.

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

Die Systemprozessornummer.

</dd> <dt>

**MaxMhz**
</dt> <dd>

Die maximal angegebene Taktfrequenz des Systemprozessors in Megahertz.

</dd> <dt>

**CurrentMhz**
</dt> <dd>

Die Prozessortaktfrequenz in Megahertz. Diese Zahl ist die maximal angegebene Prozessortaktfrequenz multipliziert mit der aktuellen Prozessordrosselung.

</dd> <dt>

**MhzLimit**
</dt> <dd>

Der Grenzwert für die Prozessortaktfrequenz in Megahertz. Diese Zahl ist die maximal angegebene Prozessortaktfrequenz multipliziert mit der aktuellen Prozessordrosselungsgrenze.

</dd> <dt>

**MaxIdleState**
</dt> <dd>

Der maximale Leerlaufzustand dieses Prozessors.

</dd> <dt>

**CurrentIdleState**
</dt> <dd>

Der aktuelle Leerlaufzustand dieses Prozessors.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Beachten Sie, dass diese Strukturdefinition versehentlich in WinNT.h ausgelassen wurde. Dieser Fehler wird in Zukunft behoben. Um ihre Anwendung zu kompilieren, schließen Sie in der Zwischenzeit die in diesem Thema enthaltene Strukturdefinition in Ihren Quellcode ein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation)
</dt> </dl>

 

 




