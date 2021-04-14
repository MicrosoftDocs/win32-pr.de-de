---
title: Komplexer EventType-Typ
description: Definiert den Stamm Knoten des Ereignis Schemas.
ms.assetid: 1ff9299b-71ee-4bb3-8a9a-fb9880dbf577
keywords:
- EventType-Ereignisprotokoll (komplexer Typ)
topic_type:
- apiref
api_name:
- EventType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1103570b6c1d9f51a8cbe8fe5628460690fb32cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391586"
---
# <a name="eventtype-complex-type"></a>Komplexer EventType-Typ

Definiert den Stamm Knoten des Ereignis Schemas.

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
| [**Binaryeventdata**](eventschema-binaryeventdata-eventtype-element.md)         | hexBinary                                                                          | Enthält die Ereignisdaten als binäres Blob. Die Ereignisdaten werden als binäres Blob gerendert, wenn die Renderingfunktion die zum Decodieren des Ereignisses verwendeten Metadaten nicht finden kann.<br/>                                                                                                                                                            |
| [**Debug-Daten**](eventschema-debugdata-eventtype-element.md)                     | [**Debug DataType**](eventschema-debugdatatype-complextype.md)                     | Enthält die Daten, die für Windows-Software-Ablaufverfolgungs-präprozessorereignisse (WPP) protokolliert werden können.<br/>                                                                                                                                                                                                                                    |
| [**EVENTDATA**](eventschema-eventdata-eventtype-element.md)                     | [**Eventdatatype**](eventschema-eventdatatype-complextype.md)                     | Enthält die Ereignisdaten. Die Reihenfolge der Datenelemente in der Vorlage bestimmt das Layout der Ereignisdaten.<br/>                                                                                                                                                                                                                 |
| [**Processingerrordata**](eventschema-processingerrordata-eventtype-element.md) | [**Processingerrordatatype**](eventschema-processingerrordatatype-complextype.md) | Enthält Details zu dem Fehler, der beim Versuch aufgetreten ist, das Ereignis zu erzeugen. Dies kann vorkommen, wenn die Ereignisdaten nicht mit der Ereignisdaten Definition im Manifest identisch sind. Die Ereignisdaten sind als binäres Blob enthalten.<br/>                                                                                                         |
| [**Renderinginfo**](eventschema-renderinginfo-eventtype-element.md)             | [**Renderinginfotype**](eventschema-renderingtype-complextype.md)                 | Enthält die gerenderten Meldungs Zeichenfolgen für das Ereignis (einschließlich der Meldungs Zeichenfolge des Ereignisses und der Meldungs Zeichenfolgen für alle Eigenschaften des Ereignisses, z. b. Ebene, Aufgabe und OpCode). Dieser Abschnitt enthält nur Ereignisse, die mit dem [Windows-Ereignis](/windows/desktop/WEC/windows-event-collector) Sammlungs Dienst erfasst wurden.<br/> |
| [**System**](eventschema-system-eventtype-element.md)                           | [**Systempropertiestype**](eventschema-systempropertiestype-complextype.md)       | Enthält Informationen, die den Anbieter und die Art der Aktivierung, das Ereignis, den Kanal, in den das Ereignis geschrieben wurde, und Systeminformationen, wie z. b. den Prozess und die Thread-IDs, identifiziert.<br/>                                                                                                                                   |
| [**UserData**](eventschema-userdata-eventtype-element.md)                       | [**Userdatatype**](eventschema-userdatatype-complextype.md)                       | Enthält die Ereignisdaten. Der Abschnitt "Benutzerdaten" der Vorlage bestimmt das Layout der Ereignisdaten.<br/>                                                                                                                                                                                                                       |



## <a name="remarks"></a>Bemerkungen

In der Regel enthält dieser Abschnitt den Abschnitt " **EventData** " oder " **UserData** ". Der **EventData** -Abschnitt wird verwendet, wenn die Vorlage keinen **UserData** -Abschnitt enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

