---
description: Identifiziert den Namen des Home-Anbieters für die bestimmte SIM/das Gerät.
ms.assetid: 05d65091-5a1d-427a-8f51-1e1b9d189571
title: HomeProviderName (MBNProfile)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HomeProviderName
api_type:
- Schema
ms.openlocfilehash: 1868be18dc7acf9d5146f987658feb006714fbcc3db35883007afd01c308609e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035828"
---
# <a name="homeprovidername-mbnprofile-element"></a>HomeProviderName (MBNProfile)-Element

Das **HomeProviderName (MBNProfile)-Element** identifiziert den Namen des Home-Anbieters für die gegebene SIM/Das Gerät.

Dieses Element ist optional und wird vom Mobilen Breitbanddienst für die interne Verwendung festgelegt. Eine Anwendung sollte dieses Feld beim Erstellen oder Aktualisieren eines Profils nicht festlegen.

``` syntax
<xs:element name="HomeProviderName"
    type="providerNameType"
 />
```

Das **HomeProviderName-Element** wird durch das [**MBNProfile-Element**](schema-mbnprofile-element.md) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> </dl>

 

 




