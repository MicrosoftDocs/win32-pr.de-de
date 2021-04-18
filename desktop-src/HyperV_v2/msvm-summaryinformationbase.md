---
description: Wird in der getsummaryinformation-Methode in der MSVM \_ virtualsystemmanagementservice-Klasse verwendet, um schnell allgemeine Informationen abzurufen, die sich auf ein virtuelles System oder eine Momentaufnahme beziehen.
ms.assetid: f8daa387-d812-4f44-bf5f-e0a0c18c6db8
title: Msvm_SummaryInformationBase-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SummaryInformationBase
- Msvm_SummaryInformationBase.InstanceID
- Msvm_SummaryInformationBase.CreationTime
- Msvm_SummaryInformationBase.ElementName
- Msvm_SummaryInformationBase.EnabledState
- Msvm_SummaryInformationBase.OtherEnabledState
- Msvm_SummaryInformationBase.HealthState
- Msvm_SummaryInformationBase.Name
- Msvm_SummaryInformationBase.Notes
- Msvm_SummaryInformationBase.Version
- Msvm_SummaryInformationBase.NumberOfProcessors
- Msvm_SummaryInformationBase.OperationalStatus
- Msvm_SummaryInformationBase.StatusDescriptions
- Msvm_SummaryInformationBase.UpTime
- Msvm_SummaryInformationBase.EnhancedSessionModeState
- Msvm_SummaryInformationBase.VirtualSwitchNames
- Msvm_SummaryInformationBase.VirtualSystemSubType
- Msvm_SummaryInformationBase.HostComputerSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 65c20239673f279babba2581c4300f373f1392bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357423"
---
# <a name="msvm_summaryinformationbase-class"></a>MSVM \_ summaryinformationbase-Klasse

Wird in der [**getsummaryinformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) -Methode in der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse verwendet, um schnell allgemeine Informationen abzurufen, die sich auf ein virtuelles System oder eine Momentaufnahme beziehen.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SummaryInformationBase : CIM_View
{
  string   InstanceID;
  DateTime CreationTime;
  string   ElementName;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   HealthState;
  string   Name;
  string   Notes;
  string   Version;
  uint16   NumberOfProcessors;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  uint64   UpTime;
  uint16   EnhancedSessionModeState;
  string   VirtualSwitchNames[];
  string   VirtualSystemSubType;
  string   HostComputerSystemName;
};
```

## <a name="members"></a>Member

Die **MSVM \_ summaryinformationbase** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ summaryinformationbase** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Zeitpunkt, zu dem das virtuelle System oder die Momentaufnahme erstellt wurde.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("CIM \_ managedelta Element. Elementname")
</dt> </dl>

Der Anzeige Name für das virtuelle System oder die Momentaufnahme.

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktuelle Zustand des virtuellen Systems oder der Momentaufnahme.

</dd> <dt>

**Enhancedsessionmodestate**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob Verbindungen im erweiterten Modus vom Host zugelassen werden, und falls zulässig, ob Sie für den virtuellen Computer verfügbar sind.

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

**Zulässig und verfügbar** (2)


</dt> <dd></dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

**Nicht zulässig** (3)


</dt> <dd></dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

**Zulässig, aber nicht verfügbar** (6)


</dt> <dd></dd> </dl>

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktuelle Integritäts Status des virtuellen Systems. Diese Eigenschaft ist für Instanzen von [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) , die eine Momentaufnahme eines virtuellen Systems darstellen, ungültig.

</dd> <dt>

**Hostcomputersystemname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Computers, auf dem dieser virtuelle Computer gehostet wird.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("CIM \_ managedelta Element. InstanceId"), [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

"InstanceId" ist eine optionale Eigenschaft, die verwendet werden kann, um eine Instanz dieser Klasse innerhalb des Gültigkeits Bereichs des instanziierten Namespace eindeutig und eindeutig zu identifizieren. Verschiedene Unterklassen dieser Klasse können diese Eigenschaft überschreiben, um Sie erforderlich zu machen, oder einen Schlüssel. Diese Unterklassen können auch die bevorzugten Algorithmen zum Sicherstellen der Eindeutigkeit ändern, die unten definiert sind.

Um die Eindeutigkeit innerhalb des Namespaces sicherzustellen, sollte der Wert von InstanceId mit dem folgenden "bevorzugten" Algorithmus erstellt werden:

<OrgID>:<LocalID>

Dabei <OrgID> <LocalID> sind und durch einen Doppelpunkt (:) und wobei <OrgID> ein urheberrechtlich geschütztes, mit einem oder ein oder anderweitig eindeutiger Name enthalten muss, der der Geschäfts Entität entspricht, die die InstanceId erstellt oder definiert, oder die eine registrierte ID ist, die der Geschäfts Entität von einer anerkannten globalen Autorität zugewiesen ist. (Diese Anforderung ähnelt der <Schema Name> \_ <Class Name> Struktur von Schema Klassennamen.) Außerdem <OrgID> darf keine Doppelpunkte (:) enthalten, um die Eindeutigkeit sicherzustellen. Wenn dieser Algorithmus verwendet wird, muss der erste Doppelpunkt, der in InstanceId angezeigt wird, zwischen und angezeigt werden <OrgID> <LocalID> .

<LocalID> wird von der Business-Entität gewählt und sollte nicht wieder verwendet werden, um verschiedene zugrunde liegende (reale) Elemente zu identifizieren. Wenn not NULL und der oben genannte "bevorzugte" Algorithmus nicht verwendet wird, muss die definierende Entität sicherstellen, dass die resultierende InstanceId nicht in allen instanceids wieder verwendet wird, die von diesem oder anderen Anbietern für den Namespace dieser Instanz erstellt werden.

Wenn für von DMTF definierte Instanzen nicht auf NULL festgelegt ist, muss der "bevorzugte" Algorithmus verwendet werden, wobei <OrgID> auf CIM festgelegt ist.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der eindeutige Name für das virtuelle System oder die Momentaufnahme.

</dd> <dt>

**Hinweise**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Anmerkungen, die dem virtuellen System oder der Momentaufnahme zugeordnet sind.

</dd> <dt>

**NumberOfProcessors**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Gesamtanzahl der virtuellen Prozessoren, die dem virtuellen System oder der Momentaufnahme zugeordnet sind.

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")
</dt> </dl>

Der aktuelle Status des Elements.

</dd> <dt>

**Otherenabledstate**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die den aktivierten oder deaktivierten Status des Elements beschreibt, wenn die **enabledstate** -Eigenschaft auf 1 ("Other") festgelegt ist. Diese Eigenschaft muss auf NULL festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.

</dd> <dt>

**Status Beschreibungen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")
</dt> </dl>

Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.

</dd> <dt>

**Betriebszeit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Zeitspanne seit dem letzten Starten des virtuellen Systems. Diese Eigenschaft ist für Instanzen von [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) , die eine Momentaufnahme eines virtuellen Systems darstellen, ungültig.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Version des virtuellen Systems im Format "Major. Minor"; Beispiel: "2,0".

</dd> <dt>

**Virtualswitchnames**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")
</dt> </dl>

Zeichen folgen, die die anzeigen amen der virtuellen Switches auflisten, mit denen der virtuelle Computer verbunden ist.

</dd> <dt>

**VirtualSystemSubType**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Untertyp des virtuellen Systems.

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

**Microsoft: Hyper-v: Untertyp: 1** ("Microsoft: Hyper-v: SubType: 1")


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

**Microsoft: Hyper-v: SubType: 2** ("Microsoft: Hyper-v: SubType: 2")


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1703, \[ nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Ansicht**](cim-view.md)
</dt> </dl>

 

