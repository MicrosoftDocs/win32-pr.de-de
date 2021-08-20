---
description: Identifiziert den Namen und die Anbieter-ID für ein Mobilfunknetz.
ms.assetid: 007ecad9-23a3-4352-b3e2-c22d0f3f449d
title: Provider (DataRoamingPartners)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Provider
api_type:
- Schema
ms.openlocfilehash: d5ce12ddf15ad57071f2717e5801fbd05f8e2925ea474345f7c376bc2445cd02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119347160"
---
# <a name="provider-dataroamingpartners-element"></a>Provider (DataRoamingPartners)-Element

Das **Provider-Element (DataRoamingPartners)** identifiziert den Namen und die Anbieter-ID für ein Mobilfunknetz.

Dieses Element verfügt über die folgenden untergeordneten Elemente.

-   [**ProviderID**](schema-providerid-providertype-element.md)
-   [**ProviderName**](schema-providername-providertype-element.md)

Dieses Element kann mehrmals innerhalb des [**DataRoamingPartners-Elements definiert**](schema-dataroamingpartners-mbnprofile-element.md) werden. Sie muss mindestens einmal definiert werden.

``` syntax
<xs:element name="Provider"
    type="providerType"
 />
```

Das **Provider-Element** wird durch das [**DataRoamingPartners-Element**](schema-dataroamingpartners-mbnprofile-element.md) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**DataRoamingPartners (MBNProfile)**](schema-dataroamingpartners-mbnprofile-element.md)
</dt> </dl>

 

 




