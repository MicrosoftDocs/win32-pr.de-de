---
description: Gibt an, wie Kenn Wörter beim Aktualisieren von Profilen behandelt werden.
ms.assetid: 74d7ceb1-d778-4a12-907b-0528d9ff45be
title: Ignorepassword (userlogonkred)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IgnorePassword
api_type:
- Schema
ms.openlocfilehash: 40211a8f848d8d0551ed39297178bc985d9efba4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350461"
---
# <a name="ignorepassword-userlogoncred-element"></a>Ignorepassword (userlogonkred)-Element

Das **ignorepassword (userlogonkred)-** Element gibt an, wie Kenn Wörter beim Aktualisieren von Profilen behandelt werden.

Wenn diese Einstellung auf " **true** " festgelegt ist und zum Zeitpunkt des Aktualisierungs Vorgangs ein Profil mit demselben Namen vorhanden ist, wird das Kennwort aus diesem Profil übernommen und in einem neuen Profil gespeichert.

Dieses Element ist optional.

``` syntax
<xs:element name="IgnorePassword"
    type="boolean"
 />
```

Das **ignorepassword** -Element wird durch das [**userlogonkred-**](schema-userlogoncred-contexttype-element.md) Element definiert.

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

 

 




