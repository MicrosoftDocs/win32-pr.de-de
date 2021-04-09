---
title: Enablequarantäne inechecks (eaptype)-Element
description: Erfahren Sie mehr über das enablequarantäne inechecks (eaptype)-Element. Dieses Element gibt an, ob NAP-Überprüfungen (Netzwerk Zugriffsschutz) durchgeführt werden sollen.
ms.assetid: bd5c7efc-f857-4e21-9cd8-0a1cbe5a87d8
keywords:
- Enablequarantäne-Element EAPHost
topic_type:
- apiref
api_name:
- EnableQuarantineChecks
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0becd1add038bb91307095eaf5cd0743d383632b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949133"
---
# <a name="enablequarantinechecks-eaptype-element"></a>Enablequarantäne inechecks (eaptype)-Element

Das **enablequarantäne inechecks (eaptype)** -Element gibt an, ob Netzwerk Zugriffsschutz (NAP)-Überprüfungen durchgeführt werden sollen.

``` syntax
<xs:element name="EnableQuarantineChecks"
    type="boolean"
 />
```

Das **enablequarantäne inechecks** -Element wird durch das [**eaptype**](mspeapconnectionpropertiesv1schema-eaptype-element.md) -Element definiert.

## <a name="remarks"></a>Bemerkungen

Wenn das **enablequarantäne** -Element auf "true" festgestellt wird, werden NAP-Überprüfungen durchgeführt. bei "false" werden keine NAP-Überprüfungen durchgeführt. Das **enablequarantäne inechecks** -Element ist optional.

## <a name="requirements"></a>Anforderungen



| Role | Mindestens unterstützte Betriebssystemversion |
|------|------------------------------|
| Client<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Server<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Eaptype**](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Eaptype**](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[mspeapconnectionpropertiesv1-Schema](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[mspeapconnectionpropertiesv1-Schema Elemente](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





