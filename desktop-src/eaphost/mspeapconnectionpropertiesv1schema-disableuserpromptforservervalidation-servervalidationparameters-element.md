---
title: DisableUserPromptForServerValidation-Element (PEAP)
description: Erfahren Sie mehr über das DisableUserPromptForServerValidation (ServerValidationParameters)-Element. Er gibt an, ob der Benutzer zur Servervalidierung aufgefordert werden soll. | DisableUserPromptForServerValidation-Element (PEAP)
ms.assetid: ddb09888-731b-4c67-939e-9f0e6769408b
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
ms.openlocfilehash: c032c4c0dcb67f60f64fe2b447fd1af7061df51ed19586f4ee15b43d6a6f870c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119561760"
---
# <a name="disableuserpromptforservervalidation-servervalidationparameters-element-peap"></a>DisableUserPromptForServerValidation (ServerValidationParameters)-Element (PEAP)

Das **DisableUserPromptForServerValidation (ServerValidationParameters)-Element** gibt an, ob der Benutzer zur Serverüberprüfung aufgefordert werden soll.

Wenn **DisableUserPromptForServerValidation** true ist, führt EAP-TLS die Serverüberprüfung ohne Benutzereingabe durch. Wenn die Überprüfung fehlschlägt, schlägt EAP-TLS die Authentifizierung fehl. Wenn **DisableUserPromptForServerValidation** auf FALSE festgelegt ist, wird der Benutzer zur Eingabe eines überprüften Serverzertifikats oder -namens oder einer Stammzertifizierungsstelle aufgefordert.

Das **DisableUserPromptForServerValidation-Element** ist optional.

``` syntax
<xs:element name="DisableUserPromptForServerValidation"
    type="boolean"
 />
```

Das **DisableUserPromptForServerValidation-Element** wird vom komplexen [**ServerValidationParameters-Typ**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) definiert.

## <a name="requirements"></a>Anforderungen



| Rolle | Unterstützte Mindestversion des Betriebssystems |
|------|------------------------------|
| Client<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Server<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

**Mögliche unmittelbar übergeordnete Elemente in der Schemainstanz**
</dt> <dt>

[**ServerValidation (EapType)**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[mspeapconnectionpropertiesv1-Schema](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[mspeapconnectionpropertiesv1-Schemaelemente](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





