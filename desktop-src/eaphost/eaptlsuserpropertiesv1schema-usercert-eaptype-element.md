---
title: UserCert-Element (eaptype)
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
ms.openlocfilehash: c23840b489bad1e06bdd0c7eb6e0033bfb1961f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743200"
---
# <a name="usercert-eaptype-element"></a>UserCert-Element (eaptype)

Das **userCert-Element (eaptype)** verweist auf den SHA-1-Hash des Zertifikats, das für die Authentifizierung verwendet werden soll.

``` syntax
<xs:element name="UserCert"
    type="hexBinary"
 />
```

Das **userCert** -Element wird durch das [**eaptype**](eaptlsuserpropertiesv1schema-eaptype-element.md) -Element definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Eaptype**](eaptlsuserpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Eaptype**](eaptlsuserpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[eaptlsuserpropertiesv1-Schema](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





