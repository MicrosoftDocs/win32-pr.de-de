---
description: Definiert einen Globally Unique Identifier Typ im Registrierungs Format.
ms.assetid: 2be73c57-b6b6-46ab-93e1-d70f8655c30e
title: Guidtype Simple Type (Leistungsindikatoren)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 758509a564c26db493fa2e9ed971aba71878cdbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865099"
---
# <a name="guidtype-simple-type-performance-counters"></a>Guidtype Simple Type (Leistungsindikatoren)

Definiert einen Globally Unique Identifier Typ im Registrierungs Format.

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

Der einfache **guidtype** -Typ ist eine **xs: String** , die durch das folgende Muster eingeschränkt ist:

-   `\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}`

    Der Wert muss ein Globally Unique Identifier Typ im Registrierungs Format sein. Beispiel: {5b2fc63a-8af4-44cb-960c-aefdced908d6}. Verwenden Sie GUIDGen.exe oder UUIDGen.exe, um eine GUID zu erstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 




