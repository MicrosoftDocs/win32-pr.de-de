---
description: Die \_ IP- \_ Adressstruktur der Reben ist eine IP-Adresse in einem Reben Netzwerk.
ms.assetid: 681753a5-08a2-48e6-9e46-c028c12ad9c1
title: VINES_IP_ADDRESS Struktur (Netmon. h)
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
ms.openlocfilehash: c198c8c109d5aa5b841272173966ec7d9fd22299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346298"
---
# <a name="vines_ip_address-structure"></a>\_IP- \_ Adressstruktur der Reben

Die **\_ IP- \_ Adress** Struktur der Reben ist eine IP-Adresse in einem Reben Netzwerk.

## <a name="syntax"></a>Syntax


```C++
typedef struct _VINES_IP_ADDRESS {
  DWORD NetID;
  WORD  SubnetID;
} VINES_IP_ADDRESS, *LPVINES_IP_ADDRESS;
```



## <a name="members"></a>Member

<dl> <dt>

**"Ntid"**
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
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




