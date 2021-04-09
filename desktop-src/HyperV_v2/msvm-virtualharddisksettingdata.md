---
description: Stellt Einstellungsdaten für eine virtuelle Festplatte bereit.
ms.assetid: 492a0b81-86b2-4d7d-a118-6ec14e3971ed
title: Msvm_VirtualHardDiskSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualHardDiskSettingData
- Msvm_VirtualHardDiskSettingData.InstanceID
- Msvm_VirtualHardDiskSettingData.Caption
- Msvm_VirtualHardDiskSettingData.Description
- Msvm_VirtualHardDiskSettingData.ElementName
- Msvm_VirtualHardDiskSettingData.Type
- Msvm_VirtualHardDiskSettingData.Format
- Msvm_VirtualHardDiskSettingData.Path
- Msvm_VirtualHardDiskSettingData.ParentPath
- Msvm_VirtualHardDiskSettingData.ParentTimestamp
- Msvm_VirtualHardDiskSettingData.ParentIdentifier
- Msvm_VirtualHardDiskSettingData.MaxInternalSize
- Msvm_VirtualHardDiskSettingData.BlockSize
- Msvm_VirtualHardDiskSettingData.LogicalSectorSize
- Msvm_VirtualHardDiskSettingData.PhysicalSectorSize
- Msvm_VirtualHardDiskSettingData.VirtualDiskId
- Msvm_VirtualHardDiskSettingData.DataAlignment
- Msvm_VirtualHardDiskSettingData.PmemAddressAbstractionType
- Msvm_VirtualHardDiskSettingData.IsPmemCompatible
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6e13efbb068d15ca4051995e7d9f317eb2ccacab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128409"
---
# <a name="msvm_virtualharddisksettingdata-class"></a><span data-ttu-id="45728-103">MSVM \_ virtualharddisksettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="45728-103">Msvm\_VirtualHardDiskSettingData class</span></span>

<span data-ttu-id="45728-104">Stellt Einstellungsdaten für eine virtuelle Festplatte bereit.</span><span class="sxs-lookup"><span data-stu-id="45728-104">Provides setting data for a virtual hard disk.</span></span>

<span data-ttu-id="45728-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="45728-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="45728-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="45728-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VirtualHardDiskSettingData : CIM_SettingData
{
  string   InstanceID;
  string   Caption = "Virtual Hard Disk Setting Data";
  string   Description = "Setting Data for a Virtual Hard Disk";
  string   ElementName;
  uint16   Type;
  uint16   Format;
  string   Path;
  string   ParentPath;
  DATETIME ParentTimestamp;
  string   ParentIdentifier;
  uint64   MaxInternalSize;
  uint32   BlockSize;
  uint32   LogicalSectorSize;
  uint32   PhysicalSectorSize;
  string   VirtualDiskId;
  uint64   DataAlignment;
  uint16   PmemAddressAbstractionType;
  boolean  IsPmemCompatible;
};
```

## <a name="members"></a><span data-ttu-id="45728-107">Member</span><span class="sxs-lookup"><span data-stu-id="45728-107">Members</span></span>

<span data-ttu-id="45728-108">Die **MSVM \_ virtualharddisksettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="45728-108">The **Msvm\_VirtualHardDiskSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="45728-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="45728-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="45728-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="45728-110">Properties</span></span>

<span data-ttu-id="45728-111">Die **MSVM \_ virtualharddisksettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="45728-111">The **Msvm\_VirtualHardDiskSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="45728-112">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="45728-112">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45728-113">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="45728-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="45728-114">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="45728-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="45728-115">Die von der virtuellen Festplatte verwendete Blockgröße in Bytes.</span><span class="sxs-lookup"><span data-stu-id="45728-115">The block size used by the virtual hard disk, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="45728-116">**Caption**</span><span class="sxs-lookup"><span data-stu-id="45728-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45728-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="45728-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45728-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45728-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45728-119">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="45728-119">A short description of the object.</span></span> <span data-ttu-id="45728-120">Diese Eigenschaft wird vom [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Einstellungen für die Festplatte der virtuellen Festplatte" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="45728-120">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Hard Disk Setting Data".</span></span>

</dd> <dt>

<span data-ttu-id="45728-121">**Dataalignment**</span><span class="sxs-lookup"><span data-stu-id="45728-121">**DataAlignment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45728-122">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="45728-122">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="45728-123">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="45728-123">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="45728-124">Gibt die gewünschte Ausrichtung (in Bytes) für die Daten Nutzlast des virtuellen Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="45728-124">Specifies the desired alignment, in bytes, for the data payload of the virtual disk</span></span>

> [!Note]  
> <span data-ttu-id="45728-125">Hinzugefügt in Windows 10, Version 1709.</span><span class="sxs-lookup"><span data-stu-id="45728-125">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="45728-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="45728-126">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45728-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="45728-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45728-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45728-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45728-129">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="45728-129">A description of the object.</span></span> <span data-ttu-id="45728-130">Diese Eigenschaft wird vom [**CIM \_ managedelta-Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Festlegen von Daten für eine virtuelle Festplatte" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="45728-130">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Setting Data for a Virtual Hard Disk".</span></span>

</dd> <dt>

<span data-ttu-id="45728-131">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="45728-131">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45728-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="45728-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45728-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45728-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45728-134">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="45728-134">A display name for the object.</span></span> <span data-ttu-id="45728-135">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="45728-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="45728-136">**Format**</span><span class="sxs-lookup"><span data-stu-id="45728-136">**Format**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45728-137">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45728-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45728-138">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="45728-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="45728-139">Das Format für die virtuelle Festplatte.</span><span class="sxs-lookup"><span data-stu-id="45728-139">The format for the virtual hard disk.</span></span> <span data-ttu-id="45728-140">Dabei handelt es sich um einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="45728-140">This will be one of the following values.</span></span>

<dt>

<span id="VHD"></span><span id="vhd"></span>

<span data-ttu-id="45728-141"><span id="VHD"></span><span id="vhd"></span>**VHD** (2)</span><span class="sxs-lookup"><span data-stu-id="45728-141"><span id="VHD"></span><span id="vhd"></span>**VHD** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VHDX"></span><span id="vhdx"></span>

<span data-ttu-id="45728-142"><span id="VHDX"></span><span id="vhdx"></span>**Vhdx** (3)</span><span class="sxs-lookup"><span data-stu-id="45728-142"><span id="VHDX"></span><span id="vhdx"></span>**VHDX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VHDSet"></span><span id="vhdset"></span><span id="VHDSET"></span>

<span data-ttu-id="45728-143"><span id="VHDSet"></span><span id="vhdset"></span><span id="VHDSET"></span>**Vhdset** (4)</span><span class="sxs-lookup"><span data-stu-id="45728-143"><span id="VHDSet"></span><span id="vhdset"></span><span id="VHDSET"></span>**VHDSet** (4)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="45728-144">In Windows 10 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="45728-144">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="45728-145">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="45728-145">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45728-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="45728-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45728-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45728-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45728-148">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="45728-148">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="45728-149">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="45728-149">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="45728-150">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="45728-150">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="45728-151">**Ispmemcompatible**</span><span class="sxs-lookup"><span data-stu-id="45728-151">**IsPmemCompatible**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45728-152">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="45728-152">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="45728-153">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="45728-153">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="45728-154">Gibt an, ob der virtuelle Datenträger als Sicherungs Speicher für ein dauerhaftes Speichergerät verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="45728-154">Specifies whether the virtual disk can be used as the backing store for a persistent memory device.</span></span>

> [!Note]  
> <span data-ttu-id="45728-155">Hinzugefügt in Windows 10, Version 1709.</span><span class="sxs-lookup"><span data-stu-id="45728-155">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="45728-156">**Logicalsector size**</span><span class="sxs-lookup"><span data-stu-id="45728-156">**LogicalSectorSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45728-157">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="45728-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="45728-158">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="45728-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="45728-159">Die von der virtuellen Festplatte verwendete logische Sektorgröße in Bytes.</span><span class="sxs-lookup"><span data-stu-id="45728-159">The logical sector size used by the virtual hard disk, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="45728-160">**MaxInternalSize**</span><span class="sxs-lookup"><span data-stu-id="45728-160">**MaxInternalSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45728-161">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="45728-161">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="45728-162">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="45728-162">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="45728-163">Die maximale Größe der virtuellen Festplatte, die vom virtuellen Computer angezeigt werden kann (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="45728-163">The maximum size of the virtual hard disk as viewable by the virtual machine, in bytes.</span></span> <span data-ttu-id="45728-164">Diese Größe wird auf das nächstgrößte Vielfache der Sektorgröße aufgerundet.</span><span class="sxs-lookup"><span data-stu-id="45728-164">This size will be rounded up to the next largest multiple of the sector size.</span></span>

</dd> <dt>

<span data-ttu-id="45728-165">**Parametifizierer**</span><span class="sxs-lookup"><span data-stu-id="45728-165">**ParentIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45728-166">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="45728-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45728-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45728-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45728-168">Der GUID, der verwendet wird, um das übergeordnete Element der virtuellen Festplatte eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="45728-168">The GUID used to uniquely identify the parent of the virtual hard disk.</span></span> <span data-ttu-id="45728-169">Wenn die virtuelle Festplatte nicht über ein übergeordnetes Element verfügt, ist dieses Feld leer.</span><span class="sxs-lookup"><span data-stu-id="45728-169">If the virtual hard disk does not have a parent, then this field is empty.</span></span>

> [!Note]  
> <span data-ttu-id="45728-170">In Windows 10 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="45728-170">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="45728-171">**ParentPath**</span><span class="sxs-lookup"><span data-stu-id="45728-171">**ParentPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45728-172">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="45728-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45728-173">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="45728-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="45728-174">Das übergeordnete Element der virtuellen Festplatte.</span><span class="sxs-lookup"><span data-stu-id="45728-174">The parent of the virtual hard disk.</span></span> <span data-ttu-id="45728-175">Wenn die virtuelle Festplatte nicht über ein übergeordnetes Element verfügt, ist diese Eigenschaft leer.</span><span class="sxs-lookup"><span data-stu-id="45728-175">If the virtual hard disk does not have a parent, then this property is empty.</span></span>

</dd> <dt>

<span data-ttu-id="45728-176">**"Parametritimestamp"**</span><span class="sxs-lookup"><span data-stu-id="45728-176">**ParentTimestamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45728-177">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="45728-177">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="45728-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45728-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45728-179">Der Zeitstempel des übergeordneten Elements der virtuellen Festplatte.</span><span class="sxs-lookup"><span data-stu-id="45728-179">The timestamp of the parent of the virtual hard disk.</span></span> <span data-ttu-id="45728-180">Wenn die virtuelle Festplatte nicht über ein übergeordnetes Element verfügt, ist dieses Feld leer.</span><span class="sxs-lookup"><span data-stu-id="45728-180">If the virtual hard disk does not have a parent, then this field is empty.</span></span>

> [!Note]  
> <span data-ttu-id="45728-181">In Windows 10 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="45728-181">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="45728-182">**Pfad**</span><span class="sxs-lookup"><span data-stu-id="45728-182">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45728-183">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="45728-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45728-184">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="45728-184">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="45728-185">Der voll qualifizierte Pfad der virtuellen Festplatte.</span><span class="sxs-lookup"><span data-stu-id="45728-185">The fully qualified path of the virtual hard disk.</span></span>

</dd> <dt>

<span data-ttu-id="45728-186">**Physicalsector size**</span><span class="sxs-lookup"><span data-stu-id="45728-186">**PhysicalSectorSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45728-187">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="45728-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="45728-188">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="45728-188">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="45728-189">Die physische Sektorgröße, die von der virtuellen Festplatte verwendet wird (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="45728-189">The physical sector size used by the virtual hard disk, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="45728-190">**Pmemaddressabstractiontype**</span><span class="sxs-lookup"><span data-stu-id="45728-190">**PmemAddressAbstractionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45728-191">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45728-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45728-192">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="45728-192">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="45728-193">Die für diese virtuelle Festplatte zu verwendende persistente Speicher Adress Abstraktion-Methode.</span><span class="sxs-lookup"><span data-stu-id="45728-193">The persistent memory address abstraction method to be used with this virtual disk.</span></span>

> [!Note]  
> <span data-ttu-id="45728-194">Hinzugefügt in Windows 10, Version 1709.</span><span class="sxs-lookup"><span data-stu-id="45728-194">Added in Windows 10, version 1709.</span></span>

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="45728-195">**Keine** (0)</span><span class="sxs-lookup"><span data-stu-id="45728-195">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="BTT"></span><span id="btt"></span>

<span data-ttu-id="45728-196">**BTT** (1)</span><span class="sxs-lookup"><span data-stu-id="45728-196">**BTT** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="45728-197">**Unbekannt** (65535)</span><span class="sxs-lookup"><span data-stu-id="45728-197">**Unknown** (65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="45728-198">**Type**</span><span class="sxs-lookup"><span data-stu-id="45728-198">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45728-199">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45728-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45728-200">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="45728-200">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="45728-201">Der Typ der virtuellen Festplatte.</span><span class="sxs-lookup"><span data-stu-id="45728-201">The type of virtual hard disk.</span></span> <span data-ttu-id="45728-202">Dabei handelt es sich um einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="45728-202">This will be one of the following values.</span></span>

<dt>

<span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>

<span data-ttu-id="45728-203">**Korrigiert** (2)</span><span class="sxs-lookup"><span data-stu-id="45728-203">**Fixed** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>

<span data-ttu-id="45728-204">**Dynamisch** (3)</span><span class="sxs-lookup"><span data-stu-id="45728-204">**Dynamic** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Differencing"></span><span id="differencing"></span><span id="DIFFERENCING"></span>

<span data-ttu-id="45728-205">**Differenzierung** (4)</span><span class="sxs-lookup"><span data-stu-id="45728-205">**Differencing** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="45728-206">**VirtualDiskId**</span><span class="sxs-lookup"><span data-stu-id="45728-206">**VirtualDiskId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45728-207">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="45728-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45728-208">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="45728-208">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="45728-209">Die GUID, die zur eindeutigen Identifizierung des virtuellen Datenträgers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="45728-209">The GUID that is used to uniquely identify the virtual disk.</span></span>

<span data-ttu-id="45728-210">Wenn die [**MSVM-Methode " \_ imagemanagementservice. getvirtualharddisksettingdata**](getvirtualharddisksettingdata-msvm-imagemanagementservice.md) " eine Instanz von " **MSVM \_ virtualharddisksettingdata**" zurückgibt, kann der Client diese Eigenschaft verwenden, um die eindeutige Datenträger-ID der virtuellen Festplatte zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="45728-210">When the [**Msvm\_ImageManagementService.GetVirtualHardDiskSettingData**](getvirtualharddisksettingdata-msvm-imagemanagementservice.md) method returns an instance of **Msvm\_VirtualHardDiskSettingData**, the client can use this property to get the unique disk ID of the VHD.</span></span>

<span data-ttu-id="45728-211">Bei der Konflikterkennung kann ein Client den **virtualdiskid** -Wert auf eine neue GUID festlegen und diese **MSVM \_ virtualharddisksettingdata** -Instanz an die [**MSVM \_ imagemanagementservice. setvirtualharddisksettingdata**](setvirtualharddisksettingdata-msvm-imagemanagementservice.md) -Methode übergeben, um die Datenträger-ID der virtuellen Festplatte zu ändern.</span><span class="sxs-lookup"><span data-stu-id="45728-211">On conflict detection or otherwise, a client can set the **VirtualDiskId** value to a new GUID and pass this **Msvm\_VirtualHardDiskSettingData** instance to the [**Msvm\_ImageManagementService.SetVirtualHardDiskSettingData**](setvirtualharddisksettingdata-msvm-imagemanagementservice.md) method to change the disk ID of the VHD.</span></span> <span data-ttu-id="45728-212">Wenn es sich bei der VHD nicht um eine vhdx-VHD handelt oder wenn die VHD angefügt ist, schlägt der Vorgang fehl.</span><span class="sxs-lookup"><span data-stu-id="45728-212">If the VHD is not a VHDX VHD, or if the VHD is attached, the operation fails.</span></span> <span data-ttu-id="45728-213">Der Vorgang schlägt auch fehl, wenn der bestandene Wert falsch formatiert ist, d. h. keine GUID ist oder alle 0s enthält.</span><span class="sxs-lookup"><span data-stu-id="45728-213">The operation also fails if the passed value is malformed, that is, not a GUID or has all 0s.</span></span> <span data-ttu-id="45728-214">Der Vorgang wird im Hintergrund erfolgreich ausgeführt, wenn der bestandene Wert mit der aktuellen Datenträger-ID identisch ist.</span><span class="sxs-lookup"><span data-stu-id="45728-214">The operation silently succeeds if the passed value is the same as the current disk ID.</span></span>

<span data-ttu-id="45728-215">Fehler, die von der Funktion " [**setvirtualdiskinformation**](/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation) " generiert werden, werden über diese Eigenschaft aufgehotet.</span><span class="sxs-lookup"><span data-stu-id="45728-215">Errors generated by the [**SetVirtualDiskInformation**](/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation) function are bubbled up through this property.</span></span> <span data-ttu-id="45728-216">Ein Client kann auch denselben Mechanismus verwenden, um den **virtualdiskid** -Wert bei der VHD-Erstellung über die [**MSVM \_ imagemanagementservice. kreatevirtualharddisk**](createvirtualharddisk-msvm-imagemanagementservice.md) -Methode im gleichen Namespace bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="45728-216">A client can also use the same mechanism to provide the **VirtualDiskId** value at VHD creation via the [**Msvm\_ImageManagementService.CreateVirtualHardDisk**](createvirtualharddisk-msvm-imagemanagementservice.md) method in the same namespace.</span></span> <span data-ttu-id="45728-217">Dies kann zum Erstellen von VHD1-oder VHD2-VHDs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="45728-217">This can be used to create VHD1 or VHD2 VHDs.</span></span>

<span data-ttu-id="45728-218">**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="45728-218">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="45728-219">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="45728-219">Requirements</span></span>



| <span data-ttu-id="45728-220">Anforderung</span><span class="sxs-lookup"><span data-stu-id="45728-220">Requirement</span></span> | <span data-ttu-id="45728-221">Wert</span><span class="sxs-lookup"><span data-stu-id="45728-221">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45728-222">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="45728-222">Minimum supported client</span></span><br/> | <span data-ttu-id="45728-223">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="45728-223">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="45728-224">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="45728-224">Minimum supported server</span></span><br/> | <span data-ttu-id="45728-225">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="45728-225">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="45728-226">Namespace</span><span class="sxs-lookup"><span data-stu-id="45728-226">Namespace</span></span><br/>                | <span data-ttu-id="45728-227">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="45728-227">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="45728-228">MOF</span><span class="sxs-lookup"><span data-stu-id="45728-228">MOF</span></span><br/>                      | <dl> <span data-ttu-id="45728-229"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="45728-229"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="45728-230">DLL</span><span class="sxs-lookup"><span data-stu-id="45728-230">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45728-231"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="45728-231"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="45728-232">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45728-232">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45728-233">**CIM- \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="45728-233">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="45728-234">**Getvirtualharddisksettingdata**</span><span class="sxs-lookup"><span data-stu-id="45728-234">**GetVirtualHardDiskSettingData**</span></span>](getvirtualharddisksettingdata-msvm-imagemanagementservice.md)
</dt> </dl>

 

