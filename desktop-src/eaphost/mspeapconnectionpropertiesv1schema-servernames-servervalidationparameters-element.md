---
title: Server Ames (servervalidationparameters)-Element (Peer Name)
description: Erfahren Sie mehr über das servernames (servervalidationparameters)-Element. Dieses Element stellt eine Liste von durch Semikolons getrennten Servernamen dar. | Server Ames (servervalidationparameters)-Element (Peer Name)
ms.assetid: 2595daa1-9f1b-40cf-9219-0e7295fdd5c3
keywords:
- Servernames-Element EAPHost
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
ms.openlocfilehash: 40aa7ba317b7ba7c3f7a06cce87ef57c2906fe4b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106354304"
---
# <a name="servernames-servervalidationparameters-element-peap"></a>Server Ames (servervalidationparameters)-Element (Peer Name)

Das Server **Ames (servervalidationparameters)** -Element stellt eine Liste von durch Semikolons getrennten Servernamen dar.

``` syntax
<xs:element name="ServerNames"
    type="string"
    minOccurs="0"
 />
```

Das **servernames** -Element wird durch den komplexen [**servervalidationparameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) -Typ definiert.

## <a name="remarks"></a>Bemerkungen

Jeder Servername wird durch Semikolons getrennt und kann durch reguläre Ausdrücke dargestellt werden. Das **servernames** -Element ist optional.

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

 

 





