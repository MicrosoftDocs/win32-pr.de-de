---
title: Eap-Element (Verbindungseigenschaften)
description: Erfahren Sie mehr über das Eap-Element. Dieses Element erfasst den ausgewählten Methodentyp und die methodenspezifische Konfiguration. | Eap-Element (Verbindungseigenschaften)
ms.assetid: 4e9f3869-257e-4b03-93f6-2eec94eaacee
keywords:
- Eap-Element EAPHost
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
ms.openlocfilehash: 7750bdb9a5f3c2d6c187b0f765eeb9d7ad88c015403719c16d0b683637b10027
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086944"
---
# <a name="eap-element-connection-properties"></a>Eap-Element (Verbindungseigenschaften)

Das **Eap-Element** erfasst den ausgewählten Methodentyp und die methodenspezifische Konfiguration.

``` syntax
<xs:element name="Eap
          
        "
    type="BaseEapParameters"
 />
```

## <a name="remarks"></a>Hinweise

Die -Methode kann die konstituierenden Elemente innerhalb des **Eap-Elements** definieren. Die -Methode führt auch eine Schemavalidierung für die Elemente in **Eap** durch.

## <a name="requirements"></a>Anforderungen



| Rolle | Unterstützte Mindestversion des Betriebssystems |
|------|------------------------------|
| Client<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Server<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[baseeapconnectionpropertiesv1-Schema](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





