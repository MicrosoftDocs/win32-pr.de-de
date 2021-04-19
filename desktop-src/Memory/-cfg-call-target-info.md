---
description: Stellt Informationen über callziele für den Ablauf Steuerungs Schutz (Control Flow Guard, cfg) dar.
ms.assetid: 8DEF907F-3F23-4122-95CE-F413FC7FD96B
title: CFG_CALL_TARGET_INFO Struktur (ntmmapi. h)
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
ms.openlocfilehash: 66177f6b478264a10c1ce0e50297d943a16407c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359025"
---
# <a name="cfg_call_target_info-structure"></a>CFG \_ - \_ Aufrufziel- \_ Informationsstruktur

Stellt Informationen über callziele für den Ablauf Steuerungs Schutz (Control Flow Guard, cfg) dar.

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

Offset relativ zu einer angegebenen (Start-) virtuellen Adresse. Dieser Offset sollte 16 Byte ausgerichtet sein.

</dd> <dt>

**Flags**
</dt> <dd>

Flags, die den Vorgang beschreiben, der für die Adresse ausgeführt werden soll. Wenn das **cfg- \_ \_ Aufrufziel \_ gültig** ist, wird die Adresse für cfg als gültig gekennzeichnet. Andernfalls wird er als ungültiges aufrufsziel gekennzeichnet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Ntmmapi. h</dt> </dl> |



 

 




