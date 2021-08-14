---
title: Komplexer InputTypeListType-Typ
description: Definiert eine Liste von Eingabetypen.
ms.assetid: e6bba894-7c17-411e-92e5-9276728a5e4b
keywords:
- Komplexer InputTypeListType-Typ EventLog
topic_type:
- apiref
api_name:
- InputTypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 156ee19a90cdbb64e742d9876a39741155a3d5172f8da05f38f666cc077fc47c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118343741"
---
# <a name="inputtypelisttype-complex-type"></a>Komplexer InputTypeListType-Typ

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
| [**inType**](eventmanifestschema-intype-inputtypelisttype-element.md) | [**InputType**](eventmanifestschema-inputtype-complextype.md) | Definiert einen Eingabetyp.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





