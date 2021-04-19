---
title: komplexer attachmentstype-Typ
description: Definiert die Elemente, mit denen eine mit einer e-Mail-Nachricht gesendete Anlage angegeben wird.
ms.assetid: b13d9346-a28d-4362-bcfc-dc11869fb8eb
keywords:
- komplexer attachmentstype-Typ Taskplaner
topic_type:
- apiref
api_name:
- attachmentsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce5bc25b74221112b487be58a729bffa47b8688d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344488"
---
# <a name="attachmentstype-complex-type"></a>komplexer attachmentstype-Typ

Definiert die Elemente, mit denen eine mit einer e-Mail-Nachricht gesendete Anlage angegeben wird.

``` syntax
<xs:complexType name="attachmentsType">
    <xs:sequence>
        <xs:element name="File"
            type="nonEmptyString"
            minOccurs="0"
            maxOccurs="8"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                          | type                                                                    | BESCHREIBUNG                                                                                |
|------------------------------------------------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**Datei**](taskschedulerschema-file-attachmentstype-element.md) | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Gibt den Pfad zu einer Datei an, die als Anlage in einer e-Mail-Nachricht gesendet wird.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





