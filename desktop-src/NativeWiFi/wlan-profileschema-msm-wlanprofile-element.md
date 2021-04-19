---
description: Enthält verschiedene Einstellungen für medienspezifische Module (MSM).
ms.assetid: 31f98af8-a577-4f6a-9a0a-b182b5a89cc3
title: MSM-Element (wlanprofile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSM
api_type:
- Schema
api_location: ''
ms.openlocfilehash: b2e1ffdc5ad27524d3d2fc5b37b3a060a90c7575
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362392"
---
# <a name="msm-wlanprofile-element"></a><span data-ttu-id="a8444-103">MSM-Element (wlanprofile)</span><span class="sxs-lookup"><span data-stu-id="a8444-103">MSM (WLANProfile) Element</span></span>

<span data-ttu-id="a8444-104">Das MSM-Element (wlanprofile) enthält verschiedene Einstellungen für medienspezifische Module (MSM).</span><span class="sxs-lookup"><span data-stu-id="a8444-104">The MSM (WLANProfile) element contains various media-specific module (MSM) settings.</span></span>

``` syntax
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
```

<span data-ttu-id="a8444-105">Das-Element wird durch das [**wlanprofile**](wlan-profileschema-wlanprofile-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="a8444-105">The element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a8444-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a8444-106">Child elements</span></span>



| <span data-ttu-id="a8444-107">Element</span><span class="sxs-lookup"><span data-stu-id="a8444-107">Element</span></span>                                                                            | <span data-ttu-id="a8444-108">type</span><span class="sxs-lookup"><span data-stu-id="a8444-108">Type</span></span>                                                              | <span data-ttu-id="a8444-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a8444-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8444-110">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="a8444-110">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)       |                                                                   | <span data-ttu-id="a8444-111">Gibt das Authentifizierungs-und Verschlüsselungs Paar an, das für dieses Profil verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a8444-111">Specifies the authentication and encryption pair to be used for this profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="a8444-112">**Genehmigung**</span><span class="sxs-lookup"><span data-stu-id="a8444-112">**authentication**</span></span>](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | <span data-ttu-id="a8444-113">Gibt das Authentifizierungs-und Verschlüsselungs Paar an, das für dieses Profil verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a8444-113">Specifies the authentication and encryption pair to be used for this profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="a8444-114">**Stech**</span><span class="sxs-lookup"><span data-stu-id="a8444-114">**connectivity**</span></span>](wlan-profileschema-connectivity-msm-element.md)                |                                                                   | <span data-ttu-id="a8444-115">Enthält verschiedene Konnektivitätseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="a8444-115">Contains various connectivity settings.</span></span> <span data-ttu-id="a8444-116">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="a8444-116">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="a8444-117">**Verschlüsselungs**</span><span class="sxs-lookup"><span data-stu-id="a8444-117">**encryption**</span></span>](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | <span data-ttu-id="a8444-118">Legt die Datenverschlüsselung fest, die zum Herstellen einer Verbindung mit dem Drahtlos Netzwerk verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a8444-118">Sets the data encryption to use to connect to the wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="a8444-119">**keyIndex**</span><span class="sxs-lookup"><span data-stu-id="a8444-119">**keyIndex**</span></span>](wlan-profileschema-keyindex-security-element.md)                   |                                                                   | <span data-ttu-id="a8444-120">Gibt an, welcher Schlüssel Index verwendet werden muss, um drahtlosen Datenverkehr zu verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="a8444-120">Specifies which key index must be used to encrypt wireless traffic.</span></span> <span data-ttu-id="a8444-121">Dies wird nur verwendet, wenn KeyType auf networkkey festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a8444-121">This is only used when keyType is set to networkKey.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="a8444-122">**keyMaterial**</span><span class="sxs-lookup"><span data-stu-id="a8444-122">**keyMaterial**</span></span>](wlan-profileschema-keymaterial-sharedkey-element.md)            | [<span data-ttu-id="a8444-123">string</span><span class="sxs-lookup"><span data-stu-id="a8444-123">string</span></span>](/dotnet/api/system.string)   | <span data-ttu-id="a8444-124">Enthält den Netzwerkschlüssel oder die Passphrase.</span><span class="sxs-lookup"><span data-stu-id="a8444-124">Contains the network key or passphrase.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="a8444-125">**keyType**</span><span class="sxs-lookup"><span data-stu-id="a8444-125">**keyType**</span></span>](wlan-profileschema-keytype-sharedkey-element.md)                    |                                                                   | <span data-ttu-id="a8444-126">Der Schlüsseltyp.</span><span class="sxs-lookup"><span data-stu-id="a8444-126">Type of key.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="a8444-127">**phytype**</span><span class="sxs-lookup"><span data-stu-id="a8444-127">**phyType**</span></span>](wlan-profileschema-phytype-connectivity-element.md)                 |                                                                   | <span data-ttu-id="a8444-128">Gibt den 802,11 Wireless LAN-Standard an, der auf dem Drahtlos Netzwerk verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a8444-128">Specifies the 802.11 wireless LAN standard used on the wireless LAN.</span></span> <span data-ttu-id="a8444-129">Der Wert "n" wird nur unter Windows Vista mit SP1 und höheren Versionen des Betriebssystems unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a8444-129">The value "n" is only supported on Windows Vista with SP1 and later versions of the operating system.</span></span><br/> <span data-ttu-id="a8444-130">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a8444-130">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="a8444-131">**PMKCacheMode**</span><span class="sxs-lookup"><span data-stu-id="a8444-131">**PMKCacheMode**</span></span>](wlan-profileschema-pmkcachemode-security-element.md)           |                                                                   | <span data-ttu-id="a8444-132">Gibt an, ob die PMK-Zwischenspeicherung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a8444-132">Indicates whether PMK caching will be used.</span></span> <span data-ttu-id="a8444-133">Dieses Element ist nur für WPA2-definierte Netzwerke gültig.</span><span class="sxs-lookup"><span data-stu-id="a8444-133">This element is valid only for WPA2-defined networks.</span></span><br/> <span data-ttu-id="a8444-134">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a8444-134">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                 |
| [<span data-ttu-id="a8444-135">**PMKCacheSize**</span><span class="sxs-lookup"><span data-stu-id="a8444-135">**PMKCacheSize**</span></span>](wlan-profileschema-pmkcachesize-security-element.md)           |                                                                   | <span data-ttu-id="a8444-136">Gibt die Anzahl der Einträge im OMK-Cache auf dem Client an.</span><span class="sxs-lookup"><span data-stu-id="a8444-136">Specifies the number of entries in the OMK cache on the client.</span></span> <span data-ttu-id="a8444-137">Dieses Element gilt nur für WPA2-definierte Netzwerke, bei denen der pmkcache-Modus auf Aktiviert festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a8444-137">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="a8444-138">Wenn der pmkcache-Modus aktiviert ist und dieses Element nicht vorhanden ist, wird die Größe des Caches standardmäßig auf 128 Einträge eingestellt.</span><span class="sxs-lookup"><span data-stu-id="a8444-138">If PMKCache mode is enabled, and this element is absent, the size of the cache defaults to 128 entries.</span></span><br/> <span data-ttu-id="a8444-139">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a8444-139">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                   |
| [<span data-ttu-id="a8444-140">**PMKCacheTTL**</span><span class="sxs-lookup"><span data-stu-id="a8444-140">**PMKCacheTTL**</span></span>](wlan-profileschema-pmkcachettl-security-element.md)             |                                                                   | <span data-ttu-id="a8444-141">Gibt die Zeitdauer in Minuten an, die ein PMK-Cache aufbewahrt wird.</span><span class="sxs-lookup"><span data-stu-id="a8444-141">Indicates the length of time, in minutes, that a PMK cache will be kept.</span></span> <span data-ttu-id="a8444-142">Dieses Element gilt nur für WPA2-definierte Netzwerke, bei denen der pmkcache-Modus auf Aktiviert festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a8444-142">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span><br/> <span data-ttu-id="a8444-143">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a8444-143">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="a8444-144">**preAuthMode**</span><span class="sxs-lookup"><span data-stu-id="a8444-144">**preAuthMode**</span></span>](wlan-profileschema-preauthmode-security-element.md)             |                                                                   | <span data-ttu-id="a8444-145">Bestimmt, ob die Vorauthentifizierung vom Client verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a8444-145">Determines if pre-authentication will be used by the client.</span></span> <span data-ttu-id="a8444-146">Die Vorauthentifizierung ermöglicht WPA2-sicheres schnelles Roaming.</span><span class="sxs-lookup"><span data-stu-id="a8444-146">Pre-authentication enables WPA2 secure fast roaming.</span></span> <span data-ttu-id="a8444-147">Dieses Element gilt nur für WPA2-definierte Netzwerke, bei denen der pmkcache-Modus auf Aktiviert festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a8444-147">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="a8444-148">Wenn der pmkcache-Modus aktiviert ist und dieses Element nicht vorhanden ist, wird der Standardwert deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a8444-148">If PMKCache mode is enabled, and this element is absent, the default value is disabled.</span></span><br/> <span data-ttu-id="a8444-149">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a8444-149">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/> |
| [<span data-ttu-id="a8444-150">**preAuthThrottle**</span><span class="sxs-lookup"><span data-stu-id="a8444-150">**preAuthThrottle**</span></span>](wlan-profileschema-preauththrottle-security-element.md)     |                                                                   | <span data-ttu-id="a8444-151">Gibt die Anzahl der Versuche bei der Vorauthentifizierung bei benachbarten APS an.</span><span class="sxs-lookup"><span data-stu-id="a8444-151">Indicates the number of tries when preauthenticating to neighboring APs.</span></span> <span data-ttu-id="a8444-152">Dieses Element gilt nur für WPA2-definierte Netzwerke, bei denen der pmkcache-Modus auf Aktiviert festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a8444-152">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="a8444-153">Wenn der pmkcache-Modus aktiviert ist und dieses Element nicht vorhanden ist, wird die Anzahl der Versuche standardmäßig auf 3 eingestellt.</span><span class="sxs-lookup"><span data-stu-id="a8444-153">If PMKCache mode is enabled, and this element is absent, the number of tries defaults to 3.</span></span><br/> <span data-ttu-id="a8444-154">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a8444-154">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="a8444-155">**protected**</span><span class="sxs-lookup"><span data-stu-id="a8444-155">**protected**</span></span>](wlan-profileschema-protected-sharedkey-element.md)                | [<span data-ttu-id="a8444-156">boolean</span><span class="sxs-lookup"><span data-stu-id="a8444-156">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="a8444-157">Gibt an, ob der Schlüssel verschlüsselt ist.</span><span class="sxs-lookup"><span data-stu-id="a8444-157">Indicates whether the key is encrypted.</span></span><br/> <span data-ttu-id="a8444-158">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element muss den Wert false aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a8444-158">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element must have a value of FALSE.</span></span><br/>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="a8444-159">**Sicherung**</span><span class="sxs-lookup"><span data-stu-id="a8444-159">**security**</span></span>](wlan-profileschema-security-msm-element.md)                        |                                                                   | <span data-ttu-id="a8444-160">Enthält verschiedene Sicherheitseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="a8444-160">Contains various security settings.</span></span> <span data-ttu-id="a8444-161">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="a8444-161">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="a8444-162">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="a8444-162">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)                 |                                                                   | <span data-ttu-id="a8444-163">Enthält die Informationen zum gemeinsamen Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="a8444-163">Contains the shared key information.</span></span> <span data-ttu-id="a8444-164">Dieses Element ist nur erforderlich, wenn für das Authentifizierungs-und Verschlüsselungs paar WEP-oder PSK-Schlüssel erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="a8444-164">This element is only required if WEP or PSK keys are required for the authentication and encryption pair.</span></span><br/>                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="a8444-165">**useOneX**</span><span class="sxs-lookup"><span data-stu-id="a8444-165">**useOneX**</span></span>](wlan-profileschema-useonex-authencryption-element.md)               | [<span data-ttu-id="a8444-166">boolean</span><span class="sxs-lookup"><span data-stu-id="a8444-166">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="a8444-167">Gibt an, ob 802.1 x verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a8444-167">Indicates whether 802.1X is used.</span></span> <span data-ttu-id="a8444-168">Dieses Flag ist optional.</span><span class="sxs-lookup"><span data-stu-id="a8444-168">This flag is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="a8444-169">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8444-169">Remarks</span></span>

<span data-ttu-id="a8444-170">Das ""-Element kann als unter [**geordnetes Element des**](wlan-profileschema-fipsmode-authencryption-element.md) [**authencryption**](wlan-profileschema-authencryption-security-element.md) -Elements eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a8444-170">The [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element can be inserted as a child of the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span> <span data-ttu-id="a8444-171">Das [**Onex**](onexschema-onex-element.md) -Element kann als untergeordnetes Element des [**Security (MSM)**](wlan-profileschema-security-msm-element.md) -Elements eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a8444-171">The [**OneX**](onexschema-onex-element.md) element can be inserted as a child of the [**security (MSM)**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="a8444-172">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a8444-172">Examples</span></span>

<span data-ttu-id="a8444-173">Beispiel Profile, die das **MSM** -Element verwenden, finden Sie unter [Beispiele für drahtlos profile](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="a8444-173">To view sample profiles that use the **MSM** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8444-174">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8444-174">Requirements</span></span>



| <span data-ttu-id="a8444-175">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8444-175">Requirement</span></span> | <span data-ttu-id="a8444-176">Wert</span><span class="sxs-lookup"><span data-stu-id="a8444-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a8444-177">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a8444-177">Minimum supported client</span></span><br/> | <span data-ttu-id="a8444-178">Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8444-178">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a8444-179">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a8444-179">Minimum supported server</span></span><br/> | <span data-ttu-id="a8444-180">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8444-180">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="a8444-181">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="a8444-181">Redistributable</span></span><br/>          | <span data-ttu-id="a8444-182">Drahtlose LAN-API für Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="a8444-182">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="a8444-183">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8444-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8444-184">Beispiele für Funk profile</span><span class="sxs-lookup"><span data-stu-id="a8444-184">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> <dt>

<span data-ttu-id="a8444-185">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="a8444-185">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a8444-186">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="a8444-186">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="a8444-187">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="a8444-187">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a8444-188">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="a8444-188">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
