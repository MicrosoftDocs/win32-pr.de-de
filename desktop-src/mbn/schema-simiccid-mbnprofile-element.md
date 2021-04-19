---
description: Identifiziert die SIM-Identifikationsnummer für GSM-Geräte.
ms.assetid: 980afba4-fc31-4da0-ba01-6eb8e3db0ac8
title: Simiccid (mbnprofile)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SimIccID
api_type:
- Schema
ms.openlocfilehash: f566253ad3e86b4f7ee7317cf125d9e649034847
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345053"
---
# <a name="simiccid-mbnprofile-element"></a>Simiccid (mbnprofile)-Element

Das **simiccid (mbnprofile)-** Element identifiziert die SIM-Identifikationsnummer für GSM-Geräte.

Dieses Element ist optional und wird vom mobilen Breitbanddienst zur internen Verwendung festgelegt. Eine Anwendung sollte dieses Feld beim Erstellen oder Aktualisieren eines Profils nicht festlegen.

``` syntax
<xs:element name="SimIccID"
    type="simIccIDType"
 />
```

Das **simiccid-** Element wird durch das [**mbnprofile**](schema-mbnprofile-element.md) -Element definiert.

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

 

 




