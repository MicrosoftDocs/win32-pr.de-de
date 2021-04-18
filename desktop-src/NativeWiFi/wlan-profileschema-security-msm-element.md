---
description: Enthält verschiedene Sicherheitseinstellungen.
ms.assetid: 1d912fb1-8fb4-4761-8991-5a50ffb0399e
title: Security (MSM)-Element (LAN_policy) (WLAN)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- security
api_type:
- Schema
api_location: ''
ms.openlocfilehash: f6ea42a83d39c328db88e992555e5d593cc778b6
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2021
ms.locfileid: "106372016"
---
# <a name="security-msm-element-lan_policy-for-wlan"></a><span data-ttu-id="9ba3b-103">Security (MSM)-Element (LAN_policy) für WLAN</span><span class="sxs-lookup"><span data-stu-id="9ba3b-103">Security (MSM) Element (LAN_policy) for WLAN</span></span>

<span data-ttu-id="9ba3b-104">Das Security (MSM)-Element enthält verschiedene Sicherheitseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-104">The security (MSM) element contains various security settings.</span></span>

``` syntax
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
```

<span data-ttu-id="9ba3b-105">Das-Element wird durch das [**MSM**](wlan-profileschema-msm-wlanprofile-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-105">The element is defined by the [**MSM**](wlan-profileschema-msm-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="9ba3b-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9ba3b-106">Child elements</span></span>



| <span data-ttu-id="9ba3b-107">Element</span><span class="sxs-lookup"><span data-stu-id="9ba3b-107">Element</span></span>                                                                            | <span data-ttu-id="9ba3b-108">type</span><span class="sxs-lookup"><span data-stu-id="9ba3b-108">Type</span></span>                                                              | <span data-ttu-id="9ba3b-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9ba3b-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9ba3b-110">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="9ba3b-110">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)       |                                                                   | <span data-ttu-id="9ba3b-111">Gibt das Authentifizierungs-und Verschlüsselungs Paar an, das für dieses Profil verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-111">Specifies the authentication and encryption pair to be used for this profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="9ba3b-112">**Genehmigung**</span><span class="sxs-lookup"><span data-stu-id="9ba3b-112">**authentication**</span></span>](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | <span data-ttu-id="9ba3b-113">Gibt das Authentifizierungs-und Verschlüsselungs Paar an, das für dieses Profil verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-113">Specifies the authentication and encryption pair to be used for this profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="9ba3b-114">**Verschlüsselungs**</span><span class="sxs-lookup"><span data-stu-id="9ba3b-114">**encryption**</span></span>](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | <span data-ttu-id="9ba3b-115">Legt die Datenverschlüsselung fest, die zum Herstellen einer Verbindung mit dem Drahtlos Netzwerk verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-115">Sets the data encryption to use to connect to the wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="9ba3b-116">**keyIndex**</span><span class="sxs-lookup"><span data-stu-id="9ba3b-116">**keyIndex**</span></span>](wlan-profileschema-keyindex-security-element.md)                   |                                                                   | <span data-ttu-id="9ba3b-117">Gibt an, welcher Schlüssel Index verwendet werden muss, um drahtlosen Datenverkehr zu verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-117">Specifies which key index must be used to encrypt wireless traffic.</span></span> <span data-ttu-id="9ba3b-118">Dies wird nur verwendet, wenn KeyType auf networkkey festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-118">This is only used when keyType is set to networkKey.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="9ba3b-119">**keyMaterial**</span><span class="sxs-lookup"><span data-stu-id="9ba3b-119">**keyMaterial**</span></span>](wlan-profileschema-keymaterial-sharedkey-element.md)            | [<span data-ttu-id="9ba3b-120">string</span><span class="sxs-lookup"><span data-stu-id="9ba3b-120">string</span></span>](/dotnet/api/system.string)   | <span data-ttu-id="9ba3b-121">Enthält den Netzwerkschlüssel oder die Passphrase.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-121">Contains the network key or passphrase.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="9ba3b-122">**keyType**</span><span class="sxs-lookup"><span data-stu-id="9ba3b-122">**keyType**</span></span>](wlan-profileschema-keytype-sharedkey-element.md)                    |                                                                   | <span data-ttu-id="9ba3b-123">Der Schlüsseltyp.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-123">Type of key.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="9ba3b-124">**PMKCacheMode**</span><span class="sxs-lookup"><span data-stu-id="9ba3b-124">**PMKCacheMode**</span></span>](wlan-profileschema-pmkcachemode-security-element.md)           |                                                                   | <span data-ttu-id="9ba3b-125">Gibt an, ob die PMK-Zwischenspeicherung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-125">Indicates whether PMK caching will be used.</span></span> <span data-ttu-id="9ba3b-126">Dieses Element ist nur für WPA2-definierte Netzwerke gültig.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-126">This element is valid only for WPA2-defined networks.</span></span><br/> <span data-ttu-id="9ba3b-127">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-127">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                 |
| [<span data-ttu-id="9ba3b-128">**PMKCacheSize**</span><span class="sxs-lookup"><span data-stu-id="9ba3b-128">**PMKCacheSize**</span></span>](wlan-profileschema-pmkcachesize-security-element.md)           |                                                                   | <span data-ttu-id="9ba3b-129">Gibt die Anzahl der Einträge im OMK-Cache auf dem Client an.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-129">Specifies the number of entries in the OMK cache on the client.</span></span> <span data-ttu-id="9ba3b-130">Dieses Element gilt nur für WPA2-definierte Netzwerke, bei denen der pmkcache-Modus auf Aktiviert festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-130">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="9ba3b-131">Wenn der pmkcache-Modus aktiviert ist und dieses Element nicht vorhanden ist, wird die Größe des Caches standardmäßig auf 128 Einträge eingestellt.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-131">If PMKCache mode is enabled, and this element is absent, the size of the cache defaults to 128 entries.</span></span><br/> <span data-ttu-id="9ba3b-132">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-132">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                   |
| [<span data-ttu-id="9ba3b-133">**PMKCacheTTL**</span><span class="sxs-lookup"><span data-stu-id="9ba3b-133">**PMKCacheTTL**</span></span>](wlan-profileschema-pmkcachettl-security-element.md)             |                                                                   | <span data-ttu-id="9ba3b-134">Gibt die Zeitdauer in Minuten an, die ein PMK-Cache aufbewahrt wird.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-134">Indicates the length of time, in minutes, that a PMK cache will be kept.</span></span> <span data-ttu-id="9ba3b-135">Dieses Element gilt nur für WPA2-definierte Netzwerke, bei denen der pmkcache-Modus auf Aktiviert festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-135">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span><br/> <span data-ttu-id="9ba3b-136">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-136">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="9ba3b-137">**preAuthMode**</span><span class="sxs-lookup"><span data-stu-id="9ba3b-137">**preAuthMode**</span></span>](wlan-profileschema-preauthmode-security-element.md)             |                                                                   | <span data-ttu-id="9ba3b-138">Bestimmt, ob die Vorauthentifizierung vom Client verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-138">Determines if pre-authentication will be used by the client.</span></span> <span data-ttu-id="9ba3b-139">Die Vorauthentifizierung ermöglicht WPA2-sicheres schnelles Roaming.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-139">Pre-authentication enables WPA2 secure fast roaming.</span></span> <span data-ttu-id="9ba3b-140">Dieses Element gilt nur für WPA2-definierte Netzwerke, bei denen der pmkcache-Modus auf Aktiviert festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-140">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="9ba3b-141">Wenn der pmkcache-Modus aktiviert ist und dieses Element nicht vorhanden ist, wird der Standardwert deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-141">If PMKCache mode is enabled, and this element is absent, the default value is disabled.</span></span><br/> <span data-ttu-id="9ba3b-142">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-142">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/> |
| [<span data-ttu-id="9ba3b-143">**preAuthThrottle**</span><span class="sxs-lookup"><span data-stu-id="9ba3b-143">**preAuthThrottle**</span></span>](wlan-profileschema-preauththrottle-security-element.md)     |                                                                   | <span data-ttu-id="9ba3b-144">Gibt die Anzahl der Versuche bei der Vorauthentifizierung bei benachbarten APS an.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-144">Indicates the number of tries when preauthenticating to neighboring APs.</span></span> <span data-ttu-id="9ba3b-145">Dieses Element gilt nur für WPA2-definierte Netzwerke, bei denen der pmkcache-Modus auf Aktiviert festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-145">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="9ba3b-146">Wenn der pmkcache-Modus aktiviert ist und dieses Element nicht vorhanden ist, wird die Anzahl der Versuche standardmäßig auf 3 eingestellt.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-146">If PMKCache mode is enabled, and this element is absent, the number of tries defaults to 3.</span></span><br/> <span data-ttu-id="9ba3b-147">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-147">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="9ba3b-148">**protected**</span><span class="sxs-lookup"><span data-stu-id="9ba3b-148">**protected**</span></span>](wlan-profileschema-protected-sharedkey-element.md)                | [<span data-ttu-id="9ba3b-149">boolean</span><span class="sxs-lookup"><span data-stu-id="9ba3b-149">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="9ba3b-150">Gibt an, ob der Schlüssel verschlüsselt ist.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-150">Indicates whether the key is encrypted.</span></span><br/> <span data-ttu-id="9ba3b-151">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element muss den Wert **false** aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-151">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element must have a value of **FALSE**.</span></span><br/>                                                                                                                                                                                                                                             |
| [<span data-ttu-id="9ba3b-152">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="9ba3b-152">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)                 |                                                                   | <span data-ttu-id="9ba3b-153">Enthält die Informationen zum gemeinsamen Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-153">Contains the shared key information.</span></span> <span data-ttu-id="9ba3b-154">Dieses Element ist nur erforderlich, wenn für das Authentifizierungs-und Verschlüsselungs paar WEP-oder PSK-Schlüssel erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-154">This element is only required if WEP or PSK keys are required for the authentication and encryption pair.</span></span><br/>                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="9ba3b-155">**useOneX**</span><span class="sxs-lookup"><span data-stu-id="9ba3b-155">**useOneX**</span></span>](wlan-profileschema-useonex-authencryption-element.md)               | [<span data-ttu-id="9ba3b-156">boolean</span><span class="sxs-lookup"><span data-stu-id="9ba3b-156">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="9ba3b-157">Gibt an, ob 802.1 x verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-157">Indicates whether 802.1X is used.</span></span> <span data-ttu-id="9ba3b-158">Dieses Flag ist optional.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-158">This flag is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="9ba3b-159">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ba3b-159">Remarks</span></span>

<span data-ttu-id="9ba3b-160">Das ""-Element kann als unter [**geordnetes Element des**](wlan-profileschema-fipsmode-authencryption-element.md) [**authencryption**](wlan-profileschema-authencryption-security-element.md) -Elements eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-160">The [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element can be inserted as a child of the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span> <span data-ttu-id="9ba3b-161">Das [**Onex**](onexschema-onex-element.md) -Element kann als untergeordnetes Element des **Security (MSM)** -Elements eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="9ba3b-161">The [**OneX**](onexschema-onex-element.md) element can be inserted as a child of the **security (MSM)** element.</span></span>

## <a name="examples"></a><span data-ttu-id="9ba3b-162">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9ba3b-162">Examples</span></span>

<span data-ttu-id="9ba3b-163">Beispiel Profile, die das **Security** -Element verwenden, finden Sie unter [Beispiele für drahtlos profile](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="9ba3b-163">To view sample profiles that use the **security** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9ba3b-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ba3b-164">Requirements</span></span>



| <span data-ttu-id="9ba3b-165">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ba3b-165">Requirement</span></span> | <span data-ttu-id="9ba3b-166">Wert</span><span class="sxs-lookup"><span data-stu-id="9ba3b-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="9ba3b-167">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9ba3b-167">Minimum supported client</span></span><br/> | <span data-ttu-id="9ba3b-168">Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ba3b-168">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9ba3b-169">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9ba3b-169">Minimum supported server</span></span><br/> | <span data-ttu-id="9ba3b-170">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ba3b-170">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="9ba3b-171">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="9ba3b-171">Redistributable</span></span><br/>          | <span data-ttu-id="9ba3b-172">Drahtlose LAN-API für Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="9ba3b-172">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="9ba3b-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ba3b-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ba3b-174">Beispiele für Funk profile</span><span class="sxs-lookup"><span data-stu-id="9ba3b-174">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> <dt>

<span data-ttu-id="9ba3b-175">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="9ba3b-175">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="9ba3b-176">**MSM**</span><span class="sxs-lookup"><span data-stu-id="9ba3b-176">**MSM**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="9ba3b-177">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="9ba3b-177">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="9ba3b-178">**MSM (wlanprofile)**</span><span class="sxs-lookup"><span data-stu-id="9ba3b-178">**MSM (WLANProfile)**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)
</dt> </dl>

 

 
