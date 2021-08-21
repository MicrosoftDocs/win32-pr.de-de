---
title: AcceptServerName (PeapExtensionsType)-Element
description: Das AcceptServerName(PeapExtensionsType)-Element gibt an, ob der Servername anhand der Namenszeichenfolge überprüft wird, die im Schema mspeapconnectionpropertiesv2 in ServerNames angegeben ist.
ms.assetid: 24409775-d00d-439f-bb0b-a9fe5fb736a7
keywords:
- AcceptServerName-Element EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b608629c9eb9d3e3fb592ead73ddc0ba9545e6b92a642adf4ce76bb0524b57ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086039"
---
# <a name="acceptservername-peapextensionstype-element"></a>AcceptServerName (PeapExtensionsType)-Element

Das **AcceptServerName-Element (PeapExtensionsType)** gibt an, ob der Servername anhand der Im [**ServerNames-Element (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) angegebenen Namenszeichenfolge überprüft wird.

``` syntax
<xs:element name="AcceptServerName"
    type="xs:boolean"
 />
```

Das **AcceptServerName-Element** wird durch das [**PeapExtensionsType-Element**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) definiert.

## <a name="remarks"></a>Hinweise

Das **AcceptServerName-Element** ist optional.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

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

[mspeapconnectionpropertiesv2-Schema](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[mspeapconnectionpropertiesv2-Schemaelemente](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





