---
description: Gibt an, ob Kontextnachrichten an die Fensterprozedur des besitzenden Fensters gesendet werden sollen.
ms.assetid: 57ecf10a-8a02-4353-b916-9080ebc0b270
title: CONTEXT_ENABLE_TYPE-Enumeration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONTEXT_ENABLE_TYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 94bffba211f75416ccae5e9a55342441b7b11b41b1a9f1f4b085ec190f991645
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110970"
---
# <a name="context_enable_type-enumeration"></a>CONTEXT \_ ENABLE \_ TYPE-Enumeration

Gibt an, ob Kontextnachrichten an die Fensterprozedur des besitzenden Fensters gesendet werden sollen.

## <a name="syntax"></a>Syntax


```C++
typedef enum _CONTEXT_ENABLE_TYPE { 
  CONTEXT_ENABLE   = 1,
  CONTEXT_DISABLE  = 2
} CONTEXT_ENABLE_TYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="CONTEXT_ENABLE"></span><span id="context_enable"></span>**CONTEXT \_ ENABLE**
</dt> <dd>

Der Tablet-Kontext sollte aktiviert sein, was dazu führt, dass Kontextmeldungen an die Fensterprozedur des besitzenden Fensters gesendet werden.

</dd> <dt>

<span id="CONTEXT_DISABLE"></span><span id="context_disable"></span>**CONTEXT \_ DISABLE**
</dt> <dd>

Der Tablet-Kontext sollte deaktiviert werden, um zu verhindern, dass weitere Kontextmeldungen an die Fensterprozedur oder die Ereignissenke des besitzenden Fensters gesendet werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITablet::CreateContext-Methode**](itablet-createcontext.md)
</dt> </dl>

 

 




