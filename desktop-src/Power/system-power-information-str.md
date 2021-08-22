---
description: Enthält Informationen zur Leerlaufzeit des Systems.
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
ms.openlocfilehash: 665c19a99bffae46cf20af8c5c634e2e9594ecd07d02f003f56d42277ce9a46f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143303"
---
# <a name="system_power_information-structure"></a>SYSTEM \_ POWER \_ INFORMATION-Struktur

Enthält Informationen zur Leerlaufzeit des Systems.

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

**MaxIdlenessAllowed**
</dt> <dd>

Die Leerlaufzeit, bei der das System als im Leerlauf befindliches System betrachtet wird, und der Leerlauftime out beginnt mit der Zählung, ausgedrückt als Prozentsatz. Wenn sie unter diese Zahl fallen, wird der Timer abgebrochen.

</dd> <dt>

**Leerlauf**
</dt> <dd>

Die aktuelle Leerlaufebene, ausgedrückt als Prozentsatz.

</dd> <dt>

**TimeRemaining**
</dt> <dd>

Die verbleibende Zeit im Leerlauftimer in Sekunden.

</dd> <dt>

**CoolingMode**
</dt> <dd>

Der aktuelle Systemkühlungsmodus. Dieser Member muss einen der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                                                 | Bedeutung                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="PO_TZ_ACTIVE"></span><span id="po_tz_active"></span><dl> <dt>**PO \_ TZ \_ ACTIVE**</dt> <dt>0</dt> </dl>                    | Das System befindet sich derzeit im Aktiven Kühlmodus.<br/>                                                |
| <span id="PO_TZ_INVALID_MODE"></span><span id="po_tz_invalid_mode"></span><dl> <dt>**PO \_ UNGÜLTIGER \_ \_ TZ-MODUS**</dt> <dt>2</dt> </dl> | Das System unterstützt keine CPU-Drosselung, oder es ist keine wärmende Zone im System definiert.<br/> |
| <span id="PO_TZ_PASSIVE"></span><span id="po_tz_passive"></span><dl> <dt>**PO \_ TZ \_ PASSIVE**</dt> <dt>1</dt> </dl>                 | Das System befindet sich derzeit im passiven Kühlmodus.<br/>                                               |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Beachten Sie, dass diese Strukturdefinition versehentlich aus WinNT.h weggelassen wurde. Dieser Fehler wird in Zukunft behoben. Fügen Sie in der Zwischenzeit die in diesem Thema enthaltene Strukturdefinition in Ihren Quellcode ein, um Ihre Anwendung zu kompilieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation)
</dt> </dl>

 

 




