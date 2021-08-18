---
title: DifferentUsername (EapType)-Element
description: Erfahren Sie mehr über das DifferentUsername-Element (EapType). Dieses Element bestimmt, welcher Benutzername EAP-TLS verwendet werden soll.
ms.assetid: f0ce41a9-c774-4d12-8a5a-a8eb1eb84cb0
keywords:
- DifferentUsername-Element EAPHost
topic_type:
- apiref
api_name:
- DifferentUsername
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2980a55e76d238578822cfc8db54a9b6c324e21d4a8f0481ab9bc91e050fb008
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984090"
---
# <a name="differentusername-eaptype-element"></a>DifferentUsername (EapType)-Element

Das **DifferentUsername-Element (EapType)** bestimmt, welcher Benutzername EAP-TLS verwendet werden soll.

``` syntax
<xs:element name="DifferentUsername"
    type="boolean"
 />
```

Das **DifferentUsername-Element** wird durch das [**EapType-Element**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) definiert.

## <a name="remarks"></a>Hinweise

Wenn das **DifferentUserName-Element** TRUE ist, sollte EAP-TLS einen anderen Benutzernamen als den Namen verwenden, der im Zertifikat angezeigt wird. Wenn das **DifferentUserName-Element** FALSE ist, verwendet EAP-TLS den Benutzernamen, der im Zertifikat angezeigt wird.

Das **DifferentUserName-Element** ist optional.

## <a name="requirements"></a>Anforderungen



| Role | Unterstützte Mindestversion des Betriebssystems |
|------|------------------------------|
| Client<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Server<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1-Schema](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1-Schemaelemente](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





