---
description: Enthält eine WLAN-Richtlinie.
ms.assetid: 16ffb682-f88b-4ca1-a902-d2db5e347975
title: WLANPolicy-Element
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
ms.openlocfilehash: e9e56e25e51a3c6e798242b390f5d8b7341d7306455f1b15eb9e450830d3c9b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064700"
---
# <a name="wlanpolicy-element"></a>WLANPolicy-Element

Das **WLANPolicy-Element** enthält eine WLAN-Richtlinie. Dieses Element ist das eindeutige Stammelement für ein Drahtlosrichtlinienprofil.

Der Zielnamespace für das **WLANPolicy-Element** ist `https://www.microsoft.com/networking/WLAN/policy/v1` .

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
| [**allowEveryoneToCreateAllUserProfiles**](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md) | boolean                                                                  | Gibt an, ob ein Benutzer ein All-User-Profil erstellen kann. <br/>                                                               |
| [**allowList**](wlan-policyschema-allowlist-networkfilter-element.md)                                                     |                                                                          | Die Liste der WLAN-Netzwerke, mit denen jeder Computer eine Verbindung herstellen darf. <br/>                                       |
| [**Blocklist**](wlan-policyschema-blocklist-networkfilter-element.md)                                                     |                                                                          | Die Liste der WLAN-Netzwerke, mit denen ein Computer keine Verbindung herstellen darf.<br/>                                                    |
| [**denyAllESS**](wlan-policyschema-denyalless-networkfilter-element.md)                                                   | boolean                                                                  | Gibt an, ob der Zugriff auf alle Infrastrukturnetzwerke blockiert ist. <br/>                                                           |
| [**denyAllIBSS**](wlan-policyschema-denyallibss-networkfilter-element.md)                                                 | boolean                                                                  | Gibt an, ob der Zugriff auf alle Ad-hoc-Netzwerke blockiert ist. <br/>                                                                   |
| [**Beschreibung**](wlan-policyschema-description-wlanpolicy-element.md)                                                    | [**nameType**](wlan-policyschema-nametype-simpletype.md)                | Die Beschreibung einer WLAN-Richtlinie. <br/>                                                                                |
| [**enableAutoConfig**](wlan-policyschema-enableautoconfig-globalflags-element.md)                                         | boolean                                                                  | Gibt an, ob Computer den integrierten automatischen Konfigurationsdienst (AutoConfig) zum Verwalten von Drahtlosverbindungen verwenden. <br/> |
| [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md)                                                    |                                                                          | Enthält die globalen Einstellungen für das Auto Configuration Module (ACM). <br/>                                                    |
| [**Namen**](wlan-policyschema-name-wlanpolicy-element.md)                                                                  | [**nameType**](wlan-policyschema-nametype-simpletype.md)                | Der Name einer WLAN-Richtlinie. <br/>                                                                                       |
| [**Netzwerk**](wlan-policyschema-network-allowlist-element.md)                                                             | [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) | Ein zulässiges Netzwerk. <br/>                                                                                                      |
| [**Netzwerk**](wlan-policyschema-network-blocklist-element.md)                                                             | [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) | Ein blockiertes Netzwerk. <br/>                                                                                                       |
| [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md)                                                |                                                                          | Die Liste der zulässigen und verweigerten Netzwerke.<br/>                                                                                  |
| [**profileList**](wlan-policyschema-profilelist-wlanpolicy-element.md)                                                    |                                                                          | Enthält eine Liste von Profilen, die auf Domänen- oder Computerebene angewendet werden sollen. <br/>                                                |
| [**showDeniedNetwork**](wlan-policyschema-showdeniednetwork-globalflags-element.md)                                       | boolean                                                                  | Gibt an, ob abgelehnte Netzwerke im **Verbinden eines Netzwerk-Assistenten** angezeigt werden. <br/>                                         |



## <a name="remarks"></a>Hinweise

Informationen zum Anzeigen der Liste der untergeordneten Elemente in einer strukturähnlichen Struktur finden Sie unter Schemaelemente der [ \_ WLAN-Richtlinie.](wlan-policyschema-elements.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 




