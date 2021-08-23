---
title: attachmentsType Complex Type
description: Definiert die Elemente, die verwendet werden, um eine Anlage anzugeben, die mit einer E-Mail gesendet wird.
ms.assetid: b13d9346-a28d-4362-bcfc-dc11869fb8eb
keywords:
- attachmentsType complex type Taskplaner
topic_type:
- apiref
api_name:
- attachmentsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0d98b266fcb15fbd47fbb2a5bb792b95e4fb765a48b2fbcf6c1185aad9475df1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772390"
---
# <a name="attachmentstype-complex-type"></a>attachmentsType Complex Type

Definiert die Elemente, die verwendet werden, um eine Anlage anzugeben, die mit einer E-Mail gesendet wird.

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



| Element                                                          | type                                                                    | Beschreibung                                                                                |
|------------------------------------------------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**Datei**](taskschedulerschema-file-attachmentstype-element.md) | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Gibt den Pfad zu einer Datei an, die als Anlage in einer E-Mail gesendet wird.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





