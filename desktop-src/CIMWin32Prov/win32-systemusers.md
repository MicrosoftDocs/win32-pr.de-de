---
description: Die \_ WMI-Klasse "Win32 systemusers Association" bezieht sich auf ein Computersystem und ein Benutzerkonto auf diesem System.
ms.assetid: 0f6cba69-86f7-4795-a47d-6fb8ed0a00b8
ms.tgt_platform: multiple
title: Win32_SystemUsers-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemUsers
- Win32_SystemUsers.GroupComponent
- Win32_SystemUsers.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a2239983d5b9c080c60d301a557b5487f8cf7fcf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958570"
---
# <a name="win32_systemusers-class"></a><span data-ttu-id="64ade-103">Win32 \_ systemusers-Klasse</span><span class="sxs-lookup"><span data-stu-id="64ade-103">Win32\_SystemUsers class</span></span>

<span data-ttu-id="64ade-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) " **Win32 \_ systemusers** Association" bezieht sich auf ein Computersystem und ein Benutzerkonto auf diesem System.</span><span class="sxs-lookup"><span data-stu-id="64ade-104">The **Win32\_SystemUsers** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a user account on that system.</span></span>

<span data-ttu-id="64ade-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="64ade-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="64ade-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="64ade-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="64ade-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="64ade-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F2-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemUsers : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_UserAccount    REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="64ade-108">Member</span><span class="sxs-lookup"><span data-stu-id="64ade-108">Members</span></span>

<span data-ttu-id="64ade-109">Die **Win32 \_ systemusers** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="64ade-109">The **Win32\_SystemUsers** class has these types of members:</span></span>

-   [<span data-ttu-id="64ade-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="64ade-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="64ade-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="64ade-111">Properties</span></span>

<span data-ttu-id="64ade-112">Die **Win32 \_ systemusers** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="64ade-112">The **Win32\_SystemUsers** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="64ade-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="64ade-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64ade-114">Datentyp: **Win32 \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="64ade-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="64ade-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="64ade-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64ade-116">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Computersystem")</span><span class="sxs-lookup"><span data-stu-id="64ade-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="64ade-117">Verweis auf die-Instanz, die das Computersystem darstellt, das das Benutzerkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="64ade-117">Reference to the instance representing the computer system containing the user account.</span></span>

</dd> <dt>

<span data-ttu-id="64ade-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="64ade-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64ade-119">Datentyp: **Win32- \_ Benutzerkonto**</span><span class="sxs-lookup"><span data-stu-id="64ade-119">Data type: **Win32\_UserAccount**</span></span>
</dt> <dt>

<span data-ttu-id="64ade-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="64ade-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64ade-121">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ User Account")</span><span class="sxs-lookup"><span data-stu-id="64ade-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_UserAccount")</span></span>
</dt> </dl>

<span data-ttu-id="64ade-122">Verweis auf die-Instanz, die das Benutzerkonto auf dem Computersystem darstellt.</span><span class="sxs-lookup"><span data-stu-id="64ade-122">Reference to the instance representing the user account on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="64ade-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64ade-123">Remarks</span></span>

<span data-ttu-id="64ade-124">Die **Win32 \_** -System Component-Klasse wird von [**CIM \_ SystemComponent**](cim-systemcomponent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="64ade-124">The **Win32\_SystemUsers** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="64ade-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64ade-125">Requirements</span></span>



| <span data-ttu-id="64ade-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64ade-126">Requirement</span></span> | <span data-ttu-id="64ade-127">Wert</span><span class="sxs-lookup"><span data-stu-id="64ade-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="64ade-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="64ade-128">Minimum supported client</span></span><br/> | <span data-ttu-id="64ade-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="64ade-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="64ade-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="64ade-130">Minimum supported server</span></span><br/> | <span data-ttu-id="64ade-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="64ade-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="64ade-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="64ade-132">Namespace</span></span><br/>                | <span data-ttu-id="64ade-133">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="64ade-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="64ade-134">MOF</span><span class="sxs-lookup"><span data-stu-id="64ade-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64ade-135"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="64ade-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="64ade-136">DLL</span><span class="sxs-lookup"><span data-stu-id="64ade-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64ade-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64ade-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64ade-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64ade-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64ade-139">**CIM- \_ SystemComponent**</span><span class="sxs-lookup"><span data-stu-id="64ade-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="64ade-140">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="64ade-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
