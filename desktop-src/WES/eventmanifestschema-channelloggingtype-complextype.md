---
title: Komplexer channelloggingtype-Typ
description: Definiert die Eigenschaften der Protokolldatei, die den Kanal sichert, z. b. die Kapazität und ob Sie sequenziell oder zirkulär ist. | Komplexer channelloggingtype-Typ
ms.assetid: 58da75dd-d303-4a57-8c9b-5fde575c3cbb
keywords:
- Ereignisprotokoll für komplexen channelloggingtype-Typ
topic_type:
- apiref
api_name:
- ChannelLoggingType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4cfaf6dfa225799befcd0c7fb068c0f779ea33eb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104132269"
---
# <a name="channelloggingtype-complex-type"></a>Komplexer channelloggingtype-Typ

Definiert die Eigenschaften der Protokolldatei, die den Kanal sichert, z. b. die Kapazität und ob Sie sequenziell oder zirkulär ist.

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
| [**Sicherung**](eventmanifestschema-autobackup-channelloggingtype-element.md) | boolean                                                           | Bestimmt, ob eine neue Protokolldatei erstellt wird, wenn die aktuelle Protokolldatei die maximale Größe erreicht. Legen Sie diese Einstellung auf **true** fest, um anzufordern, dass der Dienst eine neue Datei erstellt, wenn die Protokolldatei die maximale Größe erreicht. andernfalls **false**. Sie können die [**Automatische Sicherung**](eventmanifestschema-autobackup-channelloggingtype-element.md) nur auf **true** festlegen, wenn die [**Beibehaltung**](eventmanifestschema-retention-channelloggingtype-element.md) auf **true** festgelegt ist. Der Standardwert ist **FALSE**.<br/> Es gibt keine Beschränkung für die Anzahl der Sicherungsdateien, die vom Dienst erstellt werden können (nur durch den verfügbaren Speicherplatz beschränkt). Die Sicherungs Dateinamen weisen die Form Archive-*ChannelName* - *Zeitstempel*. evtx auf und befinden sich im Ordner% windir% \\ system32 \\ winevt \\ Logs.<br/> |
| [**MaxSize**](eventmanifestschema-maxsize-channelloggingtype-element.md)       | [**UInt64Type**](eventmanifestschema-hexint64type-simpletype.md) | Die maximale Größe der Protokolldatei in Bytes. Der Standardwert (und der minimale Wert) ist 1 MB. Wenn die physische Protokoll Größe kleiner ist als die konfigurierte maximale Größe, und im Protokoll ist zusätzlicher Speicherplatz erforderlich, um Ereignisse zu speichern, weist der Dienst einen weiteren Speicherblock zu, auch wenn die resultierende physische Größe des Protokolls größer als die konfigurierte maximale Größe ist. Der Dienst ordnet Blöcke von 1 MB zu, sodass die physische Größe auf bis zu 1 MB größer als die konfigurierte maximale Größe anwachsen kann. <br/>                                                                                                                                                                                                                                                      |
| [**zurück**](eventmanifestschema-retention-channelloggingtype-element.md)   | boolean                                                           | Bestimmt, ob die Protokolldatei eine sequenzielle oder zirkuläre Protokolldatei ist. Legen Sie für eine sequenzielle Protokolldatei auf **true** und **false** für eine zirkuläre Protokolldatei fest. Der Standardwert lautet " **false** " für Administrator-und Betriebskanal Typen und für analytische und debugkanaltypen " **true** "<br/> Zum Abfragen eines zirkulären Protokolls müssen Sie zunächst den Kanal deaktivieren.<br/>                                                                                                                                                                                                                                                                                                                                                                                                  |



## <a name="remarks"></a>Bemerkungen

Sie können das **MaxSize** -Attribut für einen beliebigen Kanaltyp angeben.

Sie können das Attribut für die **Automatische Sicherung** nur für die Typen "admin" und "Operational Channel" angeben.

Sie können das **Beibehaltungs** Attribut auf "false" (zirkuläre Protokollierung) für Administrator-und Betriebskanal Typen festlegen. Sie können das **Beibehaltungs** Attribut auf "false" (zirkuläre Protokollierung) für analytische und debugkanaltypen festlegen, aber um die Ereignisse im Windows-Ereignisanzeige anzuzeigen, müssen Sie den Kanal zunächst deaktivieren. Beachten Sie Folgendes: Wenn Sie den Kanal erneut aktivieren, werden die Ereignisse aus dem Kanal entfernt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





