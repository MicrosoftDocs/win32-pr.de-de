---
description: Gibt die Parameter an, die zum Einrichten einer Datenverbindung erforderlich sind.
ms.assetid: 7a3d3b9d-f799-4927-9c18-04b025788a4a
title: Context (mbnprofile)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Context
api_type:
- Schema
ms.openlocfilehash: dac98101dade85fbbaa63275933885241ef206fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372841"
---
# <a name="context-mbnprofile-element"></a>Context (mbnprofile)-Element

Das **context (mbnprofile)** -Element gibt die Parameter an, die zum Einrichten einer Datenverbindung erforderlich sind.

Das-Element kann die folgenden untergeordneten Elemente aufweisen.

-   [**AccessString**](schema-accessstring-contexttype-element.md)
-   [**UserLogonCred**](schema-userlogoncred-contexttype-element.md)
-   [**Komprimi**](schema-compression-contexttype-element.md)
-   [**AuthProtocol**](schema-authprotocol-contexttype-element.md)

Dieses Element kann maximal ein Vorkommen aufweisen.

``` syntax
<xs:element name="Context"
    type="contextType"
 />
```

Das **Kontext** Element wird durch das [**mbnprofile**](schema-mbnprofile-element.md) -Element definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Mbnprofile**](schema-mbnprofile-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Mbnprofile**](schema-mbnprofile-element.md)
</dt> </dl>

 

 




