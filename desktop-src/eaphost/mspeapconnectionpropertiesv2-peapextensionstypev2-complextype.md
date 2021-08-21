---
title: Komplexer PeapExtensionsTypeV2-Typ
description: Erfahren Sie mehr über den komplexen PeapExtensionsTypeV2-Typ. Dieser Typ ermöglicht zukünftige Erweiterungen des Schemas.
ms.assetid: cb011182-afec-4813-bd56-add894c74c9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baea42ec60fe84085ea5e4541848fd43b786419bedab17e938044ff0a713fa07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086029"
---
# <a name="peapextensionstypev2-complex-type"></a>Komplexer PeapExtensionsTypeV2-Typ

Der **komplexe PeapExtensionsTypeV2-Typ** ermöglicht zukünftige Verbesserungen des Schemas.


```XML
<xs:complexType name="PeapExtensionsTypeV2">
    <xs:sequence>
        <xs:any processContents="lax" 
            minOccurs="0" 
            maxOccurs="unbounded" 
            namespace="##other"
        />
    <xs:sequence>
</xs:complexType>

```



## <a name="remarks"></a>Hinweise

Das **PeapExtensionsTypeV2-Element** ist optional.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[mspeapconnectionpropertiesv2-Schema](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[Komplexe mspeapconnectionpropertiesv2-Typen](mspeapconnectionpropertiesv2schema-complex-types.md)
</dt> <dt>

[**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> </dl>

 

 




