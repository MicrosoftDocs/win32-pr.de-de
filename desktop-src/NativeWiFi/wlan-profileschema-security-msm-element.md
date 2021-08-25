---
description: Enthält verschiedene Sicherheitseinstellungen.
ms.assetid: 1d912fb1-8fb4-4761-8991-5a50ffb0399e
title: security (MSM)-Element (LAN_policy) (WLAN)
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
ms.openlocfilehash: c885f330538177cddca40c47cf6a5ad910030c6c5f4c3429ca7bd92c3b437b20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912691"
---
# <a name="security-msm-element-lan_policy-for-wlan"></a>Security (MSM)-Element (LAN_policy) für WLAN

Das Security -Element (MSM) enthält verschiedene Sicherheitseinstellungen.

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

Das -Element wird durch das [**MSM-Element**](wlan-profileschema-msm-wlanprofile-element.md) definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                            | type                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**authEncryption**](wlan-profileschema-authencryption-security-element.md)       |                                                                   | Gibt das Authentifizierungs- und Verschlüsselungspaar an, das für dieses Profil verwendet werden soll.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**Authentifizierung**](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | Gibt das Authentifizierungs- und Verschlüsselungspaar an, das für dieses Profil verwendet werden soll.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**Verschlüsselung**](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | Legt die Datenverschlüsselung fest, die zum Herstellen einer Verbindung mit dem WLAN verwendet werden soll.<br/>                                                                                                                                                                                                                                                                                                                                                   |
| [**keyIndex**](wlan-profileschema-keyindex-security-element.md)                   |                                                                   | Gibt an, welcher Schlüsselindex zum Verschlüsseln von Drahtlosdatenverkehr verwendet werden muss. Dies wird nur verwendet, wenn keyType auf networkKey festgelegt ist.<br/>                                                                                                                                                                                                                                                                                          |
| [**keyMaterial**](wlan-profileschema-keymaterial-sharedkey-element.md)            | [string](/dotnet/api/system.string)   | Enthält den Netzwerkschlüssel oder die Passphrase.<br/>                                                                                                                                                                                                                                                                                                                                                                           |
| [**Keytype**](wlan-profileschema-keytype-sharedkey-element.md)                    |                                                                   | Typ des Schlüssels.<br/>                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md)           |                                                                   | Gibt an, ob pmk caching verwendet wird. Dieses Element ist nur für WPA2-definierte Netzwerke gültig.<br/> **Windows XP mit SP3 und wlan-API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.<br/>                                                                                                                                                                                                 |
| [**PMKCacheSize**](wlan-profileschema-pmkcachesize-security-element.md)           |                                                                   | Gibt die Anzahl der Einträge im OMK-Cache auf dem Client an. Dieses Element ist nur für WPA2-definierte Netzwerke gültig, bei denen der PMKCache-Modus auf aktiviert ist. Wenn der PMKCache-Modus aktiviert ist und dieses Element nicht vorhanden ist, beträgt die Cachegröße standardmäßig 128 Einträge.<br/> **Windows XP mit SP3 und wlan-API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.<br/>                                   |
| [**PMKCacheTTL**](wlan-profileschema-pmkcachettl-security-element.md)             |                                                                   | Gibt die Dauer in Minuten an, die ein PMK-Cache beibehalten wird. Dieses Element ist nur für WPA2-definierte Netzwerke gültig, bei denen der PMKCache-Modus auf aktiviert ist.<br/> **Windows XP mit SP3 und wlan-API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.<br/>                                                                                                                                  |
| [**preAuthMode**](wlan-profileschema-preauthmode-security-element.md)             |                                                                   | Bestimmt, ob die Vorauthentifizierung vom Client verwendet wird. Die Vorauthentifizierung ermöglicht wpa2 sicheres schnelles Roaming. Dieses Element ist nur für WPA2-definierte Netzwerke gültig, bei denen der PMKCache-Modus auf aktiviert ist. Wenn der PMKCache-Modus aktiviert ist und dieses Element nicht vorhanden ist, ist der Standardwert deaktiviert.<br/> **Windows XP mit SP3 und wlan-API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.<br/> |
| [**preAuthThrottle**](wlan-profileschema-preauththrottle-security-element.md)     |                                                                   | Gibt die Anzahl der Versuche an, die bei der Vorauthentifizierung bei benachbarten APs verwendet werden. Dieses Element ist nur für WPA2-definierte Netzwerke gültig, bei denen der PMKCache-Modus auf aktiviert ist. Wenn der PMKCache-Modus aktiviert ist und dieses Element nicht vorhanden ist, wird die Anzahl der Versuche standardmäßig auf 3 festgelegt.<br/> **Windows XP mit SP3 und wlan-API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.<br/>                                      |
| [**protected**](wlan-profileschema-protected-sharedkey-element.md)                | [boolean](/dotnet/api/system.boolean) | Gibt an, ob der Schlüssel verschlüsselt ist.<br/> **Windows XP mit SP3 und wlan-API für Windows XP mit SP2:** Dieses Element muss den Wert **FALSE haben.**<br/>                                                                                                                                                                                                                                             |
| [**sharedKey**](wlan-profileschema-sharedkey-security-element.md)                 |                                                                   | Enthält die Freigegebenen Schlüsselinformationen. Dieses Element ist nur erforderlich, wenn WEP- oder PSK-Schlüssel für das Authentifizierungs- und Verschlüsselungspaar erforderlich sind.<br/>                                                                                                                                                                                                                                                                    |
| [**useOneX**](wlan-profileschema-useonex-authencryption-element.md)               | [boolean](/dotnet/api/system.boolean) | Gibt an, ob 802.1X verwendet wird. Dieses Flag ist optional.<br/>                                                                                                                                                                                                                                                                                                                                                          |



## <a name="remarks"></a>Hinweise

Das [**FIPSMode-Element**](wlan-profileschema-fipsmode-authencryption-element.md) kann als untergeordnetes Element des [**authEncryption-Elements eingefügt**](wlan-profileschema-authencryption-security-element.md) werden. Das [**OneX-Element**](onexschema-onex-element.md) kann als untergeordnetes Element des Sicherheitselements **(MSM) eingefügt** werden.

## <a name="examples"></a>Beispiele

Beispielprofile, die das Sicherheitselement **verwenden,** finden Sie unter [Beispiele für Funkprofile.](wireless-profile-samples.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista, Windows XP nur mit \[ SP3-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                |
| Verteilbare Komponente<br/>          | WLAN-API für Windows XP mit SP2<br/>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Beispiele für Drahtlosprofile](wireless-profile-samples.md)
</dt> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**Msm**](wlan-profileschema-msm-wlanprofile-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**MSM (WLANProfile)**](wlan-profileschema-msm-wlanprofile-element.md)
</dt> </dl>

 

 
