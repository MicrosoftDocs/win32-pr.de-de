---
title: EAP-Element (Verbindungs Eigenschaften)
description: Erfahren Sie mehr über das EAP-Element. Dieses Element erfasst den ausgewählten Methodentyp und die Methoden spezifische Konfiguration. | EAP-Element (Verbindungs Eigenschaften)
ms.assetid: 4e9f3869-257e-4b03-93f6-2eec94eaacee
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
ms.openlocfilehash: c39812d00ecf9a1183eb81fc03b09b146d751f0e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106357185"
---
# <a name="eap-element-connection-properties"></a>EAP-Element (Verbindungs Eigenschaften)

Das **EAP** -Element erfasst den ausgewählten Methodentyp und die Methoden spezifische Konfiguration.

``` syntax
<xs:element name="Eap
          
        "
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

[baseeapconnectionpropertiesv1-Schema](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





