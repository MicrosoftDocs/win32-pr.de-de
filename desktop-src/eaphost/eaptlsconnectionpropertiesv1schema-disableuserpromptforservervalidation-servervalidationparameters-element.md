---
title: DisableUserPromptForServerValidation (ServerValidationParameters)
description: Erfahren Sie mehr über das DisableUserPromptForServerValidation (ServerValidationParameters)-Element. Gibt an, ob der Benutzer zur Servervalidierung aufgefordert werden soll. | DisableUserPromptForServerValidation (ServerValidationParameters)
ms.assetid: d1c2f334-286b-4aac-b723-806b90fc7b1f
keywords:
- DisableUserPromptForServerValidation-Element EAPHost
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
ms.openlocfilehash: 37f412f9c6200e7d2a54d624d0a77b4df5316ea7edd0ab75b69f92c753abbcff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118273718"
---
# <a name="disableuserpromptforservervalidation-servervalidationparameters-element-tls"></a>DisableUserPromptForServerValidation (ServerValidationParameters)-Element (TLS)

Das **DisableUserPromptForServerValidation-Element (ServerValidationParameters)** gibt an, ob der Benutzer zur Serverüberprüfung aufgefordert werden soll.

Wenn **DisableUserPromptForServerValidation** true ist, führt EAP-TLS die Serverüberprüfung ohne Benutzereingabe aus. Wenn die Überprüfung fehlschlägt, schlägt EAP-TLS die Authentifizierung fehl. Wenn **DisableUserPromptForServerValidation** auf FALSE festgelegt ist, wird der Benutzer zur Eingabe eines überprüften Serverzertifikats oder -namens oder einer Stammzertifizierungsstelle aufgefordert.

Das **DisableUserPromptForServerValidation-Element** ist optional.

``` syntax
<xs:element name="DisableUserPromptForServerValidation"
    type="boolean"
 />
```

Das **DisableUserPromptForServerValidation-Element** wird durch den komplexen [**ServerValidationParameters-Typ**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) definiert.

## <a name="requirements"></a>Anforderungen



| Role | Unterstützte Mindestversion des Betriebssystems |
|------|------------------------------|
| Client<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Server<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

**Mögliche unmittelbar übergeordnete Elemente in der Schemainstanz**
</dt> <dt>

[**ServerValidation (EapType)**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1-Schema](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1-Schemaelemente](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





