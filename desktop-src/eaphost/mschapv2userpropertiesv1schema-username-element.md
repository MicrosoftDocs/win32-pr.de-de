---
title: Username-Element (CHAP)
description: Erfahren Sie mehr über das UserName-Element, das den Benutzer identifiziert, der authentifiziert wird. Weitere Informationen finden Sie in einem Syntax Beispiel.
ms.assetid: 3dd12864-5e0a-492c-a2c3-28118d21a0f2
keywords:
- Username-Element EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29065a59e150d2a4295e91b41862250d58e017b5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949115"
---
# <a name="username-element-chap"></a>Username-Element (CHAP)

Das **username** -Element identifiziert den Benutzer, der authentifiziert wird.

``` syntax
<xs:element name="Username"
    substitutionGroup="Identity"
 />
```

## <a name="remarks"></a>Bemerkungen

Wenn das **username** -Element nicht vorhanden ist, wird der Benutzername aus Winlogon abgerufen. Dieses Element ist optional.

## <a name="requirements"></a>Anforderungen



| Role | Mindestens unterstützte Betriebssystemversion |
|------|------------------------------|
| Client<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Server<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[mschapv2userpropertiesv1-Schema](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





