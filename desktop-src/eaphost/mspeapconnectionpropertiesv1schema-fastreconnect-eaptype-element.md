---
title: Fastreconnect (eaptype)-Element
description: Erfahren Sie mehr über das fastreconnect (eaptype)-Element. Dieses Element gibt an, ob eine schnelle erneute Verbindungs Herstellung durchgeführt werden soll.
ms.assetid: 075285b0-7b1b-4d3c-af27-a718f3c20394
keywords:
- Fastreconnect-Element EAPHost
topic_type:
- apiref
api_name:
- FastReconnect
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2214519db68b8c95b0e0efa91d68a7cd667b5f87
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106342375"
---
# <a name="fastreconnect-eaptype-element"></a>Fastreconnect (eaptype)-Element

Das **fastreconnect (eaptype)** -Element gibt an, ob eine schnelle erneute Verbindungs Herstellung durchgeführt werden soll.

``` syntax
<xs:element name="FastReconnect"
    type="boolean"
 />
```

Das **fastreconnect** -Element wird durch das [**eaptype**](mspeapconnectionpropertiesv1schema-eaptype-element.md) -Element definiert.

## <a name="remarks"></a>Bemerkungen

Wenn das **fastreconnect** -Element "true" ist, versucht die Peer-APP, eine schnelle erneute Verbindungs Herstellung auszuführen. der Wert false gibt an, dass die vollständige Authentifizierung von Peer-App Das **fastreconnect** -Element ist optional.

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

 

 





