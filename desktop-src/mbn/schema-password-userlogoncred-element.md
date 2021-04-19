---
description: Gibt das Kennwort an, das zum Authentifizieren eines Benutzers verwendet wird.
ms.assetid: 9c02413b-a4c7-4c1f-a150-e27cc125faf6
title: Password (userlogonkred)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Password
api_type:
- Schema
ms.openlocfilehash: b05e34bcbaa91aba5cbfbd14f2bc8534aa91dd37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346307"
---
# <a name="password-userlogoncred-element"></a>Password (userlogonkred)-Element

Das [**Kennwort (userlogonkred)-**](schema-ignorepassword-userlogoncred-element.md) Element gibt das Kennwort an, das zum Authentifizieren eines Benutzers verwendet wird.

Das-Element ist eine Zeichenfolge mit bis zu 255 Zeichen.

Dieses Element ist optional.

``` syntax
<xs:element name="Password"
    type="string"
 />
```

Das **Password** -Element wird durch das [**userlogonkred-**](schema-userlogoncred-contexttype-element.md) Element definiert.

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

 

 




