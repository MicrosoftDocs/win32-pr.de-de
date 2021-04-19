---
title: EAP-Element (Benutzer Eigenschaft)
description: Erfahren Sie mehr über das EAP-Element. Dieses Element erfasst den ausgewählten Methodentyp und die Methoden spezifische Konfiguration. | EAP-Element (Benutzer Eigenschaft)
ms.assetid: 4adef133-1d18-444a-baa3-5419b8cbe298
keywords:
- EAP-Element EAPHost
topic_type:
- apiref
api_name:
- Eap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 23f00b5162ddb42efd9fae759bab1ea47efc04dc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106363930"
---
# <a name="eap-element-user-property"></a>EAP-Element (Benutzer Eigenschaft)

Das **EAP** -Element erfasst den ausgewählten Methodentyp und die Methoden spezifische Konfiguration.

``` syntax
<xs:element name="Eap"
    type="BaseEapParameters"
 />
```

## <a name="remarks"></a>Bemerkungen

Die-Methode kann die konstituierenden Elemente innerhalb des **EAP** -Elements definieren. Die-Methode führt auch eine Schema Validierung für die Elemente in **EAP** aus.

## <a name="requirements"></a>Anforderungen



| Role | Mindestens unterstützte Betriebssystemversion |
|------|------------------------------|
| Client<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Server<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[baseeapuserpropertiesv1-Schema](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





