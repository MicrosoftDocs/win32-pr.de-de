---
description: Gibt die Übertragungsmethode an, die für EAPOL-Start Nachrichten verwendet wird.
ms.assetid: 8d49d19a-8122-4191-bb46-92a2016bcfee
title: supplicantmode-Element (Onex)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- supplicantMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 33d58bd247a220ca93ed4d2a05886be107afd4c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368731"
---
# <a name="supplicantmode-onex-element"></a>supplicantmode-Element (Onex)

Das supplicantmode (Onex)-Element gibt die Übertragungsmethode an, die für EAPOL-Start Nachrichten verwendet wird. In der folgenden Tabelle sind die möglichen Werte beschrieben.



| Wert               | BESCHREIBUNG                                                                                                                                                              |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| inhibittransmission | EAPOL-Start-Nachrichten werden nicht übertragen. Nur für kabelgebundene LAN-profile gültig.                                                                                             |
| includelta-Gewinn     | Der Client legt fest, wann EAPOL-Start Pakete auf der Grundlage der Netzwerkfunktion gesendet werden sollen. EAPOL-Start Meldungen werden nur bei Bedarf gesendet. Nur für kabelgebundene LAN-profile gültig. |
| Kompatibel           | EAPOL-Start-Nachrichten werden gemäß 802.1 x übertragen. Gültig für Kabel-und Drahtlos-LAN-Profile.                                                             |



 

Dieses Element ist optional. Wenn supplicantmode nicht in einem Profil angegeben ist, wird der Wert `compliant` für Kabel-und Drahtlos LAN-Profile verwendet.

**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird ignoriert, wenn es in einem Profil vorhanden ist.

``` syntax
<xs:element name="supplicantMode">
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
```

Das **supplicantmode** -Element wird durch das [**Onex**](onexschema-onex-element.md) -Element definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> </dl>

 

 




