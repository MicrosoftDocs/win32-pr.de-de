---
description: Enthält ein WLAN-Profil.
ms.assetid: bc97cb49-3891-4a4a-aab4-895cd9ce6908
title: Wlanprofile-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLANProfile
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 227d912128bf3f656fca7aecbaf0fe0640659465
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868635"
---
# <a name="wlanprofile-element"></a><span data-ttu-id="63fe5-103">Wlanprofile-Element</span><span class="sxs-lookup"><span data-stu-id="63fe5-103">WLANProfile Element</span></span>

<span data-ttu-id="63fe5-104">Das **wlanprofile** -Element enthält ein WLAN-Profil.</span><span class="sxs-lookup"><span data-stu-id="63fe5-104">The **WLANProfile** element contains a wireless LAN profile.</span></span> <span data-ttu-id="63fe5-105">Dieses Element ist das eindeutige root-Element für ein drahtlos Profil.</span><span class="sxs-lookup"><span data-stu-id="63fe5-105">This element is the unique root element for a wireless profile.</span></span>

<span data-ttu-id="63fe5-106">Der Ziel Namespace für das wlanprofile-Element ist `https://www.microsoft.com/networking/WLAN/profile/v1` .</span><span class="sxs-lookup"><span data-stu-id="63fe5-106">The target namespace for the WLANProfile element is `https://www.microsoft.com/networking/WLAN/profile/v1`.</span></span>

``` syntax
<xs:element name="WLANProfile">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                type="nameType"
             />
            <xs:element name="SSIDConfig"
                maxOccurs="256"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="SSID"
                            maxOccurs="256"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="hex"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="hexBinary"
                                            >
                                                <xs:minLength
                                                    value="1"
                                                 />
                                                <xs:maxLength
                                                    value="32"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="name"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="string"
                                            >
                                                <xs:minLength
                                                    value="1"
                                                 />
                                                <xs:maxLength
                                                    value="32"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
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
                        <xs:element name="nonBroadcast"
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
            <xs:element name="connectionType">
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="IBSS"
                         />
                        <xs:enumeration
                            value="ESS"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="connectionMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="auto"
                         />
                        <xs:enumeration
                            value="manual"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="autoSwitch"
                type="boolean"
                minOccurs="0"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
            <xs:element name="MSM"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="connectivity"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="phyType"
                                        minOccurs="0"
                                        maxOccurs="4"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="string"
                                            >
                                                <xs:enumeration
                                                    value="a"
                                                 />
                                                <xs:enumeration
                                                    value="b"
                                                 />
                                                <xs:enumeration
                                                    value="g"
                                                 />
                                                <xs:enumeration
                                                    value="n"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
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
                        <xs:element name="security"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="authEncryption">
                                        <xs:complexType>
                                            <xs:sequence>
                                                <xs:element name="authentication">
                                                    <xs:simpleType>
                                                        <xs:restriction
                                                            base="string"
                                                        >
                                                            <xs:enumeration
                                                                value="open"
                                                             />
                                                            <xs:enumeration
                                                                value="shared"
                                                             />
                                                            <xs:enumeration
                                                                value="WPA"
                                                             />
                                                            <xs:enumeration
                                                                value="WPAPSK"
                                                             />
                                                            <xs:enumeration
                                                                value="WPA2"
                                                             />
                                                            <xs:enumeration
                                                                value="WPA2PSK"
                                                             />
                                                        </xs:restriction>
                                                    </xs:simpleType>
                                                </xs:element>
                                                <xs:element name="encryption">
                                                    <xs:simpleType>
                                                        <xs:restriction
                                                            base="string"
                                                        >
                                                            <xs:enumeration
                                                                value="none"
                                                             />
                                                            <xs:enumeration
                                                                value="WEP"
                                                             />
                                                            <xs:enumeration
                                                                value="TKIP"
                                                             />
                                                            <xs:enumeration
                                                                value="AES"
                                                             />
                                                        </xs:restriction>
                                                    </xs:simpleType>
                                                </xs:element>
                                                <xs:element name="useOneX"
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
                                    <xs:element name="sharedKey"
                                        minOccurs="0"
                                    >
                                        <xs:complexType>
                                            <xs:sequence>
                                                <xs:element name="keyType">
                                                    <xs:simpleType>
                                                        <xs:restriction
                                                            base="string"
                                                        >
                                                            <xs:enumeration
                                                                value="networkKey"
                                                             />
                                                            <xs:enumeration
                                                                value="passPhrase"
                                                             />
                                                        </xs:restriction>
                                                    </xs:simpleType>
                                                </xs:element>
                                                <xs:element name="protected"
                                                    type="boolean"
                                                 />
                                                <xs:element name="keyMaterial"
                                                    type="string"
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
                                    <xs:element name="keyIndex"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="integer"
                                            >
                                                <xs:minInclusive
                                                    value="0"
                                                 />
                                                <xs:maxInclusive
                                                    value="3"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="PMKCacheMode"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="string"
                                            >
                                                <xs:enumeration
                                                    value="disabled"
                                                 />
                                                <xs:enumeration
                                                    value="enabled"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="PMKCacheTTL"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="integer"
                                            >
                                                <xs:minInclusive
                                                    value="5"
                                                 />
                                                <xs:maxInclusive
                                                    value="1400"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="PMKCacheSize"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="integer"
                                            >
                                                <xs:minInclusive
                                                    value="1"
                                                 />
                                                <xs:maxInclusive
                                                    value="255"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="preAuthMode"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="string"
                                            >
                                                <xs:enumeration
                                                    value="disabled"
                                                 />
                                                <xs:enumeration
                                                    value="enabled"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="preAuthThrottle"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="integer"
                                            >
                                                <xs:minInclusive
                                                    value="1"
                                                 />
                                                <xs:maxInclusive
                                                    value="16"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
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
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="IHV"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="OUIHeader">
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="OUI">
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="hexBinary"
                                            >
                                                <xs:length
                                                    value="3"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="type">
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="hexBinary"
                                            >
                                                <xs:length
                                                    value="1"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
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
                        <xs:element name="connectivity"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:any
                                        processContents="lax"
                                        namespace="##other"
                                     />
                                </xs:sequence>
                            </xs:complexType>
                        </xs:element>
                        <xs:element name="security"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:any
                                        processContents="lax"
                                        namespace="##other"
                                     />
                                </xs:sequence>
                            </xs:complexType>
                        </xs:element>
                        <xs:element name="useMSOneX"
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

## <a name="child-elements"></a><span data-ttu-id="63fe5-107">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="63fe5-107">Child elements</span></span>



| <span data-ttu-id="63fe5-108">Element</span><span class="sxs-lookup"><span data-stu-id="63fe5-108">Element</span></span>                                                                            | <span data-ttu-id="63fe5-109">type</span><span class="sxs-lookup"><span data-stu-id="63fe5-109">Type</span></span>                                                              | <span data-ttu-id="63fe5-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="63fe5-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="63fe5-111">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="63fe5-111">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)       |                                                                   | <span data-ttu-id="63fe5-112">Gibt das Authentifizierungs-und Verschlüsselungs Paar an, das für dieses Profil verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="63fe5-112">Specifies the authentication and encryption pair to be used for this profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="63fe5-113">**Genehmigung**</span><span class="sxs-lookup"><span data-stu-id="63fe5-113">**authentication**</span></span>](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | <span data-ttu-id="63fe5-114">Gibt die Authentifizierungsmethode an, die zum Herstellen einer Verbindung mit dem Drahtlos Netzwerk verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="63fe5-114">Specifies the authentication method to be used to connect to the wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="63fe5-115">**autoswitch**</span><span class="sxs-lookup"><span data-stu-id="63fe5-115">**autoSwitch**</span></span>](wlan-profileschema-autoswitch-wlanprofile-element.md)            | [<span data-ttu-id="63fe5-116">boolean</span><span class="sxs-lookup"><span data-stu-id="63fe5-116">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="63fe5-117">Bestimmt das Roamingverhalten eines automatisch verbundenen Netzwerks, wenn ein bevorzugtes Netzwerk in Reichweite ist.</span><span class="sxs-lookup"><span data-stu-id="63fe5-117">Determines the roaming behavior of an auto-connected network when a more preferred network is in range.</span></span> <span data-ttu-id="63fe5-118">Dieses Element ist optional und hat keine Auswirkung auf ein manuell verbundenes Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="63fe5-118">This element is optional and has no effect on a manually connected network.</span></span><br/> <span data-ttu-id="63fe5-119">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63fe5-119">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="63fe5-120">**connectionMode**</span><span class="sxs-lookup"><span data-stu-id="63fe5-120">**connectionMode**</span></span>](wlan-profileschema-connectionmode-wlanprofile-element.md)    |                                                                   | <span data-ttu-id="63fe5-121">Gibt an, ob die Verbindung mit dem Drahtlos LAN automatisch ("Auto") oder vom Benutzer initiiert ("manuell") erfolgen soll.</span><span class="sxs-lookup"><span data-stu-id="63fe5-121">Indicates whether connection to the wireless LAN should be automatic ("auto") or initiated ("manual") by user.</span></span> <span data-ttu-id="63fe5-122">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="63fe5-122">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="63fe5-123">**connectionType**</span><span class="sxs-lookup"><span data-stu-id="63fe5-123">**connectionType**</span></span>](wlan-profileschema-connectiontype-wlanprofile-element.md)    |                                                                   | <span data-ttu-id="63fe5-124">Gibt an, ob das Netzwerk Infrastructure ("ESS") oder Ad-hoc ("IBSS") ist.</span><span class="sxs-lookup"><span data-stu-id="63fe5-124">Indicates whether the network is infrastructure ("ESS") or ad-hoc ("IBSS").</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="63fe5-125">**Stech**</span><span class="sxs-lookup"><span data-stu-id="63fe5-125">**connectivity**</span></span>](wlan-profileschema-connectivity-msm-element.md)                |                                                                   | <span data-ttu-id="63fe5-126">Enthält verschiedene Konnektivitätseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="63fe5-126">Contains various connectivity settings.</span></span> <span data-ttu-id="63fe5-127">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="63fe5-127">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="63fe5-128">**Stech**</span><span class="sxs-lookup"><span data-stu-id="63fe5-128">**connectivity**</span></span>](wlan-profileschema-connectivity-ihv-element.md)                |                                                                   | <span data-ttu-id="63fe5-129">Enthält IHV-bezogene Konnektivitätseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="63fe5-129">Contains IHV-related connectivity settings.</span></span><br/> <span data-ttu-id="63fe5-130">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63fe5-130">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="63fe5-131">**Verschlüsselungs**</span><span class="sxs-lookup"><span data-stu-id="63fe5-131">**encryption**</span></span>](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | <span data-ttu-id="63fe5-132">Legt die Datenverschlüsselung fest, die zum Herstellen einer Verbindung mit dem Drahtlos Netzwerk verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="63fe5-132">Sets the data encryption to use to connect to the wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="63fe5-133">**hex**</span><span class="sxs-lookup"><span data-stu-id="63fe5-133">**hex**</span></span>](wlan-profileschema-hex-ssid-element.md)                                 |                                                                   | <span data-ttu-id="63fe5-134">Enthält die SSID eines Drahtlos-LANs im Hexadezimal Format.</span><span class="sxs-lookup"><span data-stu-id="63fe5-134">Contains the SSID of a wireless LAN in hexadecimal format.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="63fe5-135">**IHV**</span><span class="sxs-lookup"><span data-stu-id="63fe5-135">**IHV**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)                          |                                                                   | <span data-ttu-id="63fe5-136">Enthält optionale IHV-Einstellungen (Independent Hardware Vendor).</span><span class="sxs-lookup"><span data-stu-id="63fe5-136">Contains optional independent hardware vendor (IHV) settings.</span></span><br/> <span data-ttu-id="63fe5-137">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63fe5-137">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="63fe5-138">**keyIndex**</span><span class="sxs-lookup"><span data-stu-id="63fe5-138">**keyIndex**</span></span>](wlan-profileschema-keyindex-security-element.md)                   |                                                                   | <span data-ttu-id="63fe5-139">Gibt an, welcher Schlüssel Index verwendet werden soll, um drahtlosen Datenverkehr zu verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="63fe5-139">Specifies which key index should be used to encrypt wireless traffic.</span></span> <span data-ttu-id="63fe5-140">Dies wird nur verwendet, wenn [**KeyType**](wlan-profileschema-keytype-sharedkey-element.md) auf "networkkey" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="63fe5-140">This is only used when [**keyType**](wlan-profileschema-keytype-sharedkey-element.md) is set to "networkKey".</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="63fe5-141">**keyMaterial**</span><span class="sxs-lookup"><span data-stu-id="63fe5-141">**keyMaterial**</span></span>](wlan-profileschema-keymaterial-sharedkey-element.md)            | [<span data-ttu-id="63fe5-142">string</span><span class="sxs-lookup"><span data-stu-id="63fe5-142">string</span></span>](/dotnet/api/system.string)   | <span data-ttu-id="63fe5-143">Enthält den Netzwerkschlüssel oder die Passphrase.</span><span class="sxs-lookup"><span data-stu-id="63fe5-143">Contains the network key or passphrase.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="63fe5-144">**keyType**</span><span class="sxs-lookup"><span data-stu-id="63fe5-144">**keyType**</span></span>](wlan-profileschema-keytype-sharedkey-element.md)                    |                                                                   | <span data-ttu-id="63fe5-145">Der Schlüsseltyp.</span><span class="sxs-lookup"><span data-stu-id="63fe5-145">Type of key.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="63fe5-146">**MSM**</span><span class="sxs-lookup"><span data-stu-id="63fe5-146">**MSM**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)                          |                                                                   | <span data-ttu-id="63fe5-147">Enthält verschiedene MSM-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="63fe5-147">Contains various MSM settings.</span></span> <span data-ttu-id="63fe5-148">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="63fe5-148">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="63fe5-149">**Benennen**</span><span class="sxs-lookup"><span data-stu-id="63fe5-149">**name**</span></span>](wlan-profileschema-name-wlanprofile-element.md)                        | [<span data-ttu-id="63fe5-150">**nametype**</span><span class="sxs-lookup"><span data-stu-id="63fe5-150">**nameType**</span></span>](wlan-profileschema-nametype-simpletype.md)        | <span data-ttu-id="63fe5-151">Der Name des WLAN-Profils.</span><span class="sxs-lookup"><span data-stu-id="63fe5-151">Name of the WLAN profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="63fe5-152">**Benennen**</span><span class="sxs-lookup"><span data-stu-id="63fe5-152">**name**</span></span>](wlan-profileschema-name-ssid-element.md)                               |                                                                   | <span data-ttu-id="63fe5-153">Enthält die SSID eines drahtlosen LANs.</span><span class="sxs-lookup"><span data-stu-id="63fe5-153">Contains the SSID of a wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="63fe5-154">**nicht Broadcast**</span><span class="sxs-lookup"><span data-stu-id="63fe5-154">**nonBroadcast**</span></span>](wlan-profileschema-nonbroadcast-ssidconfig-element.md)         | [<span data-ttu-id="63fe5-155">boolean</span><span class="sxs-lookup"><span data-stu-id="63fe5-155">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="63fe5-156">Gibt an, ob das Netzwerk seine SSID überträgt.</span><span class="sxs-lookup"><span data-stu-id="63fe5-156">Indicates whether the network broadcasts its SSID.</span></span><br/> <span data-ttu-id="63fe5-157">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63fe5-157">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="63fe5-158">**Ische**</span><span class="sxs-lookup"><span data-stu-id="63fe5-158">**OUI**</span></span>](wlan-profileschema-oui-ouiheader-element.md)                            |                                                                   | <span data-ttu-id="63fe5-159">Enthält eine hexbinär Datei mit 3 Bytes, die den IHV identifiziert.</span><span class="sxs-lookup"><span data-stu-id="63fe5-159">Contains a 3 byte hexBinary that identifies the IHV.</span></span><br/> <span data-ttu-id="63fe5-160">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63fe5-160">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="63fe5-161">**Ouiheader**</span><span class="sxs-lookup"><span data-stu-id="63fe5-161">**OUIHeader**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)                      |                                                                   | <span data-ttu-id="63fe5-162">Identifiziert den IHV.</span><span class="sxs-lookup"><span data-stu-id="63fe5-162">Identifies the IHV.</span></span><br/> <span data-ttu-id="63fe5-163">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63fe5-163">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="63fe5-164">**phytype**</span><span class="sxs-lookup"><span data-stu-id="63fe5-164">**phyType**</span></span>](wlan-profileschema-phytype-connectivity-element.md)                 |                                                                   | <span data-ttu-id="63fe5-165">Gibt den 802,11 Wireless LAN-Standard an, der auf dem Drahtlos Netzwerk verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="63fe5-165">Specifies the 802.11 wireless LAN standard used on the wireless LAN.</span></span> <span data-ttu-id="63fe5-166">Der Wert "n" wird nur unter Windows Vista mit SP1 und höheren Versionen des Betriebssystems unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63fe5-166">The value "n" is only supported on Windows Vista with SP1 and later versions of the operating system.</span></span><br/> <span data-ttu-id="63fe5-167">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63fe5-167">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="63fe5-168">**PMKCacheMode**</span><span class="sxs-lookup"><span data-stu-id="63fe5-168">**PMKCacheMode**</span></span>](wlan-profileschema-pmkcachemode-security-element.md)           |                                                                   | <span data-ttu-id="63fe5-169">Gibt an, ob die PMK-Zwischenspeicherung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="63fe5-169">Indicates whether PMK caching will be used.</span></span> <span data-ttu-id="63fe5-170">Dieses Element ist nur für WPA2-definierte Netzwerke gültig.</span><span class="sxs-lookup"><span data-stu-id="63fe5-170">This element is valid only for WPA2-defined networks.</span></span><br/> <span data-ttu-id="63fe5-171">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63fe5-171">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="63fe5-172">**PMKCacheSize**</span><span class="sxs-lookup"><span data-stu-id="63fe5-172">**PMKCacheSize**</span></span>](wlan-profileschema-pmkcachesize-security-element.md)           |                                                                   | <span data-ttu-id="63fe5-173">Gibt die Anzahl der Einträge im PMK-Cache auf dem Client an.</span><span class="sxs-lookup"><span data-stu-id="63fe5-173">Specifies the number of entries in the PMK cache on the client.</span></span> <span data-ttu-id="63fe5-174">Dieses Element gilt nur für WPA2-definierte Netzwerke, bei denen [**pmkcachemode**](wlan-profileschema-pmkcachemode-security-element.md) auf "aktiviert" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="63fe5-174">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="63fe5-175">Wenn **pmkcachemode** aktiviert ist und dieses Element nicht vorhanden ist, wird die Größe des Caches standardmäßig auf 128 Einträge eingestellt.</span><span class="sxs-lookup"><span data-stu-id="63fe5-175">If **PMKCacheMode** is enabled, and this element is absent, the size of the cache defaults to 128 entries.</span></span><br/> <span data-ttu-id="63fe5-176">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63fe5-176">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="63fe5-177">**PMKCacheTTL**</span><span class="sxs-lookup"><span data-stu-id="63fe5-177">**PMKCacheTTL**</span></span>](wlan-profileschema-pmkcachettl-security-element.md)             |                                                                   | <span data-ttu-id="63fe5-178">Gibt die Zeitdauer in Minuten an, die ein PMK-Cache aufbewahrt wird.</span><span class="sxs-lookup"><span data-stu-id="63fe5-178">Indicates the length of time, in minutes, that a PMK cache will be kept.</span></span> <span data-ttu-id="63fe5-179">Dieses Element gilt nur für WPA2-definierte Netzwerke, bei denen [**pmkcachemode**](wlan-profileschema-pmkcachemode-security-element.md) auf "aktiviert" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="63fe5-179">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span><br/> <span data-ttu-id="63fe5-180">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63fe5-180">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="63fe5-181">**preAuthMode**</span><span class="sxs-lookup"><span data-stu-id="63fe5-181">**preAuthMode**</span></span>](wlan-profileschema-preauthmode-security-element.md)             |                                                                   | <span data-ttu-id="63fe5-182">Bestimmt, ob die Vorauthentifizierung vom Client verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="63fe5-182">Determines if pre-authentication will be used by the client.</span></span> <span data-ttu-id="63fe5-183">Die Vorauthentifizierung ermöglicht WPA2-sicheres schnelles Roaming.</span><span class="sxs-lookup"><span data-stu-id="63fe5-183">Pre-authentication enables WPA2 secure fast roaming.</span></span> <span data-ttu-id="63fe5-184">Dieses Element gilt nur für WPA2-definierte Netzwerke, bei denen [**pmkcachemode**](wlan-profileschema-pmkcachemode-security-element.md) auf "aktiviert" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="63fe5-184">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="63fe5-185">Wenn **pmkcachemode** aktiviert ist und dieses Element nicht vorhanden ist, wird der Standardwert deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="63fe5-185">If **PMKCacheMode** is enabled, and this element is absent, the default value is disabled.</span></span><br/> <span data-ttu-id="63fe5-186">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63fe5-186">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="63fe5-187">**preAuthThrottle**</span><span class="sxs-lookup"><span data-stu-id="63fe5-187">**preAuthThrottle**</span></span>](wlan-profileschema-preauththrottle-security-element.md)     |                                                                   | <span data-ttu-id="63fe5-188">Gibt die Anzahl der Versuche bei der Vorauthentifizierung bei benachbarten APS an.</span><span class="sxs-lookup"><span data-stu-id="63fe5-188">Indicates the number of tries when preauthenticating to neighboring APs.</span></span> <span data-ttu-id="63fe5-189">Dieses Element gilt nur für WPA2-definierte Netzwerke, bei denen [**pmkcachemode**](wlan-profileschema-pmkcachemode-security-element.md) auf "aktiviert" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="63fe5-189">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="63fe5-190">Wenn **pmkcachemode** aktiviert ist und dieses Element nicht vorhanden ist, wird für die Anzahl von versuchen standardmäßig der Wert 3 verwendet.</span><span class="sxs-lookup"><span data-stu-id="63fe5-190">If **PMKCacheMode** is enabled, and this element is absent, the number of tries defaults to 3.</span></span><br/> <span data-ttu-id="63fe5-191">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63fe5-191">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="63fe5-192">**protected**</span><span class="sxs-lookup"><span data-stu-id="63fe5-192">**protected**</span></span>](wlan-profileschema-protected-sharedkey-element.md)                | [<span data-ttu-id="63fe5-193">boolean</span><span class="sxs-lookup"><span data-stu-id="63fe5-193">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="63fe5-194">Gibt an, ob der Schlüssel verschlüsselt ist.</span><span class="sxs-lookup"><span data-stu-id="63fe5-194">Indicates whether the key is encrypted.</span></span><br/> <span data-ttu-id="63fe5-195">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element muss den Wert **false** aufweisen.</span><span class="sxs-lookup"><span data-stu-id="63fe5-195">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element must have a value of **FALSE**.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="63fe5-196">**Sicherung**</span><span class="sxs-lookup"><span data-stu-id="63fe5-196">**security**</span></span>](wlan-profileschema-security-msm-element.md)                        |                                                                   | <span data-ttu-id="63fe5-197">Enthält verschiedene Sicherheitseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="63fe5-197">Contains various security settings.</span></span> <span data-ttu-id="63fe5-198">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="63fe5-198">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="63fe5-199">**Sicherung**</span><span class="sxs-lookup"><span data-stu-id="63fe5-199">**security**</span></span>](wlan-profileschema-security-ihv-element.md)                        |                                                                   | <span data-ttu-id="63fe5-200">Enthält IHV-spezifische Sicherheitseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="63fe5-200">Contains IHV-specific security settings.</span></span> <span data-ttu-id="63fe5-201">Die Sicherheitseinstellungen von Microsoft und die IHV-Sicherheitseinstellungen schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="63fe5-201">Microsoft security settings and IHV security settings are mutually exclusive.</span></span> <span data-ttu-id="63fe5-202">Wenn beide Gruppen von Sicherheitseinstellungen im gleichen Profil vorhanden sind, ist das Profil ungültig.</span><span class="sxs-lookup"><span data-stu-id="63fe5-202">If both sets of security settings are present in the same profile, the profile is invalid.</span></span><br/> <span data-ttu-id="63fe5-203">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63fe5-203">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="63fe5-204">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="63fe5-204">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)                 |                                                                   | <span data-ttu-id="63fe5-205">Enthält die Informationen zum gemeinsamen Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="63fe5-205">Contains the shared key information.</span></span> <span data-ttu-id="63fe5-206">Dieses Element ist nur erforderlich, wenn für das Authentifizierungs-und Verschlüsselungs paar WEP-oder PSK-Schlüssel erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="63fe5-206">This element is only required if WEP or PSK keys are required for the authentication and encryption pair.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="63fe5-207">**SSID**</span><span class="sxs-lookup"><span data-stu-id="63fe5-207">**SSID**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)                         |                                                                   | <span data-ttu-id="63fe5-208">Gibt die SSID eines drahtlosen LANs an.</span><span class="sxs-lookup"><span data-stu-id="63fe5-208">Specifies the SSID of a wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="63fe5-209">**SSIDConfig**</span><span class="sxs-lookup"><span data-stu-id="63fe5-209">**SSIDConfig**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)            |                                                                   | <span data-ttu-id="63fe5-210">Enthält eine oder mehrere SSIDs zusammen mit anderen allgemeinen Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="63fe5-210">Contains one or more SSIDs along with other common settings.</span></span> <br/> <span data-ttu-id="63fe5-211">Ein Profil kann über mehrere [**ssidconfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) -Elemente verfügen, und jedes [**ssidconfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) -Element kann mehrere [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) -Elemente aufweisen.</span><span class="sxs-lookup"><span data-stu-id="63fe5-211">A profile can have multiple [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) elements and each [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) element can have multiple [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) elements.</span></span> <span data-ttu-id="63fe5-212">Allerdings berücksichtigt Windows nur das erste [**ssidconfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) -Element in einem [**wlanprofile**](wlan-profileschema-wlanprofile-element.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="63fe5-212">However, Windows only ever considers the first [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) element in a [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span><br/> <span data-ttu-id="63fe5-213">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Höchstens ein [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) -Element kann in einem Profil angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="63fe5-213">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** At most one [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element can appear in a profile.</span></span><br/> |
| [<span data-ttu-id="63fe5-214">**Sorte**</span><span class="sxs-lookup"><span data-stu-id="63fe5-214">**type**</span></span>](wlan-profileschema-type-ouiheader-element.md)                          |                                                                   | <span data-ttu-id="63fe5-215">Enthält eine **hexbinär Datei** mit 1 Byte, die zur Unterscheidung von NICs durch denselben IHV verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="63fe5-215">Contains a 1 byte **hexBinary** that is used to differentiate NICs by the same IHV.</span></span><br/> <span data-ttu-id="63fe5-216">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63fe5-216">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="63fe5-217">**usemsonex**</span><span class="sxs-lookup"><span data-stu-id="63fe5-217">**useMSOneX**</span></span>](wlan-profileschema-usemsonex-ihv-element.md)                      | [<span data-ttu-id="63fe5-218">boolean</span><span class="sxs-lookup"><span data-stu-id="63fe5-218">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="63fe5-219">Gibt den Ursprung der 802.1 x-Sicherheitseinstellungen an, die von einer IHV-Sicherheitskomponente verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="63fe5-219">Specifies the origin of 802.1X security settings used by an IHV security component.</span></span> <span data-ttu-id="63fe5-220">Wenn [**usemsonex**](wlan-profileschema-usemsonex-ihv-element.md) auf true festgelegt ist, verwenden die IHV-Sicherheitskomponenten von Microsoft definierte 802.1 x-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="63fe5-220">When [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md) is true, IHV security components use Microsoft-defined 802.1X settings.</span></span> <span data-ttu-id="63fe5-221">Wenn **usemsonex** den Wert false hat, verwenden IHV-Sicherheitskomponenten vom Hersteller bereitgestellte 802.1 x-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="63fe5-221">When **useMSOneX** is false, IHV security components use vendor-supplied 802.1X settings.</span></span> <span data-ttu-id="63fe5-222">Standardmäßig ist **usemsonex** false.</span><span class="sxs-lookup"><span data-stu-id="63fe5-222">By default, **useMSOneX** is false.</span></span> <span data-ttu-id="63fe5-223">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="63fe5-223">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="63fe5-224">**useOneX**</span><span class="sxs-lookup"><span data-stu-id="63fe5-224">**useOneX**</span></span>](wlan-profileschema-useonex-authencryption-element.md)               | [<span data-ttu-id="63fe5-225">boolean</span><span class="sxs-lookup"><span data-stu-id="63fe5-225">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="63fe5-226">Gibt an, ob 802.1 x verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="63fe5-226">Indicates whether 802.1X is used.</span></span> <span data-ttu-id="63fe5-227">Dieses Flag ist optional.</span><span class="sxs-lookup"><span data-stu-id="63fe5-227">This flag is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



## <a name="remarks"></a><span data-ttu-id="63fe5-228">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="63fe5-228">Remarks</span></span>

<span data-ttu-id="63fe5-229">Die meisten untergeordneten Elemente des wlanprofile-Elements befinden sich im- `https://www.microsoft.com/networking/WLAN/profile/v1` Namespace.</span><span class="sxs-lookup"><span data-stu-id="63fe5-229">Most child elements of the WLANProfile element are in the `https://www.microsoft.com/networking/WLAN/profile/v1` namespace.</span></span> <span data-ttu-id="63fe5-230">Es gibt zwei Ausnahmen: das " [**ppsmode**](wlan-profileschema-fipsmode-authencryption-element.md) "-Element befindet sich im `https://www.microsoft.com/networking/WLAN/profile/v2` -Namespace, und das [**Onex**](onexschema-onex-element.md) -Element befindet sich im- `https://www.microsoft.com/networking/OneX/v1` Namespace.</span><span class="sxs-lookup"><span data-stu-id="63fe5-230">There are two exceptions: the [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element is in the `https://www.microsoft.com/networking/WLAN/profile/v2` namespace and the [**OneX**](onexschema-onex-element.md) element is in the `https://www.microsoft.com/networking/OneX/v1` namespace.</span></span>

<span data-ttu-id="63fe5-231">Das ""-Element kann als unter [**geordnetes Element des**](wlan-profileschema-fipsmode-authencryption-element.md) [**authencryption**](wlan-profileschema-authencryption-security-element.md) -Elements eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="63fe5-231">The [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element can be inserted as a child of the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span> <span data-ttu-id="63fe5-232">Das [**Onex**](onexschema-onex-element.md) -Element kann als untergeordnetes Element des [**Security (MSM)**](wlan-profileschema-security-msm-element.md) -Elements eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="63fe5-232">The [**OneX**](onexschema-onex-element.md) element can be inserted as a child of the [**security (MSM)**](wlan-profileschema-security-msm-element.md) element.</span></span>

<span data-ttu-id="63fe5-233">Informationen zum Anzeigen der Liste der untergeordneten Elemente in einer Struktur ähnlichen Struktur finden Sie unter [WLAN \_ Profile Schema Elements](wlan-profileschema-elements.md).</span><span class="sxs-lookup"><span data-stu-id="63fe5-233">To view the list of child elements in a tree-like structure, see [WLAN\_profile Schema Elements](wlan-profileschema-elements.md).</span></span>

## <a name="examples"></a><span data-ttu-id="63fe5-234">Beispiele</span><span class="sxs-lookup"><span data-stu-id="63fe5-234">Examples</span></span>

<span data-ttu-id="63fe5-235">Beispiel Profile finden Sie unter [Beispiele für drahtlos profile](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="63fe5-235">To view sample profiles, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="63fe5-236">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63fe5-236">Requirements</span></span>



| <span data-ttu-id="63fe5-237">Anforderung</span><span class="sxs-lookup"><span data-stu-id="63fe5-237">Requirement</span></span> | <span data-ttu-id="63fe5-238">Wert</span><span class="sxs-lookup"><span data-stu-id="63fe5-238">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="63fe5-239">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="63fe5-239">Minimum supported client</span></span><br/> | <span data-ttu-id="63fe5-240">Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="63fe5-240">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="63fe5-241">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="63fe5-241">Minimum supported server</span></span><br/> | <span data-ttu-id="63fe5-242">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="63fe5-242">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="63fe5-243">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="63fe5-243">Redistributable</span></span><br/>          | <span data-ttu-id="63fe5-244">Drahtlose LAN-API für Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="63fe5-244">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="63fe5-245">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63fe5-245">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63fe5-246">Beispiele für Funk profile</span><span class="sxs-lookup"><span data-stu-id="63fe5-246">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 
