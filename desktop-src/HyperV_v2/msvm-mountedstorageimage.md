---
description: Stellt ausführliche Informationen über ein manuell eingebundenes Speicher Abbild bereit.
ms.assetid: 40b94c5f-c277-40c8-a55d-ebc64cb231ca
title: Msvm_MountedStorageImage-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MountedStorageImage
- Msvm_MountedStorageImage.InstanceID
- Msvm_MountedStorageImage.Caption
- Msvm_MountedStorageImage.Description
- Msvm_MountedStorageImage.ElementName
- Msvm_MountedStorageImage.InstallDate
- Msvm_MountedStorageImage.Name
- Msvm_MountedStorageImage.OperationalStatus
- Msvm_MountedStorageImage.StatusDescriptions
- Msvm_MountedStorageImage.Status
- Msvm_MountedStorageImage.HealthState
- Msvm_MountedStorageImage.CommunicationStatus
- Msvm_MountedStorageImage.DetailedStatus
- Msvm_MountedStorageImage.OperatingStatus
- Msvm_MountedStorageImage.PrimaryStatus
- Msvm_MountedStorageImage.Type
- Msvm_MountedStorageImage.Access
- Msvm_MountedStorageImage.PortNumber
- Msvm_MountedStorageImage.PathId
- Msvm_MountedStorageImage.TargetId
- Msvm_MountedStorageImage.Lun
- Msvm_MountedStorageImage.PnpDevicePath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1b6f00b137fc73bcf8f79d39e6f7bfb5a6d7c944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759649"
---
# <a name="msvm_mountedstorageimage-class"></a><span data-ttu-id="1387f-103">MSVM \_ mountedstorageimage-Klasse</span><span class="sxs-lookup"><span data-stu-id="1387f-103">Msvm\_MountedStorageImage class</span></span>

<span data-ttu-id="1387f-104">Stellt ausführliche Informationen über ein manuell eingebundenes Speicher Abbild bereit.</span><span class="sxs-lookup"><span data-stu-id="1387f-104">Provides detailed information about a manually mounted storage image.</span></span>

<span data-ttu-id="1387f-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1387f-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1387f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1387f-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MountedStorageImage : CIM_LogicalElement
{
  string   InstanceID;
  string   Caption = "Mounted Storage Image";
  string   Description = "Information about a mounted storage image.";
  string   ElementName = "Mounted Storage Image";
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[] = { "OK" };
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   Type;
  uint16   Access;
  UINT8    PortNumber;
  UINT8    PathId;
  UINT8    TargetId;
  UINT8    Lun;
  string   PnpDevicePath;
};
```

## <a name="members"></a><span data-ttu-id="1387f-107">Member</span><span class="sxs-lookup"><span data-stu-id="1387f-107">Members</span></span>

<span data-ttu-id="1387f-108">Die **MSVM \_ mountedstorageimage** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1387f-108">The **Msvm\_MountedStorageImage** class has these types of members:</span></span>

-   [<span data-ttu-id="1387f-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="1387f-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="1387f-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1387f-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1387f-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="1387f-111">Methods</span></span>

<span data-ttu-id="1387f-112">Die **MSVM \_ mountedstorageimage** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="1387f-112">The **Msvm\_MountedStorageImage** class has these methods.</span></span>



| <span data-ttu-id="1387f-113">Methode</span><span class="sxs-lookup"><span data-stu-id="1387f-113">Method</span></span>                                                                          | <span data-ttu-id="1387f-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1387f-114">Description</span></span>                                    |
|:--------------------------------------------------------------------------------|:-----------------------------------------------|
| [<span data-ttu-id="1387f-115">**Detachvirtualharddisk**</span><span class="sxs-lookup"><span data-stu-id="1387f-115">**DetachVirtualHardDisk**</span></span>](detachvirtualharddisk-msvm-mountedstorageimage.md) | <span data-ttu-id="1387f-116">Trennt das bereitgestellte Speicher Abbild.</span><span class="sxs-lookup"><span data-stu-id="1387f-116">Detaches the mounted storage image.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1387f-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1387f-117">Properties</span></span>

<span data-ttu-id="1387f-118">Die **MSVM \_ mountedstorageimage** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1387f-118">The **Msvm\_MountedStorageImage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1387f-119">**zugreifen**</span><span class="sxs-lookup"><span data-stu-id="1387f-119">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1387f-120">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1387f-120">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1387f-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1387f-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1387f-122">Der Zugriff, unter dem das Speicher Abbild bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="1387f-122">The access under which the storage image is mounted.</span></span>

<dt>

<span id="Read-only"></span><span id="read-only"></span><span id="READ-ONLY"></span>

<span data-ttu-id="1387f-123">Schreib **geschützt (1** )</span><span class="sxs-lookup"><span data-stu-id="1387f-123">**Read-only** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write"></span><span id="read_write"></span><span id="READ_WRITE"></span>

<span data-ttu-id="1387f-124">**Lese-/Schreibzugriff** (2)</span><span class="sxs-lookup"><span data-stu-id="1387f-124">**Read/Write** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1387f-125">**Caption**</span><span class="sxs-lookup"><span data-stu-id="1387f-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1387f-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1387f-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1387f-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1387f-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1387f-128">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="1387f-128">A short description of the object.</span></span> <span data-ttu-id="1387f-129">Diese Eigenschaft wird vom [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und enthält immer "eingebundenes Speicher Image".</span><span class="sxs-lookup"><span data-stu-id="1387f-129">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it always contains "Mounted Storage Image".</span></span>

</dd> <dt>

<span data-ttu-id="1387f-130">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="1387f-130">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1387f-131">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1387f-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1387f-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1387f-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1387f-133">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="1387f-133">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="1387f-134">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1387f-134">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1387f-135">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1387f-135">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1387f-136">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1387f-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1387f-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1387f-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1387f-138">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="1387f-138">A description of the object.</span></span> <span data-ttu-id="1387f-139">Diese Eigenschaft wird vom [**CIM \_ managedelta-Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und enthält immer "Informationen über ein bereitgestelltes Speicher Image".</span><span class="sxs-lookup"><span data-stu-id="1387f-139">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it always contains "Information about a mounted storage image.".</span></span>

</dd> <dt>

<span data-ttu-id="1387f-140">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="1387f-140">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1387f-141">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1387f-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1387f-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1387f-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1387f-143">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="1387f-143">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="1387f-144">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1387f-144">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1387f-145">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="1387f-145">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1387f-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1387f-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1387f-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1387f-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1387f-148">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="1387f-148">A display name for the object.</span></span> <span data-ttu-id="1387f-149">Diese Eigenschaft wird vom [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und enthält immer "eingebundenes Speicher Image".</span><span class="sxs-lookup"><span data-stu-id="1387f-149">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it always contains "Mounted Storage Image".</span></span>

</dd> <dt>

<span data-ttu-id="1387f-150">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="1387f-150">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1387f-151">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1387f-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1387f-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1387f-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1387f-153">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="1387f-153">The current health of the element.</span></span> <span data-ttu-id="1387f-154">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="1387f-154">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="1387f-155">Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="1387f-155">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="1387f-156">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 5 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1387f-156">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="1387f-157">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1387f-157">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1387f-158">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="1387f-158">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1387f-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1387f-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1387f-160">Das Datum und die Uhrzeit der Erstellung der Konfiguration der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="1387f-160">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="1387f-161">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1387f-161">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1387f-162">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1387f-162">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1387f-163">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1387f-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1387f-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1387f-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1387f-165">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="1387f-165">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1387f-166">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="1387f-166">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="1387f-167">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer **null**.</span><span class="sxs-lookup"><span data-stu-id="1387f-167">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1387f-168">**LUN**</span><span class="sxs-lookup"><span data-stu-id="1387f-168">**Lun**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1387f-169">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="1387f-169">Data type: **UINT8**</span></span>
</dt> <dt>

<span data-ttu-id="1387f-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1387f-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1387f-171">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1387f-171">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1387f-172">Die LUN-ID der SCSI-Adresse.</span><span class="sxs-lookup"><span data-stu-id="1387f-172">The SCSI address LUN ID.</span></span>

</dd> <dt>

<span data-ttu-id="1387f-173">**Name**</span><span class="sxs-lookup"><span data-stu-id="1387f-173">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1387f-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1387f-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1387f-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1387f-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1387f-176">Der Pfad zur VHD, die eingebunden wird.</span><span class="sxs-lookup"><span data-stu-id="1387f-176">The path to the VHD that is mounted.</span></span> <span data-ttu-id="1387f-177">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1387f-177">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1387f-178">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="1387f-178">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1387f-179">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1387f-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1387f-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1387f-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1387f-181">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="1387f-181">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="1387f-182">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1387f-182">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1387f-183">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="1387f-183">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1387f-184">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="1387f-184">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1387f-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1387f-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1387f-186">Der aktuelle Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="1387f-186">The current status of the object.</span></span> <span data-ttu-id="1387f-187">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1387f-187">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1387f-188">**Pathid**</span><span class="sxs-lookup"><span data-stu-id="1387f-188">**PathId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1387f-189">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="1387f-189">Data type: **UINT8**</span></span>
</dt> <dt>

<span data-ttu-id="1387f-190">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1387f-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1387f-191">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1387f-191">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1387f-192">Die ID der SCSI-Adress Pfad-ID.</span><span class="sxs-lookup"><span data-stu-id="1387f-192">The SCSI address path ID.</span></span>

</dd> <dt>

<span data-ttu-id="1387f-193">**Pnpdevicepath**</span><span class="sxs-lookup"><span data-stu-id="1387f-193">**PnpDevicePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1387f-194">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1387f-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1387f-195">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1387f-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1387f-196">Der PNP-Gerätepfad.</span><span class="sxs-lookup"><span data-stu-id="1387f-196">The PNP device path.</span></span>

<span data-ttu-id="1387f-197">**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1387f-197">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="1387f-198">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="1387f-198">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1387f-199">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="1387f-199">Data type: **UINT8**</span></span>
</dt> <dt>

<span data-ttu-id="1387f-200">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1387f-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1387f-201">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1387f-201">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1387f-202">Die Portnummer für die SCSI-Adresse.</span><span class="sxs-lookup"><span data-stu-id="1387f-202">The SCSI address port number.</span></span>

</dd> <dt>

<span data-ttu-id="1387f-203">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="1387f-203">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1387f-204">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1387f-204">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1387f-205">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1387f-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1387f-206">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="1387f-206">Provides high level status information.</span></span> <span data-ttu-id="1387f-207">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="1387f-207">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="1387f-208">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1387f-208">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1387f-209">**Status**</span><span class="sxs-lookup"><span data-stu-id="1387f-209">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1387f-210">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1387f-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1387f-211">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1387f-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1387f-212">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf "OK" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1387f-212">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="1387f-213">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="1387f-213">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1387f-214">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="1387f-214">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1387f-215">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1387f-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1387f-216">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="1387f-216">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="1387f-217">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf "OK" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1387f-217">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="1387f-218">**TargetId**</span><span class="sxs-lookup"><span data-stu-id="1387f-218">**TargetId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1387f-219">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="1387f-219">Data type: **UINT8**</span></span>
</dt> <dt>

<span data-ttu-id="1387f-220">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1387f-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1387f-221">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1387f-221">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1387f-222">Die ID des SCSI-Adress Ziels.</span><span class="sxs-lookup"><span data-stu-id="1387f-222">The SCSI address target ID.</span></span>

</dd> <dt>

<span data-ttu-id="1387f-223">**Type**</span><span class="sxs-lookup"><span data-stu-id="1387f-223">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1387f-224">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1387f-224">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1387f-225">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1387f-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1387f-226">Der Typ des bereitgestellten Speicher Abbilds.</span><span class="sxs-lookup"><span data-stu-id="1387f-226">The type of storage image mounted.</span></span>

<dt>

<span id="Virtual_Hard_Disk"></span><span id="virtual_hard_disk"></span><span id="VIRTUAL_HARD_DISK"></span>

<span data-ttu-id="1387f-227">**Virtuelle Festplatte** (0)</span><span class="sxs-lookup"><span data-stu-id="1387f-227">**Virtual Hard Disk** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO_Image"></span><span id="iso_image"></span><span id="ISO_IMAGE"></span>

<span data-ttu-id="1387f-228">**ISO-Abbild** (1)</span><span class="sxs-lookup"><span data-stu-id="1387f-228">**ISO Image** (1)</span></span>


<span data-ttu-id="1387f-229"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="1387f-229"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="1387f-230">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1387f-230">Remarks</span></span>

<span data-ttu-id="1387f-231">Der Zugriff auf die **MSVM \_ mountedstorageimage** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="1387f-231">Access to the **Msvm\_MountedStorageImage** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="1387f-232">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="1387f-232">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="1387f-233">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1387f-233">Requirements</span></span>



| <span data-ttu-id="1387f-234">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1387f-234">Requirement</span></span> | <span data-ttu-id="1387f-235">Wert</span><span class="sxs-lookup"><span data-stu-id="1387f-235">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1387f-236">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1387f-236">Minimum supported client</span></span><br/> | <span data-ttu-id="1387f-237">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1387f-237">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1387f-238">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1387f-238">Minimum supported server</span></span><br/> | <span data-ttu-id="1387f-239">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1387f-239">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1387f-240">Namespace</span><span class="sxs-lookup"><span data-stu-id="1387f-240">Namespace</span></span><br/>                | <span data-ttu-id="1387f-241">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="1387f-241">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1387f-242">MOF</span><span class="sxs-lookup"><span data-stu-id="1387f-242">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1387f-243"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1387f-243"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1387f-244">DLL</span><span class="sxs-lookup"><span data-stu-id="1387f-244">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1387f-245"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1387f-245"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1387f-246">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1387f-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1387f-247">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="1387f-247">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="1387f-248">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="1387f-248">**CIM\_LogicalElement**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicalelement)
</dt> <dt>

[<span data-ttu-id="1387f-249">Speicher Klassen</span><span class="sxs-lookup"><span data-stu-id="1387f-249">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

