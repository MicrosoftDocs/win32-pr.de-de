---
description: Identifiziert den Namen des Basis Anbieters für das angegebene SIM/Gerät.
ms.assetid: 05d65091-5a1d-427a-8f51-1e1b9d189571
title: Homeprovidername (mbnprofile)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HomeProviderName
api_type:
- Schema
ms.openlocfilehash: 3d0af51e4873915838f2d55f683d07e9098aad3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751289"
---
# <a name="homeprovidername-mbnprofile-element"></a>Homeprovidername (mbnprofile)-Element

Das Element **homeprovidername (mbnprofile)** identifiziert den Namen des Home-Anbieters für das angegebene SIM/Gerät.

Dieses Element ist optional und wird vom mobilen Breitbanddienst zur internen Verwendung festgelegt. Eine Anwendung sollte dieses Feld beim Erstellen oder Aktualisieren eines Profils nicht festlegen.

``` syntax
<xs:element name="HomeProviderName"
    type="providerNameType"
 />
```

Das **homeprovidername** -Element wird durch das [**mbnprofile**](schema-mbnprofile-element.md) -Element definiert.

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

 

 




