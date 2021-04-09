---
description: Die Win32 \_ -WMI-Klasse loadordergroupservicemembers ordnet eine Gruppe der Lade Reihenfolge und einen Basis Dienst in Beziehung.
ms.assetid: 60fa8292-b9d1-48f2-bd26-e5c9276006fc
ms.tgt_platform: multiple
title: Win32_LoadOrderGroupServiceMembers-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LoadOrderGroupServiceMembers
- Win32_LoadOrderGroupServiceMembers.GroupComponent
- Win32_LoadOrderGroupServiceMembers.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 557e9b029dcbdac06e24d1630f00488696792e25
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861651"
---
# <a name="win32_loadordergroupservicemembers-class"></a><span data-ttu-id="4aa45-103">Win32 \_ loadordergroupservicemembers-Klasse</span><span class="sxs-lookup"><span data-stu-id="4aa45-103">Win32\_LoadOrderGroupServiceMembers class</span></span>

<span data-ttu-id="4aa45-104">Die Win32- [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) **\_ loadordergroupservicemembers** ordnet eine Gruppe der Lade Reihenfolge und einen Basis Dienst in Beziehung.</span><span class="sxs-lookup"><span data-stu-id="4aa45-104">The **Win32\_LoadOrderGroupServiceMembers** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a load order group and a base service.</span></span>

> [!Note]  
> <span data-ttu-id="4aa45-105">[**Win32 \_ Systemdriver**](win32-systemdriver.md) -Objekte sind Mitglieder dieser Gruppe der Lade Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="4aa45-105">[**Win32\_SystemDriver**](win32-systemdriver.md) objects are members of that load order group.</span></span> <span data-ttu-id="4aa45-106">Nicht alle Dienste sind Mitglieder von Gruppen, und nicht alle Gruppen enthalten Dienste darin.</span><span class="sxs-lookup"><span data-stu-id="4aa45-106">Not all services are members of groups, and not all groups have services within them.</span></span>

 

<span data-ttu-id="4aa45-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4aa45-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="4aa45-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="4aa45-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4aa45-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4aa45-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EF-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_LoadOrderGroupServiceMembers : CIM_Component
{
  Win32_LoadOrderGroup REF GroupComponent;
  Win32_BaseService    REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="4aa45-110">Member</span><span class="sxs-lookup"><span data-stu-id="4aa45-110">Members</span></span>

<span data-ttu-id="4aa45-111">Die **Win32 \_ loadordergroupservicemembers** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4aa45-111">The **Win32\_LoadOrderGroupServiceMembers** class has these types of members:</span></span>

-   [<span data-ttu-id="4aa45-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4aa45-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4aa45-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4aa45-113">Properties</span></span>

<span data-ttu-id="4aa45-114">Die **Win32 \_ loadordergroupservicemembers** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4aa45-114">The **Win32\_LoadOrderGroupServiceMembers** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4aa45-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="4aa45-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aa45-116">Datentyp: **Win32 \_ LoadOrderGroup**</span><span class="sxs-lookup"><span data-stu-id="4aa45-116">Data type: **Win32\_LoadOrderGroup**</span></span>
</dt> <dt>

<span data-ttu-id="4aa45-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4aa45-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4aa45-118">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ LoadOrderGroup")</span><span class="sxs-lookup"><span data-stu-id="4aa45-118">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_LoadOrderGroup")</span></span>
</dt> </dl>

<span data-ttu-id="4aa45-119">Verweis auf die-Instanz, die die dem Basis Dienst zugeordneten Eigenschaften der Lade Auftrags Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="4aa45-119">Reference to the instance representing the load order group properties associated with the base service.</span></span>

</dd> <dt>

<span data-ttu-id="4aa45-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="4aa45-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aa45-121">Datentyp: **Win32 \_ baseservice**</span><span class="sxs-lookup"><span data-stu-id="4aa45-121">Data type: **Win32\_BaseService**</span></span>
</dt> <dt>

<span data-ttu-id="4aa45-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4aa45-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4aa45-123">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ baseservice")</span><span class="sxs-lookup"><span data-stu-id="4aa45-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_BaseService")</span></span>
</dt> </dl>

<span data-ttu-id="4aa45-124">Verweis auf die-Instanz, die den Dienst darstellt, der Mitglied einer Gruppe der Lade Reihenfolge ist.</span><span class="sxs-lookup"><span data-stu-id="4aa45-124">Reference to the instance representing the service that is a member of a load order group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4aa45-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4aa45-125">Remarks</span></span>

<span data-ttu-id="4aa45-126">Die **Win32- \_ loadordergroupservicemembers** -Klasse wird von der [**CIM- \_ Komponente**](cim-component.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="4aa45-126">The **Win32\_LoadOrderGroupServiceMembers** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4aa45-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4aa45-127">Requirements</span></span>



| <span data-ttu-id="4aa45-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4aa45-128">Requirement</span></span> | <span data-ttu-id="4aa45-129">Wert</span><span class="sxs-lookup"><span data-stu-id="4aa45-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4aa45-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4aa45-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4aa45-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4aa45-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4aa45-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4aa45-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4aa45-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4aa45-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4aa45-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="4aa45-134">Namespace</span></span><br/>                | <span data-ttu-id="4aa45-135">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4aa45-135">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4aa45-136">MOF</span><span class="sxs-lookup"><span data-stu-id="4aa45-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4aa45-137"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4aa45-137"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4aa45-138">DLL</span><span class="sxs-lookup"><span data-stu-id="4aa45-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4aa45-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4aa45-139"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4aa45-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4aa45-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4aa45-141">**CIM- \_ Komponente**</span><span class="sxs-lookup"><span data-stu-id="4aa45-141">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

<span data-ttu-id="4aa45-142">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4aa45-142">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

