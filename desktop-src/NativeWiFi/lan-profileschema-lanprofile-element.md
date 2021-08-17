---
description: Enthält ein Kabelnetzwerkprofil.
ms.assetid: f5f9fcdc-febf-4730-8be4-5e1885d9ab08
title: LANProfile-Element
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
ms.openlocfilehash: 6adaa0f4884ad275137a6c949dbc466416006f33bb6603dc61e87153d9b23361
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065100"
---
# <a name="lanprofile-element"></a>LANProfile-Element

Das LANProfile-Element enthält ein kabelgebundenes Netzwerkprofil. Dieses Element ist das eindeutige Stammelement für ein Kabelnetzwerkprofil.

Der Zielnamespace für das LANProfile-Element ist `https://www.microsoft.com/networking/LAN/profile/v1` .

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



| Element                                                                 | type    | Beschreibung                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**Msm**](lan-profileschema-msm-lanprofile-element.md)                 |         | Enthält medienspezifische Moduleinstellungen (MEDIA-Specific Module, MSM). <br/>                                                                               |
| [**OneXEnabled**](lan-profileschema-onexenabled-security-element.md)   | boolean | Gibt an, ob der automatische Konfigurationsdienst für kabelgebundene Netzwerke versucht, die Portauthentifizierung mit 802.1X zu versuchen. <br/>      |
| [**OneXEnforced**](lan-profileschema-onexenforced-security-element.md) | boolean | Gibt an, ob der automatische Konfigurationsdienst für kabelgebundene Netzwerke die Verwendung von 802.1X für die Portauthentifizierung erfordert. <br/> |
| [**Sicherheit**](lan-profileschema-security-msm-element.md)              |         | Enthält Sicherheitseinstellungen. <br/>                                                                                                  |



## <a name="remarks"></a>Hinweise

Informationen zum Anzeigen der Liste der untergeordneten Elemente in einer strukturbasierten Struktur finden Sie unter [ \_ LAN-Profilschemaelemente](lan-profileschema-elements.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 




