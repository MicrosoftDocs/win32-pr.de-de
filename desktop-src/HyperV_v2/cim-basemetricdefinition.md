---
description: Stellt eine Metrikdefinition dar, die die Metadaten für ein \_ CIM-MetricInstance-Objekt enthält.
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
ms.openlocfilehash: 0614b14f3033da5cf97dfb293f0e9cc130025dbb534331f8ec3386513d8796c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829720"
---
# <a name="cim_basemetricdefinition-class"></a>CIM \_ BaseMetricDefinition-Klasse

Stellt eine Metrikdefinition dar, die die Metadaten für ein **\_ CIM-MetricInstance-Objekt** enthält.

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

Die **CIM \_ BaseMetricDefinition-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ BaseMetricDefinition-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**BreakdownDimensions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array, das freie Formatzeichenfolgen enthält, die zum Aufbrechen von Abfragen von [**CIM \_ BaseMetricValue-Objekten**](cim-basemetricvalue.md) entlang einer bestimmten Dimension verwendet werden können. Die Zeichenfolgen sollten für die Endbenutzer der Metrikdaten aussagekräftig sein. Darüber hinaus sollten die Zeichenfolgen angeben, welche Aufbruchdimensionen von der zugrunde liegenden Instrumentierung für die Metrikdefinition unterstützt werden.

Ein Beispiel ist ein Transaktionsname, mit dem der Gesamtwert für alle Transaktionen in einen Satz von Werten, einen für jeden Transaktionsnamen, unterbricht werden kann. Weitere Beispiele sind ein Anwendungssystem oder ein Benutzergruppenname.

</dd> <dt>

**Kalkulierbare**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Merkmale der Metrik, die zum Ausführen von Berechnungen verwendet wird.

<dt>

<span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>

<span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>**Nicht berechenbar** (1)


</dt> <dd>

Eine Zeichenfolge. Arithmetische Daten sind nicht sinnvoll.

</dd> <dt>

<span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>

<span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>**Summierbar** (2)


</dt> <dd>

Es ist sinnvoll, diesen Wert über viele Instanzen von zu summieren, z. B. UnitOfWork, z. B. die Anzahl der in einem Sicherungsauftrag verarbeiteten Dateien. Wenn beispielsweise jeder Sicherungsauftrag ein UnitOfWork ist und jeder Auftrag durchschnittlich 27.000 Dateien gesichert, ist es sinnvoll zu sagen, dass 100 Sicherungsaufträge 2.700.000 Dateien verarbeitet haben.

</dd> <dt>

<span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>

<span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>**Nicht summierbar** (3)


</dt> <dd>

Es ist nicht sinnvoll, diesen Wert über viele Instanzen von UnitOfWork zu summen. Ein Beispiel wäre eine Metrik, die die Länge der Warteschlange misst, wenn ein Auftrag auf einem Server eintrifft. Wenn jeder Auftrag ein UnitOfWork ist und die durchschnittliche Warteschlangenlänge beim Eintreffen jedes Auftrags 33 beträgt, ist es nicht sinnvoll zu sagen, dass die Warteschlangenlänge für 100 Aufträge 3300 beträgt. Es ist sinnvoll zu sagen, dass der Mittelwert 33 ist.

</dd> </dl>

</dd> <dt>

**ChangeType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ BaseMetricDefinition**.**IsContinuous**")
</dt> </dl>

Gibt an, wie sich der Metrikwert ändert, indem allgemeine Attribute verwendet werden, z. B. Richtungsänderung, Mindest- und Höchstwerte und Umbruchsemantik.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd>

Der Metrik-Designer hat den ChangeType nicht qualifiziert.

</dd> <dt>

<span id="N_A"></span><span id="n_a"></span>

<span id="N_A"></span><span id="n_a"></span>**N/V** (2)


</dt> <dd>

Wenn die "IsContinuous"-Eigenschaft "false" ist, ist ChangeType nicht sinnvoll und MUSS auf "N/A" festgelegt werden.

</dd> <dt>

<span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>

<span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Zähler** (3)


</dt> <dd>

Die Metrik ist eine Zählermetrik. Diese verfügen über nicht negative ganzzahlige Werte, die sich monoton erhöhen, bis die maximal darstellbare Zahl erreicht ist, und dann umschließen und beginnen, von 0 zu steigen. Solche Leistungsindikatoren, auch als Rolloverzähler bezeichnet, können beispielsweise verwendet werden, um die Anzahl der Netzwerkfehler oder die Anzahl der verarbeiteten Transaktionen zu zählen. Die einzige Möglichkeit, mit der eine Clientanwendung umschließen kann, besteht im Abrufen des Werts des Leistungsindikators in entsprechend kurzen Intervallen.

</dd> <dt>

<span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>

<span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Messgerät** (4)


</dt> <dd>

Die Metrik ist eine Messgerätmetrik. Diese verfügen über Ganzzahl- oder Gleitkommawerte, die beliebig erhöht und verringert werden können. Ein Messgerät DARF NICHT umschließen, wenn die minimale oder maximale darstellbare Zahl erreicht wird. Stattdessen bleibt der Wert bei dieser Zahl "erhalten". Mindest- oder Höchstwerte innerhalb des darstellbaren Wertbereichs, in dem der Metrikwert "bleibt", definiert werden können oder nicht.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (5..32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Reservierter Anbieter** (32768..65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**DataType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Datentyp der Metrik.

<dt>

<span id="boolean"></span><span id="BOOLEAN"></span>

**boolean** (1)


</dt> <dd></dd> <dt>

<span id="char16"></span><span id="CHAR16"></span>

**char16** (2)


</dt> <dd></dd> <dt>

<span id="datetime"></span><span id="DATETIME"></span>

**datetime** (3)


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

**string** (10)


</dt> <dd></dd> <dt>

<span id="uint16"></span><span id="UINT16"></span>

**uint16** (11)


</dt> <dd></dd> <dt>

<span id="uint32"></span><span id="UINT32"></span>

**uint32** (12)


</dt> <dd></dd> <dt>

<span id="uint64"></span><span id="UINT64"></span>

**uint64** (13)


</dt> <dd></dd> <dt>

<span id="uint8"></span><span id="UINT8"></span>

**uint8** (14)


</dt> <dd></dd> </dl>

</dd> <dt>

**GatheringType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, wie die Metrikwerte von der zugrunde liegenden Instrumentierung erfasst werden.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd>

Gibt an, dass der GatheringType nicht bekannt ist.

</dd> <dt>

<span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>

<span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>**OnChange** (2)


</dt> <dd>

Gibt an, dass die CIM-Metrikwerte sofort aktualisiert werden, wenn sich die Werte innerhalb der gemessenen Ressource ändern. Die Werte der OnChange-Metriken spiegeln die aktuelle Situation innerhalb der Ressource zu einem beliebigen Zeitpunkt wider. Ein Beispiel ist die Anzahl der angemeldeten Benutzer, die sofort aktualisiert werden, wenn sich Benutzer anmelden und abmelden.

</dd> <dt>

<span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>

<span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>**Periodisch** (3)


</dt> <dd>

": Gibt an, dass die CIM-Metrikwerte regelmäßig aktualisiert werden. Beispielsweise wird für eine Clientanwendung ein Metrikwert, der auf die aktuelle Zeit anwendunget, während jedes Erfassungsintervalls konstant angezeigt und dann am Ende jedes Erfassungsintervalls zum neuen Wert springt.

</dd> <dt>

<span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>

<span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>**OnRequest** (4)


</dt> <dd>

Gibt an, dass der CIM-Metrikwert jedes Mal bestimmt wird, wenn eine Clientanwendung ihn liest. Die Werte der OnRequest-Metriken geben tatsächlich die aktuelle Situation innerhalb der Ressource zurück, wenn jemand sie anfordert. Sie ändern jedoch nicht "nicht beobachtet", und daher wird das Abonnieren von Wertänderungen von OnRequest-Metriken NICHT EMPFOHLEN.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (5..32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Reservierter Anbieter** (32768..65535)


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

Die eindeutige ID der Metrikdefinition. Open Software Foundation (OSF) UUID/GUIDs werden empfohlen.

</dd> <dt>

**IsContinuous**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True, wenn der Metrikwert kontinuierlich ist; andernfalls FALSE.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der Metrik. Dieser Name muss nicht eindeutig sein, sollte aber beschreibend sein und Leerzeichen enthalten.

</dd> <dt>

**ProgrammaticUnits**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die spezifischen Einheiten eines Werts. Der Wert dieser Eigenschaft sollte ein rechtlicher Wert des Qualifizierers "Programmgesteuerte Einheiten" sein, wie in Anhang C.1 von DSP0004 V2.4 oder höher definiert.

</dd> <dt>

**TimeScope**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricValue**](cim-basemetricvalue.md).**TimeStamp**", "**CIM \_ BaseMetricValue**.**Dauer**")
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

Gibt an, dass die Metrik für einen Zeitpunkt gilt. In den entsprechenden BaseMetricValue-Instanzen gibt TimeStamp den Zeitpunkt an, und Duration ist immer 0.

</dd> <dt>

<span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>

<span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>**Intervall** (3)


</dt> <dd>

Gibt an, dass die Metrik für ein Zeitintervall gilt. Für die entsprechenden BaseMetricValue-Instanzen gibt TimeStamp das Ende des Zeitintervalls und Duration die Dauer an.

</dd> <dt>

<span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>

<span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>**StartupInterval** (4)


</dt> <dd>

Gibt an, dass die Metrik für ein Zeitintervall gilt, das beim Start der gemessenen Ressource begonnen hat (d. h. das von MetricDefForMe zugeordnete ManagedElement). Für die entsprechenden BaseMetricValue-Instanzen gibt TimeStamp das Ende des Zeitintervalls an. Wenn Duration gleich 0 ist, gibt dies an, dass die Startzeit der gemessenen Ressource unbekannt ist. Andernfalls gibt Duration die Dauer zwischen dem Start der Ressource und TimeStamp an.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserviert** (5..32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Reservierter Anbieter** (32768..65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Einheiten**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Einheiten der Metrik. Beispiele hierfür sind Bytes, Pakete, Aufträge, Dateien, Millisekunden und Amps.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ ManagedElement**](cim-managedelement.md)
</dt> </dl>

 

