---
description: Gibt 802.1 x-Konfigurationsinformationen für ein Kabel-oder Drahtlos LAN-Profil an.
ms.assetid: 4528fcb5-ee8e-4824-a69e-8d67622c4b4d
title: Onex-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneX
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 4b3e3d91087a394efb7909d36d6244bfbf6115e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106363447"
---
# <a name="onex-element"></a>Onex-Element

Das Onex-Element gibt 802.1 x-Konfigurationsinformationen für ein Kabel-oder Drahtlos LAN-Profil an. Dieses Element ist das eindeutige root-Element für ein 802.1 x-Profil.

Der Ziel Namespace für das Onex-Element ist `https://www.microsoft.com/networking/OneX/v1` . Die meisten untergeordneten Elemente des Onex-Elements befinden sich im- `OneX` Namespace. Es gibt eine Ausnahme: das [**eapconfig**](onexschema-eapconfig-onex-element.md) -Element befindet sich im- `https://www.microsoft.com/provisioning/EapHostConfig` Namespace.

**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Nur das [**eapconfig**](onexschema-eapconfig-onex-element.md) -Element wird unterstützt. Andere Elemente, sofern Sie in einem Profil vorhanden sind, werden ignoriert.

``` syntax
<xs:element name="OneX">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="cacheUserData"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="heldPeriod"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="3600"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="authPeriod"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="3600"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="startPeriod"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="3600"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="maxStart"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="100"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="maxAuthFailures"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="100"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="supplicantMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="inhibitTransmission"
                         />
                        <xs:enumeration
                            value="includeLearning"
                         />
                        <xs:enumeration
                            value="compliant"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="authMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="machineOrUser"
                         />
                        <xs:enumeration
                            value="machine"
                         />
                        <xs:enumeration
                            value="user"
                         />
                        <xs:enumeration
                            value="guest"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="singleSignOn"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="type"
                            minOccurs="1"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="string"
                                >
                                    <xs:enumeration
                                        value="preLogon"
                                     />
                                    <xs:enumeration
                                        value="postLogon"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="maxDelay"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="integer"
                                >
                                    <xs:enumeration
                                        value="0"
                                     />
                                    <xs:enumeration
                                        value="120"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="userBasedVirtualLan"
                            type="boolean"
                            minOccurs="0"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="EAPConfig">
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            minOccurs="1"
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



| Element                                                                            | type    | BESCHREIBUNG                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**authmode**](onexschema-authmode-onex-element.md)                               |         | Gibt den Typ der für die Authentifizierung verwendeten Anmelde Informationen an.<br/>                                                                                                                                                        |
| [**authperiod**](onexschema-authperiod-onex-element.md)                           |         | Gibt die maximale Zeitspanne in Sekunden an, in der ein Client auf eine Antwort vom Authentifikator wartet.<br/>                                                                                                  |
| [**cacheuserdata**](onexschema-cacheuserdata-onex-element.md)                     | boolean | Gibt an, ob die Benutzer Anmelde Informationen für nachfolgende Verbindungen zwischengespeichert werden.<br/>                                                                                                                                     |
| [**Eapconfig**](onexschema-eapconfig-onex-element.md)                             |         | Gibt die EAPHost-Konfiguration an.<br/>                                                                                                                                                                              |
| [**heldperiod**](onexschema-heldperiod-onex-element.md)                           |         | Gibt die Zeitdauer in Sekunden an, in der ein Client die Authentifizierung nach einem fehlgeschlagenen Authentifizierungs Versuch nicht erneut versucht.<br/>                                                                             |
| [**maxauthfailure**](onexschema-maxauthfailures-onex-element.md)                 |         | Gibt die maximale Anzahl von Authentifizierungs Fehlern an, die für einen Satz von Anmelde Informationen zulässig sind.<br/>                                                                                                                         |
| [**MaxDelay**](onexschema-maxdelay-singlesignon-element.md)                       |         | Gibt die maximale Verzögerung in Sekunden an, bevor der Single Sign-on Verbindungsversuch fehlschlägt.<br/>                                                                                                                      |
| [**maxstart**](onexschema-maxstart-onex-element.md)                               |         | Gibt die maximale Anzahl von EAPOL-Start gesendeten Nachrichten an.<br/>                                                                                                                                                        |
| [**singleSignOn**](onexschema-singlesignon-onex-element.md)                       |         | Gibt Single Sign-on Netzwerk-Konfigurationsinformationen an.<br/>                                                                                                                                                       |
| [**startperiod**](onexschema-startperiod-onex-element.md)                         |         | Gibt die Zeitdauer in Sekunden an, die gewartet werden soll, bevor eine EAPOL-Start gesendet wird.<br/>                                                                                                                                  |
| [**supplicantmode**](onexschema-supplicantmode-onex-element.md)                   |         | Gibt die für EAPOL-Pakete verwendete Übertragungsmethode an.<br/>                                                                                                                                                      |
| [**Sorte**](onexschema-type-singlesignon-element.md)                               |         | Gibt an, wann Single Sign-on ausgeführt wird. Wenn diese Einstellung auf festgelegt `preLogon` ist, wird Single Sign-on ausgeführt, bevor sich der Benutzer anmeldet. Wenn diese Einstellung auf festgelegt `postLogon` ist, wird Single Sign-on sofort nach der Anmeldung des Benutzers ausgeführt.<br/> |
| [**userbasedvirtuallan**](onexschema-userbasedvirtuallan-singlesignon-element.md) | boolean | Gibt an, ob das vom Gerät verwendete virtuelle LAN (VLAN) basierend auf den Anmelde Informationen des Benutzers geändert wird.<br/>                                                                                                                   |



## <a name="remarks"></a>Bemerkungen

Informationen zum Anzeigen der Liste der untergeordneten Elemente in einer Struktur ähnlichen Struktur finden Sie unter [Onex-Schema Elemente](onexschema-elements.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                |
| Verteilbare Komponente<br/>          | Drahtlose LAN-API für Windows XP mit SP2<br/>                 |



 

 




