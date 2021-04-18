---
description: Enthält den Namen des Mobil Funknetzwerks.
ms.assetid: 4169babb-7616-468a-93f0-de25cce0c88b
title: ProviderName (ProviderType)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ProviderName
api_type:
- Schema
ms.openlocfilehash: 47929d508ad6d3a6567c1b52e720360f4e7cfbda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354508"
---
# <a name="providername-providertype-element"></a>ProviderName (ProviderType)-Element

Das **providerName (ProviderType)** -Element enthält den Namen des Mobil Funknetzwerks.

Das-Element ist eine Zeichenfolge mit maximal 20 Zeichen.

Dieses Element ist optional.

``` syntax
<xs:element name="ProviderName"
    type="providerNameType"
 />
```

Das **providerName** -Element wird durch den komplexen [**ProviderType**](schema-providertype-complextype.md) -Typ definiert.

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

 

 




