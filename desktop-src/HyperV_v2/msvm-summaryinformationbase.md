---
description: Wird in der GetSummaryInformation-Methode in der Msvm VirtualSystemManagementService-Klasse verwendet, um schnell allgemeine Informationen zu einem virtuellen System oder einer \_ Momentaufnahme abzurufen.
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
ms.openlocfilehash: d131a2630c0c64e4b4b6bcec371eb901665c989948a1db510b47a41d9159f06d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950099"
---
# <a name="msvm_summaryinformationbase-class"></a>Msvm \_ SummaryInformationBase-Klasse

Wird in der [**GetSummaryInformation-Methode**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) in der [**Msvm \_ VirtualSystemManagementService-Klasse**](msvm-virtualsystemmanagementservice.md) verwendet, um schnell allgemeine Informationen zu einem virtuellen System oder einer Momentaufnahme abzurufen.

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

Die **Msvm \_ SummaryInformationBase-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ SummaryInformationBase-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Creationtime**
</dt> <dd> <dl> <dt>

Datentyp: **DateTime**
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

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ManagedElement.ElementName")
</dt> </dl>

Der Benutzername für das virtuelle System oder die Momentaufnahme.

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktuelle Status des virtuellen Systems oder der Momentaufnahme.

</dd> <dt>

**EnhancedSessionModeState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob Verbindungen im erweiterten Modus vom Host zugelassen werden und ob sie für den virtuellen Computer verfügbar sind, sofern zulässig.

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

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktuelle Integritätsstatus für das virtuelle System. Diese Eigenschaft ist für Instanzen von [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) ungültig, die eine Momentaufnahme des virtuellen Systems darstellen.

</dd> <dt>

**HostComputerSystemName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Computers, der diesen virtuellen Computer hosten soll.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ManagedElement.InstanceID"), [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

InstanceID ist eine optionale Eigenschaft, die verwendet werden kann, um eine Instanz dieser Klasse innerhalb des Bereichs des instanziierenden Namespace undurchsichtig und eindeutig zu identifizieren. Verschiedene Unterklassen dieser Klasse können diese Eigenschaft überschreiben, um sie erforderlich zu machen, oder einen Schlüssel. Solche Unterklassen können auch die bevorzugten Algorithmen ändern, um die Eindeutigkeit sicherzustellen, die unten definiert sind.

Um die Eindeutigkeit innerhalb des NameSpace sicherzustellen, sollte der Wert von InstanceID mit dem folgenden "bevorzugten" Algorithmus erstellt werden:

<OrgID>:<LocalID>

Wobei und durch einen Doppelpunkt (:)) getrennt sind und wo einen urheberrechtlich geschützten, markengebundenen oder anderweitig eindeutigen Namen enthalten muss, der im Besitz der Geschäftseinheit ist, die die InstanceID erstellt oder definiert, oder die eine registrierte ID ist, die der Geschäftseinheit von einer anerkannten globalen Autorität zugewiesen <OrgID> <LocalID> <OrgID> wird. (Diese Anforderung ähnelt der <Schema Name> \_ <Class Name> Struktur von Schemaklassennamen.) Darüber hinaus darf zur Sicherstellung der <OrgID> Eindeutigkeit keinen Doppelpunkt (:). Bei Verwendung dieses Algorithmus muss der erste Doppelpunkt, der in InstanceID angezeigt wird, zwischen und <OrgID> angezeigt <LocalID> werden.

<LocalID> wird von der Geschäftsentität ausgewählt und sollte nicht wiederverwendet werden, um verschiedene zugrunde liegende (reale) Elemente zu identifizieren. Wenn nicht NULL festgelegt ist und der oben genannte "bevorzugte" Algorithmus nicht verwendet wird, muss die definierende Entität sicherstellen, dass die resultierende InstanceID nicht für instanceIDs wiederverwendet wird, die von diesem oder anderen Anbietern für den NameSpace dieser Instanz erzeugt werden.

Wenn für DMTF-definierte Instanzen nicht auf NULL festgelegt ist, muss der "bevorzugte" Algorithmus mit dem auf <OrgID> CIM festgelegten verwendet werden.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der eindeutige Name für das virtuelle System oder die Momentaufnahme.

</dd> <dt>

**Notizen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die dem virtuellen System oder der Momentaufnahme zugeordneten Hinweise.

</dd> <dt>

**NumberOfProcessors**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Gesamtzahl der virtuellen Prozessoren, die dem virtuellen System oder der Momentaufnahme zugeordnet sind.

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Der aktuelle Status des Elements.

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die den aktivierten oder deaktivierten Zustand des Elements beschreibt, wenn die **EnabledState-Eigenschaft** auf 1 ("Sonstige") festgelegt ist. Diese Eigenschaft muss auf NULL festgelegt werden, wenn **EnabledState** ein anderer Wert als 1 ist.

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Zeichenfolgen, die die verschiedenen **OperationalStatus-Arraywerte** beschreiben.

</dd> <dt>

**Verfügbarkeit**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Zeit seit dem letzten Start des virtuellen Systems. Diese Eigenschaft ist für Instanzen von [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) ungültig, die eine Momentaufnahme des virtuellen Systems darstellen.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Version des virtuellen Systems im Format "major.minor"; Beispiel: "2.0".

</dd> <dt>

**VirtualSwitchNames**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Zeichenfolgen, die die Benutzerfreundlichen Namen der virtuellen Switches auflisten, mit denen die VM verbunden ist.

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

**Microsoft:Hyper-V:SubType:1** ("Microsoft:Hyper-V:SubType:1")


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

**Microsoft:Hyper-V:SubType:2** ("Microsoft:Hyper-V:SubType:2")


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10 Desktop-Apps, Version 1703 \[\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_CIM-Ansicht**](cim-view.md)
</dt> </dl>

 

