---
title: RequireCryptoBinding (EapType)-Element
description: Gibt an, ob die Authentifizierung bei Servern erfolgen soll, die cryptobinding unterstützen.
ms.assetid: 6b6a131d-8fce-4a5c-a649-891c4617b0f2
keywords:
- RequireCryptoBinding-Element EAPHost
topic_type:
- apiref
api_name:
- RequireCryptoBinding
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c4f4169e6ac0af123085795374b06de854b261b5f22004bd726ad47488bc11d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067220"
---
# <a name="requirecryptobinding-eaptype-element"></a>RequireCryptoBinding (EapType)-Element

Das **RequireCryptoBinding -Element (EapType)** gibt an, ob die Authentifizierung bei Servern erfolgen soll, die cryptobinding unterstützen.

``` syntax
<xs:element name="RequireCryptoBinding"
    type="boolean"
 />
```

Das **RequireCryptoBinding-Element** wird durch das [**EapType-Element**](mspeapconnectionpropertiesv1schema-eaptype-element.md) definiert.

## <a name="remarks"></a>Hinweise

Wenn das **RequireCryptoBinding-Element** TRUE ist, authentifiziert sich PEAP bei Servern, die cryptobinding nicht unterstützen. false gibt an, dass PEAP sich nur bei Servern authentifiziert, die cryptobinding unterstützen. Das **RequireCryptoBinding-Element** ist optional.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[mspeapconnectionpropertiesv1-Schema](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[mspeapconnectionpropertiesv1-Schemaelemente](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





