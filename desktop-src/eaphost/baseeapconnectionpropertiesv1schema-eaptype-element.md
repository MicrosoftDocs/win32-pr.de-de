---
title: EapType-Element (v1-Schemaverbindungseigenschaft)
description: Erfahren Sie mehr über das EapType-Element. Dieses Element erfasst die methodenspezifische Konfiguration innerhalb des Eap-Elements. | EapType-Element (v1-Schemaverbindungseigenschaft)
ms.assetid: f953e150-64cf-41b2-937f-410799be4602
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
ms.openlocfilehash: 3f2681e5682ad98ab5f4185174996920315d8c3b81dde8ba69d13ca178904ded
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118498786"
---
# <a name="eaptype-element-v1-schema-connection-property"></a>EapType-Element (v1-Schemaverbindungseigenschaft)

Das **EapType-Element** erfasst die methodenspezifische Konfiguration innerhalb des Eap-Elements.

``` syntax
<xs:element name="EapType"
    type="BaseEapTypeParameters"
 />
```

## <a name="remarks"></a>Hinweise

Das **EapType-Element** ist abstrakt. Jede Methode muss ein abgeleitetes Element in den Instanzdokumenten definieren und verwenden.

## <a name="requirements"></a>Anforderungen



| Role | Unterstützte Mindestversion des Betriebssystems |
|------|------------------------------|
| Client<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Server<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[baseeapconnectionpropertiesv1-Schema](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





