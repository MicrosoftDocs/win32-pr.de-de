---
title: Innereapoptional (eaptype)-Element
description: Erfahren Sie mehr über das innereapoptional (eaptype)-Element. Dieses Element gibt an, ob Gast Zugriff durchgeführt werden soll.
ms.assetid: 2d314c89-5415-407f-84c3-c4c5c8957b39
keywords:
- Innereapoptional-Element EAPHost
topic_type:
- apiref
api_name:
- InnerEapOptional
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: be63845f389936656172b4cbb4e42de659bbf0e1
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102334"
---
# <a name="innereapoptional-eaptype-element"></a>Innereapoptional (eaptype)-Element

Das **innereapoptional (eaptype)** -Element gibt an, ob Gast Zugriff durchgeführt werden soll.

``` syntax
<xs:element name="InnerEapOptional"
    type="boolean"
 />
```

Das **innereapoptional** -Element wird durch das [**eaptype**](mspeapconnectionpropertiesv1schema-eaptype-element.md) -Element definiert.

## <a name="remarks"></a>Bemerkungen

Wenn das **innereapoptional** -Element true ist, muss das [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) -Element vorhanden sein und die innere Methode und die Konfiguration beschreiben. Wenn der Wert false ist, führt der Peer-Agent den Gast Zugriff aus. Das **innereapoptional** -Element ist optional.

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


</dt> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[mspeapconnectionpropertiesv1-Schema](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[mspeapconnectionpropertiesv1-Schema Elemente](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





