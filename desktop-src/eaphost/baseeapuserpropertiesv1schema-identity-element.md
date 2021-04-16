---
title: Identity-Element
description: Erfahren Sie mehr über das EAPHost-Identitätselement. Dieses Element erfasst die Identität, die für die Authentifizierung verwendet wird.
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
ms.openlocfilehash: 485d576155d5ac63df2776016f3aafabf8c18c25
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474277"
---
# <a name="identity-element"></a>Identity-Element

Das **Identity** -Element erfasst die Identität, die für die Authentifizierung verwendet wird.

``` syntax
<xs:element name="Identity"
    type="string"
 />
```

## <a name="remarks"></a>Bemerkungen

Das **Identity** -Element ist abstrakt. Jede Methode muss ein abgeleitetes Element in den Instanzdokumenten definieren und verwenden.

## <a name="requirements"></a>Anforderungen



| Role | Mindestens unterstützte Betriebssystemversion |
|------|------------------------------|
| Client<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Server<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[baseeapuserpropertiesv1-Schema](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





