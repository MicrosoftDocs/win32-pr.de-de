---
title: To-Element (sendEmailType)
description: Enthält die E-Mail-Adressen, an die die E-Mail gesendet wird.
ms.assetid: bf3aa878-967b-4ebd-9397-a2a499686a9f
keywords:
- So Taskplaner
topic_type:
- apiref
api_name:
- To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2367686e308eb33287dafc3ce274d039b71534048fea07bc313e0542af4e2041
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355640"
---
# <a name="to-sendemailtype-element"></a>To-Element (sendEmailType)

Enthält die E-Mail-Adressen, an die die E-Mail gesendet wird.

``` syntax
<xs:element name="To"
    type="string"
 />
```

Das **To-Element** wird durch den komplexen [**SendEmailType-Typ**](taskschedulerschema-sendemailtype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                              | Abgeleitet von                                                           | BESCHREIBUNG                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Stellt eine Aktion dar, die eine E-Mail sendet.<br/> |



## <a name="remarks"></a>Hinweise

Informationen zur C++-Entwicklung finden Sie unter [**To Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to).

Informationen zur Skriptentwicklung finden Sie unter [**EmailAction.To**](emailaction-to.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





