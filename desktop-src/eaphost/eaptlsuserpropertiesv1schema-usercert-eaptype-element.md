---
title: UserCert(EapType)-Element
description: Bezieht sich auf den SHA-1-Hash des Zertifikats, das für die Authentifizierung verwendet werden soll.
ms.assetid: 0f0fa37c-dff2-44c6-bd7c-ca54c569fcf1
keywords:
- UserCert-Element EAPHost
topic_type:
- apiref
api_name:
- UserCert
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ef25a43bf13b1cfb1e4b03f78f5772567b3bfb92f1c31bb810da7882a4d3e1c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067230"
---
# <a name="usercert-eaptype-element"></a>UserCert(EapType)-Element

Das **UserCert (EapType)-Element** verweist auf den SHA-1-Hash des Zertifikats, das für die Authentifizierung verwendet werden soll.

``` syntax
<xs:element name="UserCert"
    type="hexBinary"
 />
```

Das **UserCert-Element** wird durch das [**EapType-Element**](eaptlsuserpropertiesv1schema-eaptype-element.md) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**EapType**](eaptlsuserpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**EapType**](eaptlsuserpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[eaptlsuserpropertiesv1-Schema](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





