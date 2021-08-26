---
description: Die KEYSVC \_ TYPE-Enumeration definiert, ob ein Schlüssel für einen Computer oder Dienst gilt.
ms.assetid: 573a412a-1e9d-47ac-bd09-2319d4b9712b
title: KEYSVC_TYPE -Enumeration (Rkeysvcc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_TYPE
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 3c23cc259029cf76fcb1590e6261623827d59b48c9a0728e21c8250ca3e858f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119976093"
---
# <a name="keysvc_type-enumeration"></a>KEYSVC \_ TYPE-Enumeration

Die **KEYSVC \_ TYPE-Enumeration** definiert, ob ein Schlüssel für einen Computer oder Dienst gilt.

## <a name="syntax"></a>Syntax


```C++
typedef enum _KEYSVC_TYPE { 
  KeySvcMachine,
  KeySvcService
} KEYSVC_TYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="KeySvcMachine"></span><span id="keysvcmachine"></span><span id="KEYSVCMACHINE"></span>**KeySvcMachine**
</dt> <dd>

Der Schlüssel ist für einen Computer.

</dd> <dt>

<span id="KeySvcService"></span><span id="keysvcservice"></span><span id="KEYSVCSERVICE"></span>**KeySvcService**
</dt> <dd>

Der Schlüssel ist für einen Dienst.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Rkeysvcc.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**RKeyOpenKeyService**](rkeyopenkeyservice.md)
</dt> </dl>

 

 




