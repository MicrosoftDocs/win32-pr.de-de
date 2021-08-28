---
description: Stellt ein Ereignis dar, das bei jeder Änderung der OperationalStatus-Eigenschaft der Msvm \_ ResourcePool- oder Msvm \_ LogicalDisk-Klasse ausgelöst wird.
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
ms.openlocfilehash: 41af5f29f54dc0b5c7e63203c43160539bcaa870
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886591"
---
# <a name="msvm_storagealert-class"></a>Msvm \_ StorageAlert-Klasse

Stellt ein Ereignis dar, das bei jeder Änderung der **OperationalStatus-Eigenschaft** der [**Msvm \_ ResourcePool-**](msvm-resourcepool.md) oder [**Msvm \_ LogicalDisk-Klasse**](msvm-logicaldisk.md) ausgelöst wird.

Die folgende Syntax wird aus MOF-Code vereinfacht und enthält diese Eigenschaften.

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

Die **Msvm \_ StorageAlert-Klasse** verfügt über folgende Typen von Membern:

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

Gibt das Format der **AlertingManagedElement-Eigenschaft** an. Das Format ist ein CIMObjectPath mit dem Format *&lt; NamespacePath &gt; : &lt; ClassName &gt; . &lt; Prop1 &gt; = \\ " &lt; Value1 &gt; \\ ", " &lt; Prop2 &gt; = \\ " &lt; Value2 &gt; \\ "*, das eine Instanz im CIM-Schema angibt.

Diese Eigenschaft wird von der **CIM \_ AlertIndication-Klasse** geerbt.

Mögliche Werte sind:

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Andere** (1)
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

<span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**Quality of Service-Warnung** (3)
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

Identifiziert innerhalb des Bereichs der **OwningEntity-Eigenschaft** eindeutig das Format der **Message-Eigenschaft.** Folgende Werte sind für diese Eigenschaft möglich:

32930 ("Storage Pool QoS Insufficient Throughput Message")

</dd> <dt>

**OtherAlertingElementFormat**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die "Other"-Werte für **AlertingManagedElement** definiert. Dieser Wert MUSS auf einen Wert ungleich NULL festgelegt werden, wenn **AlertingManagedElement** auf den Wert 1 ("Other") festgelegt ist. Für alle anderen Werte von **AlertingManagedElement** muss der Wert dieser Zeichenfolge auf NULL festgelegt werden.

Diese Eigenschaft wird von der **CIM \_ AlertIndication-Klasse** geerbt.

</dd> <dt>

**OwningEntity**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Identifiziert eindeutig die Entität, die die Definition des Formats der in dieser Instanz beschriebenen **Nachricht** besitzt. Der Wert dieser Eigenschaft lautet immer "Microsoft-Windows- Hyper-V".

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

**ProbableCause**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Beschreibt die wahrscheinliche Ursache der Situation, die zur Warnungsanzeige geführt hat.

<dl> <dt>

<span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Storage Kapazitätsproblem** (50)
</dt> <dt>

<span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**Vorherige Warnung gelöscht** (59)
</dt> </dl>

</dd> <dt>

**ProbableCauseDescription**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Textbeschreibung, die dem Wert der **Eigenschaft "ProbableCause"** entspricht.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Hyper-V-WMI-Anbieter gibt keine Ereignisse für einzelne virtuelle Datenträger aus, um eine Überflutung von Clients mit Ereignissen bei umfangreichen Fehlfunktionen der zugrunde liegenden Speichersysteme zu vermeiden.

Wenn ein Client ein **Msvm \_ StorageAlert-Ereignis** empfängt und der Wert der **Eigenschaft "ProbableCause"** 50 ist (Storage Kapazitätsproblem), kann der Client ermitteln, welche virtuellen Datenträger außerhalb ihrer QoS-Richtlinie ausgeführt werden, indem er eines der folgenden Verfahren verwendet:

-   Fragen Sie alle [**Msvm \_ LogicalDisk-Instanzen**](msvm-logicaldisk.md) ab, die aus dem Ressourcenpool zugeordnet wurden, für den das Ereignis generiert wurde. Diese **Msvm \_ LogicalDisk-Instanzen** werden dem Ressourcenpool über die [**Zuordnung Msvm \_ ElementAllocatedFromPool**](msvm-elementallocatedfrompool.md) zugeordnet.
-   Filtern Sie die Ergebnisliste, indem Sie Instanzen auswählen, deren OperationalStatus unzureichenden Durchsatz enthält.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ AlertIndication**](cim-alertindication.md)
</dt> <dt>

[**Msvm \_ LogicalDisk**](msvm-logicaldisk.md)
</dt> <dt>

[**Msvm \_ ResourcePool**](msvm-resourcepoolcomponent.md)
</dt> </dl>

 

 




