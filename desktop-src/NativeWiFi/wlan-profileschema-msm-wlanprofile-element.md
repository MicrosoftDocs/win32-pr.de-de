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
# <a name="msm-wlanprofile-element"></a>MSM-Element (wlanprofile)

Das MSM-Element (wlanprofile) enthält verschiedene Einstellungen für medienspezifische Module (MSM).

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

Das-Element wird durch das [**wlanprofile**](wlan-profileschema-wlanprofile-element.md) -Element definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                            | type                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**authEncryption**](wlan-profileschema-authencryption-security-element.md)       |                                                                   | Gibt das Authentifizierungs-und Verschlüsselungs Paar an, das für dieses Profil verwendet werden soll.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**Genehmigung**](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | Gibt das Authentifizierungs-und Verschlüsselungs Paar an, das für dieses Profil verwendet werden soll.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**Stech**](wlan-profileschema-connectivity-msm-element.md)                |                                                                   | Enthält verschiedene Konnektivitätseinstellungen. Dieses Element ist optional.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**Verschlüsselungs**](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | Legt die Datenverschlüsselung fest, die zum Herstellen einer Verbindung mit dem Drahtlos Netzwerk verwendet werden soll.<br/>                                                                                                                                                                                                                                                                                                                                                   |
| [**keyIndex**](wlan-profileschema-keyindex-security-element.md)                   |                                                                   | Gibt an, welcher Schlüssel Index verwendet werden muss, um drahtlosen Datenverkehr zu verschlüsseln. Dies wird nur verwendet, wenn KeyType auf networkkey festgelegt ist.<br/>                                                                                                                                                                                                                                                                                          |
| [**keyMaterial**](wlan-profileschema-keymaterial-sharedkey-element.md)            | [string](/dotnet/api/system.string)   | Enthält den Netzwerkschlüssel oder die Passphrase.<br/>                                                                                                                                                                                                                                                                                                                                                                           |
| [**keyType**](wlan-profileschema-keytype-sharedkey-element.md)                    |                                                                   | Der Schlüsseltyp.<br/>                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**phytype**](wlan-profileschema-phytype-connectivity-element.md)                 |                                                                   | Gibt den 802,11 Wireless LAN-Standard an, der auf dem Drahtlos Netzwerk verwendet wird. Der Wert "n" wird nur unter Windows Vista mit SP1 und höheren Versionen des Betriebssystems unterstützt.<br/> **Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.<br/>                                                                                                                        |
| [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md)           |                                                                   | Gibt an, ob die PMK-Zwischenspeicherung verwendet wird. Dieses Element ist nur für WPA2-definierte Netzwerke gültig.<br/> **Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.<br/>                                                                                                                                                                                                 |
| [**PMKCacheSize**](wlan-profileschema-pmkcachesize-security-element.md)           |                                                                   | Gibt die Anzahl der Einträge im OMK-Cache auf dem Client an. Dieses Element gilt nur für WPA2-definierte Netzwerke, bei denen der pmkcache-Modus auf Aktiviert festgelegt ist. Wenn der pmkcache-Modus aktiviert ist und dieses Element nicht vorhanden ist, wird die Größe des Caches standardmäßig auf 128 Einträge eingestellt.<br/> **Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.<br/>                                   |
| [**PMKCacheTTL**](wlan-profileschema-pmkcachettl-security-element.md)             |                                                                   | Gibt die Zeitdauer in Minuten an, die ein PMK-Cache aufbewahrt wird. Dieses Element gilt nur für WPA2-definierte Netzwerke, bei denen der pmkcache-Modus auf Aktiviert festgelegt ist.<br/> **Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.<br/>                                                                                                                                  |
| [**preAuthMode**](wlan-profileschema-preauthmode-security-element.md)             |                                                                   | Bestimmt, ob die Vorauthentifizierung vom Client verwendet wird. Die Vorauthentifizierung ermöglicht WPA2-sicheres schnelles Roaming. Dieses Element gilt nur für WPA2-definierte Netzwerke, bei denen der pmkcache-Modus auf Aktiviert festgelegt ist. Wenn der pmkcache-Modus aktiviert ist und dieses Element nicht vorhanden ist, wird der Standardwert deaktiviert.<br/> **Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.<br/> |
| [**preAuthThrottle**](wlan-profileschema-preauththrottle-security-element.md)     |                                                                   | Gibt die Anzahl der Versuche bei der Vorauthentifizierung bei benachbarten APS an. Dieses Element gilt nur für WPA2-definierte Netzwerke, bei denen der pmkcache-Modus auf Aktiviert festgelegt ist. Wenn der pmkcache-Modus aktiviert ist und dieses Element nicht vorhanden ist, wird die Anzahl der Versuche standardmäßig auf 3 eingestellt.<br/> **Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.<br/>                                      |
| [**protected**](wlan-profileschema-protected-sharedkey-element.md)                | [boolean](/dotnet/api/system.boolean) | Gibt an, ob der Schlüssel verschlüsselt ist.<br/> **Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element muss den Wert false aufweisen.<br/>                                                                                                                                                                                                                                                 |
| [**Sicherung**](wlan-profileschema-security-msm-element.md)                        |                                                                   | Enthält verschiedene Sicherheitseinstellungen. Dieses Element ist optional.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| [**sharedKey**](wlan-profileschema-sharedkey-security-element.md)                 |                                                                   | Enthält die Informationen zum gemeinsamen Schlüssel. Dieses Element ist nur erforderlich, wenn für das Authentifizierungs-und Verschlüsselungs paar WEP-oder PSK-Schlüssel erforderlich sind.<br/>                                                                                                                                                                                                                                                                    |
| [**useOneX**](wlan-profileschema-useonex-authencryption-element.md)               | [boolean](/dotnet/api/system.boolean) | Gibt an, ob 802.1 x verwendet wird. Dieses Flag ist optional.<br/>                                                                                                                                                                                                                                                                                                                                                          |



## <a name="remarks"></a>Bemerkungen

Das ""-Element kann als unter [**geordnetes Element des**](wlan-profileschema-fipsmode-authencryption-element.md) [**authencryption**](wlan-profileschema-authencryption-security-element.md) -Elements eingefügt werden. Das [**Onex**](onexschema-onex-element.md) -Element kann als untergeordnetes Element des [**Security (MSM)**](wlan-profileschema-security-msm-element.md) -Elements eingefügt werden.

## <a name="examples"></a>Beispiele

Beispiel Profile, die das **MSM** -Element verwenden, finden Sie unter [Beispiele für drahtlos profile](wireless-profile-samples.md).

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

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
