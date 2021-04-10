---
title: Komplexer PeapExtensionsTypeV2-Typ
description: Erfahren Sie mehr über den komplexen PeapExtensionsTypeV2-Typ. Dieser Typ ermöglicht zukünftige Erweiterungen des Schemas.
ms.assetid: cb011182-afec-4813-bd56-add894c74c9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 869e67f16bc9b42929d227755e08bf6924dcc737
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949128"
---
# <a name="peapextensionstypev2-complex-type"></a>Komplexer PeapExtensionsTypeV2-Typ

Der komplexe Typ " **PeapExtensionsTypeV2** " ermöglicht zukünftige Erweiterungen des Schemas.


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



## <a name="remarks"></a>Bemerkungen

Das **PeapExtensionsTypeV2** -Element ist optional.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[mspeapconnectionpropertiesv2-Schema](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[komplexe mspeapconnectionpropertiesv2-Typen](mspeapconnectionpropertiesv2schema-complex-types.md)
</dt> <dt>

[**Peer-extensionstype**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> </dl>

 

 




