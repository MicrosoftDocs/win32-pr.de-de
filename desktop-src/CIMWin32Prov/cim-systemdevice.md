---
description: Die CIM- \_ SystemDevice-Zuordnung stellt eine explizite Beziehung dar, in der logische Geräte von einem System aggregiert werden können.
ms.assetid: df624a9f-0c10-44a3-8075-908e5e481e3c
ms.tgt_platform: multiple
title: CIM_SystemDevice-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemDevice
- CIM_SystemDevice.PartComponent
- CIM_SystemDevice.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dbff9a0ead8790de9ab323509c8b2f1392e6ed6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342770"
---
# <a name="cim_systemdevice-class-cimwin32-wmi-providers"></a><span data-ttu-id="e69b5-103">CIM_SystemDevice-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="e69b5-103">CIM_SystemDevice class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="e69b5-104">Die **CIM- \_ SystemDevice** -Zuordnung stellt eine explizite Beziehung dar, in der logische Geräte von einem System aggregiert werden können.</span><span class="sxs-lookup"><span data-stu-id="e69b5-104">The **CIM\_SystemDevice** association represents an explicit relationship in which logical devices can be aggregated by a system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e69b5-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e69b5-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e69b5-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e69b5-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e69b5-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e69b5-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="e69b5-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e69b5-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e69b5-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e69b5-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{4B2C30D7-BAFE-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class CIM_SystemDevice : CIM_SystemComponent
{
  CIM_LogicalDevice REF PartComponent;
  CIM_System        REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="e69b5-110">Member</span><span class="sxs-lookup"><span data-stu-id="e69b5-110">Members</span></span>

<span data-ttu-id="e69b5-111">Die **CIM- \_ SystemDevice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e69b5-111">The **CIM\_SystemDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="e69b5-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e69b5-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e69b5-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e69b5-113">Properties</span></span>

<span data-ttu-id="e69b5-114">Die **CIM- \_ SystemDevice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e69b5-114">The **CIM\_SystemDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e69b5-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="e69b5-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69b5-116">Datentyp: **CIM- \_ System**</span><span class="sxs-lookup"><span data-stu-id="e69b5-116">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="e69b5-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e69b5-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e69b5-118">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="e69b5-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="e69b5-119">Ein [**CIM- \_ System**](cim-system.md) , das das übergeordnete System in der Zuordnung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="e69b5-119">A [**CIM\_System**](cim-system.md) that describes the parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="e69b5-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="e69b5-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69b5-121">Datentyp: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="e69b5-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="e69b5-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e69b5-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e69b5-123">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("PartComponent"), [**schwach**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e69b5-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e69b5-124">Ein [**CIM \_ LogicalDevice**](cim-logicaldevice.md) , das das logische Gerät beschreibt, das eine Komponente eines Systems ist.</span><span class="sxs-lookup"><span data-stu-id="e69b5-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device that is a component of a system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e69b5-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e69b5-125">Remarks</span></span>

<span data-ttu-id="e69b5-126">Die **CIM- \_ SystemDevice** -Klasse wird von [**CIM \_ SystemComponent**](cim-systemcomponent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="e69b5-126">The **CIM\_SystemDevice** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

<span data-ttu-id="e69b5-127">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="e69b5-127">WMI does not implement this class.</span></span> <span data-ttu-id="e69b5-128">Informationen zu WMI-Klassen, die von **CIM \_ SystemDevice** abgeleitet sind, finden Sie unter [Win32](win32-provider.md)</span><span class="sxs-lookup"><span data-stu-id="e69b5-128">For WMI classes derived from **CIM\_SystemDevice**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="e69b5-129">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="e69b5-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e69b5-130">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="e69b5-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e69b5-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e69b5-131">Requirements</span></span>



| <span data-ttu-id="e69b5-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e69b5-132">Requirement</span></span> | <span data-ttu-id="e69b5-133">Wert</span><span class="sxs-lookup"><span data-stu-id="e69b5-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e69b5-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e69b5-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e69b5-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e69b5-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e69b5-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e69b5-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e69b5-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e69b5-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e69b5-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="e69b5-138">Namespace</span></span><br/>                | <span data-ttu-id="e69b5-139">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e69b5-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e69b5-140">MOF</span><span class="sxs-lookup"><span data-stu-id="e69b5-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e69b5-141"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e69b5-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e69b5-142">DLL</span><span class="sxs-lookup"><span data-stu-id="e69b5-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e69b5-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e69b5-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e69b5-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e69b5-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e69b5-145">**CIM- \_ SystemComponent**</span><span class="sxs-lookup"><span data-stu-id="e69b5-145">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

