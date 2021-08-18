---
title: Server (sendEmailType)-Element
description: Enthält den E-Mail-Server, der zum Senden der E-Mail-Nachricht verwendet wird.
ms.assetid: 4c6084d1-70c5-4d8b-8fcb-ab4cd8aab441
keywords:
- Serverelement Taskplaner
topic_type:
- apiref
api_name:
- Server
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6052ebb5e648c040c321a311a6ba18313244ab20340d5a7f6c4185e3d35f5df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002248"
---
# <a name="server-sendemailtype-element"></a>Server (sendEmailType)-Element

Enthält den E-Mail-Server, der zum Senden der E-Mail-Nachricht verwendet wird.

``` syntax
<xs:element name="Server"
    type="nonEmptyString"
 />
```

Das **Server-Element** wird durch den komplexen [**SendEmailType-Typ**](taskschedulerschema-sendemailtype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                              | Abgeleitet von                                                           | BESCHREIBUNG                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Stellt eine Aktion dar, die eine E-Mail sendet.<br/> |



## <a name="remarks"></a>Hinweise

Informationen zur C++-Entwicklung finden Sie unter [**Servereigenschaft von IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server).

Informationen zur Skriptentwicklung finden Sie unter [**EmailAction.Server.**](emailaction-server.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





