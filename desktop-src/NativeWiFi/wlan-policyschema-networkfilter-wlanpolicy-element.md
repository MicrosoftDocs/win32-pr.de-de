---
description: Definiert die Liste der zulässigen und verweigerten Netzwerke für Computer.
ms.assetid: 21502c97-36a4-4cd6-9dd0-ee44c4cc522f
title: Network Filter (wlanpolicy)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkFilter
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d78a23ba1a456f1ad45745fcc25580c27de148c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353910"
---
# <a name="networkfilter-wlanpolicy-element"></a>Network Filter (wlanpolicy)-Element

Das NetworkFilter (wlanpolicy)-Element definiert die Liste der zulässigen und verweigerten Netzwerke für Computer.

``` syntax
<xs:element name="networkFilter">
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
```

Das **NetworkFilter** -Element wird durch das [**wlanpolicy**](wlan-policyschema-wlanpolicy-element.md) -Element definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                    | type                                                                     | BESCHREIBUNG                                                                                    |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**Zulassungs**](wlan-policyschema-allowlist-networkfilter-element.md)     |                                                                          | Die Liste der Drahtlos-LAN-Netzwerke, denen jeder Computer eine Verbindung herstellen darf. <br/> |
| [**Blocklisten**](wlan-policyschema-blocklist-networkfilter-element.md)     |                                                                          | Die Liste der Drahtlos-LAN-Netzwerke, mit denen ein Computer keine Verbindung herstellen darf.<br/>              |
| [**denyalless**](wlan-policyschema-denyalless-networkfilter-element.md)   | boolean                                                                  | Gibt an, ob der Zugriff auf alle Infrastruktur Netzwerke blockiert ist. <br/>                     |
| [**denyallibss**](wlan-policyschema-denyallibss-networkfilter-element.md) | boolean                                                                  | Gibt an, ob der Zugriff auf alle Ad-hoc-Netzwerke blockiert ist. <br/>                             |
| [**Netzwerk**](wlan-policyschema-network-allowlist-element.md)             | [**networkitemtype**](wlan-policyschema-networkitemtype-complextype.md) | Ein zulässiges Netzwerk. <br/>                                                                |
| [**Netzwerk**](wlan-policyschema-network-blocklist-element.md)             | [**networkitemtype**](wlan-policyschema-networkitemtype-complextype.md) | Ein blockiertes Netzwerk. <br/>                                                                 |



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

 

 




