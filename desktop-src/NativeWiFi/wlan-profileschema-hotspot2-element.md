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
# <a name="hotspot2-wlanprofile-element"></a><span data-ttu-id="f0ce4-103">Hotspot2 (wlanprofile)-Element</span><span class="sxs-lookup"><span data-stu-id="f0ce4-103">Hotspot2 (WLANProfile) element</span></span>

<span data-ttu-id="f0ce4-104">Erweitert das WLAN-Profil Schema V1 für die Unterstützung von Hotspot 2,0-Netzwerken.</span><span class="sxs-lookup"><span data-stu-id="f0ce4-104">Extends the WLAN Profile Schema v1 to support Hotspot 2.0 networks.</span></span> <span data-ttu-id="f0ce4-105">Hotspot 2,0 ermöglicht die automatische Verbindung mit öffentlichen Wi-Fi Diensten unter Verwendung vorhandener Anmelde Informationen und der Mitgliedschaft in Dienstanbieter Netzwerken.</span><span class="sxs-lookup"><span data-stu-id="f0ce4-105">Hotspot 2.0 enables automatic connection to public Wi-Fi services using existing credentials and membership in service provider networks.</span></span> <span data-ttu-id="f0ce4-106">Dienstanbieter geben an, wie Verbindungen mithilfe der neuen Schema Elemente hergestellt werden, um zu beschreiben, welche Netzwerke verwendet werden sollen und wie Sie sich bei Ihnen authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="f0ce4-106">Service providers specify how connections are made using the new schema elements to describe which networks to use, and how to authenticate to them.</span></span>

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

<span data-ttu-id="f0ce4-107">Das-Element wird durch das [**wlanprofile**](wlan-profileschema-wlanprofile-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="f0ce4-107">The element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f0ce4-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f0ce4-108">Child elements</span></span>

| <span data-ttu-id="f0ce4-109">Element</span><span class="sxs-lookup"><span data-stu-id="f0ce4-109">Element</span></span> | <span data-ttu-id="f0ce4-110">type</span><span class="sxs-lookup"><span data-stu-id="f0ce4-110">Type</span></span> | <span data-ttu-id="f0ce4-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f0ce4-111">Description</span></span> |
|-|-|-|
| [<span data-ttu-id="f0ce4-112">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="f0ce4-112">**DomainName**</span></span>](wlan-profileschema-hotspot2-domainname-element.md) | | <span data-ttu-id="f0ce4-113">Der Domänen Name für den Heimnetzwerk Anbieter des Geräts, der den Netzwerk Operator identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f0ce4-113">The domain name for the device's Home Network Provider, identifying the operator of the network.</span></span> |
| [<span data-ttu-id="f0ce4-114">**Nairealm**</span><span class="sxs-lookup"><span data-stu-id="f0ce4-114">**NAIRealm**</span></span>](wlan-profileschema-hotspot2-nairealm-element.md) | | <span data-ttu-id="f0ce4-115">Eine Liste von NAI-Bereichs Bezeichnern (Network Access Identifier).</span><span class="sxs-lookup"><span data-stu-id="f0ce4-115">A list of Network Access Identifier (NAI) Realm identifiers.</span></span> <span data-ttu-id="f0ce4-116">Einträge in dieser Liste sind normalerweise in der Form user@domain .</span><span class="sxs-lookup"><span data-stu-id="f0ce4-116">Entries in this list are usually of the form user@domain.</span></span> |
| [<span data-ttu-id="f0ce4-117">**Network3GPP**</span><span class="sxs-lookup"><span data-stu-id="f0ce4-117">**Network3GPP**</span></span>](wlan-profileschema-hotspot2-network3gpp-element.md) | | <span data-ttu-id="f0ce4-118">Eine Liste von PLMN-IDs (Public Land Mobile Network).</span><span class="sxs-lookup"><span data-stu-id="f0ce4-118">A list of Public Land Mobile Network (PLMN) IDs.</span></span> |
| [<span data-ttu-id="f0ce4-119">**Roamingconsortium**</span><span class="sxs-lookup"><span data-stu-id="f0ce4-119">**RoamingConsortium**</span></span>](wlan-profileschema-hotspot2-roamingconsortium-element.md) | | <span data-ttu-id="f0ce4-120">Eine Liste von durch IEEE zugewiesenen organizativ eindeutigen bezeichnerbezeichner.</span><span class="sxs-lookup"><span data-stu-id="f0ce4-120">A list of Organizationally Unique Identifiers (OUI) assigned by IEEE.</span></span>  |

## <a name="examples"></a><span data-ttu-id="f0ce4-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f0ce4-121">Examples</span></span>

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
