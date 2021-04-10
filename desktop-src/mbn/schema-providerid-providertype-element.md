---
description: Gibt die Anbieter-ID des Mobil Funknetzwerks an.
ms.assetid: 5528dfec-eb1b-4af3-8d7d-03b458e5ae75
title: ProviderID (ProviderType)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ProviderID
api_type:
- Schema
ms.openlocfilehash: 750e6c3f4397f710bb1ccbcea0286be68a89e145
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214697"
---
# <a name="providerid-providertype-element"></a>ProviderID (ProviderType)-Element

Das **ProviderType-Element (ProviderType)** gibt die Anbieter-ID des Mobil Funk Netzwerks an.

Das-Element ist eine Sequenz von Ziffern mit maximal 6 Ziffern.

Dieses Element ist im [**Provider**](schema-provider-dataroamingpartners-element.md) -Element erforderlich.

``` syntax
<xs:element name="ProviderID"
    type="providerType"
 />
```

Das **ProviderID** -Element wird durch den komplexen [**ProviderType**](schema-providertype-complextype.md) -Typ definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Provider Type**](schema-providertype-complextype.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Anbieter (dataroamingpartners)**](schema-provider-dataroamingpartners-element.md)
</dt> </dl>

 

 




