---
description: Stellt ein Ereignis dar, das jedes Mal ausgelöst wird, wenn sich die OperationalStatus-Eigenschaft der \_ Msvm ResourcePool- oder Msvm \_ LogicalDisk-Klasse ändert.
ms.assetid: 20E7C22A-A151-4EDC-90D8-4BCD53C42355
title: Msvm_StorageAlert-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageAlert
- Msvm_StorageAlert.AlertingManagedElement
- Msvm_StorageAlert.AlertingElementFormat
- Msvm_StorageAlert.OtherAlertingElementFormat
- Msvm_StorageAlert.AlertType
- Msvm_StorageAlert.PerceivedSeverity
- Msvm_StorageAlert.ProbableCause
- Msvm_StorageAlert.ProbableCauseDescription
- Msvm_StorageAlert.EventTime
- Msvm_StorageAlert.OwningEntity
- Msvm_StorageAlert.MessageArguments
- Msvm_StorageAlert.MessageID
- Msvm_StorageAlert.Message
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 478b4617f56c73e425d833842b313767f85c385e9142314a7ca8978b5783f492
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950229"
---
# <a name="msvm_storagealert-class"></a>Msvm \_ StorageAlert-Klasse

Stellt ein Ereignis dar, das jedes Mal ausgelöst wird, wenn sich die **OperationalStatus-Eigenschaft** der [**Msvm \_ ResourcePool-**](msvm-resourcepool.md) oder [**Msvm \_ LogicalDisk-Klasse**](msvm-logicaldisk.md) ändert.

Die folgende Syntax wird durch MOF-Code vereinfacht und enthält diese Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Indication, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageAlert : CIM_AlertIndication
{
  string   AlertingManagedElement[];
  uint16   AlertingElementFormat;
  uint16   OtherAlertingElementFormat;
  uint16   AlertType;
  uint16   PerceivedSeverity;
  uint16   ProbableCause;
  string   ProbableCauseDescription;
  datetime EventTime;
  string   OwningEntity;
  string   MessageArguments[];
  string   MessageID;
  string   Message;
};
```

## <a name="members"></a>Member

Die **Msvm \_ StorageAlert-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ StorageAlert-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AlertingElementFormat**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **ModelCorrespondence** ("CIM \_ AlertIndication.AlertingManagedElement", "CIM \_ AlertIndication.OtherAlertingElementFormat")
</dt> </dl>

Gibt das Format der **AlertingManagedElement-Eigenschaft** an. Das Format ist ein CIMObjectPath mit dem Format *<NamespacePath> : . " <ClassName> <Prop1> = \\ <Value1> \\ ", " <Prop2> = \\ " <Value2> \\ " " ,*, das eine Instanz im CIM-Schema angibt.

Diese Eigenschaft wird von der **CIM \_ AlertIndication-Klasse geerbt.**

Mögliche Werte sind:

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)
</dt> <dt>

<span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)
</dt> </dl>

</dd> <dt>

**AlertingManagedElement**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die WMI-Pfade der Instanz, für die die Warnung generiert wird.

</dd> <dt>

**AlertType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die primäre Klassifizierung der Warnung an. Folgende Werte sind für diese Eigenschaft möglich:

<dl> <dt>

<span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**Quality of Service Warnung** (3)
</dt> </dl>

</dd> <dt>

**EventTime**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum und die Uhrzeit, zu der das zugrunde liegende Ereignis erkannt wurde.

</dd> <dt>

**Meldung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine formatierte Nachricht, die erstellt wird, indem einige oder alle dynamischen Elemente, die in der **MessageArguments-Eigenschaft** angegeben sind, mit den statischen Elementen kombiniert werden, die eindeutig durch die **MessageID-Eigenschaft** in einer Nachrichtenregistrierung oder einem anderen Katalog identifiziert werden, der der **OwningEntity-Eigenschaft** zugeordnet ist.

</dd> <dt>

**MessageArguments**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array, das den dynamischen Inhalt der Nachricht enthält. Wenn der Wert von **MessageID** 32930 ist, ist das Argument an Position 0 die **PoolID** der [**Msvm \_ ResourcePool-Instanz,**](msvm-resourcepoolcomponent.md) für die die Warnung generiert wird.

</dd> <dt>

**MessageID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Identifiziert das Format der Message-Eigenschaft innerhalb des Bereichs der **OwningEntity-Eigenschaft** eindeutig.  Folgende Werte sind für diese Eigenschaft möglich:

32930 ("Storage Pool QoS Insufficient Throughput Message")

</dd> <dt>

**OtherAlertingElementFormat**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die "Andere" Werte für **AlertingManagedElement definiert.** Dieser Wert MUSS auf einen Nicht-NULL-Wert festgelegt werden, **wenn AlertingManagedElement** auf den Wert 1 ("Other") festgelegt ist. Für alle anderen Werte von **AlertingManagedElement** muss der Wert dieser Zeichenfolge auf NULL festgelegt werden.

Diese Eigenschaft wird von der **CIM \_ AlertIndication-Klasse geerbt.**

</dd> <dt>

**OwningEntity**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Identifiziert eindeutig die Entität, die die Definition des  In dieser Instanz beschriebenen Nachrichtenformats besitzt. Der Wert dieser Eigenschaft ist immer "Microsoft-Windows- Hyper-V".

"Microsoft-Windows- Hyper-V"

</dd> <dt>

**PerceivedSeverity**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Beschreibt den Schweregrad der Warnungsanzeige. Folgende Werte sind für diese Eigenschaft möglich:

<dl> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Informationen** (2)
</dt> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Heruntergestuft/Warnung** (3)
</dt> </dl>

</dd> <dt>

**WahrscheinlichkeitCause**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Beschreibt die wahrscheinliche Ursache der Situation, die zur Warnungsanzeige führte.

<dl> <dt>

<span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Storage Kapazitätsproblem** (50)
</dt> <dt>

<span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**Vorherige Warnung wurde ausgelöst** (59)
</dt> </dl>

</dd> <dt>

**WahrscheinlichkeitCauseDescription**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Textbeschreibung, die dem Wert der **Eigenschaft "ProbableCause"** entspricht.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Hyper-V-WMI-Anbieter gibt keine Ereignisse für einzelne virtuelle Datenträger aus, um bei großen Fehlfunktionen der zugrunde liegenden Speichersysteme eine Überflutung von Clients mit Ereignissen zu vermeiden.

Wenn ein Client ein **Msvm \_ StorageAlert-Ereignis** empfängt, kann der Client mit einem der folgenden Verfahren feststellen, welche virtuellen Datenträger außerhalb der QoS-Richtlinie ausgeführt werden, wenn der Wert der **Eigenschaft "50"** (Storage Capacity Problem) ist:

-   Fragen Sie alle [**Msvm \_ LogicalDisk-Instanzen**](msvm-logicaldisk.md) ab, die aus dem Ressourcenpool zugeordnet wurden, für den das Ereignis generiert wurde. Diese **Msvm \_ LogicalDisk-Instanzen** werden dem Ressourcenpool über die [**Msvm-ElementAllocatedFromPool-Zuordnung \_**](msvm-elementallocatedfrompool.md) zugeordnet.
-   Filtern Sie die Ergebnisliste, indem Sie Instanzen auswählen, deren OperationalStatus unzureichenden Durchsatz enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ AlertIndication**](cim-alertindication.md)
</dt> <dt>

[**Msvm \_ LogicalDisk**](msvm-logicaldisk.md)
</dt> <dt>

[**Msvm \_ ResourcePool**](msvm-resourcepoolcomponent.md)
</dt> </dl>

 

 




