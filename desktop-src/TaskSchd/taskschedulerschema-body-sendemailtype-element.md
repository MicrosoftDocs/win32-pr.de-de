---
title: Body (sendEmailType)-Element
description: Enthält den Text im Text der E-Mail.
ms.assetid: fac6ddd5-6f73-427b-b213-ab946512c87a
keywords:
- Body-Element Taskplaner
topic_type:
- apiref
api_name:
- Body
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a924062b3a382bc8362bdfa45e1477b4e841222bdd1f5ac70fbb8adbc9b070b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118857963"
---
# <a name="body-sendemailtype-element"></a>Body (sendEmailType)-Element

Enthält den Text im Text der E-Mail.

``` syntax
<xs:element name="Body"
    type="string"
 />
```

Das **Body-Element** wird vom komplexen [**sendEmailType-Typ**](taskschedulerschema-sendemailtype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                              | Abgeleitet von                                                           | Beschreibung                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Stellt eine Aktion dar, die eine E-Mail sendet.<br/> |



## <a name="remarks"></a>Hinweise

Informationen zur C++-Entwicklung finden Sie unter [**Body Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body).

Informationen zur Skriptentwicklung finden Sie unter [**EmailAction.Body.**](emailaction-body.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





