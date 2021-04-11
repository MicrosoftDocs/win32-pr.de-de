---
description: Stellt ein Ereignis dar, das jedes Mal ausgelöst wird, wenn sich die OperationalStatus-Eigenschaft der MSVM \_ resourcepool-Klasse oder der MSVM \_ LogicalDisk-Klasse ändert.
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
ms.openlocfilehash: fa7f0430631082a9690cf2083f6b075ca62ee26b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042548"
---
# <a name="msvm_storagealert-class"></a>MSVM \_ storagealert-Klasse

Stellt ein Ereignis dar, das jedes Mal ausgelöst wird, wenn sich die **OperationalStatus** -Eigenschaft der [**MSVM \_ resourcepool**](msvm-resourcepool.md) -Klasse oder der [**MSVM \_ LogicalDisk**](msvm-logicaldisk.md) -Klasse ändert.

Die folgende Syntax wird aus dem MOF-Code vereinfacht und enthält diese Eigenschaften.

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

Die **MSVM \_ storagealert** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ storagealert** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Alertingelementformat**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **modelcorrespondence** ("CIM \_ alertindikation. alertingmanagedelta ement", "CIM \_ alertindikation. otheralertingelementformat")
</dt> </dl>

Gibt das Format der **alertingmanagedelta** -Eigenschaft an. Das Format ist ein cimabjectpath mit dem folgenden Format *<NamespacePath> : <ClassName> . <Prop1> = \\ " <Value1> \\ ", " <Prop2> = \\ " <Value2> \\ "*, der eine Instanz im CIM-Schema angibt.

Diese Eigenschaft wird von der **CIM \_ alertindikation** -Klasse geerbt.

Mögliche Werte sind:

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)
</dt> <dt>

<span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**Cifibjectpath** (2)
</dt> </dl>

</dd> <dt>

**Alertingmanagedelta**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die WMI-Pfade der-Instanz, für die die Warnung generiert wird.

</dd> <dt>

**AlertType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
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

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum und die Uhrzeit, zu denen das zugrunde liegende Ereignis erkannt wurde.

</dd> <dt>

**Meldung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine formatierte Nachricht, die erstellt wird, indem einige oder alle der dynamischen Elemente kombiniert werden, die in der **messagearguments** -Eigenschaft angegeben sind, und die statischen Elemente, die durch die Eigenschaft **MessageId** in einer Nachrichten Registrierung oder einem anderen der **owningentity** -Eigenschaft zugeordneten Katalog eindeutig identifiziert werden.

</dd> <dt>

**Messagearguments**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array, das den dynamischen Inhalt der Nachricht enthält. Wenn der Wert von **MessageId** 32930 ist, ist das Argument an Position 0 der **poolid** der [**MSVM \_ resourcepool**](msvm-resourcepoolcomponent.md) -Instanz, für die die Warnung generiert wird.

</dd> <dt>

**MessageId**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Identifiziert eindeutig innerhalb des Gültigkeits Bereichs der **owningentity** -Eigenschaft das Format der **Message** -Eigenschaft. Folgende Werte sind für diese Eigenschaft möglich:

32930 ("Speicher Pool-QoS unzureichende Durchsatz Nachricht")

</dd> <dt>

**Otheralertingelementformat**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die "Other"-Werte für **alertingmanagedelta Element** definiert. Dieser Wert muss auf einen Wert ungleich NULL festgelegt werden, wenn **alertingmanagedelta** auf den Wert 1 ("Other") festgelegt ist. Für alle anderen Werte von **alertingmanagedelta** muss der Wert dieser Zeichenfolge auf NULL festgelegt werden.

Diese Eigenschaft wird von der **CIM \_ alertindikation** -Klasse geerbt.

</dd> <dt>

**Owningentity**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Identifiziert die Entität eindeutig, die die Definition des Formats der in dieser Instanz beschriebenen **Meldung** besitzt. Der Wert dieser Eigenschaft lautet immer "Microsoft-Windows-Hyper-V".

"Microsoft-Windows-Hyper-V"

</dd> <dt>

**Wahrnehmgrad**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Beschreibt den Schweregrad der Warnungs Anzeige. Folgende Werte sind für diese Eigenschaft möglich:

<dl> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Informationen** (2)
</dt> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>Heruntergestuft **/Warnung** (3)
</dt> </dl>

</dd> <dt>

**Probableursache**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Beschreibt die mögliche Ursache der Situation, die zu der Warnungs Warnung geführt hat.

<dl> <dt>

<span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Speicher Kapazitäts Problem** (50)
</dt> <dt>

<span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**Vorherige Warnung gelöscht** (59)
</dt> </dl>

</dd> <dt>

**Probablecauendescription**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Textbeschreibung, die dem Wert der **probablecause** -Eigenschaft entspricht.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Hyper-V-WMI-Anbieter gibt keine Ereignisse für einzelne virtuelle Datenträger aus, um zu verhindern, dass Clients mit Ereignissen bei umfangreichen Störungen der zugrunde liegenden Speichersysteme überflutet werden.

Wenn ein Client ein **MSVM \_ storagealert** -Ereignis empfängt und der Wert der **probablecause** -Eigenschaft 50 (Speicher Kapazitäts Problem) ist, kann der Client ermitteln, welche virtuellen Datenträger außerhalb der QoS-Richtlinie ausgeführt werden, indem Sie eines der folgenden Verfahren verwenden:

-   Fragen Sie alle [**MSVM \_ LogicalDisk**](msvm-logicaldisk.md) -Instanzen ab, die aus dem Ressourcenpool zugeordnet wurden, für den das Ereignis generiert wurde. Diese **MSVM \_ LogicalDisk** -Instanzen werden dem Ressourcenpool über die [**MSVM- \_ Zuordnung elementzuordnungsedfrompool**](msvm-elementallocatedfrompool.md) zugeordnet.
-   Filtern Sie die Ergebnisliste, indem Sie Instanzen auswählen, deren OperationalStatus unzureichenden Durchsatz enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ alertindikation**](cim-alertindication.md)
</dt> <dt>

[**MSVM \_ LogicalDisk**](msvm-logicaldisk.md)
</dt> <dt>

[**MSVM- \_ resourcepool**](msvm-resourcepoolcomponent.md)
</dt> </dl>

 

 




