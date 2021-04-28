---
description: 'profileList(WLANPolicy)-Element: Enthält eine Liste von Profilen, die auf Domänen- oder Computerebene angewendet werden sollen.'
ms.assetid: b78cb095-a1da-4b1b-91d3-c5085325be05
title: profileList-Element (WLANPolicy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- profileList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 4c7478f38ba7336738325bac6872866cd570288b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109198"
---
# <a name="profilelist-wlanpolicy-element"></a>profileList-Element (WLANPolicy)

Das ProfileList-Element (WLANPolicy) enthält eine Liste von Profilen, die auf Domänen- oder Computerebene angewendet werden sollen. Dieses Element ist optional. Wenn dieses Element vorhanden ist, muss es mindestens ein Profil enthalten.

Profile sollten auf dem WLAN-Profilschema [ \_ mit](wlan-profileschema-schema.md)dem Stammelement [**WLANProfile basieren.**](wlan-profileschema-wlanprofile-element.md)

``` syntax
<xs:element name="profileList">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

Das **profileList-Element** wird durch das [**WLANPolicy-Element**](wlan-policyschema-wlanpolicy-element.md) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




