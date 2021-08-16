---
title: InnerEapOptional -Element (EapType)
description: Erfahren Sie mehr über das InnerEapOptional-Element (EapType). Dieses Element gibt an, ob der GAST-Zugriff durchzuführen ist.
ms.assetid: 2d314c89-5415-407f-84c3-c4c5c8957b39
keywords:
- InnerEapOptional-Element EAPHost
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
ms.openlocfilehash: 372163b39ea788b5c03bd25aedcc44aee172d58080fb94e3333a029a514962a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119404590"
---
# <a name="innereapoptional-eaptype-element"></a>InnerEapOptional -Element (EapType)

Das **InnerEapOptional-Element (EapType)** gibt an, ob der GAST-Zugriff verwendet werden soll.

``` syntax
<xs:element name="InnerEapOptional"
    type="boolean"
 />
```

Das **InnerEapOptional-Element** wird durch das [**EapType-Element**](mspeapconnectionpropertiesv1schema-eaptype-element.md) definiert.

## <a name="remarks"></a>Hinweise

Wenn das **InnerEapOptional-Element** TRUE ist, muss das [**Eap-Element**](baseeapconnectionpropertiesv1schema-eap-element.md) vorhanden sein und die innere Methode und ihre Konfiguration beschreiben. bei FALSE führt PEAP GASTzugriff aus. Das **InnerEapOptional-Element** ist optional.

## <a name="requirements"></a>Anforderungen



| Role | Unterstützte Mindestversion des Betriebssystems |
|------|------------------------------|
| Client<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
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

 

 





