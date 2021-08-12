---
title: EapType-Element (Basisbenutzereigenschaften)
description: Erfahren Sie mehr über das EapType-Element. Dieses Element erfasst die methodenspezifische Konfiguration innerhalb des Eap-Elements. | EapType-Element (Basisbenutzereigenschaften)
ms.assetid: 8ce81848-5b36-441f-967d-02c666ba5c6c
keywords:
- EapType-Element EAPHost
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
ms.openlocfilehash: 7d9cb6afe13b8c0060b26edbf5add618c776518b3b03e5abdc1f9131dbbcabde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118275533"
---
# <a name="eaptype-element-base-user-properties"></a>EapType-Element (Basisbenutzereigenschaften)

Das **EapType-Element** erfasst eine methodenspezifische Konfiguration innerhalb des Eap-Elements.

``` syntax
<xs:element name="EapType"
    type="BaseEapTypeParameters"
 />
```

## <a name="remarks"></a>Hinweise

Das **EapType-Element** ist abstrakt. Jede Methode muss ein abgeleitetes Element in den Instanzdokumenten definieren und verwenden.

## <a name="requirements"></a>Anforderungen



| Role | Unterstützte Mindestversion des Betriebssystems |
|-------------------------------------|------------------------------------------------------|
| Client<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Server<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[baseeapuserpropertiesv1-Schema](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





