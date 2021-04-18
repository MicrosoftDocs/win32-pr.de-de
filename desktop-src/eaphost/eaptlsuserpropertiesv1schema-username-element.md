---
title: Username-Element (TLS)
description: Erfahren Sie mehr über das UserName-Element. Dieses Element erfasst den Benutzernamen, der in der EAP-Identity-Antwort gesendet werden soll.
ms.assetid: dda4a7dd-36ba-418d-9b26-2818ef20854d
keywords:
- Username-Element EAPHost
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
ms.openlocfilehash: 2975b425bc760979b33d83182d94469532944e46
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106340736"
---
# <a name="username-element-tls"></a>Username-Element (TLS)

Das **username** -Element erfasst den Benutzernamen, der in der EAP-Identity-Antwort gesendet werden soll.

Wenn das **username** -Element nicht vorhanden ist, verwendet EAP-TLS den Namen in dem Zertifikat, auf das im [**userCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) -Element verwiesen wird.

``` syntax
<xs:element name="Username"
    substitutionGroup="Identity"
 />
```

## <a name="requirements"></a>Anforderungen



| Role | Mindestens unterstützte Betriebssystemversionen |
|------|-------------------------------|
| Client<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Server<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[eaptlsuserpropertiesv1-Schema](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





