---
description: Wird in der GetSummaryInformation-Methode in der Msvm \_ VirtualSystemManagementService-Klasse verwendet, um schnell allgemeine Informationen im Zusammenhang mit einem virtuellen System oder einer Momentaufnahme abzurufen.
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
ms.openlocfilehash: fd99ec5a0a9f3bd4bd07fa88cfc15139c69a442b
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886577"
---
# <a name="msvm_summaryinformationbase-class"></a>Msvm \_ SummaryInformationBase-Klasse

Wird in der [**GetSummaryInformation-Methode**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) in der [**Msvm \_ VirtualSystemManagementService-Klasse**](msvm-virtualsystemmanagementservice.md) verwendet, um schnell allgemeine Informationen im Zusammenhang mit einem virtuellen System oder einer Momentaufnahme abzurufen.

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

Die **Msvm \_ SummaryInformationBase-Klasse** verfügt über folgende Typen von Membern:

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

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ManagedElement.ElementName")
</dt> </dl>

Der Anzeigename für das virtuelle System oder die Momentaufnahme.

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

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Computers, der diesen virtuellen Computer hostet.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ManagedElement.InstanceID"), [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

InstanceID ist eine optionale Eigenschaft, die verwendet werden kann, um eine Instanz dieser Klasse im Bereich des instanziierenden Namespace nicht transparent und eindeutig zu identifizieren. Verschiedene Unterklassen dieser Klasse können diese Eigenschaft überschreiben, um sie erforderlich zu machen, oder einen Schlüssel. Solche Unterklassen können auch die bevorzugten Algorithmen ändern, um eindeutig zu sein, die unten definiert sind.

Um die Eindeutigkeit innerhalb des NameSpace sicherzustellen, sollte der Wert von InstanceID mit dem folgenden "bevorzugten" Algorithmus erstellt werden:

&lt;&gt;OrgID: &lt; LocalID&gt;

Dabei &lt; werden OrgID &gt; und &lt; LocalID durch einen &gt; Doppelpunkt (:) getrennt, und &lt; orgID muss einen &gt; urheberrechtlich geschützten, markengeschützten oder anderweitig eindeutigen Namen enthalten, der im Besitz der Geschäftsentität ist, die die Instanz-ID erstellt oder definiert, oder die eine registrierte ID ist, die der Geschäftseinheit von einer anerkannten globalen Autorität zugewiesen wurde. (Diese Anforderung ähnelt der <Schema Name> \_ <Class Name> Struktur von Schemaklassennamen.) Darüber hinaus &lt; darf OrgID &gt; keinen Doppelpunkt (:) enthalten, um eindeutig zu sein. Wenn Sie diesen Algorithmus verwenden, muss der erste Doppelpunkt, der in InstanceID angezeigt wird, zwischen &lt; OrgID und LocalID angezeigt &gt; &lt; &gt; werden.

&lt;LocalID &gt; wird von der Geschäftsentität ausgewählt und sollte nicht wiederverwendet werden, um verschiedene zugrunde liegende (reale) Elemente zu identifizieren. Wenn nicht NULL ist und der oben genannte "bevorzugte" Algorithmus nicht verwendet wird, muss die definierende Entität sicherstellen, dass die resultierende Instanz-ID nicht für alle InstanceIDs wiederverwendet wird, die von diesem oder anderen Anbietern für den NameSpace dieser Instanz erstellt werden.

Wenn für DMTF-definierte Instanzen nicht AUF NULL festgelegt ist, muss der "bevorzugte" Algorithmus verwendet werden, wobei die &lt; OrgID &gt; auf CIM festgelegt ist.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der eindeutige Name für das virtuelle System oder die Momentaufnahme.

</dd> <dt>

**Hinweise**
</dt> <dd> <dl> <dt>

Datentyp: **string**
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

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Der aktuelle Status des Elements.

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die den aktivierten oder deaktivierten Zustand des Elements beschreibt, wenn die **EnabledState-Eigenschaft** auf 1 ("Other") festgelegt ist. Diese Eigenschaft muss auf NULL festgelegt werden, wenn **EnabledState** ein anderer Wert als 1 ist.

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

Die Zeitspanne seit dem letzten Start des virtuellen Systems. Diese Eigenschaft ist für Instanzen von [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) ungültig, die eine Momentaufnahme des virtuellen Systems darstellen.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Version des virtuellen Systems im Format "Hauptversion.Nebenversion"; Beispiel: "2.0".

</dd> <dt>

**VirtualSwitchNames**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Zeichenfolgen, die die Anzeigenamen der virtuellen Switches auflisten, mit denen der virtuelle Computer verbunden ist.

</dd> <dt>

**VirtualSystemSubType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
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

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10 Desktop-Apps, Version 1703 \[\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_CIM-Ansicht**](cim-view.md)
</dt> </dl>

 

