---
title: ServerValidation (eaptype)-Element (Peer-APP)
description: Erfahren Sie mehr über das ServerValidation (eaptype)-Element. Dieses Element enthält Informationen zum Durchführen der Server Validierung. | ServerValidation (eaptype)-Element (Peer-APP)
ms.assetid: 5b213853-7161-456c-bbba-d3b1118f1786
keywords:
- ServerValidation-Element EAPHost
topic_type:
- apiref
api_name:
- ServerValidation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1495da3f1a1f5e69e7a6af9c64e69aa1ea354abc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106354940"
---
# <a name="servervalidation-eaptype-element-peap"></a>ServerValidation (eaptype)-Element (Peer-APP)

Das **ServerValidation (eaptype)** -Element enthält Informationen zum Durchführen der Server Validierung.

``` syntax
<xs:element name="ServerValidation"
    type="ServerValidationParameters"
 />
```

Das **ServerValidation** -Element wird durch das [**eaptype**](mspeapconnectionpropertiesv1schema-eaptype-element.md) -Element definiert.

## <a name="remarks"></a>Bemerkungen

Das **ServerValidation** -Element ist optional.

## <a name="requirements"></a>Anforderungen



| Role | Mindestens unterstützte Betriebssystemversion |
|------|------------------------------|
| Client<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Server<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Eaptype**](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Eaptype**](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[mspeapconnectionpropertiesv1-Schema](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[mspeapconnectionpropertiesv1-Schema Elemente](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





