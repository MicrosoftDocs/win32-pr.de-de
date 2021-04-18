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
# <a name="security-msm-element-lan_policy-for-wlan"></a>Security (MSM)-Element (LAN_policy) für WLAN

Das Security (MSM)-Element enthält verschiedene Sicherheitseinstellungen.

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

Das-Element wird durch das [**MSM**](wlan-profileschema-msm-wlanprofile-element.md) -Element definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                            | type                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**authEncryption**](wlan-profileschema-authencryption-security-element.md)       |                                                                   | Gibt das Authentifizierungs-und Verschlüsselungs Paar an, das für dieses Profil verwendet werden soll.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**Genehmigung**](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | Gibt das Authentifizierungs-und Verschlüsselungs Paar an, das für dieses Profil verwendet werden soll.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**Verschlüsselungs**](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | Legt die Datenverschlüsselung fest, die zum Herstellen einer Verbindung mit dem Drahtlos Netzwerk verwendet werden soll.<br/>                                                                                                                                                                                                                                                                                                                                                   |
| [**keyIndex**](wlan-profileschema-keyindex-security-element.md)                   |                                                                   | Gibt an, welcher Schlüssel Index verwendet werden muss, um drahtlosen Datenverkehr zu verschlüsseln. Dies wird nur verwendet, wenn KeyType auf networkkey festgelegt ist.<br/>                                                                                                                                                                                                                                                                                          |
| [**keyMaterial**](wlan-profileschema-keymaterial-sharedkey-element.md)            | [string](/dotnet/api/system.string)   | Enthält den Netzwerkschlüssel oder die Passphrase.<br/>                                                                                                                                                                                                                                                                                                                                                                           |
| [**keyType**](wlan-profileschema-keytype-sharedkey-element.md)                    |                                                                   | Der Schlüsseltyp.<br/>                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md)           |                                                                   | Gibt an, ob die PMK-Zwischenspeicherung verwendet wird. Dieses Element ist nur für WPA2-definierte Netzwerke gültig.<br/> **Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.<br/>                                                                                                                                                                                                 |
| [**PMKCacheSize**](wlan-profileschema-pmkcachesize-security-element.md)           |                                                                   | Gibt die Anzahl der Einträge im OMK-Cache auf dem Client an. Dieses Element gilt nur für WPA2-definierte Netzwerke, bei denen der pmkcache-Modus auf Aktiviert festgelegt ist. Wenn der pmkcache-Modus aktiviert ist und dieses Element nicht vorhanden ist, wird die Größe des Caches standardmäßig auf 128 Einträge eingestellt.<br/> **Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.<br/>                                   |
| [**PMKCacheTTL**](wlan-profileschema-pmkcachettl-security-element.md)             |                                                                   | Gibt die Zeitdauer in Minuten an, die ein PMK-Cache aufbewahrt wird. Dieses Element gilt nur für WPA2-definierte Netzwerke, bei denen der pmkcache-Modus auf Aktiviert festgelegt ist.<br/> **Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.<br/>                                                                                                                                  |
| [**preAuthMode**](wlan-profileschema-preauthmode-security-element.md)             |                                                                   | Bestimmt, ob die Vorauthentifizierung vom Client verwendet wird. Die Vorauthentifizierung ermöglicht WPA2-sicheres schnelles Roaming. Dieses Element gilt nur für WPA2-definierte Netzwerke, bei denen der pmkcache-Modus auf Aktiviert festgelegt ist. Wenn der pmkcache-Modus aktiviert ist und dieses Element nicht vorhanden ist, wird der Standardwert deaktiviert.<br/> **Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.<br/> |
| [**preAuthThrottle**](wlan-profileschema-preauththrottle-security-element.md)     |                                                                   | Gibt die Anzahl der Versuche bei der Vorauthentifizierung bei benachbarten APS an. Dieses Element gilt nur für WPA2-definierte Netzwerke, bei denen der pmkcache-Modus auf Aktiviert festgelegt ist. Wenn der pmkcache-Modus aktiviert ist und dieses Element nicht vorhanden ist, wird die Anzahl der Versuche standardmäßig auf 3 eingestellt.<br/> **Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.<br/>                                      |
| [**protected**](wlan-profileschema-protected-sharedkey-element.md)                | [boolean](/dotnet/api/system.boolean) | Gibt an, ob der Schlüssel verschlüsselt ist.<br/> **Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element muss den Wert **false** aufweisen.<br/>                                                                                                                                                                                                                                             |
| [**sharedKey**](wlan-profileschema-sharedkey-security-element.md)                 |                                                                   | Enthält die Informationen zum gemeinsamen Schlüssel. Dieses Element ist nur erforderlich, wenn für das Authentifizierungs-und Verschlüsselungs paar WEP-oder PSK-Schlüssel erforderlich sind.<br/>                                                                                                                                                                                                                                                                    |
| [**useOneX**](wlan-profileschema-useonex-authencryption-element.md)               | [boolean](/dotnet/api/system.boolean) | Gibt an, ob 802.1 x verwendet wird. Dieses Flag ist optional.<br/>                                                                                                                                                                                                                                                                                                                                                          |



## <a name="remarks"></a>Bemerkungen

Das ""-Element kann als unter [**geordnetes Element des**](wlan-profileschema-fipsmode-authencryption-element.md) [**authencryption**](wlan-profileschema-authencryption-security-element.md) -Elements eingefügt werden. Das [**Onex**](onexschema-onex-element.md) -Element kann als untergeordnetes Element des **Security (MSM)** -Elements eingefügt werden.

## <a name="examples"></a>Beispiele

Beispiel Profile, die das **Security** -Element verwenden, finden Sie unter [Beispiele für drahtlos profile](wireless-profile-samples.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                |
| Verteilbare Komponente<br/>          | Drahtlose LAN-API für Windows XP mit SP2<br/>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Beispiele für Funk profile](wireless-profile-samples.md)
</dt> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**MSM**](wlan-profileschema-msm-wlanprofile-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**MSM (wlanprofile)**](wlan-profileschema-msm-wlanprofile-element.md)
</dt> </dl>

 

 
