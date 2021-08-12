---
title: AcceptServerName-Element
description: Gibt an, ob der Servername anhand der im ServerNames (ServerValidationParameters)-Element angegebenen Namenszeichenfolge überprüft wird. | AcceptServerName-Element
ms.assetid: 307b2d2a-1678-4aa9-82ed-46d401cf0e0f
keywords:
- AcceptServerName-Element EAPHost
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
ms.openlocfilehash: 69cb60d89824c4b6bf83f4903e96b1856433e367e647d19657b70888839595f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118273701"
---
# <a name="acceptservername-element"></a>AcceptServerName-Element

Das **AcceptServerName -Element (EapType)** gibt an, ob der Servername anhand der Im [**ServerNames-Element (ServerValidationParameters)**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) angegebenen Namenszeichenfolge überprüft wird.

``` syntax
<xs:element name="AcceptServerName"
    type="xs:boolean"
 />
```

Das **AcceptServerName-Element** wird durch das [**EapType-Element**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) definiert.

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

[**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[eaptlsconnectionpropertiesv2](eaptlsconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[eaptlsconnectionpropertiesv2-Schemaelemente](eaptlsconnectionpropertiesv2schema-elements.md)
</dt> <dt>

[**AcceptServerName (EapType)**](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md)
</dt> </dl>

 

 





