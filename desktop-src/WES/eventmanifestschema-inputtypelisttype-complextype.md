---
title: Komplexer inputtypelisttype-Typ
description: Definiert eine Liste von Eingabetypen.
ms.assetid: e6bba894-7c17-411e-92e5-9276728a5e4b
keywords:
- Inputtypelisttype komplexer Typ EventLog
topic_type:
- apiref
api_name:
- InputTypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e68b4077bfb08b69a31f18d81aa55d0b5ac54f78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106035"
---
# <a name="inputtypelisttype-complex-type"></a>Komplexer inputtypelisttype-Typ

Definiert eine Liste von Eingabetypen.

``` syntax
<xs:complexType name="InputTypeListType">
    <xs:sequence>
        <xs:element name="inType"
            type="InputType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                | type                                                           | BESCHREIBUNG                       |
|------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------|
| [**intype**](eventmanifestschema-intype-inputtypelisttype-element.md) | [**InputType**](eventmanifestschema-inputtype-complextype.md) | Definiert einen Eingabetyp.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





