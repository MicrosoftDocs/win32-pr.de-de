---
title: Bcc -Element (sendEmailType)
description: Enthält die E-Mail-Adressen, die in der Bcc-Zeile einer E-Mail-Nachricht verwendet werden.
ms.assetid: c80407d0-3b3f-4efe-91de-7a3a7abc996f
keywords:
- Bcc-Element Taskplaner
topic_type:
- apiref
api_name:
- Bcc
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1409d50a0317758534724b9e2c3a9796c4dd0cb40e666f58fc65ca0771da9762
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659040"
---
# <a name="bcc-sendemailtype-element"></a>Bcc -Element (sendEmailType)

Enthält die E-Mail-Adressen, die in der Bcc-Zeile einer E-Mail-Nachricht verwendet werden.

``` syntax
<xs:element name="Bcc"
    type="string"
 />
```

Das **Bcc-Element** wird vom komplexen [**SendEmailType-Typ**](taskschedulerschema-sendemailtype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                              | Abgeleitet von                                                           | BESCHREIBUNG                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Stellt eine Aktion dar, die eine E-Mail sendet.<br/> |



## <a name="remarks"></a>Hinweise

Informationen zur C++-Entwicklung finden Sie unter [**Bcc-Eigenschaft von IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc).

Informationen zur Skriptentwicklung finden Sie unter [**EmailAction.Bcc**](emailaction-bcc.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





