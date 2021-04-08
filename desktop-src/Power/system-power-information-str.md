---
description: Enthält Informationen über die idständigkeit des Systems.
ms.assetid: f6349b7c-1835-4492-95e3-9ce142628804
title: SYSTEM_POWER_INFORMATION Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SYSTEM_POWER_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: c32a8ad86b71ea680bd2961c9196a0896b055e5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959734"
---
# <a name="system_power_information-structure"></a>Struktur der System \_ Energie \_ Informationen

Enthält Informationen über die idständigkeit des Systems.

## <a name="syntax"></a>Syntax


```C++
typedef struct _SYSTEM_POWER_INFORMATION {
  ULONG MaxIdlenessAllowed;
  ULONG Idleness;
  ULONG TimeRemaining;
  UCHAR CoolingMode;
} SYSTEM_POWER_INFORMATION, *PSYSTEM_POWER_INFORMATION;
```



## <a name="members"></a>Member

<dl> <dt>

**Maxidleness Allowed**
</dt> <dd>

Der Leerlauf, bei dem das System als im Leerlauf befindlich betrachtet wird und das Leerlauf Timeout beginnt, wird als Prozentsatz ausgedrückt. Das Ablegen unterhalb dieser Zahl bewirkt, dass der Timer abgebrochen wird.

</dd> <dt>

**Leerlauf**
</dt> <dd>

Die aktuelle Leerlauf Ebene, ausgedrückt als Prozentsatz.

</dd> <dt>

**TimeRemaining**
</dt> <dd>

Die verbleibende Zeit im Leerlaufzeit Geber in Sekunden.

</dd> <dt>

**Coolingmode**
</dt> <dd>

Der aktuelle systemkühlungs Modus. Dieser Member muss einen der folgenden Werte haben.



| Wert                                                                                                                                                                                                                                 | Bedeutung                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="PO_TZ_ACTIVE"></span><span id="po_tz_active"></span><dl> <dt>**Po \_ TZ \_ aktiv**</dt> <dt>0</dt> </dl>                    | Das System befindet sich derzeit im aktiven kühl Modus.<br/>                                                |
| <span id="PO_TZ_INVALID_MODE"></span><span id="po_tz_invalid_mode"></span><dl> <dt>**Po \_ TZ \_ ungültiger \_ Modus**</dt> <dt>2</dt> </dl> | Das System unterstützt keine CPU-Drosselung, oder im System ist keine thermische Zone definiert.<br/> |
| <span id="PO_TZ_PASSIVE"></span><span id="po_tz_passive"></span><dl> <dt>**Po \_ TZ \_ passiv**</dt> <dt>1</dt> </dl>                 | Das System befindet sich zurzeit im passiven kühl Modus.<br/>                                               |



 

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

 

 




