---
title: komplexer headerfieldtype-Typ
description: Definiert die Elemente, die zum Erstellen eines Header Felds in einer e-Mail-Nachricht verwendet werden.
ms.assetid: 66036875-1116-46eb-b2f5-8c8ad8373ab1
keywords:
- komplexer headerfieldtype-Typ Taskplaner
topic_type:
- apiref
api_name:
- headerFieldType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ddbc0ae22c6baf3fd288cbe2ead19dac506afee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342198"
---
# <a name="headerfieldtype-complex-type"></a>komplexer headerfieldtype-Typ

Definiert die Elemente, die zum Erstellen eines Header Felds in einer e-Mail-Nachricht verwendet werden.

``` syntax
<xs:complexType name="headerFieldType">
    <xs:all>
        <xs:element name="Name"
            type="nonEmptyString"
         />
        <xs:element name="Value"
            type="string"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                            | type                                                                    | BESCHREIBUNG                                                            |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**Name**](taskschedulerschema-name-headerfieldtype-element.md)   | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Gibt den Namen des Header Felds in einer e-Mail-Nachricht an.<br/> |
| [**Wert**](taskschedulerschema-value-headerfieldtype-element.md) | **string**                                                              | Gibt den Wert eines Header Felds in einer e-Mail-Nachricht an.<br/>  |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





