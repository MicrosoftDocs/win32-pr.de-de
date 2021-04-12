---
title: Disableuserpromptforservervalidation (servervalidationparameters)
description: Erfahren Sie mehr über das disableuserpromptforservervalidation (servervalidationparameters)-Element. Gibt an, ob der Benutzer zur Server Validierung aufgefordert werden soll. | Disableuserpromptforservervalidation (servervalidationparameters)
ms.assetid: d1c2f334-286b-4aac-b723-806b90fc7b1f
keywords:
- Disableuserpromptforservervalidation-Element EAPHost
topic_type:
- apiref
api_name:
- DisableUserPromptForServerValidation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 368b2593b3c55ef571e3f1892634318e54447643
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219208"
---
# <a name="disableuserpromptforservervalidation-servervalidationparameters-element-tls"></a>Disableuserpromptforservervalidation (servervalidationparameters)-Element (TLS)

Das **disableuserpromptforservervalidation (servervalidationparameters)** -Element gibt an, ob der Benutzer zur Server Validierung aufgefordert werden soll.

Wenn " **disableuserpromptforservervalidation** " den Wert "true" hat, führt EAP-TLS die Server Validierung ohne Benutzereingaben aus. Wenn die Überprüfung fehlschlägt, schlägt EAP-TLS die Authentifizierung fehl. Wenn **disableuserpromptforservervalidation** den Wert false hat, wird der Benutzer zur Eingabe eines validierten Serverzertifikats oder-Namens bzw. einer Stamm Zertifizierungsstelle (Root Certificate Authority, ca) aufgefordert.

Das **disableuserpromptforservervalidation** -Element ist optional.

``` syntax
<xs:element name="DisableUserPromptForServerValidation"
    type="boolean"
 />
```

Das **disableuserpromptforservervalidation** -Element wird durch den komplexen [**servervalidationparameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) -Typ definiert.

## <a name="requirements"></a>Anforderungen



| Role | Mindestens unterstützte Betriebssystemversion |
|------|------------------------------|
| Client<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Server<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Servervalidationparameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

**Mögliche direkt übergeordnete Elemente in der Schema Instanz**
</dt> <dt>

[**ServerValidation (eaptype)**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1-Schema](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1-Schema Elemente](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





