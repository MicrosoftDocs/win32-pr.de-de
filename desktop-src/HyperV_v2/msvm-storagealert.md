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
# <a name="msvm_storagealert-class"></a><span data-ttu-id="f0030-103">MSVM \_ storagealert-Klasse</span><span class="sxs-lookup"><span data-stu-id="f0030-103">Msvm\_StorageAlert class</span></span>

<span data-ttu-id="f0030-104">Stellt ein Ereignis dar, das jedes Mal ausgelöst wird, wenn sich die **OperationalStatus** -Eigenschaft der [**MSVM \_ resourcepool**](msvm-resourcepool.md) -Klasse oder der [**MSVM \_ LogicalDisk**](msvm-logicaldisk.md) -Klasse ändert.</span><span class="sxs-lookup"><span data-stu-id="f0030-104">Represents an event that is raised each time the **OperationalStatus** property of the [**Msvm\_ResourcePool**](msvm-resourcepool.md) or [**Msvm\_LogicalDisk**](msvm-logicaldisk.md) class changes.</span></span>

<span data-ttu-id="f0030-105">Die folgende Syntax wird aus dem MOF-Code vereinfacht und enthält diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f0030-105">The following syntax is simplified from MOF code and includes these properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0030-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0030-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="f0030-107">Member</span><span class="sxs-lookup"><span data-stu-id="f0030-107">Members</span></span>

<span data-ttu-id="f0030-108">Die **MSVM \_ storagealert** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f0030-108">The **Msvm\_StorageAlert** class has these types of members:</span></span>

-   [<span data-ttu-id="f0030-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f0030-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f0030-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f0030-110">Properties</span></span>

<span data-ttu-id="f0030-111">Die **MSVM \_ storagealert** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f0030-111">The **Msvm\_StorageAlert** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f0030-112">**Alertingelementformat**</span><span class="sxs-lookup"><span data-stu-id="f0030-112">**AlertingElementFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0030-113">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f0030-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f0030-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f0030-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0030-115">Qualifizierer: **modelcorrespondence** ("CIM \_ alertindikation. alertingmanagedelta ement", "CIM \_ alertindikation. otheralertingelementformat")</span><span class="sxs-lookup"><span data-stu-id="f0030-115">Qualifiers: **ModelCorrespondence** ("CIM\_AlertIndication.AlertingManagedElement", "CIM\_AlertIndication.OtherAlertingElementFormat")</span></span>
</dt> </dl>

<span data-ttu-id="f0030-116">Gibt das Format der **alertingmanagedelta** -Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="f0030-116">Specifies the format of the **AlertingManagedElement** property.</span></span> <span data-ttu-id="f0030-117">Das Format ist ein cimabjectpath mit dem folgenden Format *<NamespacePath> : <ClassName> . <Prop1> = \\ " <Value1> \\ ", " <Prop2> = \\ " <Value2> \\ "*, der eine Instanz im CIM-Schema angibt.</span><span class="sxs-lookup"><span data-stu-id="f0030-117">The format is a CIMObjectPath, with the format *<NamespacePath>:<ClassName>.<Prop1>=\\"<Value1>\\", "<Prop2>=\\"<Value2>\\"*, which specifies an instance in the CIM Schema.</span></span>

<span data-ttu-id="f0030-118">Diese Eigenschaft wird von der **CIM \_ alertindikation** -Klasse geerbt.</span><span class="sxs-lookup"><span data-stu-id="f0030-118">This property is inherited from the **CIM\_AlertIndication** class.</span></span>

<span data-ttu-id="f0030-119">Mögliche Werte sind:</span><span class="sxs-lookup"><span data-stu-id="f0030-119">The possible values are:</span></span>

<dl> <dt>

<span data-ttu-id="f0030-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="f0030-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f0030-121"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="f0030-121"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f0030-122"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**Cifibjectpath** (2)</span><span class="sxs-lookup"><span data-stu-id="f0030-122"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f0030-123">**Alertingmanagedelta**</span><span class="sxs-lookup"><span data-stu-id="f0030-123">**AlertingManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0030-124">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="f0030-124">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f0030-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f0030-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0030-126">Die WMI-Pfade der-Instanz, für die die Warnung generiert wird.</span><span class="sxs-lookup"><span data-stu-id="f0030-126">The WMI paths of the instance for which the alert is generated.</span></span>

</dd> <dt>

<span data-ttu-id="f0030-127">**AlertType**</span><span class="sxs-lookup"><span data-stu-id="f0030-127">**AlertType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0030-128">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f0030-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f0030-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f0030-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0030-130">Gibt die primäre Klassifizierung der Warnung an.</span><span class="sxs-lookup"><span data-stu-id="f0030-130">Specifies the primary classification of the alert.</span></span> <span data-ttu-id="f0030-131">Folgende Werte sind für diese Eigenschaft möglich:</span><span class="sxs-lookup"><span data-stu-id="f0030-131">The possible values for this property are:</span></span>

<dl> <dt>

<span data-ttu-id="f0030-132"><span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**Quality of Service Warnung** (3)</span><span class="sxs-lookup"><span data-stu-id="f0030-132"><span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**Quality of Service Alert** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f0030-133">**EventTime**</span><span class="sxs-lookup"><span data-stu-id="f0030-133">**EventTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0030-134">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="f0030-134">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f0030-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f0030-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0030-136">Das Datum und die Uhrzeit, zu denen das zugrunde liegende Ereignis erkannt wurde.</span><span class="sxs-lookup"><span data-stu-id="f0030-136">The date and time at which the underlying event was detected.</span></span>

</dd> <dt>

<span data-ttu-id="f0030-137">**Meldung**</span><span class="sxs-lookup"><span data-stu-id="f0030-137">**Message**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0030-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f0030-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0030-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f0030-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0030-140">Eine formatierte Nachricht, die erstellt wird, indem einige oder alle der dynamischen Elemente kombiniert werden, die in der **messagearguments** -Eigenschaft angegeben sind, und die statischen Elemente, die durch die Eigenschaft **MessageId** in einer Nachrichten Registrierung oder einem anderen der **owningentity** -Eigenschaft zugeordneten Katalog eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="f0030-140">A formatted message that is constructed by combining some or all of the dynamic elements that are specified in the **MessageArguments** property with the static elements uniquely identified by the **MessageID** property in a message registry or other catalog associated with the **OwningEntity** property.</span></span>

</dd> <dt>

<span data-ttu-id="f0030-141">**Messagearguments**</span><span class="sxs-lookup"><span data-stu-id="f0030-141">**MessageArguments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0030-142">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="f0030-142">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f0030-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f0030-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0030-144">Ein Array, das den dynamischen Inhalt der Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="f0030-144">An array that contains the dynamic content of the message.</span></span> <span data-ttu-id="f0030-145">Wenn der Wert von **MessageId** 32930 ist, ist das Argument an Position 0 der **poolid** der [**MSVM \_ resourcepool**](msvm-resourcepoolcomponent.md) -Instanz, für die die Warnung generiert wird.</span><span class="sxs-lookup"><span data-stu-id="f0030-145">If the value of **MessageID** is 32930, the argument at position 0 is the **PoolID** of the [**Msvm\_ResourcePool**](msvm-resourcepoolcomponent.md) instance for which the alert is generated.</span></span>

</dd> <dt>

<span data-ttu-id="f0030-146">**MessageId**</span><span class="sxs-lookup"><span data-stu-id="f0030-146">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0030-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f0030-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0030-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f0030-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0030-149">Identifiziert eindeutig innerhalb des Gültigkeits Bereichs der **owningentity** -Eigenschaft das Format der **Message** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f0030-149">Uniquely identifies, within the scope of the **OwningEntity** property, the format of the **Message** property.</span></span> <span data-ttu-id="f0030-150">Folgende Werte sind für diese Eigenschaft möglich:</span><span class="sxs-lookup"><span data-stu-id="f0030-150">The possible values for this property are:</span></span>

<span data-ttu-id="f0030-151">32930 ("Speicher Pool-QoS unzureichende Durchsatz Nachricht")</span><span class="sxs-lookup"><span data-stu-id="f0030-151">32930 ("Storage Pool QoS Insufficient Throughput Message")</span></span>

</dd> <dt>

<span data-ttu-id="f0030-152">**Otheralertingelementformat**</span><span class="sxs-lookup"><span data-stu-id="f0030-152">**OtherAlertingElementFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0030-153">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f0030-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f0030-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f0030-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0030-155">Eine Zeichenfolge, die "Other"-Werte für **alertingmanagedelta Element** definiert.</span><span class="sxs-lookup"><span data-stu-id="f0030-155">A string that defines "Other" values for **AlertingManagedElement**.</span></span> <span data-ttu-id="f0030-156">Dieser Wert muss auf einen Wert ungleich NULL festgelegt werden, wenn **alertingmanagedelta** auf den Wert 1 ("Other") festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f0030-156">This value MUST be set to a non NULL value when **AlertingManagedElement** is set to a value of 1 ("Other").</span></span> <span data-ttu-id="f0030-157">Für alle anderen Werte von **alertingmanagedelta** muss der Wert dieser Zeichenfolge auf NULL festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f0030-157">For all other values of **AlertingManagedElement**, the value of this string must be set to NULL.</span></span>

<span data-ttu-id="f0030-158">Diese Eigenschaft wird von der **CIM \_ alertindikation** -Klasse geerbt.</span><span class="sxs-lookup"><span data-stu-id="f0030-158">This property is inherited from the **CIM\_AlertIndication** class.</span></span>

</dd> <dt>

<span data-ttu-id="f0030-159">**Owningentity**</span><span class="sxs-lookup"><span data-stu-id="f0030-159">**OwningEntity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0030-160">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f0030-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0030-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f0030-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0030-162">Identifiziert die Entität eindeutig, die die Definition des Formats der in dieser Instanz beschriebenen **Meldung** besitzt.</span><span class="sxs-lookup"><span data-stu-id="f0030-162">Uniquely identifies the entity that owns the definition of the format of the **Message** described in this instance.</span></span> <span data-ttu-id="f0030-163">Der Wert dieser Eigenschaft lautet immer "Microsoft-Windows-Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="f0030-163">The value of this property is always "Microsoft-Windows- Hyper-V."</span></span>

<span data-ttu-id="f0030-164">"Microsoft-Windows-Hyper-V"</span><span class="sxs-lookup"><span data-stu-id="f0030-164">"Microsoft-Windows- Hyper-V"</span></span>

</dd> <dt>

<span data-ttu-id="f0030-165">**Wahrnehmgrad**</span><span class="sxs-lookup"><span data-stu-id="f0030-165">**PerceivedSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0030-166">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f0030-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f0030-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f0030-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0030-168">Beschreibt den Schweregrad der Warnungs Anzeige.</span><span class="sxs-lookup"><span data-stu-id="f0030-168">Describes the severity of the alert indication.</span></span> <span data-ttu-id="f0030-169">Folgende Werte sind für diese Eigenschaft möglich:</span><span class="sxs-lookup"><span data-stu-id="f0030-169">The possible values for this property are:</span></span>

<dl> <dt>

<span data-ttu-id="f0030-170"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Informationen** (2)</span><span class="sxs-lookup"><span data-stu-id="f0030-170"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Information** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f0030-171"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>Heruntergestuft **/Warnung** (3)</span><span class="sxs-lookup"><span data-stu-id="f0030-171"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degraded/Warning** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f0030-172">**Probableursache**</span><span class="sxs-lookup"><span data-stu-id="f0030-172">**ProbableCause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0030-173">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f0030-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f0030-174">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f0030-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0030-175">Beschreibt die mögliche Ursache der Situation, die zu der Warnungs Warnung geführt hat.</span><span class="sxs-lookup"><span data-stu-id="f0030-175">Describes the probable cause of the situation that resulted in the alert indication.</span></span>

<dl> <dt>

<span data-ttu-id="f0030-176"><span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Speicher Kapazitäts Problem** (50)</span><span class="sxs-lookup"><span data-stu-id="f0030-176"><span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Storage Capacity Problem** (50)</span></span>
</dt> <dt>

<span data-ttu-id="f0030-177"><span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**Vorherige Warnung gelöscht** (59)</span><span class="sxs-lookup"><span data-stu-id="f0030-177"><span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**Previous Alert Cleared** (59)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f0030-178">**Probablecauendescription**</span><span class="sxs-lookup"><span data-stu-id="f0030-178">**ProbableCauseDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0030-179">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f0030-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0030-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f0030-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0030-181">Eine Textbeschreibung, die dem Wert der **probablecause** -Eigenschaft entspricht.</span><span class="sxs-lookup"><span data-stu-id="f0030-181">A textual description that corresponds to the value of the **ProbableCause** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f0030-182">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f0030-182">Remarks</span></span>

<span data-ttu-id="f0030-183">Der Hyper-V-WMI-Anbieter gibt keine Ereignisse für einzelne virtuelle Datenträger aus, um zu verhindern, dass Clients mit Ereignissen bei umfangreichen Störungen der zugrunde liegenden Speichersysteme überflutet werden.</span><span class="sxs-lookup"><span data-stu-id="f0030-183">The Hyper-V WMI provider won't raise events for individual virtual disks to avoid flooding clients with events in case of large scale malfunctions of the underlying storage systems.</span></span>

<span data-ttu-id="f0030-184">Wenn ein Client ein **MSVM \_ storagealert** -Ereignis empfängt und der Wert der **probablecause** -Eigenschaft 50 (Speicher Kapazitäts Problem) ist, kann der Client ermitteln, welche virtuellen Datenträger außerhalb der QoS-Richtlinie ausgeführt werden, indem Sie eines der folgenden Verfahren verwenden:</span><span class="sxs-lookup"><span data-stu-id="f0030-184">When a client receives an **Msvm\_StorageAlert** event, if the value of the **ProbableCause** property is 50 ( Storage Capacity Problem ), the client can discover which virtual disks are operating outside their QoS policy by using one of these procedures:</span></span>

-   <span data-ttu-id="f0030-185">Fragen Sie alle [**MSVM \_ LogicalDisk**](msvm-logicaldisk.md) -Instanzen ab, die aus dem Ressourcenpool zugeordnet wurden, für den das Ereignis generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f0030-185">Query all the [**Msvm\_LogicalDisk**](msvm-logicaldisk.md) instances that were allocated from the resource pool for which the event was generated.</span></span> <span data-ttu-id="f0030-186">Diese **MSVM \_ LogicalDisk** -Instanzen werden dem Ressourcenpool über die [**MSVM- \_ Zuordnung elementzuordnungsedfrompool**](msvm-elementallocatedfrompool.md) zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="f0030-186">These **Msvm\_LogicalDisk** instances are associated to the resource pool via the [**Msvm\_ElementAllocatedFromPool**](msvm-elementallocatedfrompool.md) association.</span></span>
-   <span data-ttu-id="f0030-187">Filtern Sie die Ergebnisliste, indem Sie Instanzen auswählen, deren OperationalStatus unzureichenden Durchsatz enthält.</span><span class="sxs-lookup"><span data-stu-id="f0030-187">Filter the result list by selecting instances whose OperationalStatus contains  Insufficient Throughput .</span></span>

## <a name="requirements"></a><span data-ttu-id="f0030-188">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0030-188">Requirements</span></span>



| <span data-ttu-id="f0030-189">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0030-189">Requirement</span></span> | <span data-ttu-id="f0030-190">Wert</span><span class="sxs-lookup"><span data-stu-id="f0030-190">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0030-191">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f0030-191">Minimum supported client</span></span><br/> | <span data-ttu-id="f0030-192">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="f0030-192">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="f0030-193">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f0030-193">Minimum supported server</span></span><br/> | <span data-ttu-id="f0030-194">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0030-194">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f0030-195">Namespace</span><span class="sxs-lookup"><span data-stu-id="f0030-195">Namespace</span></span><br/>                | <span data-ttu-id="f0030-196">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="f0030-196">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f0030-197">MOF</span><span class="sxs-lookup"><span data-stu-id="f0030-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f0030-198"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f0030-198"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f0030-199">DLL</span><span class="sxs-lookup"><span data-stu-id="f0030-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0030-200"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f0030-200"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f0030-201">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0030-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0030-202">**CIM- \_ alertindikation**</span><span class="sxs-lookup"><span data-stu-id="f0030-202">**CIM\_AlertIndication**</span></span>](cim-alertindication.md)
</dt> <dt>

[<span data-ttu-id="f0030-203">**MSVM \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="f0030-203">**Msvm\_LogicalDisk**</span></span>](msvm-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="f0030-204">**MSVM- \_ resourcepool**</span><span class="sxs-lookup"><span data-stu-id="f0030-204">**Msvm\_ResourcePool**</span></span>](msvm-resourcepoolcomponent.md)
</dt> </dl>

 

 




