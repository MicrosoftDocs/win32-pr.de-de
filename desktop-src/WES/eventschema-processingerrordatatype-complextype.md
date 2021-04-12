---
title: Komplexer processingerrordatatype-Typ
description: Definiert einen Fehler, der beim Rendern der Ereignisdaten für das Ereignis aufgetreten ist.
ms.assetid: fd1cc78c-1da5-43c5-8c4b-8abe7e1dc1e1
keywords:
- Ereignisprotokoll des komplexen processingerrordatatype-Typs
topic_type:
- apiref
api_name:
- ProcessingErrorDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ffcc9d2beed4050a8eed34925f30e52f67d129b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105177"
---
# <a name="processingerrordatatype-complex-type"></a>Komplexer processingerrordatatype-Typ

Definiert einen Fehler, der beim Rendern der Ereignisdaten für das Ereignis aufgetreten ist. Dies kann vorkommen, wenn die Ereignisdaten nicht mit der Definition der Ereignisdaten Vorlage im Manifest identisch sind.

``` syntax
<xs:complexType name="ProcessingErrorDataType">
    <xs:sequence>
        <xs:element name="ErrorCode"
            type="unsignedInt"
         />
        <xs:element name="DataItemName"
            type="string"
         />
        <xs:element name="EventPayload"
            type="hexBinary"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                          | type        | BESCHREIBUNG                                                                          |
|----------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------------------|
| [**DataItemName**](eventschema-dataitemname-processingerrordatatype-element.md) | Zeichenfolge      | Der Name des Ereignisdaten Elements, das den Fehler verursacht hat.<br/>                    |
| [**ErrorCode**](eventschema-errorcode-processingerrordatatype-element.md)       | unsignedInt | Der Fehlercode des Fehlers, der beim Rendern der Ereignisdaten aufgetreten ist.<br/> |
| [**EventPayload**](eventschema-eventpayload-processingerrordatatype-element.md) | hexBinary   | Ein binäres Blob, das die gesamten Ereignisdaten enthält.<br/>                        |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





