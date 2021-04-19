---
description: Stellt die Einstellungen für den virtualisierungdienst dar, der auf einem einzelnen Host System vorhanden ist.
ms.assetid: E3265AFE-0117-4F59-9A6B-34CEA7A61EDD
title: Msvm_VirtualSystemManagementServiceSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementServiceSettingData
- Msvm_VirtualSystemManagementServiceSettingData.InstanceID
- Msvm_VirtualSystemManagementServiceSettingData.Caption
- Msvm_VirtualSystemManagementServiceSettingData.Description
- Msvm_VirtualSystemManagementServiceSettingData.ElementName
- Msvm_VirtualSystemManagementServiceSettingData.BiosLockString
- Msvm_VirtualSystemManagementServiceSettingData.DefaultExternalDataRoot
- Msvm_VirtualSystemManagementServiceSettingData.DefaultVirtualHardDiskPath
- Msvm_VirtualSystemManagementServiceSettingData.MaximumMacAddress
- Msvm_VirtualSystemManagementServiceSettingData.MinimumMacAddress
- Msvm_VirtualSystemManagementServiceSettingData.NumaSpanningEnabled
- Msvm_VirtualSystemManagementServiceSettingData.PrimaryOwnerContact
- Msvm_VirtualSystemManagementServiceSettingData.PrimaryOwnerName
- Msvm_VirtualSystemManagementServiceSettingData.HbaLunTimeout
- Msvm_VirtualSystemManagementServiceSettingData.MaximumWWPNAddress
- Msvm_VirtualSystemManagementServiceSettingData.MinimumWWPNAddress
- Msvm_VirtualSystemManagementServiceSettingData.CurrentWWNNAddress
- Msvm_VirtualSystemManagementServiceSettingData.DefaultVirtualHardDiskCachingMode
- Msvm_VirtualSystemManagementServiceSettingData.HypervisorRootSchedulerEnabled
- Msvm_VirtualSystemManagementServiceSettingData.EnhancedSessionModeEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 782f196fdbd3a09126a7b4d14be6789bb633f043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346691"
---
# <a name="msvm_virtualsystemmanagementservicesettingdata-class"></a><span data-ttu-id="1618f-103">MSVM \_ virtualsystemmanagementservicesettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="1618f-103">Msvm\_VirtualSystemManagementServiceSettingData class</span></span>

<span data-ttu-id="1618f-104">Stellt die Einstellungen für den virtualisierungdienst dar, der auf einem einzelnen Host System vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1618f-104">Represents the settings for the virtualization service present on a single host system.</span></span> <span data-ttu-id="1618f-105">Die Eigenschaften für diese Klasse können nicht direkt geändert werden.</span><span class="sxs-lookup"><span data-stu-id="1618f-105">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="1618f-106">Der Client muss die [**modifyservicesettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse abrufen, um diese Eigenschaften zu ändern.</span><span class="sxs-lookup"><span data-stu-id="1618f-106">The client must call the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class to modify any of these properties.</span></span>

<span data-ttu-id="1618f-107">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1618f-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1618f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1618f-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemManagementServiceSettingData : CIM_SettingData
{
  string  InstanceID = "Microsoft:host";
  string  Caption = "Hyper-V Virtual System Management Service";
  string  Description = "Settings for the Virtual System Management Service";
  string  ElementName = "Hyper-V Virtual System Management Service";
  string  BiosLockString;
  string  DefaultExternalDataRoot = "root\ProgramData\Microsoft\Windows\Virtualization";
  string  DefaultVirtualHardDiskPath = "root\Users\Public\Documents\Virtual Hard Disks";
  string  MaximumMacAddress;
  string  MinimumMacAddress;
  boolean NumaSpanningEnabled;
  string  PrimaryOwnerContact = "";
  string  PrimaryOwnerName = "Administrators";
  uint32  HbaLunTimeout;
  string  MaximumWWPNAddress;
  string  MinimumWWPNAddress;
  string  CurrentWWNNAddress;
  uint16  DefaultVirtualHardDiskCachingMode;
  boolean HypervisorRootSchedulerEnabled;
  boolean EnhancedSessionModeEnabled;
};
```

## <a name="members"></a><span data-ttu-id="1618f-109">Member</span><span class="sxs-lookup"><span data-stu-id="1618f-109">Members</span></span>

<span data-ttu-id="1618f-110">Die **MSVM \_ virtualsystemmanagementservicesettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1618f-110">The **Msvm\_VirtualSystemManagementServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="1618f-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1618f-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1618f-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1618f-112">Properties</span></span>

<span data-ttu-id="1618f-113">Die **MSVM \_ virtualsystemmanagementservicesettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1618f-113">The **Msvm\_VirtualSystemManagementServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1618f-114">**Bioslockstring**</span><span class="sxs-lookup"><span data-stu-id="1618f-114">**BiosLockString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1618f-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1618f-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1618f-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1618f-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1618f-117">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32)</span><span class="sxs-lookup"><span data-stu-id="1618f-117">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32)</span></span>
</dt> </dl>

<span data-ttu-id="1618f-118">Wird von OEMs verwendet, um zuzulassen, dass BIOS-gesperrten Windows-Betriebssysteme auf dem virtuellen Computer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1618f-118">Used by OEMs to allow BIOS-locked Windows operating systems to run in the virtual machine.</span></span> <span data-ttu-id="1618f-119">Diese Zeichenfolge muss genau 32 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="1618f-119">This string must be exactly 32 characters in length.</span></span>

<span data-ttu-id="1618f-120">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyservicesettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="1618f-120">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="1618f-121">**Caption**</span><span class="sxs-lookup"><span data-stu-id="1618f-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1618f-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1618f-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1618f-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1618f-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1618f-124">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="1618f-124">A short description of the object.</span></span> <span data-ttu-id="1618f-125">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Hyper-V Virtual System Management Service" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1618f-125">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual System Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="1618f-126">**Currentwwnnaddress**</span><span class="sxs-lookup"><span data-stu-id="1618f-126">**CurrentWWNNAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1618f-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1618f-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1618f-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1618f-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1618f-129">Die wwnn-Adresse (World Wide Node Name) für dynamisch generierte World Wide Name-Adressen, die für synthetische Hostbus Adapter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1618f-129">The world wide node name (WWNN) address for dynamically generated world wide name addresses used for synthetic host bus adapters.</span></span>

<span data-ttu-id="1618f-130">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyservicesettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="1618f-130">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="1618f-131">**Defaultexternaldataroot**</span><span class="sxs-lookup"><span data-stu-id="1618f-131">**DefaultExternalDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1618f-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1618f-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1618f-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1618f-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1618f-134">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md)".**Configurationdataroot**")</span><span class="sxs-lookup"><span data-stu-id="1618f-134">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md).**ConfigurationDataRoot**")</span></span>
</dt> </dl>

<span data-ttu-id="1618f-135">Der standardmäßige externe Daten Stamm.</span><span class="sxs-lookup"><span data-stu-id="1618f-135">The default external data root.</span></span> <span data-ttu-id="1618f-136">Standardmäßig "*root* \\ Program Data \\ Microsoft \\ Windows \\ Virtualization".</span><span class="sxs-lookup"><span data-stu-id="1618f-136">By default, "*root*\\ProgramData\\Microsoft\\Windows\\Virtualization".</span></span>

<span data-ttu-id="1618f-137">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyservicesettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="1618f-137">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="1618f-138">**Defaultvirtualharddiskcachingmode**</span><span class="sxs-lookup"><span data-stu-id="1618f-138">**DefaultVirtualHardDiskCachingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1618f-139">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1618f-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1618f-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1618f-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1618f-141">Gibt an, ob die Zwischenspeicherung im Arbeitsspeicher für Datenträger standardmäßig verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1618f-141">Indicates whether in-memory file caching should be used for disks by default.</span></span> <span data-ttu-id="1618f-142">Dieser Wert kann auf Datenträger Basis im **CachingMode** -Feld der Klasse [**MSVM \_ storagezucationsettingdata**](msvm-storageallocationsettingdata.md) überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="1618f-142">This value can be overridden on a per-disk basis in the **CachingMode** field of the [**Msvm\_StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="1618f-143">In Windows 10 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1618f-143">Added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1618f-144">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="1618f-144">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Caching"></span><span id="no_caching"></span><span id="NO_CACHING"></span>

<span data-ttu-id="1618f-145">**Kein Caching** (3)</span><span class="sxs-lookup"><span data-stu-id="1618f-145">**No Caching** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_Sharable_Parents"></span><span id="cache_sharable_parents"></span><span id="CACHE_SHARABLE_PARENTS"></span>

<span data-ttu-id="1618f-146">Zwischen **Speichern** von freigegebenen übergeordneten Elementen (4)</span><span class="sxs-lookup"><span data-stu-id="1618f-146">**Cache Sharable Parents** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1618f-147">**Defaultvirtualharddiskpath**</span><span class="sxs-lookup"><span data-stu-id="1618f-147">**DefaultVirtualHardDiskPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1618f-148">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1618f-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1618f-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1618f-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1618f-150">Der Standardpfad der virtuellen Festplatte.</span><span class="sxs-lookup"><span data-stu-id="1618f-150">The default virtual hard disk path.</span></span> <span data-ttu-id="1618f-151">Standardmäßig ist "*root* \\ Users \\ Public \\ Documents \\ Virtual Hard Disks".</span><span class="sxs-lookup"><span data-stu-id="1618f-151">By default, "*root*\\Users\\Public\\Documents\\Virtual Hard Disks".</span></span>

<span data-ttu-id="1618f-152">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyservicesettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="1618f-152">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="1618f-153">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1618f-153">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1618f-154">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1618f-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1618f-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1618f-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1618f-156">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="1618f-156">A description of the object.</span></span> <span data-ttu-id="1618f-157">Diese Eigenschaft wird vom [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Einstellungen für den Verwaltungsdienst für virtuelle Systeme" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1618f-157">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Settings for the Virtual System Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="1618f-158">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="1618f-158">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1618f-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1618f-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1618f-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1618f-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1618f-161">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="1618f-161">A display name for the object.</span></span> <span data-ttu-id="1618f-162">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Hyper-V Virtual System Management Service" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1618f-162">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual System Management Service".</span></span> <span data-ttu-id="1618f-163">Durch Ändern dieser Eigenschaft wird die **ElementName** -Eigenschaft der zugeordneten [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -Ableitung geändert.</span><span class="sxs-lookup"><span data-stu-id="1618f-163">Changing this property will change the **ElementName** property of the associated [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) derivative.</span></span>

</dd> <dt>

<span data-ttu-id="1618f-164">**Enhancedsessionmodeaktivierte**</span><span class="sxs-lookup"><span data-stu-id="1618f-164">**EnhancedSessionModeEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1618f-165">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1618f-165">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1618f-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1618f-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1618f-167">Gibt an, ob der erweiterte Sitzungs Modus auf dem Server zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="1618f-167">Indicates whether enhanced session mode is permitted on the server.</span></span> <span data-ttu-id="1618f-168">**True** gibt an, dass zulässig ist, andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="1618f-168">**True** indicates permitted, otherwise **False**.</span></span>

<span data-ttu-id="1618f-169">**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1618f-169">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="1618f-170">**Hbaluntimeout**</span><span class="sxs-lookup"><span data-stu-id="1618f-170">**HbaLunTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1618f-171">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1618f-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1618f-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1618f-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1618f-173">Gibt die Zeitspanne an, die das synthetische Fibre Channel virtuelle Gerät wartet, bis eine logische Gerätenummer (Logical Unit Number, LUN) angezeigt wird, bevor ein virtueller Computer gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="1618f-173">Specifies the amount of time that the synthetic Fibre Channel virtual device will wait for a logical unit number (LUN) to appear before starting a virtual machine.</span></span>

<span data-ttu-id="1618f-174">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyservicesettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="1618f-174">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="1618f-175">**Hypervisorrootscheduleraktivierte**</span><span class="sxs-lookup"><span data-stu-id="1618f-175">**HypervisorRootSchedulerEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1618f-176">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1618f-176">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1618f-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1618f-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1618f-178">Gibt an, ob der Hypervisor-Stamm Planer aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1618f-178">Whether or not the hypervisor root scheduler is enabled.</span></span>

> [!Note]  
> <span data-ttu-id="1618f-179">Hinzugefügt in Windows 10, Version 1709.</span><span class="sxs-lookup"><span data-stu-id="1618f-179">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="1618f-180">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1618f-180">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1618f-181">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1618f-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1618f-182">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1618f-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1618f-183">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="1618f-183">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1618f-184">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="1618f-184">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="1618f-185">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt und ist immer auf "Microsoft:*Host*" festgelegt, wobei " *Host* " der NetBIOS-Name des hostingcomputersystems ist.</span><span class="sxs-lookup"><span data-stu-id="1618f-185">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Microsoft:*host*", where *host* is the NetBIOS name of the hosting computer system.</span></span>

</dd> <dt>

<span data-ttu-id="1618f-186">**Maximummacaddress**</span><span class="sxs-lookup"><span data-stu-id="1618f-186">**MaximumMacAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1618f-187">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1618f-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1618f-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1618f-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1618f-189">Die maximale Mac-Adresse für dynamisch generierte Mac-Adressen.</span><span class="sxs-lookup"><span data-stu-id="1618f-189">The maximum MAC address for dynamically generated MAC addresses.</span></span>

<span data-ttu-id="1618f-190">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyservicesettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="1618f-190">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="1618f-191">**Maximumwwpnaddress**</span><span class="sxs-lookup"><span data-stu-id="1618f-191">**MaximumWWPNAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1618f-192">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1618f-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1618f-193">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1618f-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1618f-194">Die maximale WWPN-Adresse (World Wide Port Name) für dynamisch generierte World Wide Name-Adressen, die für synthetische Hostbus Adapter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1618f-194">The maximum world wide port name (WWPN) address for dynamically generated world wide name addresses used for synthetic host bus adapters.</span></span>

<span data-ttu-id="1618f-195">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyservicesettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="1618f-195">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="1618f-196">**Minimummacaddress**</span><span class="sxs-lookup"><span data-stu-id="1618f-196">**MinimumMacAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1618f-197">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1618f-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1618f-198">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1618f-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1618f-199">Die minimale Mac-Adresse für dynamisch generierte Mac-Adressen.</span><span class="sxs-lookup"><span data-stu-id="1618f-199">The minimum MAC address for dynamically generated MAC addresses.</span></span>

<span data-ttu-id="1618f-200">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyservicesettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="1618f-200">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="1618f-201">**Minimumwwpnaddress**</span><span class="sxs-lookup"><span data-stu-id="1618f-201">**MinimumWWPNAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1618f-202">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1618f-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1618f-203">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1618f-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1618f-204">Die minimale World Wide Port-namens Adresse für dynamisch generierte World Wide Name-Adressen, die für synthetische Hostbus Adapter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1618f-204">The minimum world wide port name address for dynamically generated world wide name addresses used for synthetic host bus adapters.</span></span>

<span data-ttu-id="1618f-205">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyservicesettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="1618f-205">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="1618f-206">**Numaspanningenabled**</span><span class="sxs-lookup"><span data-stu-id="1618f-206">**NumaSpanningEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1618f-207">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1618f-207">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1618f-208">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1618f-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1618f-209">Gibt an, ob beim Starten einer virtuellen Maschine oder beim Zuweisen von Arbeitsspeicher für eine virtuelle Maschine durch dynamischen Arbeitsspeicher von Knoten vom Typ "nicht einheitlicher Speicherzugriff" (NUMA) zugeordnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="1618f-209">Specifies whether memory can be allocated from remote nonuniform memory access (NUMA) nodes when starting a virtual machine or when assigning memory to a virtual machine by dynamic memory.</span></span> <span data-ttu-id="1618f-210">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="1618f-210">This can be one of the following values.</span></span>



| <span data-ttu-id="1618f-211">Wert</span><span class="sxs-lookup"><span data-stu-id="1618f-211">Value</span></span>                                                                                | <span data-ttu-id="1618f-212">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1618f-212">Meaning</span></span>                                                                                     |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1618f-213"><dt>**Fall**</dt></span><span class="sxs-lookup"><span data-stu-id="1618f-213"><dt>**True**</dt></span></span> </dl>  | <span data-ttu-id="1618f-214">Der Arbeitsspeicher kann sowohl über lokale als auch Remote-NUMA-Knoten zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="1618f-214">Memory can be allocated from both local and remote NUMA nodes.</span></span><br/>                   |
| <dl> <span data-ttu-id="1618f-215"><dt>**False**</dt></span><span class="sxs-lookup"><span data-stu-id="1618f-215"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="1618f-216">Der Arbeitsspeicher kann nur über den NUMA-Knoten zugewiesen werden, der dem virtuellen Computer zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="1618f-216">Memory can be allocated only from the NUMA node assigned to the virtual machine.</span></span><br/> |



 

<span data-ttu-id="1618f-217">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyservicesettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="1618f-217">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="1618f-218">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="1618f-218">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1618f-219">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1618f-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1618f-220">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1618f-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1618f-221">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Allgemeine Informationen zu DMTF \| \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="1618f-221">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="1618f-222">Beschreibt, wie der primäre Systembesitzer erreicht werden kann (z. b. Telefonnummer oder e-Mail-Adresse).</span><span class="sxs-lookup"><span data-stu-id="1618f-222">Describes how the primary system owner can be reached (for example, phone number or email address).</span></span> <span data-ttu-id="1618f-223">Standardmäßig leer.</span><span class="sxs-lookup"><span data-stu-id="1618f-223">By default, empty.</span></span> <span data-ttu-id="1618f-224">Dieser Name darf nicht länger als 256 Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="1618f-224">This name may not exceed 256 characters in length.</span></span>

<span data-ttu-id="1618f-225">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyservicesettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="1618f-225">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="1618f-226">**Primaryownername**</span><span class="sxs-lookup"><span data-stu-id="1618f-226">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1618f-227">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1618f-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1618f-228">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1618f-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1618f-229">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Allgemeine Informationen zu DMTF \| \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="1618f-229">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="1618f-230">Der Name des primären System Besitzers.</span><span class="sxs-lookup"><span data-stu-id="1618f-230">The name of the primary system owner.</span></span> <span data-ttu-id="1618f-231">Standardmäßig "Administratoren".</span><span class="sxs-lookup"><span data-stu-id="1618f-231">By default, "Administrators".</span></span> <span data-ttu-id="1618f-232">Dieser Wert darf nicht länger als 64 Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="1618f-232">This value may not exceed 64 characters in length.</span></span>

<span data-ttu-id="1618f-233">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyservicesettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="1618f-233">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1618f-234">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1618f-234">Remarks</span></span>

<span data-ttu-id="1618f-235">Der Zugriff auf die **MSVM \_ virtualsystemmanagementservicesettingdata** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="1618f-235">Access to the **Msvm\_VirtualSystemManagementServiceSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="1618f-236">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="1618f-236">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="1618f-237">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1618f-237">Requirements</span></span>



| <span data-ttu-id="1618f-238">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1618f-238">Requirement</span></span> | <span data-ttu-id="1618f-239">Wert</span><span class="sxs-lookup"><span data-stu-id="1618f-239">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1618f-240">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1618f-240">Minimum supported client</span></span><br/> | <span data-ttu-id="1618f-241">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1618f-241">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1618f-242">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1618f-242">Minimum supported server</span></span><br/> | <span data-ttu-id="1618f-243">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1618f-243">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1618f-244">Namespace</span><span class="sxs-lookup"><span data-stu-id="1618f-244">Namespace</span></span><br/>                | <span data-ttu-id="1618f-245">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="1618f-245">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1618f-246">MOF</span><span class="sxs-lookup"><span data-stu-id="1618f-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1618f-247"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1618f-247"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1618f-248">DLL</span><span class="sxs-lookup"><span data-stu-id="1618f-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1618f-249"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1618f-249"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1618f-250">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1618f-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1618f-251">**CIM- \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="1618f-251">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="1618f-252">**Modifyservicesettings**</span><span class="sxs-lookup"><span data-stu-id="1618f-252">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-virtualsystemmanagementservice.md)
</dt> <dt>

<span data-ttu-id="1618f-253">[**CIM- \_ SettingData**](/previous-versions//cc136911(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1618f-253">[**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1618f-254">Verwaltungs Klassen für virtuelle Systeme</span><span class="sxs-lookup"><span data-stu-id="1618f-254">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

