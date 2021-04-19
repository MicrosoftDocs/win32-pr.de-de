---
title: Eaptype-Element (Basis Benutzereigenschaften)
description: Erfahren Sie mehr über das eaptype-Element. Dieses Element erfasst eine Methoden spezifische Konfiguration innerhalb des EAP-Elements. | Eaptype-Element (Basis Benutzereigenschaften)
ms.assetid: 8ce81848-5b36-441f-967d-02c666ba5c6c
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
ms.openlocfilehash: 5fffa74c69b5ecbf2823cfa79ae376fed524e8ca
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106363093"
---
# <a name="eaptype-element-base-user-properties"></a>Eaptype-Element (Basis Benutzereigenschaften)

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
|-------------------------------------|------------------------------------------------------|
| Client<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Server<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[baseeapuserpropertiesv1-Schema](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





