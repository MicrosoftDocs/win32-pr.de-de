---
title: Password (eaptype)-Element
description: Erfahren Sie mehr über das Password (eaptype)-Element. Dieses Element identifiziert das Kennwort für den Benutzer oder Computer, der authentifiziert wird.
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
ms.openlocfilehash: 6da29146be7ed2f0c17d7311f79921b44cd0929e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039624"
---
# <a name="password-eaptype-element"></a>Password (eaptype)-Element

Das **Kennwort-Element (eaptype)** identifiziert das Kennwort des Benutzers oder Computers, der authentifiziert wird.

``` syntax
<xs:element name="Password"
    type="string"
 />
```

Das **Password** -Element wird durch das [**eaptype**](mschapv2userpropertiesv1schema-eaptype-element.md) -Element definiert.

## <a name="remarks"></a>Bemerkungen

Wenn das **Password-Element (eaptype)** nicht vorhanden ist, wird der Kenn Wort Hash von Winlogon abgerufen. Dieses Element ist optional.

## <a name="requirements"></a>Anforderungen



| Role | Mindestens unterstützte Betriebssystemversion |
|------|------------------------------|
| Client<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Server<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Eaptype**](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Eaptype**](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[mschapv2userpropertiesv1-Schema](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





