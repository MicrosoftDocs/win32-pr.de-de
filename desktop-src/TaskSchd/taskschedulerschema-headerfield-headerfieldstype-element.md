---
title: Headerfield (headerfieldstype)-Element
description: Enthält ein Feld für einen Header in einer e-Mail-Nachricht.
ms.assetid: ec6fc593-8798-4dd0-b589-48657b7cdeb1
keywords:
- Headerfield-Element Taskplaner
topic_type:
- apiref
api_name:
- HeaderField
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f7ac79a16bb0464f6e81d90eba38384a3c2b483
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341041"
---
# <a name="headerfield-headerfieldstype-element"></a>Headerfield (headerfieldstype)-Element

Enthält ein Feld für einen Header in einer e-Mail-Nachricht.

``` syntax
<xs:element name="HeaderField"
    type="headerFieldType"
 />
```

Das **headerfield** -Element wird durch den komplexen [**headerfieldstype**](taskschedulerschema-headerfieldstype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                        | Abgeleitet von                                                                 | BESCHREIBUNG                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**Headerfields**](taskschedulerschema-headerfields-sendemailtype-element.md) | [**headerfieldstype**](taskschedulerschema-headerfieldstype-complextype.md) | Gibt die Header Felder und deren Werte an, die im Header der e-Mail-Nachricht verwendet werden.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                            | type                                                                    | BESCHREIBUNG                                                            |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**Name**](taskschedulerschema-name-headerfieldtype-element.md)   | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Gibt den Namen des Header Felds in einer e-Mail-Nachricht an.<br/> |
| [**Wert**](taskschedulerschema-value-headerfieldtype-element.md) | **string**                                                              | Gibt den Wert eines Header Felds in einer e-Mail-Nachricht an.<br/>  |



## <a name="remarks"></a>Bemerkungen

Informationen zur C++-Entwicklung finden Sie unter [**headerfields-Eigenschaft von iemailaction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields).

Informationen zur Skript Entwicklung finden Sie unter [**emailaction. headerfields**](emailaction-headerfields.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





