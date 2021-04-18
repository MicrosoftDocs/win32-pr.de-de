---
description: Stellt die Definitions Aspekte einer Metrik dar.
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
ms.openlocfilehash: 8d1edbd722e3bf87631371b5650576917a7cfb39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106354854"
---
# <a name="msvm_basemetricdefinition-class"></a>MSVM \_ basemetricdefinition-Klasse

Stellt die Definitions Aspekte einer Metrik dar. Die **MSVM \_ basemetricdefinition** -Klasse muss den CIM- [**\_ managedelements**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) zugeordnet werden, auf die Sie angewendet wird.

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

Die **MSVM \_ basemetricdefinition** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ basemetricdefinition** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Breakdowndimensionen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Definiert eine oder mehrere Zeichen folgen, die verwendet werden können, um Abfragen für die Metrikwerte in einer bestimmten Dimension zu verfeinern. Ein Beispiel hierfür ist ein Transaktions Name, der das Unterbrechen des Gesamtwerts für alle Transaktionen in eine Gruppe von Werten ermöglicht, eine für jeden Transaktions Namen. Andere Beispiele hierfür sind Anwendungssystem-oder Benutzergruppen Name. Die Zeichen folgen sind ein kostenloses Format und sollten für die Endbenutzer der Metrikdaten sinnvoll sein. Die Zeichen folgen geben an, welche aufbruchdimensionen für diese metrikdefinition von der zugrunde liegenden Instrumentation unterstützt werden. Diese Eigenschaft wird von **CIM \_ basemetricdefinition** geerbt.

</dd> <dt>

**Bares**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Beschreibt die Merkmale der Metrik für die Durchführung von Berechnungen. Diese Eigenschaft wird von **CIM \_ basemetricdefinition** geerbt. Dieser Wert kann **null** oder einer der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                                   | Bedeutung                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span><dl> <dt>**Nicht berechenbare**</dt> <dt>1</dt> </dl> | Der Wert kann nicht berechnet werden. Z. b. eine Zeichenfolge.<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span><dl> <dt>**Summier Bare**</dt> <dt>2</dt> </dl>                         | Der Wert kann über viele Instanzen summiert werden. Wenn es sich bei jedem Sicherungsauftrag beispielsweise um eine Arbeitseinheit handelt und jeder Auftrag im Durchschnitt 27.000 Dateien sichert, werden 100 Sicherungsaufträge 2,7 Millionen Dateien verarbeitet.<br/>                                                                                                                                                                 |
| <span id="Non-summable_"></span><span id="non-summable_"></span><span id="NON-SUMMABLE_"></span><dl> <dt> **Nicht summier Bare**</dt> <dt>3</dt> </dl>    | Dieser Wert kann nicht über viele Instanzen summiert werden. Ein Beispiel wäre eine Metrik, die die Länge der Warteschlange beim Eintreffen eines Auftrags auf einem Server misst. Wenn jeder Auftrag eine Arbeitseinheit ist und die durchschnittliche Warteschlangen Länge bei Eintreffen der einzelnen Aufträge 33 beträgt, ist es nicht sinnvoll, zu sagen, dass die Warteschlangen Länge für 100 Aufträge 3300 beträgt. Es ist sinnvoll, zu sagen, dass der Mittelwert 33 ist.<br/> |



 

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des-Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**ChangeType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, wie sich der Metrikwert in Form typischer Kombinationen von präziserer Attributen ändert, wie z. b. Richtungsänderungen, Mindest-und Höchstwerte und Wrapping Semantik. Diese Eigenschaft wird von **CIM \_ basemetricdefinition** geerbt.



| Wert                                                                                                                                                                                                                                                                       | Bedeutung                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Unbekannter**</dt> Wert <dt>0</dt> </dl>                                                 | Der Metrik-Designer hat den **ChangeType** nicht qualifiziert.<br/>                                                                                                                              |
| <span id="N_A"></span><span id="n_a"></span><dl> <dt>**N/v**</dt> <dt>2</dt> </dl>                                                                                       | Wenn die **iscontinuous** -Eigenschaft den Wert "false" hat, ist **ChangeType** nicht sinnvoll und muss auf "N/v" festgelegt werden.<br/>                                                                             |
| <span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span><dl> <dt>**Gegen**</dt> <dt>3</dt> </dl>                                                 | Die Metrik ist eine gegen Metrik. Diese haben nicht negative ganzzahlige Werte, die sich erhöhen, bis die maximale darstellbare Zahl erreicht ist, und dann umschließen und die Zunahme von 0 beginnen.<br/> |
| <span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span><dl> <dt>**Messgerät**</dt> <dt>4</dt> </dl>                                                         | Die Metrik ist eine Messgeräte Metrik. Diese verfügen über ganzzahlige oder Gleit Komma Werte, die beliebig vergrößert und verringert werden können.<br/>                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF reserviert**</dt> <dt>5.. 32767</dt> </dl>                  |                                                                                                                                                                                                  |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <dt> **Anbieter reserviert**</dt> <dt>32768.. 65535</dt> </dl> | Anbieter können die **ChangeType** -Eigenschaft im reservierten Bereich des Anbieters erweitern.<br/>                                                                                                          |



 

</dd> <dt>

**DataType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Datentyp der Metrik. Diese Eigenschaft wird von **CIM \_ basemetricdefinition** geerbt.

<dl> <dt>

<span id="boolean"></span><span id="BOOLEAN"></span>**boolescher** Wert (1)
</dt> <dt>

<span id="char16"></span><span id="CHAR16"></span>**char16** (2)
</dt> <dt>

<span id="datetime"></span><span id="DATETIME"></span>**DateTime** (3)
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

<span id="string"></span><span id="STRING"></span>**Zeichenfolge** (10)
</dt> <dt>

<span id="uint16"></span><span id="UINT16"></span>**UInt16** (11)
</dt> <dt>

<span id="uint32"></span><span id="UINT32"></span>**UInt32** (12)
</dt> <dt>

<span id="uint64"></span><span id="UINT64"></span>**UInt64** (13)
</dt> <dt>

<span id="uint8_"></span><span id="UINT8_"></span>**Uint8** (14)
</dt> </dl>

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeige Name für das-Objekt. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Gatheringtype**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, wie die Metrikwerte von der zugrunde liegenden Instrumentation erfasst werden. Dies ermöglicht es der Client Anwendung, die richtige Metrik für den Zweck auszuwählen. Diese Eigenschaft wird von **CIM \_ basemetricdefinition** geerbt. Dieser Wert kann **null** oder einer der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                                                       | Bedeutung                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Unbekannter**</dt> Wert <dt>0</dt> </dl>                                                 | Der sammungstyp ist nicht bekannt.<br/>                                                                                                                                                                                                                               |
| <span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span><dl> <dt>**OnChange**</dt> <dt>2</dt> </dl>                                             | Die Metrikwerte werden sofort aktualisiert, wenn sich die Werte in der gemessenen Ressource ändern.<br/>                                                                                                                                                              |
| <span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span><dl> <dt>**Periodisch**</dt> <dt>3</dt> </dl>                                             | Die Metrikwerte werden regelmäßig aktualisiert. Beispielsweise wird für eine Client Anwendung ein Metrikwert, der sich auf die aktuelle Zeit bezieht, während jedes Sammlungs Intervalls konstant angezeigt und dann am Ende jedes Sammlungs Intervalls auf den neuen Wert springt.<br/> |
| <span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span><dl> <dt>**OnRequest**</dt> <dt>4</dt> </dl>                                         | Der Metrikwert wird jedes Mal bestimmt, wenn er von einer Client Anwendung gelesen wird.<br/>                                                                                                                                                                                        |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF reserviert**</dt> <dt>5.. 32767</dt> </dl>                  |                                                                                                                                                                                                                                                                           |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <dt> **Anbieter reserviert**</dt> <dt>32768.. 65535</dt> </dl> |                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

**Id**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Eine Zeichenfolge, die die metrikdefinition eindeutig identifiziert. Diese Eigenschaft wird von **CIM \_ basemetricdefinition** geerbt.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Eine Zeichenfolge, die eine Instanz dieser Klasse eindeutig identifiziert. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**IsContinuous**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Metrikwert kontinuierlich oder Skalar ist. Leistungsmetriken sind ein Beispiel für eine kontinuierliche Metrik. Beispiele für skalare Metriken sind Fehlercodes oder Betriebszustände. Kontinuierliche Metriken können mit der "größer als"-Beziehung verglichen werden. Diese Eigenschaft wird von **CIM \_ basemetricdefinition** geerbt.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der Metrik. Diese Eigenschaft wird von **CIM \_ basemetricdefinition** geerbt.

</dd> <dt>

**Programmaticunits**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Identifiziert die bestimmten Einheiten eines Werts. Der Wert dieser Eigenschaft ist ein gültiger Wert des Qualifizierers für programmatische Einheiten, wie in Anhang C. 1 von [DSP0004 v 2.4](https://www.dmtf.org/sites/default/files/standards/documents/DSP0004_2.5.0.pdf) oder höher definiert. Diese Eigenschaft wird von **CIM \_ basemetricdefinition** geerbt.

</dd> <dt>

**Timescope**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Zeitbereich an, für den der Metrikwert gilt. Diese Eigenschaft wird von **CIM \_ basemetricdefinition** geerbt.



| Wert                                                                                                                                                                                                                                                                       | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Unbekannter**</dt> Wert <dt>0</dt> </dl>                                                 | Der Zeitbereich wurde vom Metrik-Designer nicht qualifiziert oder ist dem Anbieter nicht bekannt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="Point"></span><span id="point"></span><span id="POINT"></span><dl> <dt>**Punkt**</dt> <dt>2</dt> </dl>                                                         | Die Metrik gilt für einen bestimmten Zeitpunkt. Die **timestamp** -Eigenschaft gibt auf der entsprechenden [**MSVM \_ basemetricvalue**](msvm-basemetricvalue.md) -Instanz den Zeitpunkt an, und die **Duration** -Eigenschaft ist immer 0.<br/>                                                                                                                                                                                                                                                                                              |
| <span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span><dl> <dt>**Intervall**</dt> <dt>3</dt> </dl>                                             | Die Metrik gilt für ein Zeitintervall. Die **timestamp** -Eigenschaft gibt das Ende des Zeitintervalls an, und die **Duration** -Eigenschaft gibt deren Dauer an. [**\_**](msvm-basemetricvalue.md)<br/>                                                                                                                                                                                                                                                                        |
| <span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span><dl> <dt>**Startupinterval**</dt> <dt>4</dt> </dl>                 | Die Metrik bezieht sich auf ein Zeitintervall, das beim Start der gemessenen Ressource begonnen hat (d. h. das von metricdefforme zugeordnete managedelta). Die **timestamp** -Eigenschaft gibt das Ende des Zeitintervalls in den entsprechenden [**MSVM \_ basemetricvalue**](msvm-basemetricvalue.md) -Instanzen an. Wenn die **Duration** -Eigenschaft den Wert 0 hat, gibt dies an, dass die Startzeit der gemessenen Ressource unbekannt ist. Andernfalls gibt **Duration** die Dauer zwischen dem Start der Ressource und dem **Zeitstempel** an.<br/> |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF reserviert**</dt> <dt>5.. 32767</dt> </dl>                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <dt> **Anbieter reserviert**</dt> <dt>32768.. 65535</dt> </dl> |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

**Einheiten**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Identifiziert die bestimmten Einheiten eines Werts, z. b. "Megabyte". Diese Eigenschaft wird von **CIM \_ basemetricdefinition** geerbt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

