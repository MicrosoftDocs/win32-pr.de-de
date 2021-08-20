---
title: 'PrincipalsType : Komplexer Typ'
description: Definiert das untergeordnete Element für das Principals-Element.
ms.assetid: a501534b-eb0f-480f-a2c9-d2015262a9a7
keywords:
- 'principalsType: komplexer Typ Taskplaner'
topic_type:
- apiref
api_name:
- principalsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fa2aecd8ea71769b51792fcc5bd26ceca11309f43697037964a900d45c0d8254
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131741"
---
# <a name="principalstype-complex-type"></a>PrincipalsType : Komplexer Typ

Definiert das untergeordnete Element für das [**Principals-Element.**](taskschedulerschema-principals-tasktype-element.md)

``` syntax
<xs:complexType name="principalsType">
    <xs:sequence>
        <xs:element name="Principal"
            type="principalType"
            maxOccurs="1"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                  | Typ                                                                   | Beschreibung                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Prinzipal**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Gibt die Sicherheitsanmeldeinformationen für einen Prinzipal an.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





