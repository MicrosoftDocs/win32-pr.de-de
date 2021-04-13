---
title: Headerfields (sendemailtype)-Element
description: Gibt die Header Felder und deren Werte an, die im Header der e-Mail-Nachricht verwendet werden.
ms.assetid: 6261f32e-3012-4ce7-b407-699374596333
keywords:
- Headerfields-Element Taskplaner
topic_type:
- apiref
api_name:
- HeaderFields
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d108f1c31b8253046ccdbf09312df4f54c7335d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518191"
---
# <a name="headerfields-sendemailtype-element"></a>Headerfields (sendemailtype)-Element

Gibt die Header Felder und deren Werte an, die im Header der e-Mail-Nachricht verwendet werden.

``` syntax
<xs:element name="HeaderFields"
    type="headerFieldsType"
 />
```

Das **headerfields** -Element wird durch den komplexen [**sendemailtype**](taskschedulerschema-sendemailtype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                              | Abgeleitet von                                                           | BESCHREIBUNG                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (Aktionsgruppe)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendemailtype**](taskschedulerschema-sendemailtype-complextype.md) | Stellt eine Aktion dar, die eine e-Mail-Nachricht sendet.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                         | type                                                                       | BESCHREIBUNG                                                    |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Headerfield**](taskschedulerschema-headerfield-headerfieldstype-element.md) | [**headerfieldtype**](taskschedulerschema-headerfieldtype-complextype.md) | Enthält ein Feld für einen Header in einer e-Mail-Nachricht. <br/> |



## <a name="remarks"></a>Bemerkungen

Informationen zur C++-Entwicklung finden Sie unter [**headerfields-Eigenschaft von iemailaction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields).

Informationen zur Skript Entwicklung finden Sie unter [**emailaction. headerfields**](emailaction-headerfields.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





