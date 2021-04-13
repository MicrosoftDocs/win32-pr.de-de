---
title: Enableidentityprivacy (identityprivacyparameters)-Element
description: Gibt an, ob die tatsächliche Identität eines Benutzers oder eine anonyme Identität gesendet wird. | Enableidentityprivacy (identityprivacyparameters)-Element
ms.assetid: 7751e5fa-895e-47f7-99d9-aa7ef2451eb1
keywords:
- Enableidentityprivacy-Element EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a96b49fe462f4ef8cedad550d1a6c87d680939
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353769"
---
# <a name="enableidentityprivacy-identityprivacyparameters-element"></a>Enableidentityprivacy (identityprivacyparameters)-Element

Das **enableidentityprivacy (identityprivacyparameters)** -Element gibt an, ob die tatsächliche Identität eines Benutzers oder eine anonyme Identität gesendet wird.

``` syntax
<xs:element name="EnableIdentityPrivacy"
    type="xs:Boolean"
    minOccurs="0"
 />
```

Das **enableidentityprivacy** -Element wird durch die [identityprivacyparameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md) definiert.

## <a name="remarks"></a>Bemerkungen

Das **enableidentityprivacy** -Element ist optional.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[Identityprivacyparameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**"Peer Erweiterungen"**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[mspeapconnectionpropertiesv2-Schema](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[mspeapconnectionpropertiesv2-Schema Elemente](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





