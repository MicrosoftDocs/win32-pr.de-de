---
title: HeaderFields -Element (sendEmailType)
description: Gibt die Headerfelder und deren Werte an, die im Header der E-Mail-Nachricht verwendet werden.
ms.assetid: 6261f32e-3012-4ce7-b407-699374596333
keywords:
- HeaderFields-Taskplaner
topic_type:
- apiref
api_name:
- HeaderFields
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2af801385c74fa26221556b713faf8db915037ef4cf7439d71a2e2d4004193d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100030"
---
# <a name="headerfields-sendemailtype-element"></a>HeaderFields -Element (sendEmailType)

Gibt die Headerfelder und deren Werte an, die im Header der E-Mail-Nachricht verwendet werden.

``` syntax
<xs:element name="HeaderFields"
    type="headerFieldsType"
 />
```

Das **HeaderFields-Element** wird durch den komplexen [**SendEmailType-Typ**](taskschedulerschema-sendemailtype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                              | Abgeleitet von                                                           | BESCHREIBUNG                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Stellt eine Aktion dar, die eine E-Mail sendet.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                         | type                                                                       | BESCHREIBUNG                                                    |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|----------------------------------------------------------------|
| [**HeaderField**](taskschedulerschema-headerfield-headerfieldstype-element.md) | [**headerFieldType**](taskschedulerschema-headerfieldtype-complextype.md) | Enthält ein Feld für einen Header in einer E-Mail. <br/> |



## <a name="remarks"></a>Hinweise

Informationen zur C++-Entwicklung finden Sie unter [**HeaderFields-Eigenschaft von IEmailAction.**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields)

Informationen zur Skriptentwicklung finden Sie unter [**EmailAction.HeaderFields**](emailaction-headerfields.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





