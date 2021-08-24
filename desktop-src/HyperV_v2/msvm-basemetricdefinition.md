---
description: Stellt die Definitionsaspekte einer Metrik dar.
ms.assetid: 861a69f6-a3bf-4e18-a9c2-931632e3cccc
title: Msvm_BaseMetricDefinition-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BaseMetricDefinition
- Msvm_BaseMetricDefinition.InstanceID
- Msvm_BaseMetricDefinition.Caption
- Msvm_BaseMetricDefinition.Description
- Msvm_BaseMetricDefinition.ElementName
- Msvm_BaseMetricDefinition.Id
- Msvm_BaseMetricDefinition.Name
- Msvm_BaseMetricDefinition.DataType
- Msvm_BaseMetricDefinition.Calculable
- Msvm_BaseMetricDefinition.Units
- Msvm_BaseMetricDefinition.BreakdownDimensions
- Msvm_BaseMetricDefinition.IsContinuous
- Msvm_BaseMetricDefinition.ChangeType
- Msvm_BaseMetricDefinition.TimeScope
- Msvm_BaseMetricDefinition.GatheringType
- Msvm_BaseMetricDefinition.ProgrammaticUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4193f934dd17224091974a705288831e28253876d05ca1b5fc4b99c9c70424e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790240"
---
# <a name="msvm_basemetricdefinition-class"></a>Msvm \_ BaseMetricDefinition-Klasse

Stellt die Definitionsaspekte einer Metrik dar. Die **Msvm \_ BaseMetricDefinition-Klasse** sollte den [**CIM \_ ManagedElements**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) zugeordnet werden, für die sie gilt.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BaseMetricDefinition : CIM_BaseMetricDefinition
{
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  string  Id;
  string  Name;
  uint16  DataType;
  uint16  Calculable;
  string  Units;
  string  BreakdownDimensions[];
  boolean IsContinuous;
  uint16  ChangeType;
  uint16  TimeScope;
  uint16  GatheringType;
  string  ProgrammaticUnits;
};
```

## <a name="members"></a>Member

Die **Msvm \_ BaseMetricDefinition-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ BaseMetricDefinition-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**BreakdownDimensions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Definiert eine oder mehrere Zeichenfolgen, die zum Verfeinern (Aufbrechen) von Abfragen für die Metrikwerte entlang einer bestimmten Dimension verwendet werden können. Ein Beispiel ist ein Transaktionsname, der es ermöglicht, den Gesamtwert für alle Transaktionen in einen Satz von Werten zu unterlegen, einen für jeden Transaktionsnamen. Andere Beispiele können der Name des Anwendungssystems oder der Benutzergruppe sein. Die Zeichenfolgen sind ein kostenloses Format und sollten für die Endbenutzer der Metrikdaten aussagekräftig sein. Die Zeichenfolgen geben an, welche Aufbruchdimensionen für diese Metrikdefinition von der zugrunde liegenden Instrumentierung unterstützt werden. Diese Eigenschaft wird von **CIM \_ BaseMetricDefinition geerbt.**

</dd> <dt>

**Kalkulierbare**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Beschreibt die Merkmale der Metrik zum Ausführen von Berechnungen. Diese Eigenschaft wird von **CIM \_ BaseMetricDefinition geerbt.** Dies kann **NULL oder** einer der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                                   | Bedeutung                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span><dl> <dt>**Nicht berechenbare**</dt> <dt>1</dt> </dl> | Der Wert kann nicht berechnet werden. Beispiel: eine Zeichenfolge.<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span><dl> <dt>**Summierbar**</dt> <dt>2</dt> </dl>                         | Der Wert kann über viele Instanzen summiert werden. Wenn z. B. jeder Sicherungsauftrag eine Arbeitseinheit ist und jeder Auftrag durchschnittlich 27.000 Dateien gesichert hat, verarbeiteten 100 Sicherungsaufträge 2.700.000 Dateien.<br/>                                                                                                                                                                 |
| <span id="Non-summable_"></span><span id="non-summable_"></span><span id="NON-SUMMABLE_"></span><dl> <dt> **Nicht summierbar**</dt> <dt>3</dt> </dl>    | Dieser Wert kann nicht über viele Instanzen summiert werden. Ein Beispiel wäre eine Metrik, die die Länge der Warteschlange misst, wenn ein Auftrag auf einem Server eintrifft. Wenn jeder Auftrag eine Arbeitseinheit ist und die durchschnittliche Warteschlangenlänge beim Eintreffen jedes Auftrags 33 beträgt, ist es nicht sinnvoll zu sagen, dass die Warteschlangenlänge für 100 Aufträge 3300 beträgt. Es ist sinnvoll zu sagen, dass der Mittelwert 33 ist.<br/> |



 

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**ChangeType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, wie sich der Metrikwert in Form typischer Kombinationen von feineren Attributen wie Richtungsänderung, Minimal- und Höchstwerten und Wrappingsemantik ändert. Diese Eigenschaft wird von **CIM \_ BaseMetricDefinition geerbt.**



| Wert                                                                                                                                                                                                                                                                       | Bedeutung                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Unbekannt**</dt> <dt>0</dt> </dl>                                                 | Der Metrik-Designer hat den **ChangeType nicht qualifiziert.**<br/>                                                                                                                              |
| <span id="N_A"></span><span id="n_a"></span><dl> <dt>**N/A**</dt> <dt>2</dt> </dl>                                                                                       | Wenn die **IsContinuous-Eigenschaft** "false" ist, ist **ChangeType** nicht sinnvoll und muss auf "N/A" festgelegt werden.<br/>                                                                             |
| <span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span><dl> <dt>**Zähler**</dt> <dt>3</dt> </dl>                                                 | Die Metrik ist eine Zählermetrik. Diese verfügen über nicht negative ganzzahlige Werte, die sich erhöhen, bis die maximale darstellbare Zahl erreicht ist, und dann umschließen und beginnen, von 0 zu steigen.<br/> |
| <span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span><dl> <dt>**Messgerät**</dt> <dt>4</dt> </dl>                                                         | Die Metrik ist eine Messgerätmetrik. Diese verfügen über Ganzzahl- oder Gleitkommawerte, die beliebig erhöht und verringert werden können.<br/>                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF Reserved**</dt> <dt>5..32767</dt> </dl>                  |                                                                                                                                                                                                  |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <dt> **Anbieter reserviert**</dt> <dt>32768..65535</dt> </dl> | Anbieter können die **ChangeType-Eigenschaft** im reservierten Bereich des Anbieters erweitern.<br/>                                                                                                          |



 

</dd> <dt>

**DataType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Datentyp der Metrik. Diese Eigenschaft wird von **CIM \_ BaseMetricDefinition geerbt.**

<dl> <dt>

<span id="boolean"></span><span id="BOOLEAN"></span>**boolean** (1)
</dt> <dt>

<span id="char16"></span><span id="CHAR16"></span>**char16** (2)
</dt> <dt>

<span id="datetime"></span><span id="DATETIME"></span>**datetime** (3)
</dt> <dt>

<span id="real32"></span><span id="REAL32"></span>**real32** (4)
</dt> <dt>

<span id="real64"></span><span id="REAL64"></span>**real64** (5)
</dt> <dt>

<span id="sint16"></span><span id="SINT16"></span>**sint16** (6)
</dt> <dt>

<span id="sint32"></span><span id="SINT32"></span>**sint32** (7)
</dt> <dt>

<span id="sint64"></span><span id="SINT64"></span>**sint64** (8)
</dt> <dt>

<span id="sint8"></span><span id="SINT8"></span>**sint8** (9)
</dt> <dt>

<span id="string"></span><span id="STRING"></span>**string** (10)
</dt> <dt>

<span id="uint16"></span><span id="UINT16"></span>**uint16** (11)
</dt> <dt>

<span id="uint32"></span><span id="UINT32"></span>**uint32** (12)
</dt> <dt>

<span id="uint64"></span><span id="UINT64"></span>**uint64** (13)
</dt> <dt>

<span id="uint8_"></span><span id="UINT8_"></span>**uint8** (14 )
</dt> </dl>

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeigename für das Objekt. Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**GatheringType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, wie die Metrikwerte von der zugrunde liegenden Instrumentierung erfasst werden. Dadurch kann die Clientanwendung die richtige Metrik für diesen Zweck auswählen. Diese Eigenschaft wird von **CIM \_ BaseMetricDefinition geerbt.** Dies kann **NULL** oder einer der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                                                       | Bedeutung                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Unbekannt**</dt> <dt>0</dt> </dl>                                                 | Der Sammlungstyp ist nicht bekannt.<br/>                                                                                                                                                                                                                               |
| <span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span><dl> <dt>**OnChange**</dt> <dt>2</dt> </dl>                                             | Die Metrikwerte werden sofort aktualisiert, wenn sich die Werte innerhalb der gemessenen Ressource ändern.<br/>                                                                                                                                                              |
| <span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span><dl> <dt>**Periodisch**</dt> <dt>3</dt> </dl>                                             | Die Metrikwerte werden regelmäßig aktualisiert. Für eine Clientanwendung wird beispielsweise ein Metrikwert, der für die aktuelle Zeit gilt, während jedes Erfassungsintervalls konstant angezeigt und dann am Ende jedes Erfassungsintervalls zum neuen Wert springt.<br/> |
| <span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span><dl> <dt>**OnRequest**</dt> <dt>4</dt> </dl>                                         | Der Metrikwert wird jedes Mal bestimmt, wenn er von einer Clientanwendung gelesen wird.<br/>                                                                                                                                                                                        |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF Reserved**</dt> <dt>5..32767</dt> </dl>                  |                                                                                                                                                                                                                                                                           |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <dt> **Reservierter Anbieter**</dt> <dt>32768..65535</dt> </dl> |                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

**Id**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Eine Zeichenfolge, die die Metrikdefinition eindeutig identifiziert. Diese Eigenschaft wird von **CIM \_ BaseMetricDefinition** geerbt.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Eine Zeichenfolge, die eine Instanz dieser Klasse eindeutig identifiziert. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**IsContinuous**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Metrikwert kontinuierlich oder skalar ist. Leistungsmetriken sind ein Beispiel für eine kontinuierliche Metrik. Beispiele für skalare Metriken sind Fehlercodes oder Betriebszustände. Kontinuierliche Metriken können mithilfe der Beziehung "größer als" verglichen werden. Diese Eigenschaft wird von **CIM \_ BaseMetricDefinition** geerbt.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der Metrik. Diese Eigenschaft wird von **CIM \_ BaseMetricDefinition** geerbt.

</dd> <dt>

**ProgrammaticUnits**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Identifiziert die spezifischen Einheiten eines Werts. Der Wert dieser Eigenschaft ist ein rechtlicher Wert des Qualifizierers "Programmgesteuerte Einheiten", wie in Anhang C.1 von [DSP0004 V2.4](https://www.dmtf.org/sites/default/files/standards/documents/DSP0004_2.5.0.pdf) oder höher definiert. Diese Eigenschaft wird von **CIM \_ BaseMetricDefinition** geerbt.

</dd> <dt>

**TimeScope**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Zeitbereich an, für den der Metrikwert gilt. Diese Eigenschaft wird von **CIM \_ BaseMetricDefinition** geerbt.



| Wert                                                                                                                                                                                                                                                                       | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Unbekannt**</dt> <dt>0</dt> </dl>                                                 | Der Zeitbereich wurde vom Metrik-Designer nicht qualifiziert oder ist dem Anbieter unbekannt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="Point"></span><span id="point"></span><span id="POINT"></span><dl> <dt>**Punkt**</dt> <dt>2</dt> </dl>                                                         | Die Metrik gilt für einen Zeitpunkt. In den entsprechenden [**Msvm \_ BaseMetricValue-Instanzen**](msvm-basemetricvalue.md) gibt die **TimeStamp-Eigenschaft** den Zeitpunkt an, und die **Duration-Eigenschaft** ist immer 0.<br/>                                                                                                                                                                                                                                                                                              |
| <span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span><dl> <dt>**Intervall**</dt> <dt>3</dt> </dl>                                             | Die Metrik gilt für ein Zeitintervall. In den entsprechenden [**Msvm \_ BaseMetricValue-Instanzen**](msvm-basemetricvalue.md) gibt die **TimeStamp-Eigenschaft** das Ende des Zeitintervalls an, und die **Duration-Eigenschaft** gibt die Dauer an.<br/>                                                                                                                                                                                                                                                                        |
| <span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span><dl> <dt>**StartupInterval**</dt> <dt>4</dt> </dl>                 | Die Metrik gilt für ein Zeitintervall, das beim Start der gemessenen Ressource begonnen hat (d. b. das von MetricDefForMe zugeordnete ManagedElement). Auf den entsprechenden [**Msvm \_ BaseMetricValue-Instanzen**](msvm-basemetricvalue.md) gibt die **TimeStamp-Eigenschaft** das Ende des Zeitintervalls an. Wenn die **Duration-Eigenschaft** 0 ist, gibt dies an, dass die Startzeit der gemessenen Ressource unbekannt ist. Andernfalls gibt **Duration** die Dauer zwischen dem Start der Ressource und **TimeStamp** an.<br/> |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF Reserved**</dt> <dt>5..32767</dt> </dl>                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <dt> **Reservierter Anbieter**</dt> <dt>32768..65535</dt> </dl> |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

**Einheiten**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Identifiziert die spezifischen Einheiten eines Werts, z. B. "Megabyte". Diese Eigenschaft wird von **CIM \_ BaseMetricDefinition** geerbt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

