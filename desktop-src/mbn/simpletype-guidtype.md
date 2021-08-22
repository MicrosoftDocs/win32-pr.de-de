---
description: Eine Zeichenfolgendarstellung einer GUID im üblichen Format.
MS-HAID: WWAN\_profile\_v4.simpleType\_guidType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: einfacher guidType-Typ (mobiles Breitband)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9469ff58d15ad51ba53a9975655e9d489c2f3a4fdb9784feb3bd41daeb0d0ea5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975069"
---
# <a name="span-idwwan_profile_v4simpletype_guidtypespanguidtype-simple-type-mobile-broadband"></a><span id="WWAN_profile_v4.simpleType_guidType"></span>einfacher guidType-Typ (mobiles Breitband)

Eine Zeichenfolgendarstellung einer GUID im üblichen Format.

``` syntax
<xs:simpleType name="guidType">
    <xs:restriction
        base="token"
    >
        <xs:pattern
            value="{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Muster

Der **einfache GuidType-Typ** ist ein Token, das durch das folgende Muster eingeschränkt wird:

-   `{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}}`

 

 



