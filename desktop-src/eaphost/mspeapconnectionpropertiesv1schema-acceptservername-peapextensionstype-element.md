---
title: AcceptServerName (PeapExtensionsType) -Element (EAPHost)
description: Das AcceptServerName-Element (PeapExtensionsType) gibt an, ob der Servername anhand der Namenszeichenfolge überprüft wird, die im Schema mspeapconnectionpropertiesv1 in ServerNames angegeben ist.
ms.assetid: 95173b57-8100-44e4-98f0-4f2a3deabce7
keywords:
- Element EAPHost
topic_type:
- apiref
api_name:
- AcceptServerName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d85a68eb497dda352f5d1860d2726f26e146545a0b1705ae52731d0cfdee9ddf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119404690"
---
# <a name="acceptservername-peapextensionstype-element-eaphost"></a>AcceptServerName (PeapExtensionsType) -Element (EAPHost)

Das **AcceptServerName-Element (PeapExtensionsType)** gibt an, ob der Servername anhand der Im [**ServerNames-Element (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) angegebenen Namenszeichenfolge überprüft wird.

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:AcceptServerName"
 />
```

Das -Element wird durch das [**PeapExtensionsType-Element**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) definiert.

## <a name="remarks"></a>Hinweise

Das **AcceptServerName-Element** ist optional.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[mspeapconnectionpropertiesv1-Schema](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[mspeapconnectionpropertiesv1-Schemaelemente](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[**AcceptServerName**](mspeapconnectionpropertiesv2-acceptservername-peapextensionstype-element.md)
</dt> </dl>

 

 





