---
title: User-Element
description: Erfahren Sie mehr über das User-Element. Dieses Element wird nicht verwendet, wenn Legacy Methoden über die EAPHost-APIs verwendet werden.
ms.assetid: d35fb4ba-5f48-431d-b2bf-738043f5d1ff
keywords:
- User-Element EAPHost
topic_type:
- apiref
api_name:
- User
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b564b6f91244a6839bc256dcdb2f79c630a4b065
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730361"
---
# <a name="user-element"></a>User-Element

Das **User** -Element wird nicht verwendet, wenn Legacy Methoden über die EAPHost-APIs verwendet werden.

``` syntax
<xs:element name="User">
    <xs:complexType>
        <xs:sequence>
            <xs:element
                maxOccurs="unbounded"
                ref="Eap"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                  | type | BESCHREIBUNG                                                                     |
|----------------------------------------------------------|------|---------------------------------------------------------------------------------|
| [**EAP**](baseeapuserpropertiesv1schema-eap-element.md) |      | Zeichnet den Methodentyp und die Methoden spezifischen Anmelde Informationen auf.<br/> |



## <a name="requirements"></a>Anforderungen



| Role | Mindestens unterstützte Betriebssystemversion |
|------|------------------------------|
| Client<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Server<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[eapuserpropertiesv1-Schema](eapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





