---
description: Eine konkrete Oberklasse für CIM-Warnungsbenachrichtigungen.
ms.assetid: ec4cf41d-decd-4f21-b805-90db4a61376d
title: CIM_AlertIndication-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AlertIndication
- CIM_AlertIndication.Description
- CIM_AlertIndication.AlertingManagedElement
- CIM_AlertIndication.AlertingElementFormat
- CIM_AlertIndication.OtherAlertingElementFormat
- CIM_AlertIndication.AlertType
- CIM_AlertIndication.OtherAlertType
- CIM_AlertIndication.PerceivedSeverity
- CIM_AlertIndication.ProbableCause
- CIM_AlertIndication.ProbableCauseDescription
- CIM_AlertIndication.Trending
- CIM_AlertIndication.RecommendedActions
- CIM_AlertIndication.EventID
- CIM_AlertIndication.EventTime
- CIM_AlertIndication.SystemCreationClassName
- CIM_AlertIndication.SystemName
- CIM_AlertIndication.ProviderName
- CIM_AlertIndication.Message
- CIM_AlertIndication.MessageArguments
- CIM_AlertIndication.MessageID
- CIM_AlertIndication.OwningEntity
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b4a5f175ba98165e1e13d86a638260871f9bab16de23b28a92144386f89a587f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829680"
---
# <a name="cim_alertindication-class"></a>CIM \_ AlertIndication-Klasse

Eine konkrete Oberklasse für CIM-Warnungsbenachrichtigungen. **CIM \_ AlertIndication** ist ein spezialisierter Typ der **\_ CIM-Indikatorklasse,** der Informationen zum Schweregrad, zur Ursache, zu empfohlenen Aktionen und zu anderen Daten für ein reales Ereignis enthält. Dieses Ereignis und seine Daten können in der CIM-Klassenhierarchie modelliert werden.

## <a name="syntax"></a>Syntax

``` syntax
[Indication, Version("2.22.0"), UMLPackagePath("CIM::Event"), AMENDMENT]
class CIM_AlertIndication : CIM_ProcessIndication
{
  string   Description;
  string   AlertingManagedElement;
  uint16   AlertingElementFormat = 0;
  string   OtherAlertingElementFormat;
  uint16   AlertType;
  string   OtherAlertType;
  uint16   PerceivedSeverity;
  uint16   ProbableCause;
  string   ProbableCauseDescription;
  uint16   Trending;
  string   RecommendedActions[];
  string   EventID;
  datetime EventTime;
  string   SystemCreationClassName;
  string   SystemName;
  string   ProviderName;
  string   Message;
  string   MessageArguments[];
  string   MessageID;
  string   OwningEntity;
};
```

## <a name="members"></a>Member

Die **CIM \_ AlertIndication-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ AlertIndication-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AlertingElementFormat**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**AlertingManagedElement**", "**CIM \_ AlertIndication**.**OtherAlertingElementFormat**")
</dt> </dl>

Das Format der **AlertingManagedElement-Eigenschaft.**

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd>

Das Format ist unbekannt oder kann von einer CIM-Clientanwendung nicht sinnvoll interpretiert werden.

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Andere** (1)


</dt> <dd>

Das Format wird durch den Wert der OtherAlertingElementFormat-Eigenschaft definiert.

</dd> <dt>

<span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>

<span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)


</dt> <dd>

Das Format ist ein CIMObjectPath, der eine Instanz im CIM-Schema angibt.

</dd> </dl>

</dd> <dt>

**AlertingManagedElement**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**AlertingElementFormat**")
</dt> </dl>

Die identifizierenden Informationen der Entität (d.h. der Instanz), für die diese Angabe generiert wird. Die -Eigenschaft enthält den Pfad einer -Instanz, die als Zeichenfolgenparameter codiert ist, wenn die Instanz im CIM-Schema modelliert wird. Wenn es sich nicht um eine CIM-Instanz handelt, enthält die -Eigenschaft eine identifizierende Zeichenfolge, die die Entität benennt, für die die Warnung generiert wird. Der Pfad oder die identifizierende Zeichenfolge wird gemäß der AlertingElementFormat-Eigenschaft formatiert.

</dd> <dt>

**AlertType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Erforderlich,**](/windows/desktop/WmiSdk/standard-qualifiers) [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU \| X733. Ereignistyp")
</dt> </dl>

Die primäre Klassifizierung der Angabe.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Andere** (1)


</dt> <dd>

\- Andere. Die OtherAlertType-Eigenschaft von Indication übermittelt ihre Klassifizierung. Die Verwendung von "Other" in einer Enumeration ist eine CIM-Standardkonvention. Dies bedeutet, dass die aktuelle Angabe nicht in die von dieser Enumeration beschriebenen Kategorien passt.

</dd> <dt>

<span id="Communications_Alert"></span><span id="communications_alert"></span><span id="COMMUNICATIONS_ALERT"></span>

<span id="Communications_Alert"></span><span id="communications_alert"></span><span id="COMMUNICATIONS_ALERT"></span>**Kommunikationswarnung** (2)


</dt> <dd>

Ein Hinweis auf diesen Typ ist im Prinzip den Prozeduren und/oder Prozessen zugeordnet, die erforderlich sind, um Informationen von einem Punkt an einen anderen zu übermitteln.

</dd> <dt>

<span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>

<span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**Quality of Service-Warnung** (3)


</dt> <dd>

Ein Hinweis auf diesen Typ ist grundsätzlich mit einer Beeinträchtigung oder Fehlern in der Leistung oder Funktion einer Entität verknüpft.

</dd> <dt>

<span id="Processing_Error"></span><span id="processing_error"></span><span id="PROCESSING_ERROR"></span>

<span id="Processing_Error"></span><span id="processing_error"></span><span id="PROCESSING_ERROR"></span>**Verarbeitungsfehler** (4)


</dt> <dd>

Ein Hinweis auf diesen Typ ist grundsätzlich einem Software- oder Verarbeitungsfehler zugeordnet.

</dd> <dt>

<span id="Device_Alert"></span><span id="device_alert"></span><span id="DEVICE_ALERT"></span>

<span id="Device_Alert"></span><span id="device_alert"></span><span id="DEVICE_ALERT"></span>**Gerätewarnung** (5)


</dt> <dd>

Ein Hinweis auf diesen Typ ist hauptsächlich einem Geräte- oder Hardwarefehler zugeordnet.

</dd> <dt>

<span id="Environmental_Alert"></span><span id="environmental_alert"></span><span id="ENVIRONMENTAL_ALERT"></span>

<span id="Environmental_Alert"></span><span id="environmental_alert"></span><span id="ENVIRONMENTAL_ALERT"></span>**Umgebungswarnung** (6)


</dt> <dd>

Umgebungswarnung. Ein Hinweis auf diesen Typ ist in erster Linie mit einer Bedingung verknüpft, die sich auf ein Gehäuse bezieht, in dem sich die Hardware befindet, oder andere Überlegungen zur Umgebung.

</dd> <dt>

<span id="Model_Change"></span><span id="model_change"></span><span id="MODEL_CHANGE"></span>

<span id="Model_Change"></span><span id="model_change"></span><span id="MODEL_CHANGE"></span>**Modelländerung** (7)


</dt> <dd>

Die Angabe adressieren Änderungen im Informationsmodell. Beispielsweise kann es eine Lebenszyklusanzeige einbetten, um die spezifische Modelländerung zu übermitteln, die benachrichtigt wird.

</dd> <dt>

<span id="Security_Alert"></span><span id="security_alert"></span><span id="SECURITY_ALERT"></span>

<span id="Security_Alert"></span><span id="security_alert"></span><span id="SECURITY_ALERT"></span>**Sicherheitswarnung** (8)


</dt> <dd>

. Ein Hinweis auf diesen Typ ist zugeordnet.

</dd> </dl>

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU \| X733. Zusätzlicher Text")
</dt> </dl>

Eine kurze Beschreibung der Anzeige.

</dd> <dt>

**EventID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**ProbableCause**")
</dt> </dl>

Ein instrumentierungs- oder anbieterspezifischer Wert, der das zugrunde liegende reale Ereignis beschreibt, das durch die Angabe dargestellt wird. Hinweise mit demselben **EventID-Wert** ungleich NULL werden von der erstellenden Entität berücksichtigt, um das gleiche Ereignis darzustellen. Der Vergleich zweier **EventID-Werte** ist nur für Warnungshinweise mit identischen Werten ungleich NULL der Eigenschaften **SystemCreateClassName,** **SystemName** und **ProviderName** definiert.

</dd> <dt>

**EventTime**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**ProbableCause**")
</dt> </dl>

Die Uhrzeit und das Datum, die angeben, wann das zugrunde liegende Ereignis zum ersten Mal erkannt wurde. Wenn diese Werte angegeben werden und die erstellende Entität diese Informationen nicht bereitstellen kann, muss diese Eigenschaft auf **NULL** festgelegt werden. Dieser Wert basiert auf dem Konzept des lokalen Datums und der Lokalen Uhrzeit des **CIM \_ ManageSystemElement-Objekts,** das die Anzeige generiert hat.

</dd> <dt>

**Meldung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**MessageID**", "**CIM \_ AlertIndication**.**MessageArguments**")
</dt> </dl>

Die formatierte Meldung für die Warnungsanzeige. Diese Nachricht wird formatiert, indem mindestens ein dynamisches Element, das in der **MessageArguments-Eigenschaft** angegeben ist, und mit den statischen Elementen kombiniert wird, die durch die **MessageID-Eigenschaft** eindeutig identifiziert werden.

</dd> <dt>

**MessageArguments**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**Meldung**", "**CIM \_ AlertIndication**.**MessageID**")
</dt> </dl>

Ein Array, das den dynamischen Inhalt der Meldung für die Warnungsanzeige enthält.

</dd> <dt>

**MessageID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**Meldung**", "**CIM \_ AlertIndication**.**MessageArguments**")
</dt> </dl>

Die eindeutige ID des Nachrichtenformats, wobei der Bereich der Organisation in **OwningEntity** angegeben ist.

</dd> <dt>

**OtherAlertingElementFormat**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**AlertingElementFormat**")
</dt> </dl>

Definiert das Format der **AlertingManagedElement-Eigenschaft,** wenn die **AlertingElementFormat-Eigenschaft** auf "1" (andere) festgelegt ist. Andernfalls muss dieser Wert auf **NULL** festgelegt werden.

</dd> <dt>

**OtherAlertType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**AlertType**")
</dt> </dl>

Eine Zeichenfolge, die den **AlertType-Wert** beschreibt, wenn die **AlertType-Eigenschaft** auf "1" (Andere Zustandsänderung) festgelegt ist.

</dd> <dt>

**OwningEntity**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die eindeutige ID der Organisation, die die Definition des Formats der **Message-Eigenschaft** besitzt. **OwningEntity** muss einen urheberrechtlich geschützten, markengeschützten oder eindeutigen Namen enthalten, der im Besitz der Geschäftsentität oder des Standardtexts ist, der das Nachrichtenformat definiert hat.

</dd> <dt>

**PerceivedSeverity**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Erforderlich,**](/windows/desktop/WmiSdk/standard-qualifiers) [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("PerceivedSeverity"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU \| X733. Wahrgenommener Schweregrad")
</dt> </dl>

Der Schweregrad der Warnungsanzeige aus Sicht des Elements, das die Warnung ausgelöst hat.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd>

Folgt der allgemeinen Verwendung.

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Andere** (1)


</dt> <dd>

Gibt an, dass der Wert des Schweregrads in der OtherSeverity-Eigenschaft gefunden werden kann.

</dd> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Informationen** (2)


</dt> <dd>

Folgt der allgemeinen Verwendung.

</dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Heruntergestuft/Warnung** (3)


</dt> <dd>

Sollte nach Bedarf verwendet werden, damit der Benutzer entscheiden kann, ob eine Aktion erforderlich ist.

</dd> <dt>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Nebenversion** (4)


</dt> <dd>

Gibt an, dass eine Aktion erforderlich ist, aber die Situation zu diesem Zeitpunkt nicht schwerwiegend ist.

</dd> <dt>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Hauptfach** (5)


</dt> <dd>

Gibt an, dass jetzt eine Aktion erforderlich ist.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Kritisch** (6)


</dt> <dd>

Jetzt ist eine Aktion erforderlich, und der Umfang ist umfangreich (möglicherweise führt ein bevorstehender Ausfall einer kritischen Ressource dazu).

</dd> <dt>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Schwerwiegend/nicht behebbar** (7)


</dt> <dd>

Gibt an, dass ein Fehler aufgetreten ist, aber es ist zu spät, maßnahmen zu ergreifen.

</dd> </dl>

</dd> <dt>

**ProbableCause**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Erforderlich,**](/windows/desktop/WmiSdk/standard-qualifiers) [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU \| X733. Wahrscheinliche Ursache", "Recommendation.ITU \| M3100.wahrscheinlichCause", "ITU-IANA-ALARM-TC"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**ProbableCauseDescription**", "**CIM \_ AlertIndication**.**EventID**", "**CIM \_ AlertIndication**.**EventTime**")
</dt> </dl>

Die wahrscheinliche Ursache der Situation, die zur Warnungsanzeige geführt hat.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Andere** (1)


</dt> <dd></dd> <dt>

<span id="Adapter_Card_Error"></span><span id="adapter_card_error"></span><span id="ADAPTER_CARD_ERROR"></span>

**Adapter-/Kartenfehler** (2)


</dt> <dd></dd> <dt>

<span id="Application_Subsystem_Failure"></span><span id="application_subsystem_failure"></span><span id="APPLICATION_SUBSYSTEM_FAILURE"></span>

**Anwendungssubsystemfehler** (3)


</dt> <dd></dd> <dt>

<span id="Bandwidth_Reduced"></span><span id="bandwidth_reduced"></span><span id="BANDWIDTH_REDUCED"></span>

**Reduzierte Bandbreite** (4)


</dt> <dd></dd> <dt>

<span id="Connection_Establishment_Error"></span><span id="connection_establishment_error"></span><span id="CONNECTION_ESTABLISHMENT_ERROR"></span>

**Verbindungseinrichtungsfehler** (5)


</dt> <dd></dd> <dt>

<span id="Communications_Protocol_Error"></span><span id="communications_protocol_error"></span><span id="COMMUNICATIONS_PROTOCOL_ERROR"></span>

**Kommunikationsprotokollfehler** (6)


</dt> <dd></dd> <dt>

<span id="Communications_Subsystem_Failure"></span><span id="communications_subsystem_failure"></span><span id="COMMUNICATIONS_SUBSYSTEM_FAILURE"></span>

**Kommunikationssubsystemfehler** (7)


</dt> <dd></dd> <dt>

<span id="Configuration_Customization_Error"></span><span id="configuration_customization_error"></span><span id="CONFIGURATION_CUSTOMIZATION_ERROR"></span>

**Konfigurations-/Anpassungsfehler** (8)


</dt> <dd></dd> <dt>

<span id="Congestion"></span><span id="congestion"></span><span id="CONGESTION"></span>

**Überlastung** (9)


</dt> <dd></dd> <dt>

<span id="Corrupt_Data"></span><span id="corrupt_data"></span><span id="CORRUPT_DATA"></span>

**Beschädigte Daten** (10)


</dt> <dd></dd> <dt>

<span id="CPU_Cycles_Limit_Exceeded"></span><span id="cpu_cycles_limit_exceeded"></span><span id="CPU_CYCLES_LIMIT_EXCEEDED"></span>

**CPU-Zyklenlimit überschritten** (11)


</dt> <dd></dd> <dt>

<span id="Dataset_Modem_Error"></span><span id="dataset_modem_error"></span><span id="DATASET_MODEM_ERROR"></span>

**Dataset-/Modemfehler** (12)


</dt> <dd></dd> <dt>

<span id="Degraded_Signal"></span><span id="degraded_signal"></span><span id="DEGRADED_SIGNAL"></span>

**Heruntergestuftes Signal** (13)


</dt> <dd></dd> <dt>

<span id="DTE-DCE_Interface_Error"></span><span id="dte-dce_interface_error"></span><span id="DTE-DCE_INTERFACE_ERROR"></span>

**DTE-DCE-Schnittstellenfehler** (14)


</dt> <dd></dd> <dt>

<span id="Enclosure_Door_Open"></span><span id="enclosure_door_open"></span><span id="ENCLOSURE_DOOR_OPEN"></span>

**Gehäusetür geöffnet** (15)


</dt> <dd></dd> <dt>

<span id="Equipment_Malfunction"></span><span id="equipment_malfunction"></span><span id="EQUIPMENT_MALFUNCTION"></span>

**Gerätefehler** (16)


</dt> <dd></dd> <dt>

<span id="Excessive_Vibration"></span><span id="excessive_vibration"></span><span id="EXCESSIVE_VIBRATION"></span>

**Übermäßige Schwingung** (17)


</dt> <dd></dd> <dt>

<span id="File_Format_Error"></span><span id="file_format_error"></span><span id="FILE_FORMAT_ERROR"></span>

**Dateiformatfehler** (18)


</dt> <dd></dd> <dt>

<span id="Fire_Detected"></span><span id="fire_detected"></span><span id="FIRE_DETECTED"></span>

**Fire Detected** (19)


</dt> <dd></dd> <dt>

<span id="Flood_Detected"></span><span id="flood_detected"></span><span id="FLOOD_DETECTED"></span>

**Überflutung erkannt** (20)


</dt> <dd></dd> <dt>

<span id="Framing_Error"></span><span id="framing_error"></span><span id="FRAMING_ERROR"></span>

**Framefehler** (21)


</dt> <dd></dd> <dt>

<span id="HVAC_Problem"></span><span id="hvac_problem"></span><span id="HVAC_PROBLEM"></span>

**HVAC-Problem** (22)


</dt> <dd></dd> <dt>

<span id="Humidity_Unacceptable"></span><span id="humidity_unacceptable"></span><span id="HUMIDITY_UNACCEPTABLE"></span>

**Luftfeuchtigkeit nicht akzeptabel** (23)


</dt> <dd></dd> <dt>

<span id="I_O_Device_Error"></span><span id="i_o_device_error"></span><span id="I_O_DEVICE_ERROR"></span>

**E/A-Gerätefehler** (24)


</dt> <dd></dd> <dt>

<span id="Input_Device_Error"></span><span id="input_device_error"></span><span id="INPUT_DEVICE_ERROR"></span>

**Eingabegerätfehler** (25)


</dt> <dd></dd> <dt>

<span id="LAN_Error"></span><span id="lan_error"></span><span id="LAN_ERROR"></span>

**LAN-Fehler** (26)


</dt> <dd></dd> <dt>

<span id="Non-Toxic_Leak_Detected"></span><span id="non-toxic_leak_detected"></span><span id="NON-TOXIC_LEAK_DETECTED"></span>

**Nicht schädlicher Verlust erkannt** (27)


</dt> <dd></dd> <dt>

<span id="Local_Node_Transmission_Error"></span><span id="local_node_transmission_error"></span><span id="LOCAL_NODE_TRANSMISSION_ERROR"></span>

**Lokaler Knotenübertragungsfehler** (28)


</dt> <dd></dd> <dt>

<span id="Loss_of_Frame"></span><span id="loss_of_frame"></span><span id="LOSS_OF_FRAME"></span>

**Verlust des Frames** (29)


</dt> <dd></dd> <dt>

<span id="Loss_of_Signal"></span><span id="loss_of_signal"></span><span id="LOSS_OF_SIGNAL"></span>

**Verlust des Signals** (30)


</dt> <dd></dd> <dt>

<span id="Material_Supply_Exhausted"></span><span id="material_supply_exhausted"></span><span id="MATERIAL_SUPPLY_EXHAUSTED"></span>

**Materialversorgung erschöpft** (31)


</dt> <dd></dd> <dt>

<span id="Multiplexer_Problem"></span><span id="multiplexer_problem"></span><span id="MULTIPLEXER_PROBLEM"></span>

**Multiplexer-Problem** (32)


</dt> <dd></dd> <dt>

<span id="Out_of_Memory"></span><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>

**Nicht genügend Arbeitsspeicher** (33)


</dt> <dd></dd> <dt>

<span id="Output_Device_Error"></span><span id="output_device_error"></span><span id="OUTPUT_DEVICE_ERROR"></span>

**Ausgabegerätfehler** (34)


</dt> <dd></dd> <dt>

<span id="Performance_Degraded"></span><span id="performance_degraded"></span><span id="PERFORMANCE_DEGRADED"></span>

**Beeinträchtigte Leistung** (35)


</dt> <dd></dd> <dt>

<span id="Power_Problem"></span><span id="power_problem"></span><span id="POWER_PROBLEM"></span>

**Energieproblem** (36)


</dt> <dd></dd> <dt>

<span id="Pressure_Unacceptable"></span><span id="pressure_unacceptable"></span><span id="PRESSURE_UNACCEPTABLE"></span>

**Druck nicht akzeptabel** (37)


</dt> <dd></dd> <dt>

<span id="Processor_Problem__Internal_Machine_Error_"></span><span id="processor_problem__internal_machine_error_"></span><span id="PROCESSOR_PROBLEM__INTERNAL_MACHINE_ERROR_"></span>

**Prozessorproblem (interner Computerfehler)** (38)


</dt> <dd></dd> <dt>

<span id="Pump_Failure"></span><span id="pump_failure"></span><span id="PUMP_FAILURE"></span>

**Pumpfehler** (39)


</dt> <dd></dd> <dt>

<span id="Queue_Size_Exceeded"></span><span id="queue_size_exceeded"></span><span id="QUEUE_SIZE_EXCEEDED"></span>

**Warteschlangengröße überschritten** (40)


</dt> <dd></dd> <dt>

<span id="Receive_Failure"></span><span id="receive_failure"></span><span id="RECEIVE_FAILURE"></span>

**Empfangsfehler** (41)


</dt> <dd></dd> <dt>

<span id="Receiver_Failure"></span><span id="receiver_failure"></span><span id="RECEIVER_FAILURE"></span>

**Empfängerfehler** (42)


</dt> <dd></dd> <dt>

<span id="Remote_Node_Transmission_Error"></span><span id="remote_node_transmission_error"></span><span id="REMOTE_NODE_TRANSMISSION_ERROR"></span>

**Remoteknotenübertragungsfehler** (43)


</dt> <dd></dd> <dt>

<span id="Resource_at_or_Nearing_Capacity"></span><span id="resource_at_or_nearing_capacity"></span><span id="RESOURCE_AT_OR_NEARING_CAPACITY"></span>

**Ressource bei oder in der Nähe der Kapazität** (44)


</dt> <dd></dd> <dt>

<span id="Response_Time_Excessive"></span><span id="response_time_excessive"></span><span id="RESPONSE_TIME_EXCESSIVE"></span>

**Übermäßige Antwortzeit** (45)


</dt> <dd></dd> <dt>

<span id="Retransmission_Rate_Excessive"></span><span id="retransmission_rate_excessive"></span><span id="RETRANSMISSION_RATE_EXCESSIVE"></span>

**Übermäßige Neuübertragungsrate** (46)


</dt> <dd></dd> <dt>

<span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>

**Softwarefehler** (47)


</dt> <dd></dd> <dt>

<span id="Software_Program_Abnormally_Terminated"></span><span id="software_program_abnormally_terminated"></span><span id="SOFTWARE_PROGRAM_ABNORMALLY_TERMINATED"></span>

**Nicht normal beendetes Softwareprogramm** (48)


</dt> <dd></dd> <dt>

<span id="Software_Program_Error__Incorrect_Results_"></span><span id="software_program_error__incorrect_results_"></span><span id="SOFTWARE_PROGRAM_ERROR__INCORRECT_RESULTS_"></span>

**Softwareprogrammfehler (falsche Ergebnisse)** (49)


</dt> <dd></dd> <dt>

<span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>

**Storage Kapazitätsproblem** (50)


</dt> <dd></dd> <dt>

<span id="Temperature_Unacceptable"></span><span id="temperature_unacceptable"></span><span id="TEMPERATURE_UNACCEPTABLE"></span>

**Temperatur nicht akzeptabel** (51)


</dt> <dd></dd> <dt>

<span id="Threshold_Crossed"></span><span id="threshold_crossed"></span><span id="THRESHOLD_CROSSED"></span>

**Schwellenwert überschritten** (52)


</dt> <dd></dd> <dt>

<span id="Timing_Problem"></span><span id="timing_problem"></span><span id="TIMING_PROBLEM"></span>

**Zeitsteuerungsproblem** (53)


</dt> <dd></dd> <dt>

<span id="Toxic_Leak_Detected"></span><span id="toxic_leak_detected"></span><span id="TOXIC_LEAK_DETECTED"></span>

Leak Leak Detected (54) **(Schädlicher Verlust erkannt** (54)


</dt> <dd></dd> <dt>

<span id="Transmit_Failure"></span><span id="transmit_failure"></span><span id="TRANSMIT_FAILURE"></span>

**Übertragungsfehler** (55)


</dt> <dd></dd> <dt>

<span id="Transmitter_Failure"></span><span id="transmitter_failure"></span><span id="TRANSMITTER_FAILURE"></span>

**Senderfehler** (56)


</dt> <dd></dd> <dt>

<span id="Underlying_Resource_Unavailable"></span><span id="underlying_resource_unavailable"></span><span id="UNDERLYING_RESOURCE_UNAVAILABLE"></span>

**Zugrunde liegende Ressource nicht verfügbar** (57)


</dt> <dd></dd> <dt>

<span id="Version_MisMatch"></span><span id="version_mismatch"></span><span id="VERSION_MISMATCH"></span>

**Version MisMatch** (58)


</dt> <dd></dd> <dt>

<span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>

**Vorherige Warnung gelöscht** (59)


</dt> <dd></dd> <dt>

<span id="Login_Attempts_Failed"></span><span id="login_attempts_failed"></span><span id="LOGIN_ATTEMPTS_FAILED"></span>

**Fehler bei Anmeldeversuchen** (60)


</dt> <dd></dd> <dt>

<span id="Software_Virus_Detected"></span><span id="software_virus_detected"></span><span id="SOFTWARE_VIRUS_DETECTED"></span>

Software virus detected (61) **(Software-Virus erkannt** (61)


</dt> <dd></dd> <dt>

<span id="Hardware_Security_Breached"></span><span id="hardware_security_breached"></span><span id="HARDWARE_SECURITY_BREACHED"></span>

**Hardwaresicherheit verletzt** (62)


</dt> <dd></dd> <dt>

<span id="Denial_of_Service_Detected"></span><span id="denial_of_service_detected"></span><span id="DENIAL_OF_SERVICE_DETECTED"></span>

**Denial-of-Service erkannt** (63)


</dt> <dd></dd> <dt>

<span id="Security_Credential_MisMatch"></span><span id="security_credential_mismatch"></span><span id="SECURITY_CREDENTIAL_MISMATCH"></span>

**MisMatch für Sicherheitsanmeldeinformationen** (64)


</dt> <dd></dd> <dt>

<span id="Unauthorized_Access"></span><span id="unauthorized_access"></span><span id="UNAUTHORIZED_ACCESS"></span>

**Nicht autorisierter Zugriff** (65)


</dt> <dd></dd> <dt>

<span id="Alarm_Received"></span><span id="alarm_received"></span><span id="ALARM_RECEIVED"></span>

**Empfangener Alarm** (66)


</dt> <dd></dd> <dt>

<span id="Loss_of_Pointer"></span><span id="loss_of_pointer"></span><span id="LOSS_OF_POINTER"></span>

**Verlust des Zeigers** (67)


</dt> <dd></dd> <dt>

<span id="Payload_Mismatch"></span><span id="payload_mismatch"></span><span id="PAYLOAD_MISMATCH"></span>

**Nutzlastkonflikt** (68)


</dt> <dd></dd> <dt>

<span id="Transmission_Error"></span><span id="transmission_error"></span><span id="TRANSMISSION_ERROR"></span>

**Übertragungsfehler** (69)


</dt> <dd></dd> <dt>

<span id="Excessive_Error_Rate"></span><span id="excessive_error_rate"></span><span id="EXCESSIVE_ERROR_RATE"></span>

**Übermäßige Fehlerrate** (70)


</dt> <dd></dd> <dt>

<span id="Trace_Problem"></span><span id="trace_problem"></span><span id="TRACE_PROBLEM"></span>

**Ablaufverfolgungsproblem** (71)


</dt> <dd></dd> <dt>

<span id="Element_Unavailable"></span><span id="element_unavailable"></span><span id="ELEMENT_UNAVAILABLE"></span>

**Element Nicht verfügbar** (72)


</dt> <dd></dd> <dt>

<span id="Element_Missing"></span><span id="element_missing"></span><span id="ELEMENT_MISSING"></span>

**Element fehlt** (73)


</dt> <dd></dd> <dt>

<span id="Loss_of_Multi_Frame"></span><span id="loss_of_multi_frame"></span><span id="LOSS_OF_MULTI_FRAME"></span>

**Verlust mehrerer Frames** (74)


</dt> <dd></dd> <dt>

<span id="Broadcast_Channel_Failure"></span><span id="broadcast_channel_failure"></span><span id="BROADCAST_CHANNEL_FAILURE"></span>

**Broadcastkanalfehler** (75)


</dt> <dd></dd> <dt>

<span id="Invalid_Message_Received"></span><span id="invalid_message_received"></span><span id="INVALID_MESSAGE_RECEIVED"></span>

**Ungültige empfangene Nachricht** (76)


</dt> <dd></dd> <dt>

<span id="Routing_Failure"></span><span id="routing_failure"></span><span id="ROUTING_FAILURE"></span>

**Routingfehler** (77)


</dt> <dd></dd> <dt>

<span id="Backplane_Failure"></span><span id="backplane_failure"></span><span id="BACKPLANE_FAILURE"></span>

**Backplane-Fehler** (78)


</dt> <dd></dd> <dt>

<span id="Identifier_Duplication"></span><span id="identifier_duplication"></span><span id="IDENTIFIER_DUPLICATION"></span>

**Bezeichnerduplizierung** (79)


</dt> <dd></dd> <dt>

<span id="Protection_Path_Failure"></span><span id="protection_path_failure"></span><span id="PROTECTION_PATH_FAILURE"></span>

**Schutzpfadfehler** (80)


</dt> <dd></dd> <dt>

<span id="Sync_Loss_or_Mismatch"></span><span id="sync_loss_or_mismatch"></span><span id="SYNC_LOSS_OR_MISMATCH"></span>

**Synchronisierungsverlust oder -konflikt** (81)


</dt> <dd></dd> <dt>

<span id="Terminal_Problem"></span><span id="terminal_problem"></span><span id="TERMINAL_PROBLEM"></span>

**Terminalproblem** (82)


</dt> <dd></dd> <dt>

<span id="Real_Time_Clock_Failure"></span><span id="real_time_clock_failure"></span><span id="REAL_TIME_CLOCK_FAILURE"></span>

**Echtzeituhrfehler** (83)


</dt> <dd></dd> <dt>

<span id="Antenna_Failure"></span><span id="antenna_failure"></span><span id="ANTENNA_FAILURE"></span>

**Antennefehler** (84)


</dt> <dd></dd> <dt>

<span id="Battery_Charging_Failure"></span><span id="battery_charging_failure"></span><span id="BATTERY_CHARGING_FAILURE"></span>

**Akkuladefehler** (85)


</dt> <dd></dd> <dt>

<span id="Disk_Failure"></span><span id="disk_failure"></span><span id="DISK_FAILURE"></span>

**Datenträgerfehler** (86)


</dt> <dd></dd> <dt>

<span id="Frequency_Hopping_Failure"></span><span id="frequency_hopping_failure"></span><span id="FREQUENCY_HOPPING_FAILURE"></span>

Frequency Hopping Failure (87) **(Fehler beim Springen** mit Häufigkeit (87))


</dt> <dd></dd> <dt>

<span id="Loss_of_Redundancy"></span><span id="loss_of_redundancy"></span><span id="LOSS_OF_REDUNDANCY"></span>

**Verlust der Redundanz** (88)


</dt> <dd></dd> <dt>

<span id="Power_Supply_Failure"></span><span id="power_supply_failure"></span><span id="POWER_SUPPLY_FAILURE"></span>

**Stromversorgungsfehler** (89)


</dt> <dd></dd> <dt>

<span id="Signal_Quality_Problem"></span><span id="signal_quality_problem"></span><span id="SIGNAL_QUALITY_PROBLEM"></span>

**Signalqualitätsproblem** (90)


</dt> <dd></dd> <dt>

<span id="Battery_Discharging"></span><span id="battery_discharging"></span><span id="BATTERY_DISCHARGING"></span>

**Akkuladevorgang** (91)


</dt> <dd></dd> <dt>

<span id="Battery_Failure"></span><span id="battery_failure"></span><span id="BATTERY_FAILURE"></span>

**Akkuausfall** (92)


</dt> <dd></dd> <dt>

<span id="Commercial_Power_Problem"></span><span id="commercial_power_problem"></span><span id="COMMERCIAL_POWER_PROBLEM"></span>

**Kommerzielles Energieproblem** (93)


</dt> <dd></dd> <dt>

<span id="Fan_Failure"></span><span id="fan_failure"></span><span id="FAN_FAILURE"></span>

**Lüfterfehler** (94)


</dt> <dd></dd> <dt>

<span id="Engine_Failure"></span><span id="engine_failure"></span><span id="ENGINE_FAILURE"></span>

**Engine-Fehler** (95)


</dt> <dd></dd> <dt>

<span id="Sensor_Failure"></span><span id="sensor_failure"></span><span id="SENSOR_FAILURE"></span>

**Sensorfehler** (96)


</dt> <dd></dd> <dt>

<span id="Fuse_Failure"></span><span id="fuse_failure"></span><span id="FUSE_FAILURE"></span>

Fuse Failure (97) **(Fuse-Fehler** (97))


</dt> <dd></dd> <dt>

<span id="Generator_Failure"></span><span id="generator_failure"></span><span id="GENERATOR_FAILURE"></span>

**Generatorfehler** (98)


</dt> <dd></dd> <dt>

<span id="Low_Battery"></span><span id="low_battery"></span><span id="LOW_BATTERY"></span>

**Niedrige Akkukapazität** (99)


</dt> <dd></dd> <dt>

<span id="Low_Fuel"></span><span id="low_fuel"></span><span id="LOW_FUEL"></span>

**Niedriger Kraftstoffverbrauch** (100)


</dt> <dd></dd> <dt>

<span id="Low_Water"></span><span id="low_water"></span><span id="LOW_WATER"></span>

**Niedriges Wasser** (101)


</dt> <dd></dd> <dt>

<span id="Explosive_Gas"></span><span id="explosive_gas"></span><span id="EXPLOSIVE_GAS"></span>

**Gas** (102)


</dt> <dd></dd> <dt>

<span id="High_Winds"></span><span id="high_winds"></span><span id="HIGH_WINDS"></span>

**Hohe Winde** (103)


</dt> <dd></dd> <dt>

<span id="Ice_Buildup"></span><span id="ice_buildup"></span><span id="ICE_BUILDUP"></span>

**Ice Buildup** (104)


</dt> <dd></dd> <dt>

<span id="Smoke"></span><span id="smoke"></span><span id="SMOKE"></span>

**Feuer** (105)


</dt> <dd></dd> <dt>

<span id="Memory_Mismatch"></span><span id="memory_mismatch"></span><span id="MEMORY_MISMATCH"></span>

**Arbeitsspeicherkonflikt** (106)


</dt> <dd></dd> <dt>

<span id="Out_of_CPU_Cycles"></span><span id="out_of_cpu_cycles"></span><span id="OUT_OF_CPU_CYCLES"></span>

Out of CPU Cycles (107) **(Aus cpu-Zyklen** (107))


</dt> <dd></dd> <dt>

<span id="Software_Environment_Problem"></span><span id="software_environment_problem"></span><span id="SOFTWARE_ENVIRONMENT_PROBLEM"></span>

**Softwareumgebungsproblem** (108)


</dt> <dd></dd> <dt>

<span id="Software_Download_Failure"></span><span id="software_download_failure"></span><span id="SOFTWARE_DOWNLOAD_FAILURE"></span>

**Softwaredownloadfehler** (109)


</dt> <dd></dd> <dt>

<span id="Element_Reinitialized"></span><span id="element_reinitialized"></span><span id="ELEMENT_REINITIALIZED"></span>

**Element erneut initialisiert** (110)


</dt> <dd></dd> <dt>

<span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>

**Timeout** (111)


</dt> <dd></dd> <dt>

<span id="Logging_Problems"></span><span id="logging_problems"></span><span id="LOGGING_PROBLEMS"></span>

**Protokollierungsprobleme** (112)


</dt> <dd></dd> <dt>

<span id="Leak_Detected"></span><span id="leak_detected"></span><span id="LEAK_DETECTED"></span>

Leak Detected (113) **(Erkannter Verlust** (113))


</dt> <dd></dd> <dt>

<span id="Protection_Mechanism_Failure"></span><span id="protection_mechanism_failure"></span><span id="PROTECTION_MECHANISM_FAILURE"></span>

**Schutzmechanismusfehler** (114)


</dt> <dd></dd> <dt>

<span id="Protecting_Resource_Failure"></span><span id="protecting_resource_failure"></span><span id="PROTECTING_RESOURCE_FAILURE"></span>

**Schützen von Ressourcenfehlern** (115)


</dt> <dd></dd> <dt>

<span id="Database_Inconsistency"></span><span id="database_inconsistency"></span><span id="DATABASE_INCONSISTENCY"></span>

**Datenbankinkonsistenz** (116)


</dt> <dd></dd> <dt>

<span id="Authentication_Failure"></span><span id="authentication_failure"></span><span id="AUTHENTICATION_FAILURE"></span>

**Authentifizierungsfehler** (117)


</dt> <dd></dd> <dt>

<span id="Breach_of_Confidentiality"></span><span id="breach_of_confidentiality"></span><span id="BREACH_OF_CONFIDENTIALITY"></span>

**Verletzung der Vertraulichkeit** (118)


</dt> <dd></dd> <dt>

<span id="Cable_Tamper"></span><span id="cable_tamper"></span><span id="CABLE_TAMPER"></span>

**Kabelmanipulation** (119)


</dt> <dd></dd> <dt>

<span id="Delayed_Information"></span><span id="delayed_information"></span><span id="DELAYED_INFORMATION"></span>

**Verzögerte Informationen** (120)


</dt> <dd></dd> <dt>

<span id="Duplicate_Information"></span><span id="duplicate_information"></span><span id="DUPLICATE_INFORMATION"></span>

**Doppelte Informationen** (121)


</dt> <dd></dd> <dt>

<span id="Information_Missing"></span><span id="information_missing"></span><span id="INFORMATION_MISSING"></span>

**Informationen fehlen** (122)


</dt> <dd></dd> <dt>

<span id="Information_Modification"></span><span id="information_modification"></span><span id="INFORMATION_MODIFICATION"></span>

**Änderung von Informationen** (123)


</dt> <dd></dd> <dt>

<span id="Information_Out_of_Sequence"></span><span id="information_out_of_sequence"></span><span id="INFORMATION_OUT_OF_SEQUENCE"></span>

Information Out of Sequence (124) **(Informationen außerhalb der Sequenz** (124))


</dt> <dd></dd> <dt>

<span id="Key_Expired"></span><span id="key_expired"></span><span id="KEY_EXPIRED"></span>

**Schlüssel abgelaufen** (125)


</dt> <dd></dd> <dt>

<span id="Non-Repudiation_Failure"></span><span id="non-repudiation_failure"></span><span id="NON-REPUDIATION_FAILURE"></span>

**Nichtabweisungsfehler** (126)


</dt> <dd></dd> <dt>

<span id="Out_of_Hours_Activity"></span><span id="out_of_hours_activity"></span><span id="OUT_OF_HOURS_ACTIVITY"></span>

**Aktivität außerhalb der Geschäftszeiten** (127)


</dt> <dd></dd> <dt>

<span id="Out_of_Service"></span><span id="out_of_service"></span><span id="OUT_OF_SERVICE"></span>

**Out of Service** (128)


</dt> <dd></dd> <dt>

<span id="Procedural_Error"></span><span id="procedural_error"></span><span id="PROCEDURAL_ERROR"></span>

**Prozeduraler Fehler** (129)


</dt> <dd></dd> <dt>

<span id="Unexpected_Information"></span><span id="unexpected_information"></span><span id="UNEXPECTED_INFORMATION"></span>

**Unerwartete Informationen** (130)


</dt> <dd></dd> </dl>

</dd> <dt>

**ProbableCauseDescription**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**ProbableCause**")
</dt> </dl>

Zusätzliche Informationen im Zusammenhang mit der **Eigenschaft "ProbableCause".**

</dd> <dt>

**ProviderName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Der Name des Anbieters, der die Angabe generiert hat.

</dd> <dt>

**RecommendedActions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU \| X733. Vorgeschlagene Reparaturaktionen")
</dt> </dl>

Beschreibungen der empfohlenen Aktionen, die zur Behebung der Ursache der Benachrichtigung erforderlich sind, sind frei.

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Der **CreationClassName-Wert** des Bereichssystems für den Anbieter, der die Anzeige generiert hat.

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Der Bereichssystemname für den Anbieter, der die Anzeige generiert hat.

</dd> <dt>

**Populär**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU \| X733. TrendIndication")
</dt> </dl>

Stellt Informationen zu Trends bereit: Nach oben, unten oder ohne Änderung.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Nicht zutreffend** (1)


</dt> <dd></dd> <dt>

<span id="Trending_Up"></span><span id="trending_up"></span><span id="TRENDING_UP"></span>

Trending Up (2) **(Trending Up** (2)


</dt> <dd></dd> <dt>

<span id="Trending_Down"></span><span id="trending_down"></span><span id="TRENDING_DOWN"></span>

**Trend nach unten** (3)


</dt> <dd></dd> <dt>

<span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>

**Keine Änderung** (4)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ ProcessIndication**](cim-processindication.md)
</dt> </dl>

 

