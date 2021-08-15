---
title: Password (EapType)-Element
description: Erfahren Sie mehr über das Password -Element (EapType). Dieses Element identifiziert das Kennwort des Benutzers oder Computers, der authentifiziert wird.
ms.assetid: d3ad95b8-2d98-420f-a680-a83b49ae2992
keywords:
- Password-Element EAPHost
topic_type:
- apiref
api_name:
- Password
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cbbcb7b0acd372bbe71ee6d22f44a736948b145378f62f40820e3de53d77b875
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118273199"
---
# <a name="password-eaptype-element"></a>Password (EapType)-Element

Das **Password -Element (EapType)** identifiziert das Kennwort des Benutzers oder Computers, der authentifiziert wird.

``` syntax
<xs:element name="Password"
    type="string"
 />
```

Das **Password-Element** wird durch das [**EapType-Element**](mschapv2userpropertiesv1schema-eaptype-element.md) definiert.

## <a name="remarks"></a>Hinweise

Wenn das **Password -Element (EapType)** nicht vorhanden ist, wird der Kennworthash von winlogon erhalten. Dieses Element ist optional.

## <a name="requirements"></a>Anforderungen



| Role | Unterstützte Mindestversion des Betriebssystems |
|------|------------------------------|
| Client<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Server<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[mschapv2userpropertiesv1-Schema](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





