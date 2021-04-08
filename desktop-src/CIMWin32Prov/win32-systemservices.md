---
description: Die \_ WMI-Klasse der Win32-Systemdienst Zuordnung bezieht sich auf ein Computersystem und ein Dienstprogramm, das im System vorhanden ist.
ms.assetid: b372e696-e1e0-4b1e-9fb8-83af8a75c405
ms.tgt_platform: multiple
title: Win32_SystemServices-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemServices
- Win32_SystemServices.GroupComponent
- Win32_SystemServices.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d8e61469729f3753256bc7fcf5598265b5c1b7dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748392"
---
# <a name="win32_systemservices-class"></a><span data-ttu-id="a18db-103">Win32- \_ systemdiensteklasse</span><span class="sxs-lookup"><span data-stu-id="a18db-103">Win32\_SystemServices class</span></span>

<span data-ttu-id="a18db-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) der Win32-System **\_ Dienst** Zuordnung bezieht sich auf ein Computersystem und ein Dienstprogramm, das im System vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a18db-104">The **Win32\_SystemServices** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a service program that exists on the system.</span></span>

<span data-ttu-id="a18db-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a18db-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a18db-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="a18db-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a18db-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a18db-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F6-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemServices : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_Service        REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="a18db-108">Member</span><span class="sxs-lookup"><span data-stu-id="a18db-108">Members</span></span>

<span data-ttu-id="a18db-109">Die **Win32- \_ systemdiensteklasse** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a18db-109">The **Win32\_SystemServices** class has these types of members:</span></span>

-   [<span data-ttu-id="a18db-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a18db-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a18db-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a18db-111">Properties</span></span>

<span data-ttu-id="a18db-112">Die **Win32- \_ systemdiensteklasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a18db-112">The **Win32\_SystemServices** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a18db-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="a18db-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a18db-114">Datentyp: **Win32 \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="a18db-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="a18db-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a18db-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a18db-116">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Computersystem")</span><span class="sxs-lookup"><span data-stu-id="a18db-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="a18db-117">Verweis auf die-Instanz, die die Eigenschaften des Computer Systems darstellt, auf dem der Dienst vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a18db-117">Reference to the instance representing the properties of the computer system on which the service exists.</span></span>

</dd> <dt>

<span data-ttu-id="a18db-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="a18db-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a18db-119">Datentyp: **Win32- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="a18db-119">Data type: **Win32\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="a18db-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a18db-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a18db-121">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32- \_ Dienst")</span><span class="sxs-lookup"><span data-stu-id="a18db-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Service")</span></span>
</dt> </dl>

<span data-ttu-id="a18db-122">Verweis auf die-Instanz, die den Dienst darstellt, der auf dem Computersystem vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a18db-122">Reference to the instance representing the service that exists on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a18db-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a18db-123">Remarks</span></span>

<span data-ttu-id="a18db-124">Die **Win32- \_ systemdiensteklasse** wird von [**CIM \_ SystemComponent**](cim-systemcomponent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="a18db-124">The **Win32\_SystemServices** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a18db-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a18db-125">Requirements</span></span>



| <span data-ttu-id="a18db-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a18db-126">Requirement</span></span> | <span data-ttu-id="a18db-127">Wert</span><span class="sxs-lookup"><span data-stu-id="a18db-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a18db-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a18db-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a18db-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a18db-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a18db-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a18db-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a18db-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a18db-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a18db-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="a18db-132">Namespace</span></span><br/>                | <span data-ttu-id="a18db-133">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a18db-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a18db-134">MOF</span><span class="sxs-lookup"><span data-stu-id="a18db-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a18db-135"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a18db-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a18db-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a18db-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a18db-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a18db-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a18db-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a18db-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a18db-139">**CIM- \_ SystemComponent**</span><span class="sxs-lookup"><span data-stu-id="a18db-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="a18db-140">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="a18db-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
