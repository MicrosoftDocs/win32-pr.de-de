---
title: Username-Element (TLS)
description: Erfahren Sie mehr über das Username-Element. Dieses Element erfasst den Benutzernamen, der in der antwort EAP-Identity gesendet werden soll.
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
ms.openlocfilehash: 6748ac8c352540d2288cf3bf3c790004d832ba47961fbc7b9e8211fa712ccb6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117720119"
---
# <a name="username-element-tls"></a>Username-Element (TLS)

Das **Username-Element** erfasst den Benutzernamen, der in der antwort EAP-Identity gesendet werden soll.

Wenn das **Username-Element** nicht vorhanden ist, verwendet EAP-TLS den Namen im Zertifikat, auf das im [**UserCert-Element**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) verwiesen wird.

``` syntax
<xs:element name="Username"
    substitutionGroup="Identity"
 />
```

## <a name="requirements"></a>Anforderungen



| Role | Unterstützte Mindestversionen des Betriebssystems |
|------|-------------------------------|
| Client<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Server<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[eaptlsuserpropertiesv1-Schema](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





