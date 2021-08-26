---
title: Komplexer ChannelLoggingType-Typ
description: Definiert die Eigenschaften der Protokolldatei, die den Kanal sichern, z. B. die Kapazität und ob sie sequenziell oder kreisförmig ist. | Komplexer ChannelLoggingType-Typ
ms.assetid: 58da75dd-d303-4a57-8c9b-5fde575c3cbb
keywords:
- Komplexer ChannelLoggingType-Typ EventLog
topic_type:
- apiref
api_name:
- ChannelLoggingType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e696837b1132a0b82ad428e7404892ae73de88e4435325d988b7936b3a6ba534
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032280"
---
# <a name="channelloggingtype-complex-type"></a>Komplexer ChannelLoggingType-Typ

Definiert die Eigenschaften der Protokolldatei, die den Kanal sichern, z. B. die Kapazität und ob sie sequenziell oder kreisförmig ist.

``` syntax
<xs:complexType name="ChannelLoggingType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="autoBackup"
            type="boolean"
            minOccurs="0"
         />
        <xs:element name="retention"
            type="boolean"
            default="0"
            minOccurs="0"
         />
        <xs:element name="maxSize"
            type="UInt64Type"
            default="1048576"
            minOccurs="0"
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



| Element                                                                         | type                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Autobackup**](eventmanifestschema-autobackup-channelloggingtype-element.md) | boolean                                                           | Bestimmt, ob eine neue Protokolldatei erstellt werden soll, wenn die aktuelle Protokolldatei ihre maximale Größe erreicht. Legen Sie auf **TRUE fest,** um an fordern, dass der Dienst eine neue Datei erstellt, wenn die Protokolldatei ihre maximale Größe erreicht. andernfalls **FALSE.** Sie können [**autoBackup nur dann auf**](eventmanifestschema-autobackup-channelloggingtype-element.md) TRUE **festlegen,** [**wenn die Aufbewahrung**](eventmanifestschema-retention-channelloggingtype-element.md) auf TRUE **festgelegt ist.** Der Standardwert ist **FALSE**.<br/> Es gibt keine Beschränkung für die Anzahl der Sicherungsdateien, die der Dienst erstellen kann (beschränkt nur durch den verfügbaren Speicherplatz). Die Namen der Sicherungsdateien haben das Formular Archive-*channelName* - *timestamp*.evtx und befinden sich im Ordner %windir% \\ System32 \\ winevt \\ Logs.<br/> |
| [**Maxsize**](eventmanifestschema-maxsize-channelloggingtype-element.md)       | [**UInt64Type**](eventmanifestschema-hexint64type-simpletype.md) | Die maximale Größe der Protokolldatei in Bytes. Der Standardwert (und der Mindestwert) beträgt 1 MB. Wenn die physische Protokollgröße kleiner als die konfigurierte maximale Größe ist und im Protokoll zusätzlicher Speicherplatz zum Speichern von Ereignissen erforderlich ist, weist der Dienst einen weiteren Speicherplatzblock zu, auch wenn die resultierende physische Größe des Protokolls größer als die konfigurierte maximale Größe ist. Der Dienst ordnet Blöcke von 1 MB zu, sodass die physische Größe bis zu 1 MB größer als die konfigurierte maximale Größe werden kann. <br/>                                                                                                                                                                                                                                                      |
| [**Speicherung**](eventmanifestschema-retention-channelloggingtype-element.md)   | boolean                                                           | Bestimmt, ob die Protokolldatei eine sequenzielle oder zirkuläre Protokolldatei ist. Legen Sie **für eine sequenzielle** Protokolldatei auf TRUE und **für** eine zirkuläre Protokolldatei auf FALSE fest. Der Standardwert ist **false für** die Kanaltypen Admin und Operational und **true** für Analyse- und Debugkanaltypen.<br/> Um ein zirkuläres Protokoll abfragen zu können, müssen Sie zuerst den Kanal deaktivieren.<br/>                                                                                                                                                                                                                                                                                                                                                                                                  |



## <a name="remarks"></a>Hinweise

Sie können das **maxSize-Attribut** für jeden Kanaltyp angeben.

Sie können das **AutoBackup-Attribut nur** für die Kanaltypen Admin und Operational angeben.

Sie können das **Aufbewahrungsattribut** für Administrator- und Betriebskanaltypen auf FALSE (zirkuläre Protokollierung) festlegen. Sie können  das Aufbewahrungsattribut für Analyse- und Debugkanaltypen auf FALSE (zirkuläre Protokollierung) festlegen. Zum Anzeigen der Ereignisse im Windows Ereignisanzeige müssen Sie jedoch zuerst den Kanal deaktivieren. Beachten Sie, dass die Ereignisse aus dem Kanal entfernt werden, wenn Sie den Kanal erneut aktivieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





