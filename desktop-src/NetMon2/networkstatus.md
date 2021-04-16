---
description: Die networkstatus-Struktur beschreibt den aktuellen Status des NPP.
ms.assetid: e5e07480-cfc3-408f-9ca2-48a697e4b875
title: Networkstatus-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NETWORKSTATUS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 067a57dabfb5222deb27de44c60c6eb121cd8c36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530227"
---
# <a name="networkstatus-structure"></a>Networkstatus-Struktur

Die **networkstatus** -Struktur beschreibt den aktuellen Status des NPP.

## <a name="syntax"></a>Syntax


```C++
typedef struct _NETWORKSTATUS {
  DWORD State;
  DWORD Flags;
} NETWORKSTATUS, *LPNETWORKSTATUS;
```



## <a name="members"></a>Member

<dl> <dt>

**State**
</dt> <dd>

Gibt den aktuellen Zustand des NPP an.



| Wert                                                                                                                                                                                                          | Bedeutung                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="NETWORKSTATUS_STATE_VOID"></span><span id="networkstatus_state_void"></span><dl> <dt>**networkstatus- \_ Zustand ist \_ ungültig.**</dt> </dl>                | Der npp ist nicht verbunden, oder er ist verbunden, und die Erfassung wird nicht gestartet.<br/> |
| <span id="NETWORKSTATUS_STATE_CAPTURING"></span><span id="networkstatus_state_capturing"></span><dl> <dt>**networkstatus- \_ Zustands \_ Erfassung**</dt> </dl> | Der NPP erfasst Daten.<br/>                                                   |
| <span id="NETWORKSTATUS_STATE_PAUSED"></span><span id="networkstatus_state_paused"></span><dl> <dt>**der networkstatus-Zustand wurde angehalten. \_ \_**</dt> </dl>          | Der NPP wurde während der Datenerfassung angehalten.<br/>                                     |



 

</dd> <dt>

**Flags**
</dt> <dd>

Flags, die den aktuellen Zustand des NPP beschreiben.



| Wert                                                                                                                                                                                                                             | Bedeutung                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="NETWORKSTATUS_FLAGS_TRIGGER_PENDING"></span><span id="networkstatus_flags_trigger_pending"></span><dl> <dt>**netzwerkstatusflags-Auslösung \_ \_ \_ Ausstehend**</dt> </dl> | Für den npp ist ein ausstehender Auslösung vorhanden.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie diese Struktur verwenden, müssen Sie den Arbeitsspeicher für die Struktur zuordnen, bevor Sie verwendet werden kann, und den Arbeitsspeicher freigeben, wenn die Struktur nicht mehr benötigt wird.

Die Liste "Siehe auch" am Ende dieses Themas listet alle Methoden auf, die diese Struktur verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Idelta-DC:: QueryStatus](idelaydc-querystatus.md)
</dt> <dt>

[IESP:: QueryStatus](iesp-querystatus.md)
</dt> <dt>

["Iran:: QueryStatus"](irtc-querystatus.md)
</dt> <dt>

[IStats:: QueryStatus](istats-querystatus.md)
</dt> </dl>

 

 




