---
title: Subject-Element (sendEmailType)
description: Enthält den Betreff der E-Mail-Nachricht.
ms.assetid: 2ccaa983-4dca-4e45-ba8d-2a93e23f7e8c
keywords:
- Subject-Element Taskplaner
topic_type:
- apiref
api_name:
- Subject
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 15bf3c84befd9dd8f4c9c4a544fc920b7066184c6bf367c404bb14f22f573b92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611188"
---
# <a name="subject-sendemailtype-element"></a>Subject-Element (sendEmailType)

Enthält den Betreff der E-Mail-Nachricht.

``` syntax
<xs:element name="Subject"
    type="string"
 />
```

Das **Subject-Element** wird durch den komplexen [**SendEmailType-Typ**](taskschedulerschema-sendemailtype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                              | Abgeleitet von                                                           | Beschreibung                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Stellt eine Aktion dar, die eine E-Mail sendet.<br/> |



## <a name="remarks"></a>Hinweise

Informationen zur C++-Entwicklung finden Sie unter [**Subject-Eigenschaft von IEmailAction.**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject)

Informationen zur Skriptentwicklung finden Sie unter [**EmailAction.Subject.**](emailaction-subject.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





