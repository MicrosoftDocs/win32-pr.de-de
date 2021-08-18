---
description: Stellt Informationen zu Aufrufzielen für Control Flow Guard (CFG) dar.
ms.assetid: 8DEF907F-3F23-4122-95CE-F413FC7FD96B
title: CFG_CALL_TARGET_INFO-Struktur (Ntmmapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFG_CALL_TARGET_INFO
api_type:
- HeaderDef
api_location:
- ntmmapi.h
ms.openlocfilehash: e3bd7d351e890a968f2fa01ddffa6c8e3be16164d78393894055f55660c516bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040280"
---
# <a name="cfg_call_target_info-structure"></a>CFG \_ CALL \_ TARGET \_ INFO-Struktur

Stellt Informationen zu Aufrufzielen für Control Flow Guard (CFG) dar.

## <a name="syntax"></a>Syntax


```C++
typedef struct _CFG_CALL_TARGET_INFO {
  ULONG_PTR Offset;
  ULONG_PTR Flags;
} CFG_CALL_TARGET_INFO, *PCFG_CALL_TARGET_INFO;
```



## <a name="members"></a>Member

<dl> <dt>

**Offset**
</dt> <dd>

Offset relativ zu einer angegebenen (Start-)virtuellen Adresse. Dieser Offset sollte 16 Byte ausgerichtet sein.

</dd> <dt>

**Flags**
</dt> <dd>

Flags, die den Vorgang beschreiben, der für die Adresse ausgeführt werden soll. Wenn **CFG \_ CALL TARGET \_ \_ VALID** festgelegt ist, wird die Adresse als gültig für CFG gekennzeichnet. Andernfalls wird es als ungültiges Aufrufziel gekennzeichnet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Ntmmapi.h</dt> </dl> |



 

 




