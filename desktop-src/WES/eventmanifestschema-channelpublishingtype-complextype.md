---
title: Komplexer channelpublishingtype-Typ
description: Definiert die Protokollierungs Eigenschaften für die Sitzung, die vom Kanal verwendet wird. | Komplexer channelpublishingtype-Typ
ms.assetid: 4b3980f4-8652-4070-97c0-99cd1a9fc85a
keywords:
- Ereignisprotokoll des komplexen channelpublishingtype-Typs
topic_type:
- apiref
api_name:
- ChannelPublishingType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af84685f25705f6f8c54a85b9befb6df791593ed
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106350631"
---
# <a name="channelpublishingtype-complex-type"></a>Komplexer channelpublishingtype-Typ

Definiert die Protokollierungs Eigenschaften für die Sitzung, die vom Kanal verwendet wird.

``` syntax
<xs:complexType name="ChannelPublishingType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="level"
            type="UInt8Type"
            default="0"
            minOccurs="0"
         />
        <xs:element name="keywords"
            type="UInt64Type"
            default="0"
            minOccurs="0"
         />
        <xs:element name="controlGuid"
            type="GUIDType"
            minOccurs="0"
         />
        <xs:element name="bufferSize"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="minBuffers"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="fileMax"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="maxBuffers"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="latency"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="clockType"
            default="SystemTime"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="xs:string"
                >
                    <xs:enumeration
                        value="SystemTime"
                     />
                    <xs:enumeration
                        value="QPC"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="sidType"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="xs:string"
                >
                    <xs:enumeration
                        value="None"
                     />
                    <xs:enumeration
                        value="Publishing"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
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



| Element                                                                              | type                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**bufferSize**](eventmanifestschema-buffersize-channelpublishingtype-element.md)   | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | Die Größe des Arbeitsspeichers in Kilobytes, die für jeden Puffer belegt werden soll. Wenn Sie eine relativ niedrige Ereignisrate erwarten, sollte die Größe des Puffers auf die Seitengröße des Arbeitsspeichers festgelegt werden. Wenn erwartet wird, dass die Ereignisrate relativ hoch ist, sollten Sie eine größere Puffergröße angeben und die maximale Anzahl von Puffern erhöhen.<br/> Die Puffergröße wirkt sich auf die Rate aus, mit der Puffer aufgefüllt werden und geleert werden müssen. Obwohl eine kleine Puffergröße weniger Arbeitsspeicher erfordert, erhöht sich die Rate, mit der Puffer geleert werden müssen.<br/> Die Standardpuffergröße für analytische und Debugkanäle beträgt 4 KB, und für admin und Operational beträgt der Wert 64 KB.<br/>                                                                                                                |
| [**clocktype**](eventmanifestschema-clocktype-channelpublishingtype-element.md)     |                                                                   | Die zu verwendende Takt Auflösung, wenn der Zeitstempel für jedes Ereignis protokolliert wird. Sie können SYSTEMTIME oder QPC angeben. SYSTEMTIME bietet einen Zeitstempel mit niedriger Auflösung (10 Millisekunden), ist aber vergleichsweise kostengünstiger. Der Standardwert ist SYSTEMTIME. <br/> Der Query Performance Counter (QPC) bietet einen Zeitstempel mit hoher Auflösung (100 nanoseconds), ist aber vergleichsweise kostengünstiger. Wenn Sie über hohe Ereignis Raten verfügen oder wenn der Consumer Ereignisse aus unterschiedlichen Puffern zusammenfasst, sollten Sie QPC durchführen.<br/>                                                                                                                                                                                                                                 |
| [**controlguid**](eventmanifestschema-controlguid-channelpublishingtype-element.md) | [**Guidtype**](eventmanifestschema-guidtype-simpletype.md)       | Gibt die Sitzungs-GUID für eine ETW-Sitzung an, die WPP-Ereignisse enthält. Diese Einstellung ist nur für Kanäle vom Typ Debug zulässig. Diese Kanäle können nicht vollständig aktiviert werden, wenn Schlüsselwörter auf NULL (0x0000000000000000) festgelegt sind. Sie müssen mit Schlüsselwörtern aktiviert werden, die auf 0xFFFFFFFFFFFFFFFF festgelegt sind.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **filemax**                                                                          | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | Die maximale Anzahl von Wiederholungen, die der Dienst beim Aktivieren des Kanals eine neue Protokolldatei erstellen soll (schließt den Neustart des Computers ein). Wenn der Wert 0 oder 1 ist, überschreibt der Dienst die Protokolldatei jedes Mal, wenn der Kanal aktiviert ist und die vorherigen Ereignisse verloren gehen. Wenn der Wert größer als 1 ist, erstellt der Dienst jedes Mal, wenn der Kanal aktiviert ist, eine neue Protokolldatei, um die Ereignisse beizubehalten. Der Standardwert ist 1, und der Höchstwert, den Sie angeben können, ist 16.<br/> Der Dienst fügt eine dreistellige Dezimalzahl zwischen 0 und filemax 1 an jeden Dateinamen an. Beispielsweise *filename*. ETL.xxx, wobei xxx die dreistellige Dezimalzahl ist. Die Dateien befinden sich in% windir% \\ system32 \\ winevt \\ Logs.<br/> |
| [**Keywords**](eventmanifestschema-keywords-channelpublishingtype-element.md)       | [**UInt64Type**](eventmanifestschema-hexint64type-simpletype.md) | Eine Bitmaske, die die Kategorie der Ereignisse bestimmt, die in den Kanal geschrieben werden. Wenn der Wert des Attributs " **Keywords** " den Wert 0 hat, werden alle Ereignisse, die der Anbieter schreibt, in den Kanal geschrieben. Andernfalls werden nur Ereignisse, die ein Schlüsselwort definiert haben, das in den **Schlüsselwörtern** Bitmaske enthalten ist, in den Channel geschrieben. Die Standardeinstellung ist 0.<br/> Bei debugkanälen, bei denen das controlguid-Attribut festgelegt ist, muss das **Keywords** -Attribut auf 0xFFFFFFFFFFFFFFFF festgelegt werden.<br/> Die Sitzung übergibt den Schlüsselwort Wert an den Anbieter, wenn er den Anbieter aktiviert.<br/>                                                                                                                                                                            |
| [**Schleifen**](eventmanifestschema-latency-channelpublishingtype-element.md)         | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | Die Wartezeit in Millisekunden, bevor die Puffer geleert werden. Bei Null leert etw die Puffer, sobald Sie voll sind. Bei einem Wert ungleich NULL leert etw alle Puffer, die Ereignisse auf Grundlage des Werts enthalten, auch wenn der Puffer nicht voll ist. Normalerweise möchten Sie Puffer nur dann leeren, wenn Sie voll sind. Wenn Sie die Puffer bereinigen, können Sie die Dateigröße der Protokolldatei mit dem nicht gefüllten Pufferbereich vergrößern. Der Standardwert beträgt 1 Sekunde für Administrator-und Betriebs Protokolle und 5 Sekunden für analytische und Debugprotokolle.<br/>                                                                                                                                                                                                                               |
| [**Level**](eventmanifestschema-level-channelpublishingtype-element.md)             | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | Der Schweregrad der Ereignisse, die in den Kanal geschrieben werden sollen. Der Dienst schreibt Ereignisse in den Kanal, der einen Ebenenwert hat, der kleiner oder gleich dem angegebenen Wert ist. Der Standardwert ist 0 (null), was bedeutet, dass Ereignisse mit beliebigen Ebenen protokolliert werden.<br/> Die Sitzung übergibt den Wert für die Ebene an den Anbieter, wenn Sie den Anbieter aktiviert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**MaxBuffers**](eventmanifestschema-maxbuffers-channelpublishingtype-element.md)   | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | Die maximale Anzahl von Puffern, die für die Sitzung zuzuordnen sind. In der Regel ist dieser Wert die minimale Anzahl von Puffern plus 20. Dieser Wert muss größer oder gleich dem für minbuffers angegebenen Wert sein.<br/> Der Standardwert für die maximale Anzahl von Puffern für analytische und Debugkanäle beträgt 10 KB. für admin und Operational beträgt der Wert 64 KB.<br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| [**minbuffers**](eventmanifestschema-minbuffers-channelpublishingtype-element.md)   | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | Die Mindestanzahl an Puffern, die für die Sitzung zuzuordnen sind. Der Standardwert ist 0.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**SIDType**](eventmanifestschema-sidtype-channelpublishingtype-element.md)         |                                                                   | Bestimmt, ob eine Sicherheits-ID (SID) des Prinzipals mit jedem Ereignis eingeschlossen werden soll, das in den Kanal geschrieben wird. Wenn Sie die SID mit dem Ereignis einschließen möchten, legen Sie dieses Attribut auf "Publishing" fest. Die SID wird auf der Grundlage der Thread Identität festgelegt, wenn das Ereignis geschrieben wird. Wenn Sie die SID nicht mit dem Ereignis einschließen möchten, legen Sie dieses Attribut auf "None" fest. Der Standardwert ist "Publishing".<br/>                                                                                                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a>Bemerkungen

Sie können diese Veröffentlichungsinformationen für analytische und debugkanaltypen oder für jeden Kanal angeben, der die benutzerdefinierte Isolation angibt.

Obwohl Sie Ebenen und Schlüsselwörter angeben können, sollten Sie berücksichtigen, dass es sich hierbei um die einzigen Ereignisse handelt, die Sie vom Anbieter für diesen Kanal erhalten.

Wenn ein Puffer voll ist, leert etw den Puffer in die Protokolldatei. Wenn die Puffer schneller ausgefüllt werden, als Sie geleert werden können, werden neue Puffer zugewiesen und dem Pufferpool der Sitzung hinzugefügt, bis die maximale Anzahl angegeben wird. Über diesen Grenzwert hinaus verwirft die Sitzung eingehende Ereignisse, bis ein Puffer verfügbar wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





