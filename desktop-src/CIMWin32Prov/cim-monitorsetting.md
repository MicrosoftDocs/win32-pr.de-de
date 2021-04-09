---
description: Die CIM \_ -monitorsetting-Klasse ordnet die Monitor Auflösung dem Desktop Monitor zu, auf den Sie angewendet wird.
ms.assetid: 4bf0b2d5-b901-4294-a33b-9c8a87785af0
ms.tgt_platform: multiple
title: CIM_MonitorSetting-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MonitorSetting
- CIM_MonitorSetting.Setting
- CIM_MonitorSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dc947f4bb484ec5392204747e583fbf80bbf88cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861324"
---
# <a name="cim_monitorsetting-class"></a><span data-ttu-id="e6ec8-103">CIM- \_ monitorsetting-Klasse</span><span class="sxs-lookup"><span data-stu-id="e6ec8-103">CIM\_MonitorSetting class</span></span>

<span data-ttu-id="e6ec8-104">Die **CIM- \_ monitorsetting** -Klasse ordnet die Monitor Auflösung dem Desktop Monitor zu, auf den Sie angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="e6ec8-104">The **CIM\_MonitorSetting** class associates the monitor resolution with the desktop monitor to which it applies.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e6ec8-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e6ec8-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e6ec8-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e6ec8-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e6ec8-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="e6ec8-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e6ec8-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e6ec8-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6ec8-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6ec8-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCED-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_MonitorSetting : CIM_ElementSetting
{
  CIM_MonitorResolution REF Setting;
  CIM_DesktopMonitor    REF Element;
};
```

## <a name="members"></a><span data-ttu-id="e6ec8-110">Member</span><span class="sxs-lookup"><span data-stu-id="e6ec8-110">Members</span></span>

<span data-ttu-id="e6ec8-111">Die **CIM- \_ monitorsetting** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e6ec8-111">The **CIM\_MonitorSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="e6ec8-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e6ec8-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e6ec8-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e6ec8-113">Properties</span></span>

<span data-ttu-id="e6ec8-114">Die **CIM- \_ monitorsetting** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e6ec8-114">The **CIM\_MonitorSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e6ec8-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="e6ec8-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6ec8-116">Datentyp: **CIM \_ Desktopmonitor**</span><span class="sxs-lookup"><span data-stu-id="e6ec8-116">Data type: **CIM\_DesktopMonitor**</span></span>
</dt> <dt>

<span data-ttu-id="e6ec8-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6ec8-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6ec8-118">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element")</span><span class="sxs-lookup"><span data-stu-id="e6ec8-118">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element")</span></span>
</dt> </dl>

<span data-ttu-id="e6ec8-119">Ein [**CIM Desktop \_ Monitor**](cim-desktopmonitor.md) , der den Desktop Monitor beschreibt.</span><span class="sxs-lookup"><span data-stu-id="e6ec8-119">A [**CIM\_DesktopMonitor**](cim-desktopmonitor.md) describing the desktop monitor.</span></span>

</dd> <dt>

<span data-ttu-id="e6ec8-120">**Einstellung**</span><span class="sxs-lookup"><span data-stu-id="e6ec8-120">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6ec8-121">Datentyp: **CIM \_ monitorresolution**</span><span class="sxs-lookup"><span data-stu-id="e6ec8-121">Data type: **CIM\_MonitorResolution**</span></span>
</dt> <dt>

<span data-ttu-id="e6ec8-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6ec8-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6ec8-123">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting")</span><span class="sxs-lookup"><span data-stu-id="e6ec8-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting")</span></span>
</dt> </dl>

<span data-ttu-id="e6ec8-124">Eine [**CIM \_**](cim-monitorresolution.md) -Monitor Auflösung, die die Monitor Auflösung beschreibt, die dem Desktop Monitor zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e6ec8-124">A [**CIM\_MonitorResolution**](cim-monitorresolution.md) describing the monitor resolution associated with the desktop monitor.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e6ec8-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6ec8-125">Remarks</span></span>

<span data-ttu-id="e6ec8-126">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="e6ec8-126">WMI does not implement this class.</span></span>

<span data-ttu-id="e6ec8-127">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="e6ec8-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e6ec8-128">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="e6ec8-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6ec8-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6ec8-129">Requirements</span></span>



| <span data-ttu-id="e6ec8-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6ec8-130">Requirement</span></span> | <span data-ttu-id="e6ec8-131">Wert</span><span class="sxs-lookup"><span data-stu-id="e6ec8-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6ec8-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e6ec8-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e6ec8-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e6ec8-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e6ec8-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e6ec8-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e6ec8-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e6ec8-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e6ec8-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="e6ec8-136">Namespace</span></span><br/>                | <span data-ttu-id="e6ec8-137">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e6ec8-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e6ec8-138">MOF</span><span class="sxs-lookup"><span data-stu-id="e6ec8-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e6ec8-139"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e6ec8-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e6ec8-140">DLL</span><span class="sxs-lookup"><span data-stu-id="e6ec8-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6ec8-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6ec8-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6ec8-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6ec8-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6ec8-143">**CIM- \_ Element Setting**</span><span class="sxs-lookup"><span data-stu-id="e6ec8-143">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> </dl>

 

