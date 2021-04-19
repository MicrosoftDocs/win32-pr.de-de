---
title: Disableuserpromptforservervalidation-Element (Peer-APP)
description: Erfahren Sie mehr über das disableuserpromptforservervalidation (servervalidationparameters)-Element. Gibt an, ob der Benutzer zur Server Validierung aufgefordert werden soll. | Disableuserpromptforservervalidation-Element (Peer-APP)
ms.assetid: ddb09888-731b-4c67-939e-9f0e6769408b
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
ms.openlocfilehash: 168ce6e371495901f2ed93fb69b605a807bc363c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106363920"
---
# <a name="disableuserpromptforservervalidation-servervalidationparameters-element-peap"></a>Disableuserpromptforservervalidation (servervalidationparameters)-Element (Peer-APP)

Das **disableuserpromptforservervalidation (servervalidationparameters)** -Element gibt an, ob der Benutzer zur Server Validierung aufgefordert werden soll.

Wenn " **disableuserpromptforservervalidation** " den Wert "true" hat, führt EAP-TLS die Server Validierung ohne Benutzereingaben aus. Wenn die Überprüfung fehlschlägt, schlägt EAP-TLS die Authentifizierung fehl. Wenn **disableuserpromptforservervalidation** den Wert false hat, wird der Benutzer zur Eingabe eines validierten Serverzertifikats oder-Namens bzw. einer Stamm Zertifizierungsstelle (Root Certificate Authority, ca) aufgefordert.

Das **disableuserpromptforservervalidation** -Element ist optional.

``` syntax
<xs:element name="DisableUserPromptForServerValidation"
    type="boolean"
 />
```

Das **disableuserpromptforservervalidation** -Element wird durch den komplexen [**servervalidationparameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) -Typ definiert.

## <a name="requirements"></a>Anforderungen



| Role | Mindestens unterstützte Betriebssystemversion |
|------|------------------------------|
| Client<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Server<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Servervalidationparameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

**Mögliche direkt übergeordnete Elemente in der Schema Instanz**
</dt> <dt>

[**ServerValidation (eaptype)**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[mspeapconnectionpropertiesv1-Schema](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[mspeapconnectionpropertiesv1-Schema Elemente](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





