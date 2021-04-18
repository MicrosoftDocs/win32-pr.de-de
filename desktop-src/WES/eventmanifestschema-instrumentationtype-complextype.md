---
title: Komplexer InstrumentationType-Typ
description: Definiert den Inhalt des Instrumentations Abschnitts des Manifests.
ms.assetid: dbbb978d-50dd-44c0-8bd1-3e48b41afb88
keywords:
- Instrumentierungstyp komplexer Typ EventLog
topic_type:
- apiref
api_name:
- InstrumentationType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1679ae310a996458aad3e25aba74955036094e00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340373"
---
# <a name="instrumentationtype-complex-type"></a>Komplexer InstrumentationType-Typ

Definiert den Inhalt des Instrumentations Abschnitts des Manifests.

``` syntax
<xs:complexType name="InstrumentationType">
    <xs:sequence>
        <xs:element name="events"
            type="EventsType"
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



| Element                                                                  | type                                                             | BESCHREIBUNG                                                        |
|--------------------------------------------------------------------------|------------------------------------------------------------------|--------------------------------------------------------------------|
| [**events**](eventmanifestschema-events-instrumentationtype-element.md) | [**Eventstype**](eventmanifestschema-eventstype-complextype.md) | Enthält eine Liste der Anbieter, die das Manifest definiert.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





