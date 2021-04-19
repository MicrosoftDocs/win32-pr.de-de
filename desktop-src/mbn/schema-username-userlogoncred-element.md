---
description: Gibt den Benutzernamen für die Anmeldung an.
ms.assetid: a312de24-2a81-4fac-9c23-4e67e171e692
title: UserName (userlogonkred)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UserName
api_type:
- Schema
ms.openlocfilehash: 53ad1bde74f2d2a1649fa5fdee23ef70ab53b09d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348166"
---
# <a name="username-userlogoncred-element"></a>UserName (userlogonkred)-Element

Das **username (userlogonkred)-** Element gibt den Benutzernamen für die Anmeldung an.

Das-Element ist eine Zeichenfolge mit maximal 255 Zeichen.

Dieses Element ist optional.

``` syntax
<xs:element name="UserName"
    type="nameType"
 />
```

Das **username** -Element wird durch das [**userlogonkred-**](schema-userlogoncred-contexttype-element.md) Element definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**UserLogonCred**](schema-userlogoncred-contexttype-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Userlogonkred (ContextType)**](schema-userlogoncred-contexttype-element.md)
</dt> </dl>

 

 




