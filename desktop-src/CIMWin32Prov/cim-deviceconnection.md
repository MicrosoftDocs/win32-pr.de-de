---
description: Die CIM- \_ deviceconnetction-Zuordnungs Klasse stellt zwei oder mehr verbundene Geräte dar.
ms.assetid: 82095cd6-1843-4db2-9fe8-3e225611bd3b
ms.tgt_platform: multiple
title: CIM_DeviceConnection-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceConnection
- CIM_DeviceConnection.Dependent
- CIM_DeviceConnection.Antecedent
- CIM_DeviceConnection.NegotiatedDataWidth
- CIM_DeviceConnection.NegotiatedSpeed
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b8179287686439ea31c19d700a785de7fff47659
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214194"
---
# <a name="cim_deviceconnection-class-cimwin32-wmi-providers"></a><span data-ttu-id="00344-103">CIM_DeviceConnection-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="00344-103">CIM_DeviceConnection class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="00344-104">Die **CIM- \_ deviceconnetction** -Zuordnungs Klasse stellt zwei oder mehr verbundene Geräte dar.</span><span class="sxs-lookup"><span data-stu-id="00344-104">The **CIM\_DeviceConnection** association class represents two or more connected devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="00344-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="00344-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="00344-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="00344-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="00344-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="00344-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="00344-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="00344-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="00344-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="00344-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C53C-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_DeviceConnection : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_LogicalDevice REF Antecedent;
  uint32                NegotiatedDataWidth;
  uint64                NegotiatedSpeed;
};
```

## <a name="members"></a><span data-ttu-id="00344-110">Member</span><span class="sxs-lookup"><span data-stu-id="00344-110">Members</span></span>

<span data-ttu-id="00344-111">Die **CIM- \_ deviceconnetction** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="00344-111">The **CIM\_DeviceConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="00344-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="00344-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="00344-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="00344-113">Properties</span></span>

<span data-ttu-id="00344-114">Die **CIM- \_ deviceconnetction** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="00344-114">The **CIM\_DeviceConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="00344-115">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="00344-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00344-116">Datentyp: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="00344-116">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="00344-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="00344-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00344-118">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="00344-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="00344-119">Ein [**CIM \_ LogicalDevice**](cim-logicaldevice.md) , das ein logisches Gerät beschreibt.</span><span class="sxs-lookup"><span data-stu-id="00344-119">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes a logical device.</span></span>

</dd> <dt>

<span data-ttu-id="00344-120">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="00344-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00344-121">Datentyp: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="00344-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="00344-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="00344-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00344-123">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="00344-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="00344-124">Ein [**CIM \_ LogicalDevice**](cim-logicaldevice.md) , das ein zweites logisches Gerät beschreibt, das mit dem vorgängergerät verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="00344-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes a second logical device connected to the Antecedent device.</span></span>

</dd> <dt>

<span data-ttu-id="00344-125">**Aushandateddatawidth**</span><span class="sxs-lookup"><span data-stu-id="00344-125">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00344-126">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="00344-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="00344-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="00344-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00344-128">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits")</span><span class="sxs-lookup"><span data-stu-id="00344-128">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="00344-129">Wenn mehrere Bus-oder Verbindungsdaten breiten möglich sind, definiert diese Eigenschaft die jeweils verwendete Eigenschaft zwischen den Geräten.</span><span class="sxs-lookup"><span data-stu-id="00344-129">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="00344-130">Die Daten Breite wird in Bits angegeben.</span><span class="sxs-lookup"><span data-stu-id="00344-130">Data width is specified in bits.</span></span> <span data-ttu-id="00344-131">Wenn die Daten Breite nicht ausgehandelt wird oder diese Informationen für die Geräteverwaltung nicht verfügbar oder wichtig sind, sollte die-Eigenschaft auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="00344-131">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="00344-132">**Aushandatedspeed**</span><span class="sxs-lookup"><span data-stu-id="00344-132">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00344-133">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="00344-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="00344-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="00344-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00344-135">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="00344-135">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="00344-136">Wenn mehrere Bus-oder Verbindungsgeschwindigkeiten möglich sind, definiert diese Eigenschaft die zwischen den Geräten verwendete.</span><span class="sxs-lookup"><span data-stu-id="00344-136">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="00344-137">Die Geschwindigkeit wird in Bits pro Sekunde angegeben.</span><span class="sxs-lookup"><span data-stu-id="00344-137">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="00344-138">Wenn Verbindungs-oder Busgeschwindigkeiten nicht ausgehandelt werden oder diese Informationen für die Geräteverwaltung nicht verfügbar oder wichtig sind, sollte die-Eigenschaft auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="00344-138">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="00344-139">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="00344-139">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="00344-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="00344-140">Remarks</span></span>

<span data-ttu-id="00344-141">Die **CIM- \_ deviceconnetction** -Klasse wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="00344-141">The **CIM\_DeviceConnection** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="00344-142">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="00344-142">WMI does not implement this class.</span></span> <span data-ttu-id="00344-143">Weitere Informationen zu Klassen, die von **CIM \_ deviceconnetction** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="00344-143">For more information about classes derived from **CIM\_DeviceConnection**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="00344-144">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="00344-144">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="00344-145">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="00344-145">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="00344-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00344-146">Requirements</span></span>



| <span data-ttu-id="00344-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="00344-147">Requirement</span></span> | <span data-ttu-id="00344-148">Wert</span><span class="sxs-lookup"><span data-stu-id="00344-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="00344-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="00344-149">Minimum supported client</span></span><br/> | <span data-ttu-id="00344-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="00344-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="00344-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="00344-151">Minimum supported server</span></span><br/> | <span data-ttu-id="00344-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="00344-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="00344-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="00344-153">Namespace</span></span><br/>                | <span data-ttu-id="00344-154">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="00344-154">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="00344-155">MOF</span><span class="sxs-lookup"><span data-stu-id="00344-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="00344-156"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="00344-156"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="00344-157">DLL</span><span class="sxs-lookup"><span data-stu-id="00344-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00344-158"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00344-158"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00344-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00344-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00344-160">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="00344-160">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

