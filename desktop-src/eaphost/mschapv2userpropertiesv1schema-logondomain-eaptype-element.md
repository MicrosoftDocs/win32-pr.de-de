---
title: LogonDomain (eaptype)-Element
description: Erfahren Sie mehr über das LogonDomain (eaptype)-Element. Dieses Element identifiziert die Domäne des Benutzers oder Computers, der authentifiziert wird.
ms.assetid: a93793cd-29ee-47f9-8d91-895844c08bae
keywords:
- LogonDomain-Element EAPHost
topic_type:
- apiref
api_name:
- LogonDomain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3dbbe57bcd29459f6e9807d8f39aedb4faa72a1b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039594"
---
# <a name="logondomain-eaptype-element"></a>LogonDomain (eaptype)-Element

Das **LogonDomain (eaptype)** -Element identifiziert die Domäne des Benutzers oder Computers, der authentifiziert wird.

``` syntax
<xs:element name="LogonDomain
          
        "
    type="string"
 />
```

Das **LogonDomain** -Element wird durch das [**eaptype**](mschapv2userpropertiesv1schema-eaptype-element.md) -Element definiert.

## <a name="remarks"></a>Bemerkungen

Wenn das **LogonDomain (eaptype)** -Element nicht vorhanden ist, wird die Domäne von Winlogon verwendet. Dieses Element ist optional.

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

 

 





