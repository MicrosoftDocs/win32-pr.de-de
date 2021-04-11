---
description: Identifiziert den Namen und die Anbieter-ID für ein Mobilfunknetz.
ms.assetid: 007ecad9-23a3-4352-b3e2-c22d0f3f449d
title: Provider-Element (dataroamingpartners)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Provider
api_type:
- Schema
ms.openlocfilehash: b5b36c973bf44175b90e25fd2a141fed3624d8b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129009"
---
# <a name="provider-dataroamingpartners-element"></a>Provider-Element (dataroamingpartners)

Das **Provider-Element (dataroamingpartners)** identifiziert den Namen und die Anbieter-ID für ein Mobilfunknetz.

Dieses Element verfügt über die folgenden untergeordneten Elemente.

-   [**ProviderID**](schema-providerid-providertype-element.md)
-   [**ProviderName**](schema-providername-providertype-element.md)

Dieses Element kann im [**dataroamingpartners**](schema-dataroamingpartners-mbnprofile-element.md) -Element mehrmals definiert werden. Sie muss mindestens einmal definiert werden.

``` syntax
<xs:element name="Provider"
    type="providerType"
 />
```

Das **Provider** -Element wird durch das [**dataroamingpartners**](schema-dataroamingpartners-mbnprofile-element.md) -Element definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Dataroamingpartners (mbnprofile)**](schema-dataroamingpartners-mbnprofile-element.md)
</dt> </dl>

 

 




