---
description: Definiert einen global eindeutigen Bezeichnertyp im Registrierungsformat.
ms.assetid: 2be73c57-b6b6-46ab-93e1-d70f8655c30e
title: Einfacher GUIDType-Typ (Leistungsindikatoren)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 305195784a3578242caefc1fb7eb9bcd8dbd5b557d89d8752bc8242f648abbdc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119624920"
---
# <a name="guidtype-simple-type-performance-counters"></a>Einfacher GUIDType-Typ (Leistungsindikatoren)

Definiert einen global eindeutigen Bezeichnertyp im Registrierungsformat.

``` syntax
<xs:simpleType name="GUIDType">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Muster

Der **einfache GUIDType-Typ** ist ein **xs:string-Objekt,** das durch das folgende Muster eingeschränkt ist:

-   `\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}`

    Der Wert muss ein global eindeutiger Bezeichnertyp im Registrierungsformat sein. Beispiel: {5b2fc63a-8af4-44cb-960c-aefdced908d6}. Verwenden GUIDGen.exe oder UUIDGen.exe, um eine GUID zu erstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 




