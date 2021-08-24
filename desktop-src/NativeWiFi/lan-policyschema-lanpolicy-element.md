---
description: Enthält eine LAN-Richtlinie für kabelgebundene Verbindungen.
ms.assetid: c06bdbc4-4199-4eec-a22f-684745912970
title: LANPolicy-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LANPolicy
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 468e9fb0500c4a514b7b0a9dddea023f0851b9f7ba783504548f2285810ffffa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780180"
---
# <a name="lanpolicy-element"></a>LANPolicy-Element

Das LANPolicy-Element enthält eine Lan-Richtlinie für kabelgebundene Verbindungen. Dieses Element ist das eindeutige Stammelement für ein Kabelnetzwerkrichtlinienprofil.

Der Zielnamespace für das **LANPolicy-Element** ist `https://www.microsoft.com/networking/LAN/policy/v1` .

``` syntax
<xs:element name="LANPolicy">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                type="nameType"
             />
            <xs:element name="description"
                type="nameType"
                minOccurs="0"
             />
            <xs:element name="globalFlags">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="enableAutoConfig"
                            type="boolean"
                         />
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="profileList"
                minOccurs="0"
            >
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
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                           | Typ                                                     | Beschreibung                                                                                                                                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Beschreibung**](lan-policyschema-description-lanpolicy-element.md)             | [**nameType**](lan-policyschema-nametype-simpletype.md) | Enthält die Beschreibung einer Kabel-LAN-Richtlinie. <br/>                                                                                                                          |
| [**enableAutoConfig**](lan-policyschema-enableautoconfig-globalflags-element.md) | boolean                                                  | Gibt an, ob Computer den integrierten automatischen Konfigurationsdienst verwenden, um Verbindungen mit kabelgebundenen Netzwerken zu verwalten, die eine Layer-2-Authentifizierung erfordern (z. B. 802.1X).<br/> |
| [**globalFlags**](lan-policyschema-globalflags-lanpolicy-element.md)             |                                                          | Enthält die globalen Einstellungen für die automatische Konfiguration verkabelter Netzwerke. <br/>                                                                                          |
| [**Namen**](lan-policyschema-name-lanpolicy-element.md)                           | [**nameType**](lan-policyschema-nametype-simpletype.md) | Enthält den Namen einer Kabel-LAN-Richtlinie. <br/>                                                                                                                                 |
| [**profileList**](lan-policyschema-profilelist-lanpolicy-element.md)             |                                                          | Enthält eine Liste der Profile, die auf Domänen- oder Computerebene angewendet werden sollen. <br/>                                                                                                |



## <a name="remarks"></a>Hinweise

Informationen zum Anzeigen der Liste der untergeordneten Elemente in einer strukturbasierten Struktur finden Sie unter [ \_ LAN-Richtlinienschemaelemente.](lan-policyschema-elements.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 




