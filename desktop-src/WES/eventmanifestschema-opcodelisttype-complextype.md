---
title: Komplexer OpcodeListType-Typ
description: Definiert eine Liste von Opcodes, die verwendet werden, um die Vorgänge einer Komponente der Anwendung zu identifizieren.
ms.assetid: 0cbca036-b32e-4fc4-96ee-1dd5bee019bf
keywords:
- Komplexer OpcodeListType-Typ EventLog
topic_type:
- apiref
api_name:
- OpcodeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c44a2c2fa38957f302dfe3861a89f57dbe51d44ca737268a8988f8c138be8b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767300"
---
# <a name="opcodelisttype-complex-type"></a>Komplexer OpcodeListType-Typ

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



| Element                                                             | Typ                                                             | Beschreibung                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------|
| [**Opcode**](eventmanifestschema-opcode-opcodelisttype-element.md) | [**OpcodeType**](eventmanifestschema-opcodetype-complextype.md) | Definiert einen Vorgang innerhalb einer Komponente der Anwendung.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





