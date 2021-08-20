---
title: User-Element
description: Erfahren Sie mehr über das User-Element. Dieses Element wird nicht verwendet, wenn Legacymethoden über die EAPHost-APIs verwendet werden.
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
ms.openlocfilehash: d0f21b22320029bf1d10a209eae6a3b2192512a541c1e681b71e112d488c87ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086404"
---
# <a name="user-element"></a>User-Element

Das **User-Element** wird nicht verwendet, wenn Legacymethoden über die EAPHost-APIs verwendet werden.

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



| Element                                                  | Typ | Beschreibung                                                                     |
|----------------------------------------------------------|------|---------------------------------------------------------------------------------|
| [**Eap**](baseeapuserpropertiesv1schema-eap-element.md) |      | Erfasst die Methodentyp- und methodenspezifischen Anmeldeinformationsinformationen.<br/> |



## <a name="requirements"></a>Anforderungen



| Rolle | Unterstützte Mindestversion des Betriebssystems |
|------|------------------------------|
| Client<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Server<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[eapuserpropertiesv1-Schema](eapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





