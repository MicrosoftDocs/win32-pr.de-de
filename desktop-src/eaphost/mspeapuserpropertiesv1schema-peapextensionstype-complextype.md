---
title: Komplexer Dateityp "Peer apextensionstype" (Verbindungs Eigenschaften)
description: Erfahren Sie mehr über den komplexen Typ "apapextensionstype". Dieser Typ ermöglicht zukünftige Erweiterungen des Schemas.
ms.assetid: d4f7784d-d426-4da6-bf81-40716f185416
keywords:
- Komplexer Typ von "etapextensionstype" EAPHost
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
ms.openlocfilehash: 4bf7e22a013bbd7a931b61b55ae0013bb42f4e41
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316485"
---
# <a name="peapextensionstype-complex-type-connection-properties"></a>Komplexer Dateityp "Peer apextensionstype" (Verbindungs Eigenschaften)

Der komplexe Typ " **Peer apextensionstype** " ermöglicht zukünftige Erweiterungen des Schemas.

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

## <a name="remarks"></a>Bemerkungen

Der komplexe Typ " **Peer apextensionstype** " ist optional.

## <a name="requirements"></a>Anforderungen



| Role | Mindestens unterstützte Betriebssystemversion |
|------|------------------------------|
| Client<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Server<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[mspeapuserpropertiesv1-Schema](mspeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





