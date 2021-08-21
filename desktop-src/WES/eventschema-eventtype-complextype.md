---
title: Komplexer EventType-Typ
description: Definiert den Stammknoten des Ereignisschemas.
ms.assetid: 1ff9299b-71ee-4bb3-8a9a-fb9880dbf577
keywords:
- 'EventType: komplexer EventLog-Typ'
topic_type:
- apiref
api_name:
- EventType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: da5948021c4a2db50776544c38adfa4ddc6e8ce5bcc1285c879ef528dec759e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957900"
---
# <a name="eventtype-complex-type"></a>Komplexer EventType-Typ

Definiert den Stammknoten des Ereignisschemas.

``` syntax
<xs:complexType name="EventType">
    <xs:sequence>
        <xs:element name="System"
            type="SystemPropertiesType"
         />
        <xs:choice>
            <xs:element name="EventData"
                type="EventDataType"
                minOccurs="0"
             />
            <xs:element name="UserData"
                type="UserDataType"
                minOccurs="0"
             />
            <xs:element name="DebugData"
                type="DebugDataType"
                minOccurs="0"
             />
            <xs:element name="BinaryEventData"
                type="hexBinary"
                minOccurs="0"
             />
            <xs:element name="ProcessingErrorData"
                type="ProcessingErrorDataType"
                minOccurs="0"
             />
        </xs:choice>
        <xs:element name="RenderingInfo"
            type="RenderingInfoType"
            minOccurs="0"
         />
        <xs:any
            minOccurs="0"
            maxOccurs="unbounded"
            processContents="lax"
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



| Element                                                                          | type                                                                               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BinaryEventData**](eventschema-binaryeventdata-eventtype-element.md)         | hexBinary                                                                          | Enthält die Ereignisdaten als binäres Blob. Die Ereignisdaten werden als binäres Blob gerendert, wenn die Renderingfunktion die Zum Decodieren des Ereignisses verwendeten Metadaten nicht finden kann.<br/>                                                                                                                                                            |
| [**DebugData**](eventschema-debugdata-eventtype-element.md)                     | [**DebugDataType**](eventschema-debugdatatype-complextype.md)                     | Enthält die Daten, die für Windows WPP-Ereignisse (Software Trace Preprocessor) protokolliert werden können.<br/>                                                                                                                                                                                                                                    |
| [**Eventdata**](eventschema-eventdata-eventtype-element.md)                     | [**EventDataType**](eventschema-eventdatatype-complextype.md)                     | Enthält die Ereignisdaten. Die Reihenfolge der Datenelemente in der Vorlage bestimmt das Layout der Ereignisdaten.<br/>                                                                                                                                                                                                                 |
| [**ProcessingErrorData**](eventschema-processingerrordata-eventtype-element.md) | [**ProcessingErrorDataType**](eventschema-processingerrordatatype-complextype.md) | Enthält Details zu dem Fehler, der beim Rendern des Ereignisses aufgetreten ist. Dies kann auftreten, wenn die Ereignisdaten nicht mit der Ereignisdatendefinition im Manifest übereinstimmen. Die Ereignisdaten sind als binäres Blob enthalten.<br/>                                                                                                         |
| [**RenderingInfo**](eventschema-renderinginfo-eventtype-element.md)             | [**RenderingInfoType**](eventschema-renderingtype-complextype.md)                 | Enthält die gerenderten Meldungszeichenfolgen für das Ereignis (enthält die Meldungszeichenfolge des Ereignisses und die Meldungszeichenfolgen für alle Ereigniseigenschaften wie Ebene, Aufgabe und Opcode). Nur Ereignisse, die mithilfe des [Ereignissammlerdiensts](/windows/desktop/WEC/windows-event-collector) Windows wurden, enthalten diesen Abschnitt.<br/> |
| [**System**](eventschema-system-eventtype-element.md)                           | [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md)       | Enthält Informationen, die den Anbieter und dessen Aktivierung, das Ereignis, den Kanal, in den das Ereignis geschrieben wurde, und Systeminformationen wie prozess- und thread-IDs identifizieren.<br/>                                                                                                                                   |
| [**UserData**](eventschema-userdata-eventtype-element.md)                       | [**UserDataType**](eventschema-userdatatype-complextype.md)                       | Enthält die Ereignisdaten. Der Benutzerdatenabschnitt der Vorlage bestimmt das Layout der Ereignisdaten.<br/>                                                                                                                                                                                                                       |



## <a name="remarks"></a>Hinweise

In der Regel enthält dieser Abschnitt den **Abschnitt EventData** oder **UserData.** Der **Abschnitt EventData** wird verwendet, wenn die Vorlage keinen **UserData-Abschnitt** enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

