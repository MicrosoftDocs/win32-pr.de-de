---
title: Eaptype-Element (V1-Schema Verbindungs Eigenschaft)
description: Erfahren Sie mehr über das eaptype-Element. Dieses Element erfasst eine Methoden spezifische Konfiguration innerhalb des EAP-Elements. | Eaptype-Element (V1-Schema Verbindungs Eigenschaft)
ms.assetid: f953e150-64cf-41b2-937f-410799be4602
keywords:
- Eaptype-Element EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 88361931946f8a209c5b1c41bd17fcbd0e44096d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761661"
---
# <a name="eaptype-element-v1-schema-connection-property"></a>Eaptype-Element (V1-Schema Verbindungs Eigenschaft)

Das **eaptype** -Element erfasst eine Methoden spezifische Konfiguration innerhalb des EAP-Elements.

``` syntax
<xs:element name="EapType"
    type="BaseEapTypeParameters"
 />
```

## <a name="remarks"></a>Bemerkungen

Das **eaptype** -Element ist abstrakt. Jede Methode muss ein abgeleitetes Element in den Instanzdokumenten definieren und verwenden.

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

 

 





