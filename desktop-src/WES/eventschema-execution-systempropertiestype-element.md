---
title: Execution (systempropertiestype)-Element
description: Enthält Informationen über den Prozess und den Thread, der das Ereignis protokolliert hat.
ms.assetid: 4d2feb0d-a3e6-479c-aa34-cd95a708add5
keywords:
- Ausführungs Element-Ereignisprotokoll
topic_type:
- apiref
api_name:
- Execution
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 64137153ffb0f1ba9816f060f0d5af0a2c6ee8cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740360"
---
# <a name="execution-systempropertiestype-element"></a>Execution (systempropertiestype)-Element

Enthält Informationen über den Prozess und den Thread, der das Ereignis protokolliert hat.

``` syntax
<xs:element name="Execution">
    <xs:complexType>
        <xs:attribute name="ProcessID"
            type="unsignedInt"
            use="required"
         />
        <xs:attribute name="ThreadID"
            type="unsignedInt"
            use="required"
         />
        <xs:attribute name="ProcessorID"
            type="unsignedByte"
            use="optional"
         />
        <xs:attribute name="SessionID"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="KernelTime"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="UserTime"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="ProcessorTime"
            type="unsignedInt"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

Das **Execution** -Element wird durch den komplexen [**systempropertiestype**](eventschema-systempropertiestype-complextype.md) -Typ definiert.

## <a name="attributes"></a>Attributes



| Name          | type         | BESCHREIBUNG                                                                                               |
|---------------|--------------|-----------------------------------------------------------------------------------------------------------|
| Kernelzeit    | unsignedInt  | Verstrichene Ausführungszeit für Kernel Modus-Anweisungen in CPU-Zeiteinheiten.<br/>                        |
| ProcessID     | unsignedInt  | Gibt den Prozess an, der das Ereignis generiert hat<br/>                                               |
| ProcessorId   | unsignedByte | Die Identifikationsnummer für den Prozessor, der das Ereignis verarbeitet hat.<br/>                          |
| Processortime | unsignedInt  | Für private ETW-Sitzungen die verstrichene Ausführungszeit für benutzermodusanweisungen in CPU-Ticks.<br/> |
| SessionID     | unsignedInt  | Die Identifikationsnummer für die Terminal Server Sitzung, in der das Ereignis aufgetreten ist.<br/>         |
| ThreadID      | unsignedInt  | Gibt den Thread an, der das Ereignis generiert hat<br/>                                                |
| Usertime      | unsignedInt  | Verstrichene Ausführungszeit für benutzermodusanweisungen in CPU-Zeiteinheiten.<br/>                          |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Systempropertiestype**](eventschema-systempropertiestype-complextype.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**System (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





