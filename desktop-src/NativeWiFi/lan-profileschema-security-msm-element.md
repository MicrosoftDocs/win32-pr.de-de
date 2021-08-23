---
description: Enthält Sicherheitseinstellungen für kabelgebundene Netzwerke.
ms.assetid: 08470cf4-3722-4cb9-9877-13eca2f7d04e
title: Security(MSM)-Element (LAN_policy)
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
ms.openlocfilehash: 8f66021f61536e8c8f09663e9ec2513b11d1ec87829f5c100b48cbf15d98cdd2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685060"
---
# <a name="security-msm-element-lan_policy"></a>Security(MSM)-Element (LAN_policy)

Das Security -Element (MSM) enthält Sicherheitseinstellungen für kabelgebundene Netzwerke. Dieses Element ist optional.

``` syntax
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
```

Das **Sicherheitselement** wird durch das [**MSM-Element**](lan-profileschema-msm-lanprofile-element.md) definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                 | Typ    | Beschreibung                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**OneXEnabled**](lan-profileschema-onexenabled-security-element.md)   | boolean | Gibt an, ob der automatische Konfigurationsdienst für kabelgebundene Netzwerke versucht, die Portauthentifizierung mit 802.1X durchzuführen. <br/>      |
| [**OneXEnforced**](lan-profileschema-onexenforced-security-element.md) | boolean | Gibt an, ob der automatische Konfigurationsdienst für kabelgebundene Netzwerke die Verwendung von 802.1X für die Portauthentifizierung erfordert. <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**Msm**](lan-profileschema-msm-lanprofile-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**MSM (LANProfile)**](lan-profileschema-msm-lanprofile-element.md)
</dt> </dl>

 

 




