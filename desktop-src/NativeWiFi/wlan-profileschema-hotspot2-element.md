---
description: Erweitert das WLAN-Profil Schema V1 für die Unterstützung von Hotspot 2,0-Netzwerken.
ms.assetid: DE30DBCB-80B9-43D0-8DE1-56BBA99DBF31
title: Hotspot2 (wlanprofile)-Element
ms.topic: reference
ms.date: 10/08/2019
topic_type:
- APIRef
- kbSyntax
api_name:
- Hotspot2
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 0e372c1025a74dfb304cacdb0f3a4cf18bcdbabd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372861"
---
# <a name="hotspot2-wlanprofile-element"></a>Hotspot2 (wlanprofile)-Element

Erweitert das WLAN-Profil Schema V1 für die Unterstützung von Hotspot 2,0-Netzwerken. Hotspot 2,0 ermöglicht die automatische Verbindung mit öffentlichen Wi-Fi Diensten unter Verwendung vorhandener Anmelde Informationen und der Mitgliedschaft in Dienstanbieter Netzwerken. Dienstanbieter geben an, wie Verbindungen mithilfe der neuen Schema Elemente hergestellt werden, um zu beschreiben, welche Netzwerke verwendet werden sollen und wie Sie sich bei Ihnen authentifizieren.

``` syntax
<xs:element name="Hotspot2">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="DomainName"
                minOccurs="0"
             />
            <xs:element name="NAIRealm"
                minOccurs="0"
             />
            <xs:element name="Network3GPP"
                minOccurs="0"
             />
            <xs:element name="RoamingConsortium"
                minOccurs="0"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

Das-Element wird durch das [**wlanprofile**](wlan-profileschema-wlanprofile-element.md) -Element definiert.

## <a name="child-elements"></a>Untergeordnete Elemente

| Element | type | BESCHREIBUNG |
|-|-|-|
| [**DomainName**](wlan-profileschema-hotspot2-domainname-element.md) | | Der Domänen Name für den Heimnetzwerk Anbieter des Geräts, der den Netzwerk Operator identifiziert. |
| [**Nairealm**](wlan-profileschema-hotspot2-nairealm-element.md) | | Eine Liste von NAI-Bereichs Bezeichnern (Network Access Identifier). Einträge in dieser Liste sind normalerweise in der Form user@domain . |
| [**Network3GPP**](wlan-profileschema-hotspot2-network3gpp-element.md) | | Eine Liste von PLMN-IDs (Public Land Mobile Network). |
| [**Roamingconsortium**](wlan-profileschema-hotspot2-roamingconsortium-element.md) | | Eine Liste von durch IEEE zugewiesenen organizativ eindeutigen bezeichnerbezeichner.  |

## <a name="examples"></a>Beispiele

```xml
<Hotspot2>
  <DomainName>contoso.com</DomainName>
  <NAIRealm>
    <name>test1@contoso.com</name>
    <name>test2@contoso.com</name>
  </NAIRealm>
  <Network3GPP>
    <PLMNID>12345</PLMNID>
    <PLMNID>123456</PLMNID>
  </Network3GPP>
  <RoamingConsortium>
    <OUI>00AABB</OUI>
    <OUI>001122</OUI>
  </RoamingConsortium>
</Hotspot2>
```
