---
description: Stellt eine metrikdefinition dar, die die Metadaten für ein CIM \_ metricinstance-Objekt enthält.
ms.assetid: 6abfb0dc-e80b-4ca6-89d9-2e43283d0abe
title: CIM_BaseMetricDefinition-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BaseMetricDefinition
- CIM_BaseMetricDefinition.Id
- CIM_BaseMetricDefinition.Name
- CIM_BaseMetricDefinition.DataType
- CIM_BaseMetricDefinition.Calculable
- CIM_BaseMetricDefinition.Units
- CIM_BaseMetricDefinition.BreakdownDimensions
- CIM_BaseMetricDefinition.IsContinuous
- CIM_BaseMetricDefinition.ChangeType
- CIM_BaseMetricDefinition.TimeScope
- CIM_BaseMetricDefinition.GatheringType
- CIM_BaseMetricDefinition.ProgrammaticUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cac965ed1eae59f1c269d897a12e9aa116183eb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350977"
---
# <a name="cim_basemetricdefinition-class"></a>CIM \_ basemetricdefinition-Klasse

Stellt eine metrikdefinition dar, die die Metadaten für ein **CIM \_ metricinstance** -Objekt enthält.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_BaseMetricDefinition : CIM_ManagedElement
{
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

Die **CIM \_ basemetricdefinition** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ basemetricdefinition** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Breakdowndimensionen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array, das freie Format Zeichenfolgen enthält, die verwendet werden können, um Abfragen von [**CIM \_ basemetricvalue**](cim-basemetricvalue.md) -Objekten an einer bestimmten Dimension zu unterbrechen. Die Zeichen folgen sollten für die Endbenutzer der Metrikdaten sinnvoll sein. Außerdem sollten die Zeichen folgen durch die zugrunde liegende Instrumentation angeben, welche aufbruchteil Dimensionen für die metrikdefinition unterstützt werden.

Ein Beispiel hierfür ist ein Transaktions Name, der das Unterbrechen des Gesamtwerts für alle Transaktionen in eine Reihe von Werten zulässt, eine für jeden Transaktions Namen. Bei anderen Beispielen handelt es sich um ein Anwendungssystem oder einen Benutzergruppen Namen.

</dd> <dt>

**Bares**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Merkmale der Metrik, die zum Durchführen von Berechnungen verwendet wird.

<dt>

<span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>

<span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>**Nicht berechenbar** (1)


</dt> <dd>

Eine Zeichenfolge. Arithmetik ist nicht sinnvoll.

</dd> <dt>

<span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>

<span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>**Sumable** (2)


</dt> <dd>

Es ist sinnvoll, diesen Wert über viele Instanzen von zu addieren, z. b. uni-fwork, wie z. b. die Anzahl der Dateien, die in einem Sicherungsauftrag verarbeitet werden. Wenn es sich bei jedem Sicherungsauftrag beispielsweise um einen Unito-work-Vorgang handelt und jeder Auftrag 27.000 Dateien im Durchschnitt sichert, ist es sinnvoll, zu sagen, dass 100 Sicherungsaufträge 2,7 Millionen Dateien verarbeitet haben.

</dd> <dt>

<span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>

<span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>**Nicht summier Bar** (3)


</dt> <dd>

Es ist nicht sinnvoll, diesen Wert über viele Instanzen von Uni-fwork zu addieren. Ein Beispiel wäre eine Metrik, die die Länge der Warteschlange beim Eintreffen eines Auftrags auf einem Server misst. Wenn es sich bei jedem Auftrag um einen unitwork-Vorgang handelt und die durchschnittliche Warteschlangen Länge bei Eintreffen der einzelnen Aufträge 33 beträgt, ist es nicht sinnvoll, zu sagen, dass die Warteschlangen Länge für 100 Aufträge 3300 beträgt. Es ist sinnvoll, zu sagen, dass der Mittelwert 33 ist.

</dd> </dl>

</dd> <dt>

**ChangeType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ basemetricdefinition**".**Iscontinuous**")
</dt> </dl>

Gibt an, wie sich der Metrikwert mithilfe allgemeiner Attribute ändert, wie z. b. Richtungsänderung, Mindest-und Höchstwerte und Wrapping Semantik.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd>

Der Metrik-Designer hat den ChangeType nicht qualifiziert.

</dd> <dt>

<span id="N_A"></span><span id="n_a"></span>

<span id="N_A"></span><span id="n_a"></span>**N/v** (2)


</dt> <dd>

Wenn die Eigenschaft "iscontinuous" den Wert "false" hat, ist ChangeType nicht sinnvoll und muss auf "N/v" festgelegt werden.

</dd> <dt>

<span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>

<span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Counter** (3)


</dt> <dd>

Die Metrik ist eine gegen Metrik. Diese verfügen über nicht negative ganzzahlige Werte, die monoton ansteigen, bis die maximale darstellbare Zahl erreicht und dann umbrochen wird und die Zunahme von 0 beginnt. Solche Leistungsindikatoren, auch als Rollover-Indikatoren bezeichnet, können zum Beispiel zum zählen der Anzahl von Netzwerkfehlern oder der Anzahl der verarbeiteten Transaktionen verwendet werden. Die einzige Möglichkeit für eine Client Anwendung, Wrap-Problem Umgehungen nachzuverfolgen, besteht darin, den Wert des Zählers in angemessenen kurzen Intervallen abzurufen.

</dd> <dt>

<span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>

<span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Messgerät** (4)


</dt> <dd>

Die Metrik ist eine Messgeräte Metrik. Diese verfügen über ganzzahlige oder Gleit Komma Werte, die beliebig vergrößert und verringert werden können. Ein Messgerät darf nicht bei Erreichen der minimalen oder maximalen darstellbaren Zahl eingeschlossen werden, sondern der Wert "Sticks" an dieser Zahl. Minimale oder maximale Werte innerhalb des darstellbaren Wertebereichs, bei dem der Metrikwert "Sticks" ist oder nicht definiert werden kann.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (5.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Anbieter reserviert** (32768.65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**DataType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Datentyp der Metrik.

<dt>

<span id="boolean"></span><span id="BOOLEAN"></span>

**boolescher** Wert (1)


</dt> <dd></dd> <dt>

<span id="char16"></span><span id="CHAR16"></span>

**char16** (2)


</dt> <dd></dd> <dt>

<span id="datetime"></span><span id="DATETIME"></span>

**DateTime** (3)


</dt> <dd></dd> <dt>

<span id="real32"></span><span id="REAL32"></span>

**real32** (4)


</dt> <dd></dd> <dt>

<span id="real64"></span><span id="REAL64"></span>

**real64** (5)


</dt> <dd></dd> <dt>

<span id="sint16"></span><span id="SINT16"></span>

**sint16** (6)


</dt> <dd></dd> <dt>

<span id="sint32"></span><span id="SINT32"></span>

**sint32** (7)


</dt> <dd></dd> <dt>

<span id="sint64"></span><span id="SINT64"></span>

**sint64** (8)


</dt> <dd></dd> <dt>

<span id="sint8"></span><span id="SINT8"></span>

**sint8** (9)


</dt> <dd></dd> <dt>

<span id="string"></span><span id="STRING"></span>

**Zeichenfolge** (10)


</dt> <dd></dd> <dt>

<span id="uint16"></span><span id="UINT16"></span>

**UInt16** (11)


</dt> <dd></dd> <dt>

<span id="uint32"></span><span id="UINT32"></span>

**UInt32** (12)


</dt> <dd></dd> <dt>

<span id="uint64"></span><span id="UINT64"></span>

**UInt64** (13)


</dt> <dd></dd> <dt>

<span id="uint8"></span><span id="UINT8"></span>

**Uint8** (14)


</dt> <dd></dd> </dl>

</dd> <dt>

**Gatheringtype**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, wie die Metrikwerte von der zugrunde liegenden Instrumentation erfasst werden.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd>

Gibt an, dass der gatheringtype nicht bekannt ist.

</dd> <dt>

<span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>

<span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>**OnChange** (2)


</dt> <dd>

Gibt an, dass die CIM-Metrikwerte sofort aktualisiert werden, wenn sich die Werte in der gemessenen Ressource ändern. Die Werte von OnChange-Metriken entsprechen wirklich der aktuellen Situation innerhalb der Ressource. Ein Beispiel hierfür ist die Anzahl der angemeldeten Benutzer, die sofort aktualisiert werden, wenn sich Benutzer anmelden und abmelden.

</dd> <dt>

<span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>

<span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>**Periodisch** (3)


</dt> <dd>

": Gibt an, dass die CIM-Metrikwerte regelmäßig aktualisiert werden. Beispielsweise wird für eine Client Anwendung ein Metrikwert, der auf die aktuelle Zeit angewendet wird, während jedes Sammlungs Intervalls konstant angezeigt und dann am Ende jedes Sammlungs Intervalls auf den neuen Wert überspringt.

</dd> <dt>

<span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>

<span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>**OnRequest** (4)


</dt> <dd>

Gibt an, dass der CIM-Metrikwert bei jedem Lesen durch eine Client Anwendung bestimmt wird. Die Werte von OnRequest-Metriken geben tatsächlich die aktuelle Situation innerhalb der Ressource zurück, wenn jemand Sie anfordert. Allerdings werden Sie nicht als "nicht überwacht" geändert, weshalb das Abonnieren von Wertänderungen von OnRequest-Metriken nicht empfohlen wird.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (5.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Anbieter reserviert** (32768.65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Id**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Die eindeutige ID der metrikdefinition. Die UUID/GUIDs von Open Software Foundation (OSF) werden empfohlen.

</dd> <dt>

**IsContinuous**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True, wenn der Metrikwert kontinuierlich ist. andernfalls false.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der Metrik. Dieser Name muss nicht eindeutig sein, sollte jedoch beschreibend sein und Leerzeichen enthalten.

</dd> <dt>

**Programmaticunits**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die spezifischen Einheiten eines Werts. Der Wert dieser Eigenschaft muss ein gültiger Wert des Qualifizierers für programmgesteuerte Einheiten sein, wie in Anhang C. 1 von DSP0004 v 2.4 oder höher definiert.

</dd> <dt>

**Timescope**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ basemetricvalue**](cim-basemetricvalue.md)".**Zeitstempel**","**CIM \_ basemetricvalue**.**Dauer**")
</dt> </dl>

Der Zeitbereich, der für den Metrik-Designer gilt.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd>

Gibt an, dass der Zeitbereich vom Metrik-Designer nicht qualifiziert wurde oder dem Anbieter unbekannt ist.

</dd> <dt>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>**Punkt** (2)


</dt> <dd>

Gibt an, dass die Metrik für einen bestimmten Zeitpunkt gilt. In den entsprechenden basemetricvalue-Instanzen gibt Timestamp den Zeitpunkt und die Dauer immer 0 an.

</dd> <dt>

<span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>

<span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>**Intervall** (3)


</dt> <dd>

Gibt an, dass die Metrik für ein Zeitintervall gilt. In den entsprechenden basemetricvalue-Instanzen gibt Timestamp das Ende des Zeitintervalls an, und die Dauer gibt deren Dauer an.

</dd> <dt>

<span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>

<span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>**Startupinterval** (4)


</dt> <dd>

Gibt an, dass die Metrik für ein Zeitintervall gilt, das beim Start der gemessenen Ressource begonnen hat (d. h. das von metricdefforme zugeordnete managedelta). In den entsprechenden basemetricvalue-Instanzen gibt Timestamp das Ende des Zeitintervalls an. Wenn Duration gleich 0 ist, gibt dies an, dass die Startzeit der gemessenen Ressource unbekannt ist. Andernfalls gibt Duration die Dauer zwischen dem Start der Ressource und dem Zeitstempel an.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (5.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Anbieter reserviert** (32768.65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Einheiten**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Einheiten der Metrik. Beispiele hierfür sind bytes, Pakete, Aufträge, Dateien, Millisekunden und Amps.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ managedelta**](cim-managedelement.md)
</dt> </dl>

 

