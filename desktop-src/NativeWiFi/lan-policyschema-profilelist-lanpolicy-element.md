---
description: 'profileList (LANPolicy)-Element: Enthält eine Liste von Profilen, die auf Domänen- oder Computerebene angewendet werden sollen.'
ms.assetid: 4f010449-0c6b-4a01-8253-4f82cd628f0a
title: profileList -Element (LANPolicy)
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
ms.openlocfilehash: 5d18ebc99f48bf72599afe750863d684b8158608
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090778"
---
# <a name="profilelist-lanpolicy-element"></a>profileList -Element (LANPolicy)

Das Element profileList (LANPolicy) enthält eine Liste von Profilen, die auf Domänen- oder Computerebene angewendet werden sollen. Profile müssen auf dem [ \_ LAN-Profilschema](lan-profileschema-schema.md)mit dem Stammelement [**LANProfile**](lan-profileschema-lanprofile-element.md)basieren. Profile, die auf einem anderen Schema basieren, werden ignoriert.

Wenn [**enableAutoConfig**](lan-policyschema-enableautoconfig-globalflags-element.md) auf FALSE festgelegt ist, darf dieses Element nicht in einem LAN-Richtlinienprofil vorhanden sein. Wenn **enableAutoConfig** auf TRUE festgelegt ist, ist dieses Element erforderlich.

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

Das **profileList-Element** wird durch das [**LANPolicy-Element**](lan-policyschema-lanpolicy-element.md) definiert.

## <a name="remarks"></a>Bemerkungen

Dieses Element sollte genau ein Netzwerkprofil enthalten. Wenn in der Richtlinie mehr als ein Profil angegeben ist, wird nur das erste Netzwerk angewendet.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**LANPolicy**](lan-policyschema-lanpolicy-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**LANPolicy**](lan-policyschema-lanpolicy-element.md)
</dt> </dl>

 

 




