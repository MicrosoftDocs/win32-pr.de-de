---
description: Die CIM \_ deviceaccessedbyfile-Zuordnungs Klasse gibt das logische Gerät an, auf das über die CIM \_ Devicefile-Klasse zugegriffen wird.
ms.assetid: 8ba44f40-8b84-4f5c-b719-aded10877654
ms.tgt_platform: multiple
title: CIM_DeviceAccessedByFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceAccessedByFile
- CIM_DeviceAccessedByFile.Dependent
- CIM_DeviceAccessedByFile.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: cf84d2e7943dfe6da88f81ef6963190553f028e7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861268"
---
# <a name="cim_deviceaccessedbyfile-class"></a><span data-ttu-id="fb039-103">CIM \_ deviceaccessedbyfile-Klasse</span><span class="sxs-lookup"><span data-stu-id="fb039-103">CIM\_DeviceAccessedByFile class</span></span>

<span data-ttu-id="fb039-104">Die **CIM \_ deviceaccessedbyfile** -Zuordnungs Klasse gibt das logische Gerät an, auf das über die [**CIM \_ Devicefile**](cim-devicefile.md) -Klasse zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="fb039-104">The **CIM\_DeviceAccessedByFile** association class specifies the logical device accessed by using the referenced [**CIM\_DeviceFile**](cim-devicefile.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fb039-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="fb039-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fb039-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fb039-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fb039-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="fb039-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="fb039-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="fb039-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb039-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb039-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{05D1FFF2-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceAccessedByFile : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_DeviceFile    REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="fb039-110">Member</span><span class="sxs-lookup"><span data-stu-id="fb039-110">Members</span></span>

<span data-ttu-id="fb039-111">Die **CIM \_ deviceaccessedbyfile** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="fb039-111">The **CIM\_DeviceAccessedByFile** class has these types of members:</span></span>

-   [<span data-ttu-id="fb039-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fb039-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fb039-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fb039-113">Properties</span></span>

<span data-ttu-id="fb039-114">Die **CIM \_ deviceaccessedbyfile** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fb039-114">The **CIM\_DeviceAccessedByFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fb039-115">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="fb039-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb039-116">Datentyp: **CIM \_ Devicefile**</span><span class="sxs-lookup"><span data-stu-id="fb039-116">Data type: **CIM\_DeviceFile**</span></span>
</dt> <dt>

<span data-ttu-id="fb039-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb039-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb039-118">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="fb039-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="fb039-119">Eine [**CIM- \_ Devicefile**](cim-devicefile.md) , in der die Gerätedatei beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="fb039-119">A [**CIM\_DeviceFile**](cim-devicefile.md) that describes the device file.</span></span>

</dd> <dt>

<span data-ttu-id="fb039-120">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="fb039-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb039-121">Datentyp: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="fb039-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="fb039-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fb039-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb039-123">Qualifizierer: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span><span class="sxs-lookup"><span data-stu-id="fb039-123">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="fb039-124">Ein [**CIM \_ LogicalDevice**](cim-logicaldevice.md) , das das Gerät beschreibt, auf das mithilfe der Gerätedatei zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="fb039-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the device that is accessed using the device file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fb039-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb039-125">Remarks</span></span>

<span data-ttu-id="fb039-126">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="fb039-126">WMI does not implement this class.</span></span>

<span data-ttu-id="fb039-127">Die **CIM \_ deviceaccessedbyfile** -Klasse wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="fb039-127">The **CIM\_DeviceAccessedByFile** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="fb039-128">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="fb039-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fb039-129">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="fb039-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb039-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb039-130">Requirements</span></span>



| <span data-ttu-id="fb039-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb039-131">Requirement</span></span> | <span data-ttu-id="fb039-132">Wert</span><span class="sxs-lookup"><span data-stu-id="fb039-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb039-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fb039-133">Minimum supported client</span></span><br/> | <span data-ttu-id="fb039-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fb039-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fb039-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fb039-135">Minimum supported server</span></span><br/> | <span data-ttu-id="fb039-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fb039-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fb039-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="fb039-137">Namespace</span></span><br/>                | <span data-ttu-id="fb039-138">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fb039-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fb039-139">MOF</span><span class="sxs-lookup"><span data-stu-id="fb039-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fb039-140"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="fb039-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fb039-141">DLL</span><span class="sxs-lookup"><span data-stu-id="fb039-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb039-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb039-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb039-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb039-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb039-144">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="fb039-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

