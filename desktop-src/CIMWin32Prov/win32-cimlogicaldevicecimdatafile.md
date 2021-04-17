---
description: Die Win32 \_ -WMI-Klasse cimlogicaldevicecimdatafile ordnet logische Geräte und Datendateien in Beziehung, die die vom Gerät verwendeten Treiberdateien angeben. Diese Klasse wird verwendet, um zu ermitteln, welche Gerätetreiber von einem Gerät verwendet werden.
ms.assetid: 892272de-920d-4fa0-adbc-f584ed6e8748
ms.tgt_platform: multiple
title: Win32_CIMLogicalDeviceCIMDataFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CIMLogicalDeviceCIMDataFile
- Win32_CIMLogicalDeviceCIMDataFile.Dependent
- Win32_CIMLogicalDeviceCIMDataFile.Antecedent
- Win32_CIMLogicalDeviceCIMDataFile.Purpose
- Win32_CIMLogicalDeviceCIMDataFile.PurposeDescription
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15db6209360cbd150a722dc98b6255afd696cbe9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524000"
---
# <a name="win32_cimlogicaldevicecimdatafile-class"></a><span data-ttu-id="833c8-104">Win32 \_ cimlogicaldevicecimdatafile-Klasse</span><span class="sxs-lookup"><span data-stu-id="833c8-104">Win32\_CIMLogicalDeviceCIMDataFile class</span></span>

<span data-ttu-id="833c8-105">Die Win32- [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) **\_ cimlogicaldevicecimdatafile** ordnet logische Geräte und Datendateien in Beziehung, die die vom Gerät verwendeten Treiberdateien angeben.</span><span class="sxs-lookup"><span data-stu-id="833c8-105">The **Win32\_CIMLogicalDeviceCIMDataFile** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates logical devices and data files, indicating the driver files used by the device.</span></span> <span data-ttu-id="833c8-106">Diese Klasse wird verwendet, um zu ermitteln, welche Gerätetreiber von einem Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="833c8-106">This class is used to discover which device drivers a device uses.</span></span>

<span data-ttu-id="833c8-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="833c8-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="833c8-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="833c8-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="833c8-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="833c8-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C510-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_CIMLogicalDeviceCIMDataFile : CIM_Dependency
{
  CIM_DataFile      REF Dependent;
  CIM_LogicalDevice REF Antecedent;
  uint16                Purpose;
  string                PurposeDescription;
};
```

## <a name="members"></a><span data-ttu-id="833c8-110">Member</span><span class="sxs-lookup"><span data-stu-id="833c8-110">Members</span></span>

<span data-ttu-id="833c8-111">Die Win32-Klasse " **\_ cimlogicaldevicecimdatafile** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="833c8-111">The **Win32\_CIMLogicalDeviceCIMDataFile** class has these types of members:</span></span>

-   [<span data-ttu-id="833c8-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="833c8-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="833c8-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="833c8-113">Properties</span></span>

<span data-ttu-id="833c8-114">Die Win32-Klasse " **\_ cimlogicaldevicecimdatafile** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="833c8-114">The **Win32\_CIMLogicalDeviceCIMDataFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="833c8-115">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="833c8-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="833c8-116">Datentyp: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="833c8-116">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="833c8-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="833c8-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="833c8-118">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="833c8-118">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="833c8-119">Ein [**CIM \_ LogicalDevice**](cim-logicaldevice.md) , das die Eigenschaften des logischen Geräts darstellt, das von der Datendatei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="833c8-119">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents the properties of the logical device that is being used by the data file.</span></span>

</dd> <dt>

<span data-ttu-id="833c8-120">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="833c8-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="833c8-121">Datentyp: **CIM \_ DataFile**</span><span class="sxs-lookup"><span data-stu-id="833c8-121">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="833c8-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="833c8-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="833c8-123">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ DataFile")</span><span class="sxs-lookup"><span data-stu-id="833c8-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_DataFile")</span></span>
</dt> </dl>

<span data-ttu-id="833c8-124">Eine [**CIM- \_ Datendatei**](cim-datafile.md) , die die Eigenschaften der Datendatei darstellt, die dem logischen Gerät zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="833c8-124">A [**CIM\_DataFile**](cim-datafile.md) that represents the properties of the data file assigned to the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="833c8-125">**Zweck**</span><span class="sxs-lookup"><span data-stu-id="833c8-125">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="833c8-126">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="833c8-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="833c8-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="833c8-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="833c8-128">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM")</span><span class="sxs-lookup"><span data-stu-id="833c8-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM")</span></span>
</dt> </dl>

<span data-ttu-id="833c8-129">Rolle, die die Datendatei in Bezug auf das zugehörige logische Gerät spielt.</span><span class="sxs-lookup"><span data-stu-id="833c8-129">Role that the data file plays with regard to its associated logical device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="833c8-130">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="833c8-130">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="833c8-131">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="833c8-131">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>

<span data-ttu-id="833c8-132">**Treiber** (2)</span><span class="sxs-lookup"><span data-stu-id="833c8-132">**Driver** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Configuration_Software"></span><span id="configuration_software"></span><span id="CONFIGURATION_SOFTWARE"></span>

<span data-ttu-id="833c8-133">**Konfigurations Software** (3)</span><span class="sxs-lookup"><span data-stu-id="833c8-133">**Configuration Software** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Software"></span><span id="application_software"></span><span id="APPLICATION_SOFTWARE"></span>

<span data-ttu-id="833c8-134">**Anwendungs Software** (4)</span><span class="sxs-lookup"><span data-stu-id="833c8-134">**Application Software** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Instrumentation"></span><span id="instrumentation"></span><span id="INSTRUMENTATION"></span>

<span data-ttu-id="833c8-135">**Instrumentation** (5)</span><span class="sxs-lookup"><span data-stu-id="833c8-135">**Instrumentation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Firmware"></span><span id="firmware"></span><span id="FIRMWARE"></span>

<span data-ttu-id="833c8-136">**Firmware** (6)</span><span class="sxs-lookup"><span data-stu-id="833c8-136">**Firmware** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="833c8-137">**Zweck Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="833c8-137">**PurposeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="833c8-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="833c8-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="833c8-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="833c8-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="833c8-140">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM")</span><span class="sxs-lookup"><span data-stu-id="833c8-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM")</span></span>
</dt> </dl>

<span data-ttu-id="833c8-141">Erweitert den Wert der Eigenschaft **Zweck** dieser Klasse.</span><span class="sxs-lookup"><span data-stu-id="833c8-141">Extends the value of the **Purpose** property of this class.</span></span>

<span data-ttu-id="833c8-142">Beispiel: "Disketten Treiber"</span><span class="sxs-lookup"><span data-stu-id="833c8-142">Example: "Floppy Disk Driver"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="833c8-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="833c8-143">Remarks</span></span>

<span data-ttu-id="833c8-144">Die Win32-Klasse " **\_ cimlogicaldevicecimdatafile** " ist von der [**CIM- \_ Abhängigkeit**](cim-logicaldevice.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="833c8-144">The **Win32\_CIMLogicalDeviceCIMDataFile** class is derived from [**CIM\_Dependency**](cim-logicaldevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="833c8-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="833c8-145">Requirements</span></span>



| <span data-ttu-id="833c8-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="833c8-146">Requirement</span></span> | <span data-ttu-id="833c8-147">Wert</span><span class="sxs-lookup"><span data-stu-id="833c8-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="833c8-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="833c8-148">Minimum supported client</span></span><br/> | <span data-ttu-id="833c8-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="833c8-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="833c8-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="833c8-150">Minimum supported server</span></span><br/> | <span data-ttu-id="833c8-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="833c8-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="833c8-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="833c8-152">Namespace</span></span><br/>                | <span data-ttu-id="833c8-153">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="833c8-153">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="833c8-154">MOF</span><span class="sxs-lookup"><span data-stu-id="833c8-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="833c8-155"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="833c8-155"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="833c8-156">DLL</span><span class="sxs-lookup"><span data-stu-id="833c8-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="833c8-157"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="833c8-157"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="833c8-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="833c8-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="833c8-159">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="833c8-159">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

<span data-ttu-id="833c8-160">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="833c8-160">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

