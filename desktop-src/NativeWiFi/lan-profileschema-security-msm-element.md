---
description: Enthält Sicherheitseinstellungen für verkabelte Netzwerke.
ms.assetid: 08470cf4-3722-4cb9-9877-13eca2f7d04e
title: Security (MSM)-Element (LAN_policy)
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
ms.openlocfilehash: 2bd052679f207cd0778f212a73663d4dfd8ce165
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "106357290"
---
# <a name="security-msm-element-lan_policy"></a>Security (MSM)-Element (LAN_policy)

Das Security (MSM)-Element enthält Sicherheitseinstellungen für verkabelte Netzwerke. Dieses Element ist optional.

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

Das **Security** -Element wird durch das [**MSM**](lan-profileschema-msm-lanprofile-element.md) -Element definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                 | type    | BESCHREIBUNG                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**Onexaktiviert**](lan-profileschema-onexenabled-security-element.md)   | boolean | Gibt an, ob der Dienst für die automatische Konfiguration von Kabel Netzwerken mithilfe von 802.1 x eine Port Authentifizierung durchführen soll. <br/>      |
| [**Onexerzwungen**](lan-profileschema-onexenforced-security-element.md) | boolean | Gibt an, ob für den automatischen Konfigurations Dienst für verkabelte Netzwerke die Verwendung von 802.1 x für die Port Authentifizierung erforderlich ist. <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**MSM**](lan-profileschema-msm-lanprofile-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**MSM (lanprofile)**](lan-profileschema-msm-lanprofile-element.md)
</dt> </dl>

 

 




