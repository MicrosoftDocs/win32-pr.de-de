---
description: Enthält ein WLAN-Profil.
ms.assetid: bc97cb49-3891-4a4a-aab4-895cd9ce6908
title: WLANProfile-Element
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
ms.openlocfilehash: f7dae0d600553411a5a0a9287ab78d052a9ab9a0aa3c94220638adaf78dc5f11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912472"
---
# <a name="wlanprofile-element"></a>WLANProfile-Element

Das **WLANProfile-Element** enthält ein WLAN-Profil. Dieses Element ist das eindeutige Stammelement für ein Drahtlosprofil.

Der Zielnamespace für das WLANProfile-Element ist `https://www.microsoft.com/networking/WLAN/profile/v1` .

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

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                            | type                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**authEncryption**](wlan-profileschema-authencryption-security-element.md)       |                                                                   | Gibt das Authentifizierungs- und Verschlüsselungspaar an, das für dieses Profil verwendet werden soll.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**Authentifizierung**](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | Gibt die Authentifizierungsmethode an, die zum Herstellen einer Verbindung mit dem WLAN verwendet werden soll.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md)            | [boolean](/dotnet/api/system.boolean) | Bestimmt das Roamingverhalten eines automatisch verbundenen Netzwerks, wenn sich ein bevorzugtes Netzwerk im Bereich befindet. Dieses Element ist optional und hat keine Auswirkungen auf ein manuell verbundenes Netzwerk.<br/> **Windows XP mit SP3 und wlan-API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md)    |                                                                   | Gibt an, ob die Verbindung mit dem Wlan automatisch (automatisch) oder vom Benutzer initiiert ("manuell") erfolgen soll. Dieses Element ist optional.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md)    |                                                                   | Gibt an, ob das Netzwerk eine Infrastruktur ("ESS") oder ad-hoc ("IBSS") ist.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**Verbindung**](wlan-profileschema-connectivity-msm-element.md)                |                                                                   | Enthält verschiedene Konnektivitätseinstellungen. Dieses Element ist optional.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**Verbindung**](wlan-profileschema-connectivity-ihv-element.md)                |                                                                   | Enthält IHV-bezogene Konnektivitätseinstellungen.<br/> **Windows XP mit SP3 und wlan-API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**Verschlüsselung**](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | Legt die Datenverschlüsselung fest, die zum Herstellen einer Verbindung mit dem WLAN verwendet werden soll.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Hex**](wlan-profileschema-hex-ssid-element.md)                                 |                                                                   | Enthält die SSID eines Drahtlos-LAN im Hexadezimalformat.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**Ihv**](wlan-profileschema-ihv-wlanprofile-element.md)                          |                                                                   | Enthält optionale IHV-Einstellungen (Independent Hardware Vendor).<br/> **Windows XP mit SP3 und wlan-API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**keyIndex**](wlan-profileschema-keyindex-security-element.md)                   |                                                                   | Gibt an, welcher Schlüsselindex zum Verschlüsseln von Drahtlosdatenverkehr verwendet werden soll. Dies wird nur verwendet, wenn [**keyType**](wlan-profileschema-keytype-sharedkey-element.md) auf "networkKey" festgelegt ist.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**keyMaterial**](wlan-profileschema-keymaterial-sharedkey-element.md)            | [string](/dotnet/api/system.string)   | Enthält den Netzwerkschlüssel oder die Passphrase.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**Keytype**](wlan-profileschema-keytype-sharedkey-element.md)                    |                                                                   | Typ des Schlüssels.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**Msm**](wlan-profileschema-msm-wlanprofile-element.md)                          |                                                                   | Enthält verschiedene MSM-Einstellungen. Dieses Element ist optional.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**Namen**](wlan-profileschema-name-wlanprofile-element.md)                        | [**nameType**](wlan-profileschema-nametype-simpletype.md)        | Name des WLAN-Profils.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**Namen**](wlan-profileschema-name-ssid-element.md)                               |                                                                   | Enthält die SSID eines Drahtlos-LAN.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**NonBroadcast**](wlan-profileschema-nonbroadcast-ssidconfig-element.md)         | [boolean](/dotnet/api/system.boolean) | Gibt an, ob das Netzwerk seine SSID überträgt.<br/> **Windows XP mit SP3 und wlan-API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**Oui**](wlan-profileschema-oui-ouiheader-element.md)                            |                                                                   | Enthält ein hexadezimalesBinary mit 3 Byte, das die IHV identifiziert.<br/> **Windows XP mit SP3 und wlan-API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md)                      |                                                                   | Identifiziert die IHV.<br/> **Windows XP mit SP3 und wlan-API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**phyType**](wlan-profileschema-phytype-connectivity-element.md)                 |                                                                   | Gibt den 802.11-WLAN-Standard an, der für das Drahtlos-LAN verwendet wird. Der Wert "n" wird nur auf Windows Vista mit SP1 und neueren Versionen des Betriebssystems unterstützt.<br/> **Windows XP mit SP3 und wlan-API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md)           |                                                                   | Gibt an, ob die PMK-Zwischenspeicherung verwendet wird. Dieses Element ist nur für WPA2-definierte Netzwerke gültig.<br/> **Windows XP mit SP3 und wlan-API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**PMKCacheSize**](wlan-profileschema-pmkcachesize-security-element.md)           |                                                                   | Gibt die Anzahl der Einträge im PMK-Cache auf dem Client an. Dieses Element ist nur für WPA2-definierte Netzwerke gültig, für die [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) auf "enabled" festgelegt ist. Wenn **PMKCacheMode** aktiviert ist und dieses Element nicht vorhanden ist, beträgt die Größe des Cache standardmäßig 128 Einträge.<br/> **Windows XP mit SP3 und wlan-API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                           |
| [**PMKCacheTTL**](wlan-profileschema-pmkcachettl-security-element.md)             |                                                                   | Gibt die Zeitspanne in Minuten an, die ein PMK-Cache beibehalten wird. Dieses Element ist nur für WPA2-definierte Netzwerke gültig, für die [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) auf "enabled" festgelegt ist.<br/> **Windows XP mit SP3 und wlan-API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**preAuthMode**](wlan-profileschema-preauthmode-security-element.md)             |                                                                   | Bestimmt, ob die Vorauthentifizierung vom Client verwendet wird. Die Vorauthentifizierung ermöglicht sicheres schnelles Roaming mit WPA2. Dieses Element ist nur für WPA2-definierte Netzwerke gültig, für die [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) auf "enabled" festgelegt ist. Wenn **PMKCacheMode** aktiviert ist und dieses Element nicht vorhanden ist, ist der Standardwert deaktiviert.<br/> **Windows XP mit SP3 und wlan-API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                         |
| [**preAuthThrottle**](wlan-profileschema-preauththrottle-security-element.md)     |                                                                   | Gibt die Anzahl der Versuche bei der Vorauthentifizierung bei benachbarten APs an. Dieses Element ist nur für WPA2-definierte Netzwerke gültig, für die [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) auf "enabled" festgelegt ist. Wenn **PMKCacheMode** aktiviert ist und dieses Element nicht vorhanden ist, beträgt die Anzahl der Versuche standardmäßig 3.<br/> **Windows XP mit SP3 und wlan-API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                              |
| [**protected**](wlan-profileschema-protected-sharedkey-element.md)                | [boolean](/dotnet/api/system.boolean) | Gibt an, ob der Schlüssel verschlüsselt ist.<br/> **Windows XP mit SP3 und wlan-API für Windows XP mit SP2:** Dieses Element muss den Wert **FALSE** aufweisen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**Sicherheit**](wlan-profileschema-security-msm-element.md)                        |                                                                   | Enthält verschiedene Sicherheitseinstellungen. Dieses Element ist optional.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**Sicherheit**](wlan-profileschema-security-ihv-element.md)                        |                                                                   | Enthält IHV-spezifische Sicherheitseinstellungen. Microsoft-Sicherheitseinstellungen und IHV-Sicherheitseinstellungen schließen sich gegenseitig aus. Wenn beide Sicherheitseinstellungen im gleichen Profil vorhanden sind, ist das Profil ungültig.<br/> **Windows XP mit SP3 und wlan-API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**sharedKey**](wlan-profileschema-sharedkey-security-element.md)                 |                                                                   | Enthält die Freigegebenen Schlüsselinformationen. Dieses Element ist nur erforderlich, wenn WEP- oder PSK-Schlüssel für das Authentifizierungs- und Verschlüsselungspaar erforderlich sind.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**Ssid**](wlan-profileschema-ssid-ssidconfig-element.md)                         |                                                                   | Gibt die SSID eines WLAN an.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md)            |                                                                   | Enthält mindestens ein SSIDs-System zusammen mit anderen allgemeinen Einstellungen. <br/> Ein Profil kann mehrere [**SSIDConfig-Elemente**](wlan-profileschema-ssidconfig-wlanprofile-element.md) enthalten, und jedes [**SSIDConfig-Element**](wlan-profileschema-ssidconfig-wlanprofile-element.md) kann mehrere [**SSID-Elemente**](wlan-profileschema-ssid-ssidconfig-element.md) enthalten. Allerdings berücksichtigt Windows immer nur das erste [**SSIDConfig-Element**](wlan-profileschema-ssidconfig-wlanprofile-element.md) in einem [**WLANProfile-Element.**](wlan-profileschema-wlanprofile-element.md)<br/> **Windows XP mit SP3 und wlan-API für Windows XP mit SP2:** In einem Profil kann nur ein [**SSID-Element**](wlan-profileschema-ssid-ssidconfig-element.md) angezeigt werden.<br/> |
| [**Typ**](wlan-profileschema-type-ouiheader-element.md)                          |                                                                   | Enthält eine hexadezimalbinäre 1-Byte-Datei, die verwendet wird, um NICs durch dieselbe IHV zu unterscheiden. <br/> **Windows XP mit SP3 und wlan-API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md)                      | [boolean](/dotnet/api/system.boolean) | Gibt den Ursprung von 802.1X-Sicherheitseinstellungen an, die von einer IHV-Sicherheitskomponente verwendet werden. Wenn [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md) true ist, verwenden IHV-Sicherheitskomponenten von Microsoft definierte 802.1X-Einstellungen. Wenn **useMSOneX** false ist, verwenden IHV-Sicherheitskomponenten vom Anbieter bereitgestellte 802.1X-Einstellungen. Standardmäßig ist **useMSOneX** false. Dieses Element ist optional.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [**useOneX**](wlan-profileschema-useonex-authencryption-element.md)               | [boolean](/dotnet/api/system.boolean) | Gibt an, ob 802.1X verwendet wird. Dieses Flag ist optional.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



## <a name="remarks"></a>Hinweise

Die meisten untergeordneten Elemente des WLANProfile-Elements befinden sich im `https://www.microsoft.com/networking/WLAN/profile/v1` -Namespace. Es gibt zwei Ausnahmen: Das [**FIPSMode-Element**](wlan-profileschema-fipsmode-authencryption-element.md) befindet sich im `https://www.microsoft.com/networking/WLAN/profile/v2` -Namespace und das [**OneX-Element**](onexschema-onex-element.md) im `https://www.microsoft.com/networking/OneX/v1` -Namespace.

Das [**FIPSMode-Element**](wlan-profileschema-fipsmode-authencryption-element.md) kann als untergeordnetes Element des [**authEncryption-Elements eingefügt**](wlan-profileschema-authencryption-security-element.md) werden. Das [**OneX-Element**](onexschema-onex-element.md) kann als untergeordnetes Element des Sicherheitselements [**(MSM) eingefügt**](wlan-profileschema-security-msm-element.md) werden.

Informationen zum Anzeigen der Liste der untergeordneten Elemente in einer strukturbasierten Struktur finden Sie unter [ \_ WLAN-Profilschemaelemente](wlan-profileschema-elements.md).

## <a name="examples"></a>Beispiele

Beispielprofile finden Sie unter [Beispiele für Drahtlosprofile.](wireless-profile-samples.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista, Windows XP nur mit \[ SP3-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                |
| Verteilbare Komponente<br/>          | WLAN-API für Windows XP mit SP2<br/>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Beispiele für Drahtlosprofile](wireless-profile-samples.md)
</dt> </dl>

 

 
