---
description: Gibt an, ob Kontext Meldungen an die Fenster Prozedur des besitzenden Fensters gesendet werden sollen.
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
ms.openlocfilehash: cd741eeff1cc3e2ce055a84dd646c3aa2563f217
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758856"
---
# <a name="context_enable_type-enumeration"></a>Kontext \_ enable \_ Type-Enumeration

Gibt an, ob Kontext Meldungen an die Fenster Prozedur des besitzenden Fensters gesendet werden sollen.

## <a name="syntax"></a>Syntax


```C++
typedef enum _CONTEXT_ENABLE_TYPE { 
  CONTEXT_ENABLE   = 1,
  CONTEXT_DISABLE  = 2
} CONTEXT_ENABLE_TYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="CONTEXT_ENABLE"></span><span id="context_enable"></span>**Kontext \_ Aktivierung**
</dt> <dd>

Der Tablet-Kontext sollte aktiviert werden, was dazu führt, dass Kontext Meldungen an die Fenster Prozedur des besitzenden Fensters gesendet werden.

</dd> <dt>

<span id="CONTEXT_DISABLE"></span><span id="context_disable"></span>**Kontext \_ Deaktivieren**
</dt> <dd>

Der Tablet-Kontext sollte deaktiviert werden, wodurch verhindert wird, dass weitere Kontext Nachrichten an die Fenster Prozedur oder Ereignis Senke des besitzenden Fensters gesendet werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITablet:: kreatecontext-Methode**](itablet-createcontext.md)
</dt> </dl>

 

 




