---
title: Komplexer ProcessingErrorDataType-Typ
description: Definiert einen Fehler, der beim Rendern der Ereignisdaten für das Ereignis aufgetreten ist.
ms.assetid: fd1cc78c-1da5-43c5-8c4b-8abe7e1dc1e1
keywords:
- Komplexer ProcessingErrorDataType-Typ EventLog
topic_type:
- apiref
api_name:
- ProcessingErrorDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ee34e566bafa72812303fcb1f41b664a45aa77772e6ee818b9cb79bc94cbb51
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904525"
---
# <a name="processingerrordatatype-complex-type"></a>Komplexer ProcessingErrorDataType-Typ

Definiert einen Fehler, der beim Rendern der Ereignisdaten für das Ereignis aufgetreten ist. Dies kann auftreten, wenn die Ereignisdaten nicht mit der Definition der Ereignisdatenvorlage im Manifest übereinstimmen.

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
| [**DataItemName**](eventschema-dataitemname-processingerrordatatype-element.md) | Zeichenfolge      | Der Name des Ereignisdatenelements, das den Fehler verursacht hat.<br/>                    |
| [**Errorcode**](eventschema-errorcode-processingerrordatatype-element.md)       | unsignedInt | Der Fehlercode des Fehlers, der beim Rendern der Ereignisdaten aufgetreten ist.<br/> |
| [**EventPayload**](eventschema-eventpayload-processingerrordatatype-element.md) | hexBinary   | Ein binäres Blob, das die gesamten Ereignisdaten enthält.<br/>                        |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





