---
title: ServerNames (ServerValidationParameters)-Element (PEAP)
description: Erfahren Sie mehr über das ServerNames -Element (ServerValidationParameters). Dieses Element stellt eine Liste von durch Semikolons getrennten Servernamen dar. | ServerNames (ServerValidationParameters)-Element (PEAP)
ms.assetid: 2595daa1-9f1b-40cf-9219-0e7295fdd5c3
keywords:
- ServerNames-Element EAPHost
topic_type:
- apiref
api_name:
- ServerNames
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f3f9de6ee28077b5206a9783ef7722864a479e1e5f26b78e4402ac79c6e4be5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984010"
---
# <a name="servernames-servervalidationparameters-element-peap"></a>ServerNames (ServerValidationParameters)-Element (PEAP)

Das **ServerNames (ServerValidationParameters)-Element** stellt eine Liste von durch Semikolons getrennten Servernamen dar.

``` syntax
<xs:element name="ServerNames"
    type="string"
    minOccurs="0"
 />
```

Das **ServerNames-Element** wird vom komplexen [**ServerValidationParameters-Typ**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) definiert.

## <a name="remarks"></a>Hinweise

Jeder Servername ist durch Semikolons getrennt und kann durch reguläre Ausdrücke dargestellt werden. Das **ServerNames-Element** ist optional.

## <a name="requirements"></a>Anforderungen



| Role | Unterstützte Mindestversion des Betriebssystems |
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

 

 





