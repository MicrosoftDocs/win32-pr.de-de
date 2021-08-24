---
description: Die \_ \_ VINES-IP-ADRESSstruktur ist eine IP-Adresse in einem Vines-Netzwerk.
ms.assetid: 681753a5-08a2-48e6-9e46-c028c12ad9c1
title: VINES_IP_ADDRESS-Struktur (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VINES_IP_ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 23a590679fd2b4a147a8bc0f92a4d4c7b4afb8c746526de9fba7cfc388e4e1c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742200"
---
# <a name="vines_ip_address-structure"></a>\_ \_ VINES-IP-ADRESSstruktur

Die **\_ VINES-IP-ADRESSstruktur \_** ist eine IP-Adresse in einem Vines-Netzwerk.

## <a name="syntax"></a>Syntax


```C++
typedef struct _VINES_IP_ADDRESS {
  DWORD NetID;
  WORD  SubnetID;
} VINES_IP_ADDRESS, *LPVINES_IP_ADDRESS;
```



## <a name="members"></a>Member

<dl> <dt>

**NetID**
</dt> <dd>

Der Bezeichner eines bestimmten Computers in einem bestimmten Subnetz.

</dd> <dt>

**SubnetID**
</dt> <dd>

Der Bezeichner eines bestimmten Subnetzes im gesamten Netzwerk.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




