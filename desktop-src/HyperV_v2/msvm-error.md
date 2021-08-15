---
description: Enthält Informationen zum Schweregrad, zur Ursache, zu empfohlenen Aktionen und zu anderen Daten im Zusammenhang mit dem Ausfall eines CIM-Vorgangs.
ms.assetid: 128B9ECE-D26C-4A7D-BFB7-69CD986B0DBA
title: Msvm_Error-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Error
- Msvm_Error.ErrorType
- Msvm_Error.OtherErrorType
- Msvm_Error.OwningEntity
- Msvm_Error.MessageID
- Msvm_Error.Message
- Msvm_Error.MessageArguments
- Msvm_Error.PerceivedSeverity
- Msvm_Error.ProbableCause
- Msvm_Error.ProbableCauseDescription
- Msvm_Error.RecommendedActions
- Msvm_Error.ErrorSource
- Msvm_Error.ErrorSourceFormat
- Msvm_Error.OtherErrorSourceFormat
- Msvm_Error.CIMStatusCode
- Msvm_Error.CIMStatusCodeDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 03ef036fc9c325b5087e597602fafec29abc484aa5a02a4395aaff3c25e59238
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117994497"
---
# <a name="msvm_error-class"></a>Msvm \_ Error-Klasse

Eine spezialisierte Klasse, die Informationen zum Schweregrad, zur Ursache, zu empfohlenen Aktionen und anderen Daten im Zusammenhang mit dem Ausfall eines CIM-Vorgangs enthält.

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Error : CIM_Error
{
  uint16 ErrorType;
  string OtherErrorType;
  string OwningEntity;
  string MessageID;
  string Message;
  string MessageArguments[];
  uint16 PerceivedSeverity;
  uint16 ProbableCause;
  string ProbableCauseDescription;
  string RecommendedActions[];
  string ErrorSource;
  uint16 ErrorSourceFormat = 0;
  string OtherErrorSourceFormat;
  uint32 CIMStatusCode;
  string CIMStatusCodeDescription;
};
```

## <a name="members"></a>Member

Die **Msvm \_ Error-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ Error-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**CIMStatusCode**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der CIM-Statuscode, der diese Instanz kennzeichnet. Diese Eigenschaft definiert die Statuscodes, die von einem konformen CIM-Server oder -Listener zurückgegeben werden können. Nicht alle Statuscodes sind für jeden Vorgang gültig. Die Spezifikation für jeden Vorgang sollte die Statuscodes definieren, die von diesem Vorgang zurückgegeben werden können. Die folgenden Werte für CIM-Statuscode sind definiert. Diese Eigenschaft wird vom [**\_ CIM-Fehler**](/previous-versions//cc150671(v=vs.85))geerbt.



| Wert                                                                                                                                                                                                                                                                                          | Bedeutung                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span id="CIM_ERR_FAILED"></span><span id="cim_err_failed"></span><dl> <dt>**CIM \_ FEHLER \_ BEI ERR**</dt> <dt>1</dt> </dl>                                                                       | Ein allgemeiner Fehler ist aufgetreten, der nicht durch einen spezifischeren Fehlercode abgedeckt wird.<br/>    |
| <span id="CIM_ERR_ACCESS_DENIED"></span><span id="cim_err_access_denied"></span><dl> <dt>**CIM \_ ERR \_ ACCESS \_ DENIED**</dt> <dt>2</dt> </dl>                                                 | Der Zugriff auf eine CIM-Ressource war für den Client nicht verfügbar.<br/>                      |
| <span id="CIM_ERR_INVALID_NAMESPACE"></span><span id="cim_err_invalid_namespace"></span><dl> <dt>**CIM \_ ERR \_ INVALID \_ NAMESPACE**</dt> <dt>3</dt> </dl>                                     | Der Zielnamespace ist nicht vorhanden.<br/>                                           |
| <span id="CIM_ERR_INVALID_PARAMETER"></span><span id="cim_err_invalid_parameter"></span><dl> <dt>**CIM \_ ERR \_ INVALID \_ PARAMETER**</dt> <dt>4</dt> </dl>                                     | Mindestens ein Parameterwert, der an die Methode übergeben wurde, war ungültig.<br/>                |
| <span id="CIM_ERR_INVALID_CLASS"></span><span id="cim_err_invalid_class"></span><dl> <dt>**CIM \_ UNGÜLTIGE \_ \_ ERR-KLASSE**</dt> <dt>5</dt> </dl>                                                 | Die angegebene Klasse ist nicht vorhanden.<br/>                                            |
| <span id="CIM_ERR_NOT_FOUND"></span><span id="cim_err_not_found"></span><dl> <dt>**CIM \_ ERR \_ NICHT \_ GEFUNDEN**</dt> <dt>6</dt> </dl>                                                             | Das angeforderte Objekt konnte nicht gefunden werden.<br/>                                       |
| <span id="CIM_ERR_NOT_SUPPORTED"></span><span id="cim_err_not_supported"></span><dl> <dt>**CIM \_ ERR \_ WIRD NICHT \_ UNTERSTÜTZT**</dt> <dt>7</dt> </dl>                                                 | Der angeforderte Vorgang wird nicht unterstützt.<br/>                                      |
| <span id="CIM_ERR_CLASS_HAS_CHILDREN"></span><span id="cim_err_class_has_children"></span><dl> <dt>**CIM \_ \_ERR-KLASSE \_ VERFÜGT ÜBER \_ UNTERGEORDNETE ELEMENTE**</dt> <dt>8</dt> </dl>                                 | Der Vorgang kann für diese Klasse nicht ausgeführt werden, da er Über -Instanzen verfügt.<br/>        |
| <span id="CIM_ERR_CLASS_HAS_INSTANCES"></span><span id="cim_err_class_has_instances"></span><dl> <dt>**CIM \_ DIE \_ ERR-KLASSE \_ VERFÜGT \_ ÜBER INSTANZEN**</dt> <dt>9.</dt> </dl>                              | Der Vorgang kann für diese Klasse nicht ausgeführt werden, da sie Über -Instanzen verfügt.<br/>          |
| <span id="CIM_ERR_INVALID_SUPERCLASS"></span><span id="cim_err_invalid_superclass"></span><dl> <dt>**CIM \_ ERR \_ INVALID \_ SUPERCLASS**</dt> <dt>10</dt> </dl>                                 | Der Vorgang kann nicht ausgeführt werden, da die angegebene Oberklasse nicht vorhanden ist.<br/> |
| <span id="CIM_ERR_ALREADY_EXISTS"></span><span id="cim_err_already_exists"></span><dl> <dt>**CIM \_ ERR \_ \_ IST BEREITS VORHANDEN**</dt> <dt>11</dt> </dl>                                             | Der Vorgang kann nicht ausgeführt werden, da bereits ein Objekt vorhanden ist.<br/>              |
| <span id="CIM_ERR_NO_SUCH_PROPERTY"></span><span id="cim_err_no_such_property"></span><dl> <dt>**CIM \_ ERR \_ NO \_ SUCH \_ PROPERTY**</dt> <dt>12</dt> </dl>                                      | Die angegebene Eigenschaft ist nicht vorhanden.<br/>                                         |
| <span id="CIM_ERR_TYPE_MISMATCH"></span><span id="cim_err_type_mismatch"></span><dl> <dt>**CIM \_ \_ERR-TYPKONFLIKT \_**</dt> <dt>13</dt> </dl>                                                | Der angegebene Wert ist mit dem Typ nicht kompatibel.<br/>                              |
| <span id="CIM_ERR_QUERY_LANGUAGE_NOT_SUPPORTED"></span><span id="cim_err_query_language_not_supported"></span><dl> <dt>**CIM \_ ERR QUERY LANGUAGE NOT SUPPORTED 14 \_ (ERR-ABFRAGESPRACHE \_ WIRD NICHT \_ \_ UNTERSTÜTZT**</dt> <dt>14)</dt> </dl> | Die Abfragesprache wird nicht erkannt oder unterstützt.<br/>                             |
| <span id="CIM_ERR_INVALID_QUERY"></span><span id="cim_err_invalid_query"></span><dl> <dt>**CIM \_ UNGÜLTIGE \_ \_ ERR-ABFRAGE**</dt> <dt>15</dt> </dl>                                                | Die Abfrage ist für die angegebene Abfragesprache ungültig.<br/>                       |
| <span id="CIM_ERR_METHOD_NOT_AVAILABLE"></span><span id="cim_err_method_not_available"></span><dl> <dt>**CIM \_ \_ERR-METHODE \_ NICHT \_ VERFÜGBAR**</dt> <dt>16</dt> </dl>                          | Die extrinsische Methode konnte nicht ausgeführt werden.<br/>                                    |
| <span id="CIM_ERR_METHOD_NOT_FOUND"></span><span id="cim_err_method_not_found"></span><dl> <dt>**CIM \_ \_ERR-METHODE \_ NICHT \_ GEFUNDEN**</dt> <dt>17</dt> </dl>                                      | Die angegebene extrinsische Methode ist nicht vorhanden.<br/>                                 |
| <span id="CIM_ERR_UNEXPECTED_RESPONSE"></span><span id="cim_err_unexpected_response"></span><dl> <dt>**CIM \_ UNERWARTETE \_ \_ ERR-ANTWORT**</dt> <dt>18</dt> </dl>                              | Die zurückgegebene Antwort auf den asynchronen Vorgang wurde nicht erwartet.<br/>          |
| <span id="CIM_ERR_INVALID_RESPONSE_DESTINATION"></span><span id="cim_err_invalid_response_destination"></span><dl> <dt>**CIM \_ ERR \_ INVALID \_ RESPONSE \_ DESTINATION**</dt> <dt>19</dt> </dl>  | Das angegebene Ziel für die asynchrone Antwort ist ungültig.<br/>          |
| <span id="CIM_ERR_NAMESPACE_NOT_EMPTY"></span><span id="cim_err_namespace_not_empty"></span><dl> <dt>**CIM \_ \_ERR-NAMESPACE \_ NICHT \_ LEER**</dt> <dt>20</dt> </dl>                             | Der angegebene Namespace ist nicht leer.<br/>                                          |
| <span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span><dl> <dt>**DMTF reserviert**</dt> <dt>21 = *Wert*</dt> </dl>                            | Reservierte Werte.<br/>                                                               |



 

</dd> <dt>

**CIMStatusCodeDescription**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die eine vom Benutzer lesbare Beschreibung der **CIMStatusCode-Eigenschaft** enthält. Diese Beschreibung kann zwar die Definition von **CIMStatusCode** erweitern, muss jedoch mit der Definition von CIMStatusCode konsistent sein. Diese Eigenschaft wird vom [**\_ CIM-Fehler**](/previous-versions//cc150671(v=vs.85))geerbt.

</dd> <dt>

**ErrorSource**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die identifizierenden Informationen der Entität (der Instanz), die den Fehler generiert. Wenn diese Entität im CIM-Schema modelliert wird, enthält diese Eigenschaft den Pfad der Instanz, die als Zeichenfolgenparameter codiert ist. Wenn sie nicht modelliert ist, enthält die -Eigenschaft eine identifizierende Zeichenfolge, die die Entität benennt, die den Fehler generiert hat. Der Pfad oder die identifizierende Zeichenfolge wird gemäß der **ErrorSourceFormat-Eigenschaft** formatiert. Diese Eigenschaft wird vom [**\_ CIM-Fehler**](/previous-versions//cc150671(v=vs.85))geerbt.

</dd> <dt>

**ErrorSourceFormat**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Format der **ErrorSource-Eigenschaft** kann basierend auf dem Wert dieser Eigenschaft interpretiert werden. Diese Eigenschaft wird von [**\_ CIM-Fehler**](/previous-versions//cc150671(v=vs.85))geerbt und immer auf 0 festgelegt.



| Wert                                                                                                                                                                                                                                                        | Bedeutung                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Unbekannt**</dt> <dt>0</dt> </dl>                                  | Das Format ist unbekannt oder kann von einer CIM-Clientanwendung nicht sinnvoll interpretiert werden.<br/>                                         |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**Andere**</dt> <dt>1</dt> </dl>                                          | Das Format wird durch den Wert der **OtherErrorSourceFormat-Eigenschaft** definiert.<br/>                                               |
| <span id="CIMObjectHandle"></span><span id="cimobjecthandle"></span><span id="CIMOBJECTHANDLE"></span><dl> <dt>**CIMObjectHandle**</dt> <dt>2</dt> </dl> | Ein CIM-Objekthandle, das mit der MOF-Syntax codiert ist, die für das objectHandle-Nichtterminal definiert ist, wird verwendet, um die Entität zu identifizieren.<br/> |



 

</dd> <dt>

**ErrorType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Primäre Klassifizierung des Fehlers. Die folgenden Werte sind definiert. Diese Eigenschaft wird vom [**\_ CIM-Fehler**](/previous-versions//cc150671(v=vs.85))geerbt.



| Wert                                                                                                                                                                                                                                                                                                         | Bedeutung                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Unbekannt**</dt> <dt>0</dt> </dl>                                                                                   |                                                                                                                                                          |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**Andere**</dt> <dt>1</dt> </dl>                                                                                           |                                                                                                                                                          |
| <span id="Communications_Error"></span><span id="communications_error"></span><span id="COMMUNICATIONS_ERROR"></span><dl> <dt>**Kommunikationsfehler**</dt> <dt>2</dt> </dl>                               | Fehler dieses Typs sind in erster Linie den Prozeduren und/oder Prozessen zugeordnet, die erforderlich sind, um Informationen von einem Punkt zum anderen zu übermitteln.<br/> |
| <span id="Quality_of_Service_Error"></span><span id="quality_of_service_error"></span><span id="QUALITY_OF_SERVICE_ERROR"></span><dl> <dt>**Quality of Service Fehler**</dt> <dt>3</dt> </dl>               | Fehler dieses Typs sind in erster Linie mit Fehlern verbunden, die zu einer verringerten Funktionalität oder Leistung führen.<br/>                             |
| <span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span><dl> <dt>**Softwarefehler**</dt> <dt>4</dt> </dl>                                                       | Fehler dieses Typs sind in erster Linie einem Software- oder Verarbeitungsfehler zugeordnet.<br/>                                                            |
| <span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span><dl> <dt>**Hardwarefehler**</dt> <dt>5</dt> </dl>                                                       | Fehler dieses Typs sind in erster Linie mit einem Geräte- oder Hardwarefehler verbunden.<br/>                                                         |
| <span id="Environmental_Error"></span><span id="environmental_error"></span><span id="ENVIRONMENTAL_ERROR"></span><dl> <dt>**Umgebungsfehler**</dt> <dt>6</dt> </dl>                                   | Fehler dieses Typs sind in erster Linie mit einer Fehlerbedingung im Zusammenhang mit der Einrichtung oder anderen Überlegungen zur Umgebung verbunden.<br/>      |
| <span id="Security_Error"></span><span id="security_error"></span><span id="SECURITY_ERROR"></span><dl> <dt>**Sicherheitsfehler**</dt> <dt>7</dt> </dl>                                                       | Fehler dieses Typs sind mit Sicherheitsverletzungen, der Erkennung von Viren und ähnlichen Problemen verbunden.<br/>                                        |
| <span id="Oversubscription_Error"></span><span id="oversubscription_error"></span><span id="OVERSUBSCRIPTION_ERROR"></span><dl> <dt>**Überbeschriftungsfehler**</dt> <dt>8</dt> </dl>                       | Fehler dieses Typs sind in erster Linie mit dem Fehler verbunden, genügend Ressourcen zum Abschließen des Vorgangs zu reservieren.<br/>                   |
| <span id="Unavailable_Resource_Error"></span><span id="unavailable_resource_error"></span><span id="UNAVAILABLE_RESOURCE_ERROR"></span><dl> <dt>**Ressourcenfehler 9 nicht**</dt> <dt>verfügbar</dt> </dl>       | Fehler dieses Typs sind in erster Linie mit dem Fehler beim Zugriff auf eine erforderliche Ressource verbunden.<br/>                                                |
| <span id="Unsupported_Operation_Error"></span><span id="unsupported_operation_error"></span><span id="UNSUPPORTED_OPERATION_ERROR"></span><dl> <dt>**Nicht unterstützter Vorgangsfehler**</dt> <dt>10</dt> </dl> | Fehler dieses Typs sind in erster Linie Anforderungen zugeordnet, die nicht unterstützt werden.<br/>                                                          |



 

</dd> <dt>

**Meldung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die formatierte Meldung. Diese Nachricht wird erstellt, indem der in **MessageArguments** beschriebene dynamische Inhalt der Nachricht auf die Formatzeichenfolge, die im Bereich von **OwningEntity** eindeutig identifiziert wird, von MessageID verwendet **wird.** Diese Eigenschaft wird vom [**CIM-Fehler \_ geerbt.**](/previous-versions//cc150671(v=vs.85))

</dd> <dt>

**MessageArguments**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array, das den dynamischen Inhalt der Nachricht enthält. Diese Eigenschaft wird vom [**CIM-Fehler \_ geerbt.**](/previous-versions//cc150671(v=vs.85))

</dd> <dt>

**MessageID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine nicht transparente Zeichenfolge, die innerhalb des Bereichs von **OwningEntity** das Format der Nachricht eindeutig identifiziert. Diese Eigenschaft wird vom [**CIM-Fehler \_ geerbt.**](/previous-versions//cc150671(v=vs.85))

</dd> <dt>

**OtherErrorSourceFormat**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die "Other"-Werte für **ErrorSourceFormat definiert.** Dieser Wert muss auf einen Wert festgelegt werden, der nicht NULL ist, wenn **ErrorSourceFormat** auf den Wert 1 (Other) festgelegt ist. Für alle anderen Werte von **ErrorSourceFormat** muss der Wert dieser Zeichenfolge auf NULL **festgelegt werden.** Diese Eigenschaft wird vom [**CIM-Fehler \_ geerbt.**](/previous-versions//cc150671(v=vs.85))

</dd> <dt>

**OtherErrorType**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die **den ErrorType** beschreibt, wenn 1, (Other) als **ErrorType angegeben wird.** Diese Eigenschaft wird vom [**CIM-Fehler \_ geerbt.**](/previous-versions//cc150671(v=vs.85))

</dd> <dt>

**OwningEntity**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die die Entität eindeutig identifiziert, die die Definition des Formats der in dieser Instanz beschriebenen Nachricht besitzt. **OwningEntity** muss einen urheberrechtlich geschützten, markengemarkenen oder anderweitig eindeutigen Namen enthalten, der im Besitz der Geschäftsentität oder des Standards ist, die das Format definiert. Diese Eigenschaft wird vom [**CIM-Fehler \_ geerbt.**](/previous-versions//cc150671(v=vs.85))

</dd> <dt>

**PerceivedSeverity**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein aufzählter Wert, der den Schweregrad des Fehlers aus Sicht des Notifizierers beschreibt: 2 – Niedrig sollte für nichtkritische Probleme wie ungültige Parameter, falsche Verwendung und nicht unterstützte Funktionen verwendet werden. 3 – Mittel sollte verwendet werden, um anzugeben, dass eine Aktion erforderlich ist, aber die Situation ist derzeit nicht schwerwiegend. 4 – Hoch sollte verwendet werden, um anzugeben, dass jetzt eine Aktion erforderlich ist. 5 – Schwerwiegender Fehler sollte verwendet werden, um auf einen Datenverlust oder einen nicht behebbaren System- oder Dienstfehler hindeuten zu können. Diese Eigenschaft wird vom [**CIM-Fehler \_ geerbt.**](/previous-versions//cc150671(v=vs.85))

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)
</dt> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>**Niedrig** (2)
</dt> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>**Mittel** (3)
</dt> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>**Hoch** (4)
</dt> <dt>

<span id="Fatal_"></span><span id="fatal_"></span><span id="FATAL_"></span>**Schwerwiegender** Fehler (5 )
</dt> </dl>

</dd> <dt>

**WahrscheinlichkeitCause**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein aufzählter Wert, der die wahrscheinliche Ursache des Fehlers beschreibt. Diese Eigenschaft wird vom [**CIM-Fehler \_ geerbt.**](/previous-versions//cc150671(v=vs.85))

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)
</dt> <dt>

<span id="Adapter_Card_Error"></span><span id="adapter_card_error"></span><span id="ADAPTER_CARD_ERROR"></span>**Adapter-/Kartenfehler** (2)
</dt> <dt>

<span id="Application_Subsystem_Failure"></span><span id="application_subsystem_failure"></span><span id="APPLICATION_SUBSYSTEM_FAILURE"></span>**Fehler des Anwendungssubsystems** (3)
</dt> <dt>

<span id="Bandwidth_Reduced"></span><span id="bandwidth_reduced"></span><span id="BANDWIDTH_REDUCED"></span>**Bandbreite reduziert** (4)
</dt> <dt>

<span id="Connection_Establishment_Error"></span><span id="connection_establishment_error"></span><span id="CONNECTION_ESTABLISHMENT_ERROR"></span>**Verbindungseinrichtungsfehler** (5)
</dt> <dt>

<span id="Communications_Protocol_Error"></span><span id="communications_protocol_error"></span><span id="COMMUNICATIONS_PROTOCOL_ERROR"></span>**Kommunikationsprotokollfehler** (6)
</dt> <dt>

<span id="Communications_Subsystem_Failure"></span><span id="communications_subsystem_failure"></span><span id="COMMUNICATIONS_SUBSYSTEM_FAILURE"></span>**Kommunikationssubsystemfehler** (7)
</dt> <dt>

<span id="Configuration_Customization_Error"></span><span id="configuration_customization_error"></span><span id="CONFIGURATION_CUSTOMIZATION_ERROR"></span>**Konfiguration/Anpassungsfehler** (8)
</dt> <dt>

<span id="Congestion"></span><span id="congestion"></span><span id="CONGESTION"></span>**Überlastung** (9)
</dt> <dt>

<span id="Corrupt_Data"></span><span id="corrupt_data"></span><span id="CORRUPT_DATA"></span>**Beschädigte Daten** (10)
</dt> <dt>

<span id="CPU_Cycles_Limit_Exceeded"></span><span id="cpu_cycles_limit_exceeded"></span><span id="CPU_CYCLES_LIMIT_EXCEEDED"></span>**Grenzwert für CPU-Zyklen überschritten** (11)
</dt> <dt>

<span id="Dataset_Modem_Error"></span><span id="dataset_modem_error"></span><span id="DATASET_MODEM_ERROR"></span>**Dataset-/Modemfehler** (12)
</dt> <dt>

<span id="Degraded_Signal"></span><span id="degraded_signal"></span><span id="DEGRADED_SIGNAL"></span>**Heruntergestuftes Signal** (13)
</dt> <dt>

<span id="DTE-DCE_Interface_Error"></span><span id="dte-dce_interface_error"></span><span id="DTE-DCE_INTERFACE_ERROR"></span>**DTE-DCE-Schnittstellenfehler** (14)
</dt> <dt>

<span id="Enclosure_Door_Open"></span><span id="enclosure_door_open"></span><span id="ENCLOSURE_DOOR_OPEN"></span>**Gehäusetür geöffnet** (15)
</dt> <dt>

<span id="Equipment_Malfunction"></span><span id="equipment_malfunction"></span><span id="EQUIPMENT_MALFUNCTION"></span>**Gerätefehler** (16)
</dt> <dt>

<span id="Excessive_Vibration"></span><span id="excessive_vibration"></span><span id="EXCESSIVE_VIBRATION"></span>**Übermäßige Schwingung** (17)
</dt> <dt>

<span id="File_Format_Error"></span><span id="file_format_error"></span><span id="FILE_FORMAT_ERROR"></span>**Dateiformatfehler** (18)
</dt> <dt>

<span id="Fire_Detected"></span><span id="fire_detected"></span><span id="FIRE_DETECTED"></span>Fire Detected (19) **(Erkanntes** Feuer (19))
</dt> <dt>

<span id="Flood_Detected"></span><span id="flood_detected"></span><span id="FLOOD_DETECTED"></span>**Überflutung erkannt** (20)
</dt> <dt>

<span id="Framing_Error"></span><span id="framing_error"></span><span id="FRAMING_ERROR"></span>**Rahmenfehler** (21)
</dt> <dt>

<span id="HVAC_Problem"></span><span id="hvac_problem"></span><span id="HVAC_PROBLEM"></span>**HVAC-Problem** (22)
</dt> <dt>

<span id="Humidity_Unacceptable"></span><span id="humidity_unacceptable"></span><span id="HUMIDITY_UNACCEPTABLE"></span>**Luftfeuchtigkeit nicht akzeptabel** (23)
</dt> <dt>

<span id="I_O_Device_Error"></span><span id="i_o_device_error"></span><span id="I_O_DEVICE_ERROR"></span>**E/A-Gerätefehler** (24)
</dt> <dt>

<span id="Input_Device_Error"></span><span id="input_device_error"></span><span id="INPUT_DEVICE_ERROR"></span>**Eingabegerätefehler** (25)
</dt> <dt>

<span id="LAN_Error"></span><span id="lan_error"></span><span id="LAN_ERROR"></span>**LAN-Fehler** (26)
</dt> <dt>

<span id="Non-Toxic_Leak_Detected"></span><span id="non-toxic_leak_detected"></span><span id="NON-TOXIC_LEAK_DETECTED"></span>**Nicht schädlicher Leck erkannt** (27)
</dt> <dt>

<span id="Local_Node_Transmission_Error"></span><span id="local_node_transmission_error"></span><span id="LOCAL_NODE_TRANSMISSION_ERROR"></span>**Übertragungsfehler des lokalen Knotens** (28)
</dt> <dt>

<span id="Loss_of_Frame"></span><span id="loss_of_frame"></span><span id="LOSS_OF_FRAME"></span>**Verlust des Frames** (29)
</dt> <dt>

<span id="Loss_of_Signal"></span><span id="loss_of_signal"></span><span id="LOSS_OF_SIGNAL"></span>**Verlust des Signals** (30)
</dt> <dt>

<span id="__31____________Material_Supply_Exhausted"></span><span id="__31____________material_supply_exhausted"></span><span id="__31____________MATERIAL_SUPPLY_EXHAUSTED"></span>**//31 Material Supply Exhausted** (31)
</dt> <dt>

<span id="Multiplexer_Problem"></span><span id="multiplexer_problem"></span><span id="MULTIPLEXER_PROBLEM"></span>**Multiplexer-Problem** (32)
</dt> <dt>

<span id="Out_of_Memory"></span><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>**Nicht genügend Arbeitsspeicher** (33)
</dt> <dt>

<span id="Output_Device_Error"></span><span id="output_device_error"></span><span id="OUTPUT_DEVICE_ERROR"></span>**Fehler beim Ausgabegerät** (34)
</dt> <dt>

<span id="Performance_Degraded"></span><span id="performance_degraded"></span><span id="PERFORMANCE_DEGRADED"></span>**Leistungsverschlechterung** (35)
</dt> <dt>

<span id="Power_Problem"></span><span id="power_problem"></span><span id="POWER_PROBLEM"></span>**Energieproblem** (36)
</dt> <dt>

<span id="Pressure_Unacceptable"></span><span id="pressure_unacceptable"></span><span id="PRESSURE_UNACCEPTABLE"></span>**Druck nicht akzeptabel** (37)
</dt> <dt>

<span id="Processor_Problem__Internal_Machine_Error_"></span><span id="processor_problem__internal_machine_error_"></span><span id="PROCESSOR_PROBLEM__INTERNAL_MACHINE_ERROR_"></span>**Prozessorproblem (Interner Computerfehler)** (38)
</dt> <dt>

<span id="Pump_Failure"></span><span id="pump_failure"></span><span id="PUMP_FAILURE"></span>**Pumpfehler** (39)
</dt> <dt>

<span id="Queue_Size_Exceeded"></span><span id="queue_size_exceeded"></span><span id="QUEUE_SIZE_EXCEEDED"></span>**Warteschlangengröße überschritten** (40)
</dt> <dt>

<span id="Receive_Failure"></span><span id="receive_failure"></span><span id="RECEIVE_FAILURE"></span>**Empfangsfehler** (41)
</dt> <dt>

<span id="Receiver_Failure"></span><span id="receiver_failure"></span><span id="RECEIVER_FAILURE"></span>**Empfängerfehler** (42)
</dt> <dt>

<span id="Remote_Node_Transmission_Error"></span><span id="remote_node_transmission_error"></span><span id="REMOTE_NODE_TRANSMISSION_ERROR"></span>**Remoteknotenübertragungsfehler** (43)
</dt> <dt>

<span id="Resource_at_or_Nearing_Capacity"></span><span id="resource_at_or_nearing_capacity"></span><span id="RESOURCE_AT_OR_NEARING_CAPACITY"></span>**Ressource mit oder nahezuer Kapazität** (44)
</dt> <dt>

<span id="Response_Time_Excessive"></span><span id="response_time_excessive"></span><span id="RESPONSE_TIME_EXCESSIVE"></span>**Übermäßige Antwortzeit** (45)
</dt> <dt>

<span id="Retransmission_Rate_Excessive"></span><span id="retransmission_rate_excessive"></span><span id="RETRANSMISSION_RATE_EXCESSIVE"></span>**Übermäßige Neuübertragungsrate** (46)
</dt> <dt>

<span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>**Softwarefehler** (47)
</dt> <dt>

<span id="Software_Program_Abnormally_Terminated"></span><span id="software_program_abnormally_terminated"></span><span id="SOFTWARE_PROGRAM_ABNORMALLY_TERMINATED"></span>**Softwareprogramm nicht normal beendet** (48)
</dt> <dt>

<span id="Software_Program_Error__Incorrect_Results_"></span><span id="software_program_error__incorrect_results_"></span><span id="SOFTWARE_PROGRAM_ERROR__INCORRECT_RESULTS_"></span>**Softwareprogrammfehler (falsche Ergebnisse)** (49)
</dt> <dt>

<span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Storage Kapazitätsproblem** (50)
</dt> <dt>

<span id="Temperature_Unacceptable"></span><span id="temperature_unacceptable"></span><span id="TEMPERATURE_UNACCEPTABLE"></span>**Temperatur nicht akzeptabel** (51)
</dt> <dt>

<span id="Threshold_Crossed"></span><span id="threshold_crossed"></span><span id="THRESHOLD_CROSSED"></span>**Schwellenwert überschritten** (52)
</dt> <dt>

<span id="Timing_Problem"></span><span id="timing_problem"></span><span id="TIMING_PROBLEM"></span>**Zeitsteuerungsproblem** (53)
</dt> <dt>

<span id="Toxic_Leak_Detected"></span><span id="toxic_leak_detected"></span><span id="TOXIC_LEAK_DETECTED"></span>**Schädlicher Leck erkannt** (54)
</dt> <dt>

<span id="Transmit_Failure"></span><span id="transmit_failure"></span><span id="TRANSMIT_FAILURE"></span>**Übertragungsfehler** (55)
</dt> <dt>

<span id="Transmitter_Failure"></span><span id="transmitter_failure"></span><span id="TRANSMITTER_FAILURE"></span>**Senderfehler** (56)
</dt> <dt>

<span id="Underlying_Resource_Unavailable"></span><span id="underlying_resource_unavailable"></span><span id="UNDERLYING_RESOURCE_UNAVAILABLE"></span>**Zugrunde liegende Ressource nicht verfügbar** (57)
</dt> <dt>

<span id="Version_Mismatch"></span><span id="version_mismatch"></span><span id="VERSION_MISMATCH"></span>**Versionskonflikt** (58)
</dt> <dt>

<span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**Vorherige Warnung wurde ausgelöst** (59)
</dt> <dt>

<span id="__60____________Login_Attempts_Failed"></span><span id="__60____________login_attempts_failed"></span><span id="__60____________LOGIN_ATTEMPTS_FAILED"></span>**/60 Fehlgeschlagene Anmeldeversuche** (60)
</dt> <dt>

<span id="Software_Virus_Detected"></span><span id="software_virus_detected"></span><span id="SOFTWARE_VIRUS_DETECTED"></span>**Software virus detected** (61)
</dt> <dt>

<span id="Hardware_Security_Breached"></span><span id="hardware_security_breached"></span><span id="HARDWARE_SECURITY_BREACHED"></span>**Hardwaresicherheitsverletzung** (62)
</dt> <dt>

<span id="Denial_of_Service_Detected"></span><span id="denial_of_service_detected"></span><span id="DENIAL_OF_SERVICE_DETECTED"></span>**Denial of Service erkannt** (63)
</dt> <dt>

<span id="Security_Credential_Mismatch"></span><span id="security_credential_mismatch"></span><span id="SECURITY_CREDENTIAL_MISMATCH"></span>**Nicht übereinstimmende Sicherheits-Anmeldeinformationen** (64)
</dt> <dt>

<span id="Unauthorized_Access"></span><span id="unauthorized_access"></span><span id="UNAUTHORIZED_ACCESS"></span>**Nicht autorisierter Zugriff** (65)
</dt> <dt>

<span id="Alarm_Received"></span><span id="alarm_received"></span><span id="ALARM_RECEIVED"></span>**Alarm empfangen** (66)
</dt> <dt>

<span id="Loss_of_Pointer"></span><span id="loss_of_pointer"></span><span id="LOSS_OF_POINTER"></span>**Verlust des Zeigers** (67)
</dt> <dt>

<span id="Payload_Mismatch"></span><span id="payload_mismatch"></span><span id="PAYLOAD_MISMATCH"></span>**Nutzlastkonflikt** (68)
</dt> <dt>

<span id="Transmission_Error"></span><span id="transmission_error"></span><span id="TRANSMISSION_ERROR"></span>**Übertragungsfehler** (69)
</dt> <dt>

<span id="Excessive_Error_Rate"></span><span id="excessive_error_rate"></span><span id="EXCESSIVE_ERROR_RATE"></span>**Übermäßige Fehlerrate** (70)
</dt> <dt>

<span id="Trace_Problem"></span><span id="trace_problem"></span><span id="TRACE_PROBLEM"></span>**Ablaufverfolgungsproblem** (71)
</dt> <dt>

<span id="Element_Unavailable"></span><span id="element_unavailable"></span><span id="ELEMENT_UNAVAILABLE"></span>**Element Nicht verfügbar** (72)
</dt> <dt>

<span id="Element_Missing"></span><span id="element_missing"></span><span id="ELEMENT_MISSING"></span>**Fehlendes Element** (73)
</dt> <dt>

<span id="Loss_of_Multi_Frame"></span><span id="loss_of_multi_frame"></span><span id="LOSS_OF_MULTI_FRAME"></span>**Verlust von Mehreren Rahmen** (74)
</dt> <dt>

<span id="Broadcast_Channel_Failure"></span><span id="broadcast_channel_failure"></span><span id="BROADCAST_CHANNEL_FAILURE"></span>**Broadcastkanalfehler** (75)
</dt> <dt>

<span id="Invalid_Message_Received"></span><span id="invalid_message_received"></span><span id="INVALID_MESSAGE_RECEIVED"></span>**Ungültige Nachricht empfangen** (76)
</dt> <dt>

<span id="Routing_Failure"></span><span id="routing_failure"></span><span id="ROUTING_FAILURE"></span>**Routingfehler** (77)
</dt> <dt>

<span id="Backplane_Failure"></span><span id="backplane_failure"></span><span id="BACKPLANE_FAILURE"></span>**Backplanefehler** (78)
</dt> <dt>

<span id="Identifier_Duplication"></span><span id="identifier_duplication"></span><span id="IDENTIFIER_DUPLICATION"></span>**Bezeichnerduplizierung** (79)
</dt> <dt>

<span id="Protection_Path_Failure"></span><span id="protection_path_failure"></span><span id="PROTECTION_PATH_FAILURE"></span>**Schutzpfadfehler** (80)
</dt> <dt>

<span id="Sync_Loss_or_Mismatch"></span><span id="sync_loss_or_mismatch"></span><span id="SYNC_LOSS_OR_MISMATCH"></span>**Synchronisierungsverlust oder Konflikt** (81)
</dt> <dt>

<span id="Terminal_Problem"></span><span id="terminal_problem"></span><span id="TERMINAL_PROBLEM"></span>**Terminalproblem** (82)
</dt> <dt>

<span id="Real_Time_Clock_Failure"></span><span id="real_time_clock_failure"></span><span id="REAL_TIME_CLOCK_FAILURE"></span>**Echtzeituhrfehler** (83)
</dt> <dt>

<span id="Antenna_Failure"></span><span id="antenna_failure"></span><span id="ANTENNA_FAILURE"></span>**Antennesfehler** (84)
</dt> <dt>

<span id="Battery_Charging_Failure"></span><span id="battery_charging_failure"></span><span id="BATTERY_CHARGING_FAILURE"></span>**Akkuladefehler** (85)
</dt> <dt>

<span id="Disk_Failure"></span><span id="disk_failure"></span><span id="DISK_FAILURE"></span>**Datenträgerfehler** (86)
</dt> <dt>

<span id="Frequency_Hopping_Failure"></span><span id="frequency_hopping_failure"></span><span id="FREQUENCY_HOPPING_FAILURE"></span>**Frequency Hopping Failure** (87)
</dt> <dt>

<span id="Loss_of_Redundancy"></span><span id="loss_of_redundancy"></span><span id="LOSS_OF_REDUNDANCY"></span>**Redundanzverlust** (88)
</dt> <dt>

<span id="Power_Supply_Failure"></span><span id="power_supply_failure"></span><span id="POWER_SUPPLY_FAILURE"></span>**Stromversorgungsfehler** (89)
</dt> <dt>

<span id="Signal_Quality_Problem"></span><span id="signal_quality_problem"></span><span id="SIGNAL_QUALITY_PROBLEM"></span>**Signalqualitätsproblem** (90)
</dt> <dt>

<span id="__91____________Battery_Discharging"></span><span id="__91____________battery_discharging"></span><span id="__91____________BATTERY_DISCHARGING"></span>**/91 Akkuentladung** (91)
</dt> <dt>

<span id="Battery_Failure"></span><span id="battery_failure"></span><span id="BATTERY_FAILURE"></span>**Akkuausfall** (92)
</dt> <dt>

<span id="Commercial_Power_Problem"></span><span id="commercial_power_problem"></span><span id="COMMERCIAL_POWER_PROBLEM"></span>**Kommerzielle Energieproblem** (93)
</dt> <dt>

<span id="Fan_Failure"></span><span id="fan_failure"></span><span id="FAN_FAILURE"></span>**Lüfterfehler** (94)
</dt> <dt>

<span id="Engine_Failure"></span><span id="engine_failure"></span><span id="ENGINE_FAILURE"></span>Engine Failure (95) **(Engine-Fehler** (95))
</dt> <dt>

<span id="Sensor_Failure"></span><span id="sensor_failure"></span><span id="SENSOR_FAILURE"></span>**Sensorfehler** (96)
</dt> <dt>

<span id="Fuse_Failure"></span><span id="fuse_failure"></span><span id="FUSE_FAILURE"></span>**Fuse-Fehler** (97)
</dt> <dt>

<span id="Generator_Failure"></span><span id="generator_failure"></span><span id="GENERATOR_FAILURE"></span>**Generatorfehler** (98)
</dt> <dt>

<span id="Low_Battery"></span><span id="low_battery"></span><span id="LOW_BATTERY"></span>**Niedrige Akkukapazität** (99)
</dt> <dt>

<span id="Low_Fuel"></span><span id="low_fuel"></span><span id="LOW_FUEL"></span>**Niedriger Kraftstoff** (100)
</dt> <dt>

<span id="Low_Water"></span><span id="low_water"></span><span id="LOW_WATER"></span>**Niedrig** (101)
</dt> <dt>

<span id="Explosive_Gas"></span><span id="explosive_gas"></span><span id="EXPLOSIVE_GAS"></span>**Gas** (102)
</dt> <dt>

<span id="High_Winds"></span><span id="high_winds"></span><span id="HIGH_WINDS"></span>**Hoher Wind** (103)
</dt> <dt>

<span id="Ice_Buildup"></span><span id="ice_buildup"></span><span id="ICE_BUILDUP"></span>**Ice Buildup** (104)
</dt> <dt>

<span id="Smoke"></span><span id="smoke"></span><span id="SMOKE"></span>Smoke (105) **(Qualm** (105))
</dt> <dt>

<span id="Memory_Mismatch"></span><span id="memory_mismatch"></span><span id="MEMORY_MISMATCH"></span>**Arbeitsspeicherkonflikt** (106)
</dt> <dt>

<span id="Out_of_CPU_Cycles"></span><span id="out_of_cpu_cycles"></span><span id="OUT_OF_CPU_CYCLES"></span>**Out of CPU Cycles** (107)
</dt> <dt>

<span id="Software_Environment_Problem"></span><span id="software_environment_problem"></span><span id="SOFTWARE_ENVIRONMENT_PROBLEM"></span>**Softwareumgebungsproblem** (108)
</dt> <dt>

<span id="Software_Download_Failure"></span><span id="software_download_failure"></span><span id="SOFTWARE_DOWNLOAD_FAILURE"></span>**Softwaredownloadfehler** (109)
</dt> <dt>

<span id="Element_Reinitialized"></span><span id="element_reinitialized"></span><span id="ELEMENT_REINITIALIZED"></span>**Element erneut initialisiert** (110)
</dt> <dt>

<span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>**Timeout** (111)
</dt> <dt>

<span id="Logging_Problems"></span><span id="logging_problems"></span><span id="LOGGING_PROBLEMS"></span>**Protokollierungsprobleme** (112)
</dt> <dt>

<span id="Leak_Detected"></span><span id="leak_detected"></span><span id="LEAK_DETECTED"></span>Leak Detected (113) **(Leck erkannt** (113))
</dt> <dt>

<span id="Protection_Mechanism_Failure"></span><span id="protection_mechanism_failure"></span><span id="PROTECTION_MECHANISM_FAILURE"></span>**Schutzmechanismusfehler** (114)
</dt> <dt>

<span id="__115____________Protecting_Resource_Failure"></span><span id="__115____________protecting_resource_failure"></span><span id="__115____________PROTECTING_RESOURCE_FAILURE"></span>**//115 Protecting Resource Failure** (115)
</dt> <dt>

<span id="Database_Inconsistency"></span><span id="database_inconsistency"></span><span id="DATABASE_INCONSISTENCY"></span>**Datenbankinkonsistenz** (116)
</dt> <dt>

<span id="Authentication_Failure"></span><span id="authentication_failure"></span><span id="AUTHENTICATION_FAILURE"></span>**Authentifizierungsfehler** (117)
</dt> <dt>

<span id="Breach_of_Confidentiality"></span><span id="breach_of_confidentiality"></span><span id="BREACH_OF_CONFIDENTIALITY"></span>**Verletzung der Vertraulichkeit** (118)
</dt> <dt>

<span id="Cable_Tamper"></span><span id="cable_tamper"></span><span id="CABLE_TAMPER"></span>**Kabelmanipulation** (119)
</dt> <dt>

<span id="Delayed_Information"></span><span id="delayed_information"></span><span id="DELAYED_INFORMATION"></span>**Verzögerte Informationen** (120)
</dt> <dt>

<span id="Duplicate_Information"></span><span id="duplicate_information"></span><span id="DUPLICATE_INFORMATION"></span>**Doppelte Informationen** (121)
</dt> <dt>

<span id="Information_Missing"></span><span id="information_missing"></span><span id="INFORMATION_MISSING"></span>**Fehlende Informationen** (122)
</dt> <dt>

<span id="Information_Modification"></span><span id="information_modification"></span><span id="INFORMATION_MODIFICATION"></span>**Änderung von** Informationen (123)
</dt> <dt>

<span id="Information_Out_of_Sequence"></span><span id="information_out_of_sequence"></span><span id="INFORMATION_OUT_OF_SEQUENCE"></span>**Informationen nicht sequenziert** (124)
</dt> <dt>

<span id="Key_Expired"></span><span id="key_expired"></span><span id="KEY_EXPIRED"></span>**Schlüssel abgelaufen** (125)
</dt> <dt>

<span id="Non-Repudiation_Failure"></span><span id="non-repudiation_failure"></span><span id="NON-REPUDIATION_FAILURE"></span>**Nichtabstreitbarkeitsfehler** (126)
</dt> <dt>

<span id="Out_of_Hours_Activity"></span><span id="out_of_hours_activity"></span><span id="OUT_OF_HOURS_ACTIVITY"></span>**Aktivität "Out of Hours"** (127)
</dt> <dt>

<span id="Out_of_Service"></span><span id="out_of_service"></span><span id="OUT_OF_SERVICE"></span>**Out of Service** (128)
</dt> <dt>

<span id="Procedural_Error"></span><span id="procedural_error"></span><span id="PROCEDURAL_ERROR"></span>**Prozeduraler Fehler** (129)
</dt> <dt>

<span id="Unexpected_Information_"></span><span id="unexpected_information_"></span><span id="UNEXPECTED_INFORMATION_"></span>**Unerwartete Informationen** (130 )
</dt> </dl>

</dd> <dt>

**ProbableCauseDescription**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die die wahrscheinliche Ursache des Fehlers beschreibt. Diese Eigenschaft wird vom [**\_ CIM-Fehler**](/previous-versions//cc150671(v=vs.85))geerbt.

</dd> <dt>

**RecommendedActions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die empfohlene Aktionen zum Beheben des Fehlers beschreibt. Diese Eigenschaft wird vom [**\_ CIM-Fehler**](/previous-versions//cc150671(v=vs.85))geerbt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Zugriff auf die **Msvm \_ Error-Klasse** kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_CIM-Fehler**](cim-error.md)
</dt> <dt>

[**\_CIM-Fehler**](/previous-versions//cc150671(v=vs.85))
</dt> <dt>

[Verwaltungsklassen für virtuelle Systeme](virtual-system-management-classes.md)
</dt> </dl>

 

