---
title: Komplexer DataType-Typ (Windows-Ereignisprotokoll)
description: Definiert ein Datenelement.
ms.assetid: f3b7de63-1ac1-429d-9e36-1f13c26c9618
keywords:
- DataType Complex-Typ EventLog
topic_type:
- apiref
api_name:
- DataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d3ac6e545cbe8567bbe041568c442f762743ad0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341057"
---
# <a name="datatype-complex-type"></a>Komplexer DataType-Typ

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



| Name | type   | BESCHREIBUNG                                                                                                                                                              |
|------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Name | Zeichenfolge | Der Name eines Datenelements, das in der Vorlage definiert wurde (siehe den komplexen Typ " [**templateitemtype**](eventmanifestschema-templateitemtype-complextype.md) ").<br/> |
| type | QName  | Nicht verwendet.<br/>                                                                                                                                                     |



## <a name="remarks"></a>Bemerkungen

Das Datenelement kann ein Datenelement der obersten Ebene oder ein Datenelement in einer Struktur sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





