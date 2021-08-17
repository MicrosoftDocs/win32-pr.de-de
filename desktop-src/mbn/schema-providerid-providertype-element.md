---
description: Gibt die Anbieter-ID des Mobilfunknetzes an.
ms.assetid: 5528dfec-eb1b-4af3-8d7d-03b458e5ae75
title: ProviderID -Element (providerType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ProviderID
api_type:
- Schema
ms.openlocfilehash: b40ac5abab2abf850d927c21f0de66ad419987f594f28dffcd380ead7f982d63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959790"
---
# <a name="providerid-providertype-element"></a>ProviderID -Element (providerType)

Das **ProviderID (providerType)-Element** gibt die Anbieter-ID des Mobilfunknetzes an.

Das Element ist eine Sequenz von Ziffern mit maximal sechs Ziffern.

Dieses Element ist innerhalb des [**Provider-Elements**](schema-provider-dataroamingpartners-element.md) erforderlich.

``` syntax
<xs:element name="ProviderID"
    type="providerType"
 />
```

Das **ProviderID-Element** wird vom komplexen [**providerType-Typ**](schema-providertype-complextype.md) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                         |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**Providertype**](schema-providertype-complextype.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**Anbieter (DataRoamingPartners)**](schema-provider-dataroamingpartners-element.md)
</dt> </dl>

 

 




