---
title: AnonymousUserName (identityprivacyparameters)-Element
description: Enthält eine anonyme Identität, die anstelle der true-Identifizierung eines Benutzers verwendet wird. Sie wird während der ersten Phase der Peer-Authentifizierung gesendet, wenn die Identität als nur-Text gesendet wird.
ms.assetid: 74a33a75-cf21-4346-a984-f2f8564c3b57
keywords:
- AnonymousUserName-Element EAPHost
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
ms.openlocfilehash: 6bbc973160a8865e246a6cec87ce02ced136d786
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392055"
---
# <a name="anonymoususername-identityprivacyparameters-element"></a>AnonymousUserName (identityprivacyparameters)-Element

Das **AnonymousUserName (identityprivacyparameters)** -Element enthält eine anonyme Identität, die anstelle der true-Identifikation eines Benutzers verwendet wird. Sie wird während der ersten Phase der Peer-Authentifizierung gesendet, wenn die **Identität** als nur-Text gesendet wird.

Die Verwendung der anonymen Identität wird vom [**enableidentityprivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) -Element bestimmt.

``` syntax
<xs:element name="AnonymousUserName"
    type="xs:String"
    minOccurs="0"
 />
```

Das **AnonymousUserName** -Element wird durch die [identityprivacyparameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md) definiert.

## <a name="remarks"></a>Bemerkungen

Das **AnonymousUserName** -Element ist optional.

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

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[mspeapconnectionpropertiesv2-Schema](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[mspeapconnectionpropertiesv2-Schema Elemente](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





