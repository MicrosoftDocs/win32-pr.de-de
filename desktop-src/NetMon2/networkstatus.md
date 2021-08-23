---
description: Die NETWORKSTATUS-Struktur beschreibt den aktuellen Status des NPP.
ms.assetid: e5e07480-cfc3-408f-9ca2-48a697e4b875
title: NETWORKSTATUS-Struktur (Netmon.h)
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
ms.openlocfilehash: 3031cd8bd8f1af4e5ea5f03aec93b9a2f28b3ec098a8110563bb89869c97ae3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799520"
---
# <a name="networkstatus-structure"></a>NETWORKSTATUS-Struktur

Die **NETWORKSTATUS-Struktur** beschreibt den aktuellen Status des NPP.

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

Gibt den aktuellen Status des NPP an.



| Wert                                                                                                                                                                                                          | Bedeutung                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="NETWORKSTATUS_STATE_VOID"></span><span id="networkstatus_state_void"></span><dl> <dt>**NETWORKSTATUS \_ STATE \_ VOID**</dt> </dl>                | Das NPP ist nicht verbunden, oder es ist verbunden, und die Erfassung wird nicht gestartet.<br/> |
| <span id="NETWORKSTATUS_STATE_CAPTURING"></span><span id="networkstatus_state_capturing"></span><dl> <dt>**\_ \_ NETWORKSTATUS-ZUSTANDSERFASSUNG**</dt> </dl> | Das NPP erfasst Daten.<br/>                                                   |
| <span id="NETWORKSTATUS_STATE_PAUSED"></span><span id="networkstatus_state_paused"></span><dl> <dt>**NETWORKSTATUS \_ STATE \_ PAUSED**</dt> </dl>          | Das NPP wurde angehalten, während Daten erfasst wurden.<br/>                                     |



 

</dd> <dt>

**Flags**
</dt> <dd>

Flags, die den aktuellen Zustand des NPP beschreiben.



| Wert                                                                                                                                                                                                                             | Bedeutung                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="NETWORKSTATUS_FLAGS_TRIGGER_PENDING"></span><span id="networkstatus_flags_trigger_pending"></span><dl> <dt>**NETWORKSTATUS \_ FLAGS \_ TRIGGER \_ PENDING**</dt> </dl> | Für das NPP ist ein Trigger ausstehend.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn Sie diese Struktur verwenden, müssen Sie den Arbeitsspeicher für die Struktur zuordnen, bevor sie verwendet werden kann, und den Arbeitsspeicher freigeben, wenn die Struktur nicht mehr benötigt wird.

Die Liste Siehe auch am Ende dieses Themas listet alle Methoden auf, die diese Struktur verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[IDelaydC::QueryStatus](idelaydc-querystatus.md)
</dt> <dt>

[IESP::QueryStatus](iesp-querystatus.md)
</dt> <dt>

[IRTC::QueryStatus](irtc-querystatus.md)
</dt> <dt>

[IStats::QueryStatus](istats-querystatus.md)
</dt> </dl>

 

 




