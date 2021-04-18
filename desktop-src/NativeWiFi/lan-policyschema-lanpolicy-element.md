---
description: Enthält eine verkabelte LAN-Richtlinie.
ms.assetid: c06bdbc4-4199-4eec-a22f-684745912970
title: Lanpolicy-Element
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
ms.openlocfilehash: 1b424a47405aa8f32276019a85902bd51b173cc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347477"
---
# <a name="lanpolicy-element"></a>Lanpolicy-Element

Das lanpolicy-Element enthält eine verkabelte LAN-Richtlinie. Dieses Element ist das eindeutige root-Element für ein kabelgebundenes Netzwerk Richtlinien Profil.

Der Ziel Namespace für das **lanpolicy** -Element ist `https://www.microsoft.com/networking/LAN/policy/v1` .

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



| Element                                                                           | type                                                     | BESCHREIBUNG                                                                                                                                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Beschreibung**](lan-policyschema-description-lanpolicy-element.md)             | [**nametype**](lan-policyschema-nametype-simpletype.md) | Enthält die Beschreibung einer kabelgebundenen LAN-Richtlinie. <br/>                                                                                                                          |
| [**enableautoconfig**](lan-policyschema-enableautoconfig-globalflags-element.md) | boolean                                                  | Gibt an, ob Computer den integrierten automatischen Konfigurations Dienst zum Verwalten von Verbindungen mit verkabelten Netzwerken verwenden, die Layer 2-Authentifizierung erfordern (z. b. 802.1 x).<br/> |
| [**globalflags**](lan-policyschema-globalflags-lanpolicy-element.md)             |                                                          | Enthält die globalen Einstellungen für die automatische Konfiguration von verkabelten Netzwerken. <br/>                                                                                          |
| [**Benennen**](lan-policyschema-name-lanpolicy-element.md)                           | [**nametype**](lan-policyschema-nametype-simpletype.md) | Enthält den Namen einer kabelgebundenen LAN-Richtlinie. <br/>                                                                                                                                 |
| [**Profilliste**](lan-policyschema-profilelist-lanpolicy-element.md)             |                                                          | Enthält eine Liste der Profile, die auf Domänen-oder Computer Ebene angewendet werden sollen. <br/>                                                                                                |



## <a name="remarks"></a>Bemerkungen

Informationen zum Anzeigen der Liste der untergeordneten Elemente in einer Struktur ähnlichen Struktur finden Sie unter [LAN- \_ Richtlinien Schema Elemente](lan-policyschema-elements.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 




