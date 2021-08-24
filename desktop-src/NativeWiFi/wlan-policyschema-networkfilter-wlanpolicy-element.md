---
description: Definiert die Liste der zulässigen und verweigerten Netzwerke für Computer.
ms.assetid: 21502c97-36a4-4cd6-9dd0-ee44c4cc522f
title: networkFilter (WLANPolicy)-Element
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
ms.openlocfilehash: 1fff0738b8497bd52bee02a04402c77e959e2689c66e47519be20c95a58d56a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684380"
---
# <a name="networkfilter-wlanpolicy-element"></a>networkFilter (WLANPolicy)-Element

Das element networkFilter (WLANPolicy) definiert die Liste der zulässigen und verweigerten Netzwerke für Computer.

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

Das **networkFilter-Element** wird durch das [**WLANPolicy-Element**](wlan-policyschema-wlanpolicy-element.md) definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                    | Typ                                                                     | Beschreibung                                                                                    |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**allowList**](wlan-policyschema-allowlist-networkfilter-element.md)     |                                                                          | Die Liste der WLAN-Netzwerke, mit denen jeder Computer eine Verbindung herstellen darf. <br/> |
| [**Blocklist**](wlan-policyschema-blocklist-networkfilter-element.md)     |                                                                          | Die Liste der WLAN-Netzwerke, mit denen ein Computer keine Verbindung herstellen darf.<br/>              |
| [**denyAllESS**](wlan-policyschema-denyalless-networkfilter-element.md)   | boolean                                                                  | Gibt an, ob der Zugriff auf alle Infrastrukturnetzwerke blockiert ist. <br/>                     |
| [**denyAllIBSS**](wlan-policyschema-denyallibss-networkfilter-element.md) | boolean                                                                  | Gibt an, ob der Zugriff auf alle Ad-hoc-Netzwerke blockiert ist. <br/>                             |
| [**Netzwerk**](wlan-policyschema-network-allowlist-element.md)             | [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) | Ein zulässiges Netzwerk. <br/>                                                                |
| [**Netzwerk**](wlan-policyschema-network-blocklist-element.md)             | [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) | Ein blockiertes Netzwerk. <br/>                                                                 |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




