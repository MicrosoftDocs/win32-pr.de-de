---
title: Komplexer opcodelisttype-Typ
description: Definiert eine Liste von Opcodes, die verwendet werden, um die Vorgänge einer Komponente der Anwendung zu identifizieren.
ms.assetid: 0cbca036-b32e-4fc4-96ee-1dd5bee019bf
keywords:
- Opcodelisttype komplexer Typ EventLog
topic_type:
- apiref
api_name:
- OpcodeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dce0942ef0268f50b25987a6be0fd4fffeebd614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476527"
---
# <a name="opcodelisttype-complex-type"></a>Komplexer opcodelisttype-Typ

Definiert eine Liste von Opcodes, die verwendet werden, um die Vorgänge einer Komponente der Anwendung zu identifizieren.

``` syntax
<xs:complexType name="OpcodeListType">
    <xs:sequence>
        <xs:element name="opcode"
            type="OpcodeType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                             | type                                                             | BESCHREIBUNG                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------|
| [**OpCode**](eventmanifestschema-opcode-opcodelisttype-element.md) | [**OpCodeType**](eventmanifestschema-opcodetype-complextype.md) | Definiert einen Vorgang innerhalb einer Komponente der Anwendung.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





