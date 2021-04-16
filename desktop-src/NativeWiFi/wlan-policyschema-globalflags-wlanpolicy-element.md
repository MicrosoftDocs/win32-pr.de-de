---
description: Enthält die globalen Einstellungen für das Auto Configuration Module (ACM).
ms.assetid: fb2b96d0-38cc-44fe-a82a-97e73b6a8f2a
title: globalflags-Element (wlanpolicy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- globalFlags
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 97d0b8ee90407efd94ac46cc1df6b084b9dcc54d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530092"
---
# <a name="globalflags-wlanpolicy-element"></a>globalflags-Element (wlanpolicy)

Das globalflags-Element (wlanpolicy) enthält die globalen Einstellungen für das Auto Configuration Module (ACM). Dieses Element ist obligatorisch.

``` syntax
<xs:element name="globalFlags">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="enableAutoConfig"
                type="boolean"
             />
            <xs:element name="showDeniedNetwork"
                type="boolean"
             />
            <xs:element name="allowEveryoneToCreateAllUserProfiles"
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

Das **globalflags** -Element wird durch das [**wlanpolicy**](wlan-policyschema-wlanpolicy-element.md) -Element definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                                                    | type    | BESCHREIBUNG                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**"Zuweisung von" "" "".**](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md) | boolean | Gibt an, ob ein Benutzer ein Profil für alle Benutzer erstellen kann. <br/>                                                               |
| [**enableautoconfig**](wlan-policyschema-enableautoconfig-globalflags-element.md)                                         | boolean | Gibt an, ob Computer den integrierten automatischen Konfigurations Dienst (AutoConfig) zum Verwalten von Drahtlos Verbindungen verwenden. <br/> |
| [**showdeniednetwork**](wlan-policyschema-showdeniednetwork-globalflags-element.md)                                       | boolean | Gibt an, ob abgelehnte Netzwerke im Assistenten **zum Herstellen einer Verbindung mit einem Netzwerk** angezeigt werden. <br/>                                         |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Wlanpolicy**](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Wlanpolicy**](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




