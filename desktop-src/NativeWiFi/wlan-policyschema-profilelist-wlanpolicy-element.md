---
description: Enthält eine Liste der Profile, die auf Domänen-oder Computer Ebene angewendet werden sollen.
ms.assetid: b78cb095-a1da-4b1b-91d3-c5085325be05
title: ProfileList-Element (wlanpolicy)
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
ms.openlocfilehash: 9c11fbeb41b43faa31b170dcc856bb0823631001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366135"
---
# <a name="profilelist-wlanpolicy-element"></a>ProfileList-Element (wlanpolicy)

Das ProfileList-Element (wlanpolicy) enthält eine Liste von Profilen, die auf Domänen-oder Computer Ebene angewendet werden sollen. Dieses Element ist optional. Wenn dieses Element vorhanden ist, muss es mindestens ein Profil enthalten.

Profile müssen auf dem WLAN- [ \_ Profil Schema](wlan-profileschema-schema.md)mit einem Stamm Element von [**wlanprofile**](wlan-profileschema-wlanprofile-element.md)basieren.

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

Das **ProfileList** -Element wird durch das [**wlanpolicy**](wlan-policyschema-wlanpolicy-element.md) -Element definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Wlanpolicy**](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Wlanpolicy**](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




