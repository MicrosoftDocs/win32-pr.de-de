---
title: Komplexer PeapExtensionsType-Typ (Verbindungseigenschaften)
description: Erfahren Sie mehr über den komplexen PeapExtensionsType-Typ. Dieser Typ ermöglicht zukünftige Verbesserungen am Schema.
ms.assetid: d4f7784d-d426-4da6-bf81-40716f185416
keywords:
- Komplexer PeapExtensionsType-Typ EAPHost
topic_type:
- apiref
api_name:
- PeapExtensionsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9a72fa87b3f1cf5ba4a65c179895c22e5a208616ed8c9b2ffb9f046e5de9b92e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983920"
---
# <a name="peapextensionstype-complex-type-connection-properties"></a>Komplexer PeapExtensionsType-Typ (Verbindungseigenschaften)

Der komplexe **PeapExtensionsType-Typ** ermöglicht zukünftige Verbesserungen am Schema.

``` syntax
<xs:complexType name="PeapExtensionsType">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="remarks"></a>Hinweise

Der komplexe **PeapExtensionsType-Typ** ist optional.

## <a name="requirements"></a>Anforderungen



| Role | Unterstützte Mindestversion des Betriebssystems |
|------|------------------------------|
| Client<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Server<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[mspeapuserpropertiesv1-Schema](mspeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





