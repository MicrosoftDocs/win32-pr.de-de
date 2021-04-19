---
title: Guidtype Simple Type (eventmanifest-Schema)
description: Definiert einen Globally Unique Identifier Typ im Registrierungs Format. | Guidtype Simple Type (eventmanifest-Schema)
ms.assetid: c35fa54b-5a2e-46de-a1c7-fc408b00ee68
keywords:
- Guidtype Simple Type EventLog
topic_type:
- apiref
api_name:
- GUIDType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 474715cf4e9c11536ca227ecdb5609b13be7e222
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106373476"
---
# <a name="guidtype-simple-type-eventmanifest-schema"></a>Guidtype Simple Type (eventmanifest-Schema)

Definiert einen Globally Unique Identifier Typ im Registrierungs Format.

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

Der einfache **guidtype** -Typ ist eine Zeichenfolge, die durch das folgende Muster eingeschränkt ist:

-   `\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}`

    Der Wert muss ein Globally Unique Identifier Typ im Registrierungs Format sein. Beispiel: {5b2fc63a-8af4-44cb-960c-aefdced908d6}. Verwenden Sie GUIDGen.exe oder UUIDGen.exe, um eine GUID zu erstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





