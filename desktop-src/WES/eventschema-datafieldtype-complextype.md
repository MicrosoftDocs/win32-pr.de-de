---
title: Komplexer Datentyp "DataType" (Windows Ereignisprotokoll)
description: Definiert ein Datenelement.
ms.assetid: f3b7de63-1ac1-429d-9e36-1f13c26c9618
keywords:
- Komplexer DataType-Typ EventLog
topic_type:
- apiref
api_name:
- DataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ba1fcbf217b16fb675a7a4eca00c8faa201737c07eea35a809f85617e96e9445
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119620280"
---
# <a name="datatype-complex-type"></a>Komplexer Datentyp "DataType"

Definiert ein Datenelement.

``` syntax
<xs:complexType name="DataType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="Name"
                type="string"
                use="optional"
             />
            <xs:attribute name="Type"
                type="QName"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Attributes



| Name | type   | Beschreibung                                                                                                                                                              |
|------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Name | Zeichenfolge | Der Name eines Datenelements, das in der Vorlage definiert wurde (siehe komplexer [**TemplateItemType-Typ).**](eventmanifestschema-templateitemtype-complextype.md)<br/> |
| type | QName  | Wird nicht verwendet.<br/>                                                                                                                                                     |



## <a name="remarks"></a>Hinweise

Das Datenelement kann ein Datenelement der obersten Ebene oder ein Datenelement in einer -Struktur sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





