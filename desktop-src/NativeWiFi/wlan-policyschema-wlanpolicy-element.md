---
description: Enthält eine Drahtlos-LAN-Richtlinie.
ms.assetid: 16ffb682-f88b-4ca1-a902-d2db5e347975
title: Wlanpolicy-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLANPolicy
api_type:
- Schema
api_location: ''
ms.openlocfilehash: ec26a3cab15014deabca4e9332c1fbef7a788b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130433"
---
# <a name="wlanpolicy-element"></a>Wlanpolicy-Element

Das **wlanpolicy** -Element enthält eine Drahtlos-LAN-Richtlinie. Dieses Element ist das eindeutige root-Element für ein drahtlos Richtlinien Profil.

Der Ziel Namespace für das **wlanpolicy** -Element ist `https://www.microsoft.com/networking/WLAN/policy/v1` .

``` syntax
<xs:element name="WLANPolicy">
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
                        <xs:element name="showDeniedNetwork"
                            type="boolean"
                         />
                        <xs:element name="allowEveryoneToCreateAllUserProfiles"
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
            <xs:element name="networkFilter"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="allowList"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="network"
                                        type="networkItemType"
                                        maxOccurs="unbounded"
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
                        <xs:element name="blockList"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="network"
                                        type="networkItemType"
                                        maxOccurs="unbounded"
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
                        <xs:element name="denyAllIBSS"
                            type="boolean"
                            minOccurs="0"
                         />
                        <xs:element name="denyAllESS"
                            type="boolean"
                            minOccurs="0"
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



| Element                                                                                                                    | type                                                                     | BESCHREIBUNG                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**"Zuweisung von" "" "".**](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md) | boolean                                                                  | Gibt an, ob ein Benutzer ein Profil für alle Benutzer erstellen kann. <br/>                                                               |
| [**Zulassungs**](wlan-policyschema-allowlist-networkfilter-element.md)                                                     |                                                                          | Die Liste der Drahtlos-LAN-Netzwerke, denen jeder Computer eine Verbindung herstellen darf. <br/>                                       |
| [**Blocklisten**](wlan-policyschema-blocklist-networkfilter-element.md)                                                     |                                                                          | Die Liste der Drahtlos-LAN-Netzwerke, mit denen ein Computer keine Verbindung herstellen darf.<br/>                                                    |
| [**denyalless**](wlan-policyschema-denyalless-networkfilter-element.md)                                                   | boolean                                                                  | Gibt an, ob der Zugriff auf alle Infrastruktur Netzwerke blockiert ist. <br/>                                                           |
| [**denyallibss**](wlan-policyschema-denyallibss-networkfilter-element.md)                                                 | boolean                                                                  | Gibt an, ob der Zugriff auf alle Ad-hoc-Netzwerke blockiert ist. <br/>                                                                   |
| [**Beschreibung**](wlan-policyschema-description-wlanpolicy-element.md)                                                    | [**nametype**](wlan-policyschema-nametype-simpletype.md)                | Die Beschreibung einer Drahtlos-LAN-Richtlinie. <br/>                                                                                |
| [**enableautoconfig**](wlan-policyschema-enableautoconfig-globalflags-element.md)                                         | boolean                                                                  | Gibt an, ob Computer den integrierten automatischen Konfigurations Dienst (AutoConfig) zum Verwalten von Drahtlos Verbindungen verwenden. <br/> |
| [**globalflags**](wlan-policyschema-globalflags-wlanpolicy-element.md)                                                    |                                                                          | Enthält die globalen Einstellungen für das Auto Configuration Module (ACM). <br/>                                                    |
| [**Benennen**](wlan-policyschema-name-wlanpolicy-element.md)                                                                  | [**nametype**](wlan-policyschema-nametype-simpletype.md)                | Der Name einer Drahtlos-LAN-Richtlinie. <br/>                                                                                       |
| [**Netzwerk**](wlan-policyschema-network-allowlist-element.md)                                                             | [**networkitemtype**](wlan-policyschema-networkitemtype-complextype.md) | Ein zulässiges Netzwerk. <br/>                                                                                                      |
| [**Netzwerk**](wlan-policyschema-network-blocklist-element.md)                                                             | [**networkitemtype**](wlan-policyschema-networkitemtype-complextype.md) | Ein blockiertes Netzwerk. <br/>                                                                                                       |
| [**Network Filter**](wlan-policyschema-networkfilter-wlanpolicy-element.md)                                                |                                                                          | Die Liste der zugelassenen und verweigerten Netzwerke.<br/>                                                                                  |
| [**Profilliste**](wlan-policyschema-profilelist-wlanpolicy-element.md)                                                    |                                                                          | Enthält eine Liste der Profile, die auf Domänen-oder Computer Ebene angewendet werden sollen. <br/>                                                |
| [**showdeniednetwork**](wlan-policyschema-showdeniednetwork-globalflags-element.md)                                       | boolean                                                                  | Gibt an, ob abgelehnte Netzwerke im Assistenten **zum Herstellen einer Verbindung mit einem Netzwerk** angezeigt werden. <br/>                                         |



## <a name="remarks"></a>Bemerkungen

Informationen zum Anzeigen der Liste der untergeordneten Elemente in einer Struktur ähnlichen Struktur finden Sie unter [WLAN- \_ Richtlinien Schema Elemente](wlan-policyschema-elements.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 




