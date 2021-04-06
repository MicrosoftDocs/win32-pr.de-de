---
title: Komplexer systempropertiestype-Typ
description: Definiert die Informationen, die den Anbieter identifizieren und wie er aktiviert wurde, das Ereignis, den Kanal, in den das Ereignis geschrieben wurde, und Systeminformationen, wie z. b. die Prozess-und Thread-IDs.
ms.assetid: f86f7940-86cf-49ba-8f09-bf6f473d60fd
keywords:
- Ereignisprotokoll für komplexen systempropertiestype-Typ
topic_type:
- apiref
api_name:
- SystemPropertiesType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce78a804c52ed492bd4b2a42332f8eda36b4c3be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742721"
---
# <a name="systempropertiestype-complex-type"></a>Komplexer systempropertiestype-Typ

Definiert die Informationen, die den Anbieter identifizieren und wie er aktiviert wurde, das Ereignis, den Kanal, in den das Ereignis geschrieben wurde, und Systeminformationen, wie z. b. die Prozess-und Thread-IDs.

``` syntax
<xs:complexType name="SystemPropertiesType">
    <xs:sequence>
        <xs:element name="Provider">
            <xs:complexType>
                <xs:attribute name="Name"
                    type="anyURI"
                    use="optional"
                 />
                <xs:attribute name="Guid"
                    type="GUIDType"
                    use="optional"
                 />
                <xs:attribute name="EventSourceName"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="EventID">
            <xs:complexType>
                <xs:simpleContent>
                    <xs:extension
                        base="unsignedShort"
                    >
                        <xs:attribute name="Qualifiers"
                            type="unsignedShort"
                            use="optional"
                         />
                    </xs:extension>
                </xs:simpleContent>
            </xs:complexType>
        </xs:element>
        <xs:element name="Version"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Level"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Task"
            type="unsignedShort"
            minOccurs="0"
         />
        <xs:element name="Opcode"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Keywords"
            type="HexInt64Type"
            minOccurs="0"
         />
        <xs:element name="TimeCreated"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="SystemTime"
                    type="dateTime"
                    use="optional"
                 />
                <xs:attribute name="RawTime"
                    type="unsignedLong"
                    use="optional"
                 />
            </xs:complexType>
            <xs:key name="uniqueAtt">
                <xs:selector
                    xpath="."
                 />
                <xs:field
                    xpath="@SystemTime|@RawTime"
                 />
            </xs:key>
        </xs:element>
        <xs:element name="EventRecordID"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:simpleContent>
                    <xs:extension
                        base="unsignedLong"
                     />
                </xs:simpleContent>
            </xs:complexType>
        </xs:element>
        <xs:element name="Correlation"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="ActivityID"
                    type="GUIDType"
                    use="optional"
                 />
                <xs:attribute name="RelatedActivityID"
                    type="GUIDType"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="Execution"
            minOccurs="0"
        >
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
        <xs:element name="Channel"
            type="anyURI"
            minOccurs="0"
         />
        <xs:element name="Computer"
            type="string"
         />
        <xs:element name="Security"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="UserID"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
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



| Element                                                                         | type                                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Channel**](eventschema-channel-systempropertiestype-element.md)             | anyURI                                                      | Der Kanal, auf dem das Ereignis protokolliert wurde.<br/>                                                                                                                                                                                                                                                                                        |
| [**Computer**](eventschema-computer-systempropertiestype-element.md)           | Zeichenfolge                                                      | Der Name des Computers, auf dem das Ereignis aufgetreten ist.<br/>                                                                                                                                                                                                                                                                             |
| [**Ungs**](eventschema-correlation-systempropertiestype-element.md)     |                                                             | Die Aktivitäts Bezeichner, mit denen Consumer verwandte Ereignisse gruppieren können.<br/>                                                                                                                                                                                                                                                 |
| [**EventID**](eventschema-eventid-systempropertiestype-element.md)             |                                                             | Der Bezeichner, den der Anbieter verwendet hat, um das Ereignis zu identifizieren.<br/>                                                                                                                                                                                                                                                                      |
| [**Eventrecordid**](eventschema-eventrecordid-systempropertiestype-element.md) |                                                             | Die Datensatznummer, die dem Ereignis bei der Protokollierung zugewiesen wurde.<br/>                                                                                                                                                                                                                                                                       |
| [**Ausführung**](eventschema-execution-systempropertiestype-element.md)         |                                                             | Enthält Informationen über den Prozess und den Thread, der das Ereignis protokolliert hat.<br/>                                                                                                                                                                                                                                                          |
| [**Keywords**](eventschema-keywords-systempropertiestype-element.md)           | [**HexInt64Type**](eventschema-hexint64type-simpletype.md) | Eine Bitmaske der Schlüsselwörter, die im Ereignis definiert sind. Schlüsselwörter werden verwendet, um Ereignis Typen zu klassifizieren (z. b. Ereignisse, die dem Lesen von Daten zugeordnet sind).<br/>                                                                                                                                                                                 |
| [**Geringen**](eventschema-level-systempropertiestype-element.md)                 | unsignedByte                                                | Der im Ereignis definierte Schweregrad.<br/>                                                                                                                                                                                                                                                                                          |
| [**Opcode**](eventschema-opcode-systempropertiestype-element.md)               | unsignedByte                                                | Der im Ereignis definierte Opcode. Task und Opcode werden typlogisch verwendet, um die Position in der Anwendung zu identifizieren, von der das Ereignis protokolliert wurde.<br/>                                                                                                                                                                                  |
| [**Anbieter**](eventschema-provider-systempropertiestype-element.md)           |                                                             | Identifiziert den Anbieter, der das Ereignis protokolliert hat. Die Attribute **Name** und **GUID** sind enthalten, wenn der Anbieter ein Instrumentierungs Manifest zum Definieren der Ereignisse verwendet hat. Andernfalls wird das **eventSourceName** -Attribut eingeschlossen, wenn das Ereignis von einem Legacy Ereignis Anbieter (mit der [Ereignis Protokollierungs](/windows/desktop/EventLog/event-logging) -API) protokolliert wird.<br/> |
| [**Sicherheit**](eventschema-security-systempropertiestype-element.md)           |                                                             | Identifiziert den Benutzer, der das Ereignis protokolliert hat.<br/>                                                                                                                                                                                                                                                                                        |
| [**Aufgabe**](eventschema-task-systempropertiestype-element.md)                   | unsignedShort                                               | Die im Ereignis definierte Aufgabe. Task und Opcode werden in der Regel verwendet, um die Position in der Anwendung zu identifizieren, von der das Ereignis protokolliert wurde.<br/>                                                                                                                                                                                    |
| [**TimeCreated**](eventschema-timecreated-systempropertiestype-element.md)     |                                                             | Der Zeitstempel, der angibt, wann das Ereignis protokolliert wurde. Der Zeitstempel schließt entweder das **SYSTEMTIME** -Attribut oder das **rawtime** -Attribut ein.<br/>                                                                                                                                                                           |
| [**Version**](schema-version-systempropertiestype-element.md)                  | unsignedByte                                                | Die Versionsnummer der Ereignis Definition.<br/>                                                                                                                                                                                                                                                                                     |



## <a name="attributes"></a>Attributes



| Name              | type                                                | BESCHREIBUNG                                                                                                                                                                                                                                                                                             |
|-------------------|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aktivitäts-ID        | [**Guidtype**](eventschema-guidtype-simpletype.md) | Ein-Globally Unique Identifier, der die aktuelle Aktivität bezeichnet. Die mit diesem Bezeichner veröffentlichten Ereignisse sind Teil derselben Aktivität.<br/>                                                                                                                                         |
| EventSourceName   | Zeichenfolge                                              | Der Name der Ereignis Quelle, die das Ereignis veröffentlicht hat (wenn die Ereignis Quelle von der Legacy- [Ereignisprotokollierungs](/windows/desktop/EventLog/event-logging) -API stammt).<br/>                                                                                                                                                      |
| GUID              | [**Guidtype**](eventschema-guidtype-simpletype.md) | Der Globally Unique Identifier, der den Anbieter eindeutig identifiziert.<br/>                                                                                                                                                                                                                        |
| Kernelzeit        | unsignedInt                                         | Verstrichene Ausführungszeit für Kernel Modus-Anweisungen in CPU-Zeiteinheiten. Wenn Sie eine private ETW-Sitzung verwenden, verwenden Sie stattdessen den Wert im processortime-Member. Nur verfügbar für Ereignisse, die in einer Ereignis Ablauf Verfolgungs Protokoll-Datei (ETL-Datei) protokolliert werden.<br/>                                               |
| Name              | anyURI                                              | Der Name des Anbieters.<br/>                                                                                                                                                                                                                                                                    |
| ProcessID         | unsignedInt                                         | Gibt den Prozess an, der das Ereignis generiert hat<br/>                                                                                                                                                                                                                                             |
| ProcessorId       | unsignedByte                                        | Die Identifikationsnummer für den Prozessor, der das Ereignis verarbeitet hat. Nur verfügbar für Ereignisse, die in einer Ereignis Ablauf Verfolgungs Protokoll-Datei (ETL-Datei) protokolliert werden.<br/>                                                                                                                                             |
| Processortime     | unsignedInt                                         | Für private ETW-Sitzungen die verstrichene Ausführungszeit für benutzermodusanweisungen in CPU-Ticks. Nur verfügbar für Ereignisse, die in einer Ereignis Ablauf Verfolgungs Protokoll-Datei (ETL-Datei) protokolliert werden.<br/>                                                                                                                    |
| Qualifizierer        | **unsignedShort**                                   | Ein Legacy Anbieter verwendet eine 32-Bit-Nummer, um seine Ereignisse zu identifizieren. Wenn das Ereignis von einem Legacy Anbieter protokolliert wird, enthält der Wert des **EventID-** Elements die nieder wertigen 16 Bits des Ereignis Bezeichners, und das **qualifiziererattribut** enthält die höherwertigen 16 Bits des Ereignis Bezeichners.<br/> |
| Rawtime           | unsignedLong                                        | Der rohzeit Stempel Wert. das Format des Zeitstempels hängt von der Zeit Quelle ab, die zum Erfassen der Ablauf Verfolgung verwendet wird. Der unformatierte Zeitstempel bietet eine höhere Genauigkeit als die Systemzeit. Die gerenderte Ereignis Ausgabe enthält nur eine unformatierte Zeit, wenn Sie TraceRpt.exe mit dem Schalter-RTS verwenden.<br/>                 |
| RelatedActivityID | [**Guidtype**](eventschema-guidtype-simpletype.md) | Ein-Globally Unique Identifier, der die Aktivität identifiziert, an die das Steuerelement übertragen wurde. Die zugehörigen Ereignisse haben dann diesen Bezeichner als ActivityId-Bezeichner.<br/>                                                                                                            |
| SessionID         | unsignedInt                                         | Die Identifikationsnummer für die Terminal Server Sitzung, in der das Ereignis aufgetreten ist. Nur verfügbar für Ereignisse, die in einer Ereignis Ablauf Verfolgungs Protokoll-Datei (ETL-Datei) protokolliert werden.<br/>                                                                                                                            |
| SystemTime        | dateTime                                            | Die Systemzeit, zu der das Ereignis protokolliert wurde.<br/>                                                                                                                                                                                                                                                |
| ThreadID          | unsignedInt                                         | Gibt den Thread an, der das Ereignis generiert hat<br/>                                                                                                                                                                                                                                              |
| UserID            | Zeichenfolge                                              | Die Sicherheits-ID (SID) des Benutzers in Form einer Zeichenfolge.<br/>                                                                                                                                                                                                                                    |
| Usertime          | unsignedInt                                         | Verstrichene Ausführungszeit für benutzermodusanweisungen in CPU-Zeiteinheiten. Wenn Sie eine private ETW-Sitzung verwenden, verwenden Sie stattdessen den Wert im processortime-Member. Nur verfügbar für Ereignisse, die in einer Ereignis Ablauf Verfolgungs Protokoll-Datei (ETL-Datei) protokolliert werden.<br/>                                                 |



## <a name="remarks"></a>Bemerkungen

Standardmäßig enthält das Ereignis den voll qualifizierten Domänen Namen (Fully Qualified Domain Name, FQDN) eines Computers. Wenn Sie anstelle des FQDN den NetBIOS-Namen verwenden möchten, müssen Sie unter dem folgenden Registrierungsschlüssel einen DWORD-Registrierungs Wert mit dem Namen "compatflags" erstellen und den Wert von "compatflags" auf "0x2" festlegen.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               WINEVT
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

