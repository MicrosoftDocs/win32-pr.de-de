---
title: Einfacher GUIDType-Typ (EventManifest-Schema)
description: Definiert einen global eindeutigen Bezeichnertyp im Registrierungsformat. | Einfacher GUIDType-Typ (EventManifest-Schema)
ms.assetid: c35fa54b-5a2e-46de-a1c7-fc408b00ee68
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
ms.openlocfilehash: 0ff7d5b0b65e7c434b6281098531e4eae5e76cf1565b21f6b1a3ffbca46af37b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118343716"
---
# <a name="guidtype-simple-type-eventmanifest-schema"></a>Einfacher GUIDType-Typ (EventManifest-Schema)

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



 

 





