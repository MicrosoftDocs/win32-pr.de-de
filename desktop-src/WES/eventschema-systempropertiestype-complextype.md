---
title: Komplexer SystemPropertiesType-Typ
description: Definiert die Informationen, die den Anbieter identifizieren und wie er aktiviert wurde, das Ereignis, den Kanal, in den das Ereignis geschrieben wurde, und Systeminformationen wie prozess- und thread-IDs.
ms.assetid: f86f7940-86cf-49ba-8f09-bf6f473d60fd
keywords:
- Komplexer SystemPropertiesType-Typ EventLog
topic_type:
- apiref
api_name:
- SystemPropertiesType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4f7391362938502f0c307faab4d7b9166633647b093e5154b3aa56512c6ee4e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119620240"
---
# <a name="systempropertiestype-complex-type"></a>Komplexer SystemPropertiesType-Typ

Definiert die Informationen, die den Anbieter identifizieren und wie er aktiviert wurde, das Ereignis, den Kanal, in den das Ereignis geschrieben wurde, und Systeminformationen wie prozess- und thread-IDs.

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



| Element                                                                         | type                                                        | Beschreibung                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Channel**](eventschema-channel-systempropertiestype-element.md)             | anyURI                                                      | Der Kanal, in dem das Ereignis protokolliert wurde.<br/>                                                                                                                                                                                                                                                                                        |
| [**Computer**](eventschema-computer-systempropertiestype-element.md)           | Zeichenfolge                                                      | Der Name des Computers, auf dem das Ereignis aufgetreten ist.<br/>                                                                                                                                                                                                                                                                             |
| [**Korrelation**](eventschema-correlation-systempropertiestype-element.md)     |                                                             | Die Aktivitätsbezeichner, die Consumer zum Gruppieren verwandter Ereignisse verwenden können.<br/>                                                                                                                                                                                                                                                 |
| [**Eventid**](eventschema-eventid-systempropertiestype-element.md)             |                                                             | Der Bezeichner, den der Anbieter zum Identifizieren des Ereignisses verwendet hat.<br/>                                                                                                                                                                                                                                                                      |
| [**EventRecordID**](eventschema-eventrecordid-systempropertiestype-element.md) |                                                             | Die Datensatznummer, die dem Ereignis zugewiesen wurde, als es protokolliert wurde.<br/>                                                                                                                                                                                                                                                                       |
| [**Ausführung**](eventschema-execution-systempropertiestype-element.md)         |                                                             | Enthält Informationen zum Prozess und Thread, der das Ereignis protokolliert hat.<br/>                                                                                                                                                                                                                                                          |
| [**Keywords**](eventschema-keywords-systempropertiestype-element.md)           | [**HexInt64Type**](eventschema-hexint64type-simpletype.md) | Eine Bitmaske der im -Ereignis definierten Schlüsselwörter. Schlüsselwörter werden verwendet, um Ereignistypen zu klassifizieren (z. B. Ereignisse, die dem Lesen von Daten zugeordnet sind).<br/>                                                                                                                                                                                 |
| [**Ebene**](eventschema-level-systempropertiestype-element.md)                 | unsignedByte                                                | Der im Ereignis definierte Schweregrad.<br/>                                                                                                                                                                                                                                                                                          |
| [**Opcode**](eventschema-opcode-systempropertiestype-element.md)               | unsignedByte                                                | Der im -Ereignis definierte Opcode. Task und Opcode werden typisierend verwendet, um den Speicherort in der Anwendung zu identifizieren, von dem aus das Ereignis protokolliert wurde.<br/>                                                                                                                                                                                  |
| [**Anbieter**](eventschema-provider-systempropertiestype-element.md)           |                                                             | Identifiziert den Anbieter, der das Ereignis protokolliert hat. Die Attribute **Name** und **GUID** sind enthalten, wenn der Anbieter ein Instrumentierungsmanifest verwendet hat, um seine Ereignisse zu definieren. Andernfalls ist das **EventSourceName-Attribut** enthalten, wenn ein Legacyereignisanbieter (mithilfe der [Ereignisprotokollierungs-API)](/windows/desktop/EventLog/event-logging) das Ereignis protokolliert hat.<br/> |
| [**Security**](eventschema-security-systempropertiestype-element.md)           |                                                             | Identifiziert den Benutzer, der das Ereignis protokolliert hat.<br/>                                                                                                                                                                                                                                                                                        |
| [**Aufgabe**](eventschema-task-systempropertiestype-element.md)                   | unsignedShort                                               | Die im -Ereignis definierte Aufgabe. Task und Opcode werden in der Regel verwendet, um den Speicherort in der Anwendung zu identifizieren, von dem aus das Ereignis protokolliert wurde.<br/>                                                                                                                                                                                    |
| [**TimeCreated**](eventschema-timecreated-systempropertiestype-element.md)     |                                                             | Der Zeitstempel, der angibt, wann das Ereignis protokolliert wurde. Der Zeitstempel enthält entweder das **SystemTime-Attribut** oder das **RawTime-Attribut.**<br/>                                                                                                                                                                           |
| [**Version**](schema-version-systempropertiestype-element.md)                  | unsignedByte                                                | Die Versionsnummer der Ereignisdefinition.<br/>                                                                                                                                                                                                                                                                                     |



## <a name="attributes"></a>Attributes



| Name              | type                                                | Beschreibung                                                                                                                                                                                                                                                                                             |
|-------------------|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aktivitäts-ID        | [**GUIDType**](eventschema-guidtype-simpletype.md) | Ein global eindeutiger Bezeichner, der die aktuelle Aktivität identifiziert. Die Ereignisse, die mit diesem Bezeichner veröffentlicht werden, sind Teil derselben Aktivität.<br/>                                                                                                                                         |
| EventSourceName   | Zeichenfolge                                              | Der Name der Ereignisquelle, die das Ereignis veröffentlicht hat (wenn die Ereignisquelle aus der [Legacy-Ereignisprotokollierungs-API](/windows/desktop/EventLog/event-logging) stammt).<br/>                                                                                                                                                      |
| Guid              | [**GUIDType**](eventschema-guidtype-simpletype.md) | Der global eindeutige Bezeichner, der den Anbieter eindeutig identifiziert.<br/>                                                                                                                                                                                                                        |
| KernelTime        | unsignedInt                                         | Verstrichene Ausführungszeit für Kernelmodusanweisungen in CPU-Zeiteinheiten. Wenn Sie eine private ETW-Sitzung verwenden, verwenden Sie stattdessen den Wert im ProcessorTime-Member. Nur für Ereignisse verfügbar, die in einer Ereignisablaufverfolgungsprotokolldatei (ETL-Datei) protokolliert werden.<br/>                                               |
| Name              | anyURI                                              | Der Name des Anbieters.<br/>                                                                                                                                                                                                                                                                    |
| ProcessID         | unsignedInt                                         | Gibt den Prozess an, der das Ereignis generiert hat<br/>                                                                                                                                                                                                                                             |
| ProcessorID       | unsignedByte                                        | Die ID des Prozessors, der das Ereignis verarbeitet hat. Nur für Ereignisse verfügbar, die in einer Ereignisablaufverfolgungsprotokolldatei (ETL-Datei) protokolliert werden.<br/>                                                                                                                                             |
| ProcessorTime     | unsignedInt                                         | Bei privaten ETW-Sitzungen die verstrichene Ausführungszeit für Anweisungen im Benutzermodus in CPU-Ticks. Nur für Ereignisse verfügbar, die in einer Ereignisablaufverfolgungsprotokolldatei (ETL-Datei) protokolliert werden.<br/>                                                                                                                    |
| Qualifizierer        | **unsignedShort**                                   | Ein Legacyanbieter verwendet eine 32-Bit-Zahl, um seine Ereignisse zu identifizieren. Wenn das Ereignis von einem Legacyanbieter protokolliert wird, enthält der Wert des **EventID-Elements** die niedrigen 16 Bits des Ereignisbezeichners, und das **Qualifier-Attribut** enthält die 16 Bits des Ereignisbezeichners in hoher Reihenfolge.<br/> |
| RawTime           | unsignedLong                                        | Der unformatierte Zeitstempelwert. Das Format des Zeitstempels hängt von der Zeitquelle ab, die zum Erfassen der Ablaufverfolgung verwendet wird. Der unformatierte Zeitstempel bietet eine höhere Genauigkeit als die Systemzeit. Die Ausgabe des gerenderten Ereignisses enthält nur rohe Zeit, wenn Sie TraceRpt.exe mit dem Schalter -rts verwenden.<br/>                 |
| RelatedActivityID | [**GUIDType**](eventschema-guidtype-simpletype.md) | Ein global eindeutiger Bezeichner, der die Aktivität identifiziert, an die das Steuerelement übertragen wurde. Die zugehörigen Ereignisse verfügen dann über diesen Bezeichner als ActivityID-Bezeichner.<br/>                                                                                                            |
| SessionID         | unsignedInt                                         | Die ID für die Terminalserversitzung, in der das Ereignis aufgetreten ist. Nur für Ereignisse verfügbar, die in einer Ereignisablaufverfolgungsprotokolldatei (ETL-Datei) protokolliert werden.<br/>                                                                                                                            |
| SystemTime        | dateTime                                            | Die Systemzeit, zu der das Ereignis protokolliert wurde.<br/>                                                                                                                                                                                                                                                |
| ThreadID          | unsignedInt                                         | Gibt den Thread an, der das Ereignis generiert hat<br/>                                                                                                                                                                                                                                              |
| UserID            | Zeichenfolge                                              | Die Sicherheits-ID (SID) des Benutzers in Zeichenfolgenform.<br/>                                                                                                                                                                                                                                    |
| UserTime          | unsignedInt                                         | Verstrichene Ausführungszeit für Anweisungen im Benutzermodus in CPU-Zeiteinheiten. Wenn Sie eine private ETW-Sitzung verwenden, verwenden Sie stattdessen den Wert im ProcessorTime-Member. Nur für Ereignisse verfügbar, die in einer Ereignisablaufverfolgungsprotokolldatei (ETL-Datei) protokolliert werden.<br/>                                                 |



## <a name="remarks"></a>Hinweise

Standardmäßig enthält das Ereignis den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Computers. Um den NETBIOS-Namen anstelle des FQDN zu verwenden, müssen Sie unter dem folgenden Registrierungsschlüssel einen DWORD-Registrierungswert namens CompatFlags erstellen und den Wert von CompatFlags auf 0x2 festlegen.

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
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

