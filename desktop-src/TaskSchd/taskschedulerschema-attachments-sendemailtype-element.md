---
title: Attachments-Element (sendEmailType)
description: Enthält eine Liste der Anlagen in der E-Mail-Nachricht.
ms.assetid: 5ae22481-af70-42eb-a964-e63d800be17d
keywords:
- Attachments-Element Taskplaner
topic_type:
- apiref
api_name:
- Attachments
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8aa87679c6d6db725c26deee817fe04acacca85e39d3a8f75c04cba9680ea846
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132065"
---
# <a name="attachments-sendemailtype-element"></a>Attachments-Element (sendEmailType)

Enthält eine Liste der Anlagen in der E-Mail-Nachricht.

``` syntax
<xs:element name="Attachments"
    type="attachmentsType"
 />
```

Das **Attachments-Element** wird vom komplexen [**SendEmailType-Typ**](taskschedulerschema-sendemailtype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                              | Abgeleitet von                                                           | Beschreibung                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Stellt eine Aktion dar, die eine E-Mail sendet.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                          | Typ                                                                    | Beschreibung                                                                                |
|------------------------------------------------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**Datei**](taskschedulerschema-file-attachmentstype-element.md) | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Gibt den Pfad zu einer Datei an, die als Anlage in einer E-Mail gesendet wird.<br/> |



## <a name="remarks"></a>Hinweise

Informationen zur C++-Entwicklung finden Sie unter [**Attachments-Eigenschaft von IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).

Informationen zur Skriptentwicklung finden Sie unter [**EmailAction.Attachments.**](emailaction-attachments.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





