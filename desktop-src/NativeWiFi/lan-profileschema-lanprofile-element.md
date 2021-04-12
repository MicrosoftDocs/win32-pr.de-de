---
description: Enthält ein kabelgebundenes Netzwerk Profil.
ms.assetid: f5f9fcdc-febf-4730-8be4-5e1885d9ab08
title: Lanprofile-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LANProfile
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 58ad88c9f975455bdd2d77a0ef8ee028d9027d9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216926"
---
# <a name="lanprofile-element"></a>Lanprofile-Element

Das lanprofile-Element enthält ein kabelgebundenes Netzwerk Profil. Dieses Element ist das eindeutige root-Element für ein Kabelnetzwerk Profil.

Der Ziel Namespace für das lanprofile-Element ist `https://www.microsoft.com/networking/LAN/profile/v1` .

``` syntax
<xs:element name="LANProfile">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="MSM">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="security">
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="OneXEnforced"
                                        type="boolean"
                                     />
                                    <xs:element name="OneXEnabled"
                                        type="boolean"
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



| Element                                                                 | type    | BESCHREIBUNG                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**MSM**](lan-profileschema-msm-lanprofile-element.md)                 |         | Enthält Einstellungen für medienspezifische Module (MSM). <br/>                                                                               |
| [**Onexaktiviert**](lan-profileschema-onexenabled-security-element.md)   | boolean | Gibt an, ob der Dienst für die automatische Konfiguration von Kabel Netzwerken mithilfe von 802.1 x eine Port Authentifizierung durchführen soll. <br/>      |
| [**Onexerzwungen**](lan-profileschema-onexenforced-security-element.md) | boolean | Gibt an, ob für den automatischen Konfigurations Dienst für verkabelte Netzwerke die Verwendung von 802.1 x für die Port Authentifizierung erforderlich ist. <br/> |
| [**Sicherung**](lan-profileschema-security-msm-element.md)              |         | Enthält Sicherheitseinstellungen. <br/>                                                                                                  |



## <a name="remarks"></a>Bemerkungen

Informationen zum Anzeigen der Liste der untergeordneten Elemente in einer Struktur ähnlichen Struktur finden Sie unter [LAN- \_ Profil Schema Elemente](lan-profileschema-elements.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 




