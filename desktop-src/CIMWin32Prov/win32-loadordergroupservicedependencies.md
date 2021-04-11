---
description: Die \_ WMI-Klasse "Win32 loadordergroupservicedependenassociation" verknüpft einen Basis Dienst und eine Gruppe der Lade Reihenfolge, von der der Dienst gestartet wird.
ms.assetid: 56739b80-9028-4a2e-85ed-973a078860c1
ms.tgt_platform: multiple
title: Win32_LoadOrderGroupServiceDependencies-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LoadOrderGroupServiceDependencies
- Win32_LoadOrderGroupServiceDependencies.Antecedent
- Win32_LoadOrderGroupServiceDependencies.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b95d1aa01def951802434e787931ce348d04ccb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127481"
---
# <a name="win32_loadordergroupservicedependencies-class"></a><span data-ttu-id="535a4-103">Win32 \_ loadordergroupservicedependen-Klasse</span><span class="sxs-lookup"><span data-stu-id="535a4-103">Win32\_LoadOrderGroupServiceDependencies class</span></span>

<span data-ttu-id="535a4-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) " **Win32 \_ loadordergroupservicedependenassociation** " verknüpft einen Basis Dienst und eine Gruppe der Lade Reihenfolge, von der der Dienst gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="535a4-104">The **Win32\_LoadOrderGroupServiceDependencies** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a base service and a load order group that the service depends on to start running.</span></span>

<span data-ttu-id="535a4-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="535a4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="535a4-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="535a4-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="535a4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="535a4-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FC-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_LoadOrderGroupServiceDependencies : CIM_Dependency
{
  Win32_LoadOrderGroup REF Antecedent;
  Win32_BaseService    REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="535a4-108">Member</span><span class="sxs-lookup"><span data-stu-id="535a4-108">Members</span></span>

<span data-ttu-id="535a4-109">Die **Win32 \_ loadordergroupservicedependen-** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="535a4-109">The **Win32\_LoadOrderGroupServiceDependencies** class has these types of members:</span></span>

-   [<span data-ttu-id="535a4-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="535a4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="535a4-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="535a4-111">Properties</span></span>

<span data-ttu-id="535a4-112">Die **Win32 \_ loadordergroupservicedependen-** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="535a4-112">The **Win32\_LoadOrderGroupServiceDependencies** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="535a4-113">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="535a4-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="535a4-114">Datentyp: **Win32 \_ LoadOrderGroup**</span><span class="sxs-lookup"><span data-stu-id="535a4-114">Data type: **Win32\_LoadOrderGroup**</span></span>
</dt> <dt>

<span data-ttu-id="535a4-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="535a4-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="535a4-116">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ LoadOrderGroup")</span><span class="sxs-lookup"><span data-stu-id="535a4-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_LoadOrderGroup")</span></span>
</dt> </dl>

<span data-ttu-id="535a4-117">Verweis auf die-Instanz, die die Eigenschaften der Gruppe der Lade Reihenfolge darstellt, die gestartet werden muss, bevor der abhängige Basis Dienst dieser Klasse gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="535a4-117">Reference to the instance representing the properties of the load order group that must start before the dependent base service of this class can start.</span></span>

</dd> <dt>

<span data-ttu-id="535a4-118">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="535a4-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="535a4-119">Datentyp: **Win32 \_ baseservice**</span><span class="sxs-lookup"><span data-stu-id="535a4-119">Data type: **Win32\_BaseService**</span></span>
</dt> <dt>

<span data-ttu-id="535a4-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="535a4-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="535a4-121">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ baseservice")</span><span class="sxs-lookup"><span data-stu-id="535a4-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_BaseService")</span></span>
</dt> </dl>

<span data-ttu-id="535a4-122">Verweis auf die-Instanz, die die Eigenschaften des Basis Dienes darstellt, der von der Gruppe der Lade Reihenfolge abhängig ist, damit Sie gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="535a4-122">Reference to the instance representing the properties of the base service that is dependent upon the load order group to start running.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="535a4-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="535a4-123">Remarks</span></span>

<span data-ttu-id="535a4-124">Die **Win32-Klasse \_ loadordergroupservicedependenist** von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="535a4-124">The **Win32\_LoadOrderGroupServiceDependencies** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="535a4-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="535a4-125">Requirements</span></span>



| <span data-ttu-id="535a4-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="535a4-126">Requirement</span></span> | <span data-ttu-id="535a4-127">Wert</span><span class="sxs-lookup"><span data-stu-id="535a4-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="535a4-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="535a4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="535a4-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="535a4-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="535a4-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="535a4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="535a4-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="535a4-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="535a4-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="535a4-132">Namespace</span></span><br/>                | <span data-ttu-id="535a4-133">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="535a4-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="535a4-134">MOF</span><span class="sxs-lookup"><span data-stu-id="535a4-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="535a4-135"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="535a4-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="535a4-136">DLL</span><span class="sxs-lookup"><span data-stu-id="535a4-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="535a4-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="535a4-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="535a4-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="535a4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="535a4-139">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="535a4-139">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

<span data-ttu-id="535a4-140">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="535a4-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

