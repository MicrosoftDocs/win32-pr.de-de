---
description: Enthält eine Liste der Profile, die auf Domänen-oder Computer Ebene angewendet werden sollen.
ms.assetid: 4f010449-0c6b-4a01-8253-4f82cd628f0a
title: ProfileList-Element (lanpolicy)
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
ms.openlocfilehash: b85c284262c070f7a9349933f99ad858cf047913
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373158"
---
# <a name="profilelist-lanpolicy-element"></a>ProfileList-Element (lanpolicy)

Das ProfileList-Element (lanpolicy) enthält eine Liste der Profile, die auf der Domänen-oder Computer Ebene angewendet werden sollen. Profile müssen auf dem LAN- [ \_ Profil Schema](lan-profileschema-schema.md)mit einem Stamm Element von " [**lanprofile**](lan-profileschema-lanprofile-element.md)" basieren. Profile, die auf einem beliebigen anderen Schema basieren, werden ignoriert.

Wenn [**enableautoconfig**](lan-policyschema-enableautoconfig-globalflags-element.md) auf false festgelegt ist, darf dieses Element nicht in einem LAN-Richtlinien Profil vorhanden sein. Wenn **enableautoconfig** auf true festgelegt ist, ist dieses Element erforderlich.

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

Das **ProfileList** -Element wird durch das [**lanpolicy**](lan-policyschema-lanpolicy-element.md) -Element definiert.

## <a name="remarks"></a>Bemerkungen

Dieses Element sollte genau ein Netzwerk Profil enthalten. Wenn mehr als ein Profil in der Richtlinie angegeben ist, wird nur das erste Netzwerk angewendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Lanpolicy**](lan-policyschema-lanpolicy-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Lanpolicy**](lan-policyschema-lanpolicy-element.md)
</dt> </dl>

 

 




