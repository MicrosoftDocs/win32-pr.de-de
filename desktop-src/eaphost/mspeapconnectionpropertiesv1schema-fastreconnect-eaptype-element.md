---
title: FastReconnect(EapType)-Element
description: Erfahren Sie mehr über das FastReconnect-Element (EapType). Dieses Element gibt an, ob eine schnelle wiederherzustellende Verbindung ausgeführt werden soll.
ms.assetid: 075285b0-7b1b-4d3c-af27-a718f3c20394
keywords:
- FastReconnect-Element EAPHost
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
ms.openlocfilehash: 1bda956d698ebefef956e85557c6d940baa02f6bcc9ef7cca0081fd668107e18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119238720"
---
# <a name="fastreconnect-eaptype-element"></a>FastReconnect(EapType)-Element

Das **Element FastReconnect (EapType)** gibt an, ob eine schnelle erneute Verbindung ausgeführt werden soll.

``` syntax
<xs:element name="FastReconnect"
    type="boolean"
 />
```

Das **FastReconnect-Element** wird durch das [**EapType-Element**](mspeapconnectionpropertiesv1schema-eaptype-element.md) definiert.

## <a name="remarks"></a>Hinweise

Wenn das **FastReconnect-Element** TRUE ist, versucht PEAP, eine schnelle wiederherzustellende Verbindung durchzuführen. False gibt an, dass PEAP die vollständige Authentifizierung ausführt. Das **FastReconnect-Element** ist optional.

## <a name="requirements"></a>Anforderungen



| Role | Unterstützte Mindestversion des Betriebssystems |
|------|------------------------------|
| Client<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Server<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[mspeapconnectionpropertiesv1-Schema](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[mspeapconnectionpropertiesv1-Schemaelemente](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





