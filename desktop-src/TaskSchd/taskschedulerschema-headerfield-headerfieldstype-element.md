---
title: HeaderField-Element (headerFieldsType)
description: Enthält ein Feld für einen Header in einer E-Mail-Nachricht.
ms.assetid: ec6fc593-8798-4dd0-b589-48657b7cdeb1
keywords:
- HeaderField-Element Taskplaner
topic_type:
- apiref
api_name:
- HeaderField
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 918e432ce7a8ea2d43769b9d9ee1315a4b35bce6f2c0cb23f1153ec7afe1a599
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139213"
---
# <a name="headerfield-headerfieldstype-element"></a>HeaderField-Element (headerFieldsType)

Enthält ein Feld für einen Header in einer E-Mail-Nachricht.

``` syntax
<xs:element name="HeaderField"
    type="headerFieldType"
 />
```

Das **HeaderField-Element** wird durch den komplexen [**headerFieldsType-Typ**](taskschedulerschema-headerfieldstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                        | Abgeleitet von                                                                 | Beschreibung                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**HeaderFields**](taskschedulerschema-headerfields-sendemailtype-element.md) | [**headerFieldsType**](taskschedulerschema-headerfieldstype-complextype.md) | Gibt die Headerfelder und deren Werte an, die im Header der E-Mail-Nachricht verwendet werden.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                            | type                                                                    | Beschreibung                                                            |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**Name**](taskschedulerschema-name-headerfieldtype-element.md)   | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Gibt den Namen des Headerfelds in einer E-Mail an.<br/> |
| [**Wert**](taskschedulerschema-value-headerfieldtype-element.md) | **string**                                                              | Gibt den Wert eines Headerfelds in einer E-Mail an.<br/>  |



## <a name="remarks"></a>Hinweise

Informationen zur C++-Entwicklung finden Sie unter [**HeaderFields-Eigenschaft von IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields).

Informationen zur Skriptentwicklung finden Sie unter [**EmailAction.HeaderFields.**](emailaction-headerfields.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





