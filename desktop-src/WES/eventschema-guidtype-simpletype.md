---
title: Einfacher GUIDType-Typ (Ereignisschema)
description: Definiert einen global eindeutigen Bezeichnertyp im Registrierungsformat. | Einfacher GUIDType-Typ (Ereignisschema)
ms.assetid: dbc305ef-6f07-4a70-9013-b89ccec889ea
keywords:
- GUIDType simple type EventLog
topic_type:
- apiref
api_name:
- GUIDType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a2fb7c0cd759b8b58b0db801819ed365f5b25fdb5abdcf886430e8bb2582cbde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750622"
---
# <a name="guidtype-simple-type-event-schema"></a>Einfacher GUIDType-Typ (Ereignisschema)

Definiert einen global eindeutigen Bezeichnertyp im Registrierungsformat.

``` syntax
<xs:simpleType name="GUIDType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Muster

Der einfache **GUIDType-Typ** ist eine Zeichenfolge, die durch das folgende Muster eingeschränkt ist:

-   `\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}`

    Der Wert muss ein global eindeutiger Bezeichnertyp im Registrierungsformat sein. Beispiel: {5b2fc63a-8af4-44cb-960c-aefdced908d6}. Verwenden Sie GUIDGen.exe oder UUIDGen.exe, um eine GUID zu erstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





