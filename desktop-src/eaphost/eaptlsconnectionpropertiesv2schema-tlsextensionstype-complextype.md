---
title: Komplexer tlsextensionstype-Typ
description: Erfahren Sie mehr über den komplexen tlsextensionstype-Typ. Dieser Typ ermöglicht zukünftige Erweiterungen des Schemas.
ms.assetid: 5e4f8ef8-1adb-4683-8001-ba7d2d392523
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833a93b9ecb0ba32a95e4c85856ac015f5135fb5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730329"
---
# <a name="tlsextensionstype-complex-type"></a>Komplexer tlsextensionstype-Typ

Der komplexe Typ **tlsextensionstype** ermöglicht zukünftige Erweiterungen des Schemas.


```XML
<xs:complexType name="TLSExtensionsType">
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

Das **tlsextensionstype** -Element ist optional.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>


</dt> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[eaptlsconnectionpropertiesv2](eaptlsconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[komplexe eaptlsconnectionpropertiesv2-Typen](eaptlsconnectionpropertiesv2schema-complex-types.md)
</dt> <dt>

[**Tlsextensions (tlsextensionstype)**](eaptlsconnectionpropertiesv2schema-performservervalidation-eaptype-element.md)
</dt> </dl>

 

 




