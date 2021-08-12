---
title: Identity-Element
description: Erfahren Sie mehr über das EAPHost Identity-Element. Dieses Element erfasst die identität, die für die Authentifizierung verwendet wird.
ms.assetid: 464979f0-6a2b-43e7-a207-2fbd1e2e5f51
keywords:
- Identity-Element EAPHost
topic_type:
- apiref
api_name:
- Identity
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad88e84583be2b392ce8a4dfdaec7495f1c063fa13d4327004bfbecbc1f925ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118275467"
---
# <a name="identity-element"></a>Identity-Element

Das **Identity-Element** erfasst die identität, die für die Authentifizierung verwendet wird.

``` syntax
<xs:element name="Identity"
    type="string"
 />
```

## <a name="remarks"></a>Hinweise

Das **Identity-Element** ist abstrakt. Jede Methode muss ein abgeleitetes Element in den Instanzdokumenten definieren und verwenden.

## <a name="requirements"></a>Anforderungen



| Role | Unterstützte Mindestversion des Betriebssystems |
|------|------------------------------|
| Client<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Server<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[baseeapuserpropertiesv1-Schema](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





