---
description: Die \_ WMI-Klasse "Win32 systemresources Association" bezieht sich auf eine System Ressource und das Computersystem, auf dem Sie sich befindet.
ms.assetid: 90bff0b0-7c1d-44bf-b67e-aefeaa4b4a83
ms.tgt_platform: multiple
title: Win32_SystemResources-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemResources
- Win32_SystemResources.GroupComponent
- Win32_SystemResources.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fe96467e4bc609fa9426edd3c977b5596ea95fe7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958376"
---
# <a name="win32_systemresources-class"></a><span data-ttu-id="49fed-103">Win32- \_ systemresources-Klasse</span><span class="sxs-lookup"><span data-stu-id="49fed-103">Win32\_SystemResources class</span></span>

<span data-ttu-id="49fed-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) " **Win32 \_ systemresources** Association" bezieht sich auf eine System Ressource und das Computersystem, auf dem Sie sich befindet.</span><span class="sxs-lookup"><span data-stu-id="49fed-104">The **Win32\_SystemResources** association [WMI class](../wmisdk/retrieving-a-class.md) relates a system resource and the computer system it resides on.</span></span>

<span data-ttu-id="49fed-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="49fed-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="49fed-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="49fed-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="49fed-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="49fed-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemResources : CIM_ComputerSystemResource
{
  Win32_ComputerSystem REF GroupComponent;
  CIM_SystemResource   REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="49fed-108">Member</span><span class="sxs-lookup"><span data-stu-id="49fed-108">Members</span></span>

<span data-ttu-id="49fed-109">Die **Win32- \_ systemresources** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="49fed-109">The **Win32\_SystemResources** class has these types of members:</span></span>

-   [<span data-ttu-id="49fed-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="49fed-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="49fed-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="49fed-111">Properties</span></span>

<span data-ttu-id="49fed-112">Die **Win32- \_ systemresources** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="49fed-112">The **Win32\_SystemResources** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="49fed-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="49fed-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49fed-114">Datentyp: **Win32 \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="49fed-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="49fed-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49fed-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49fed-116">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Computersystem")</span><span class="sxs-lookup"><span data-stu-id="49fed-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="49fed-117">Verweis auf die-Instanz, die das Computersystem darstellt, auf dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="49fed-117">Reference to the instance representing the computer system where the resource is located.</span></span>

</dd> <dt>

<span data-ttu-id="49fed-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="49fed-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49fed-119">Datentyp: **CIM \_ Systemresource**</span><span class="sxs-lookup"><span data-stu-id="49fed-119">Data type: **CIM\_SystemResource**</span></span>
</dt> <dt>

<span data-ttu-id="49fed-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49fed-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49fed-121">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ Systemresource")</span><span class="sxs-lookup"><span data-stu-id="49fed-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_SystemResource")</span></span>
</dt> </dl>

<span data-ttu-id="49fed-122">Verweis auf die Instanz, die die Ressource (z. b. e/a-Dienste und Arbeitsspeicher Ressourcen) darstellt, die auf dem Computersystem verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="49fed-122">Reference to the instance representing the resource (such as I/O services and memory resources) available on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49fed-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="49fed-123">Remarks</span></span>

<span data-ttu-id="49fed-124">Die **Win32- \_ systemresources** -Klasse wird von [**CIM \_ computersystemresource**](cim-computersystemresource.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="49fed-124">The **Win32\_SystemResources** class is derived from [**CIM\_ComputerSystemResource**](cim-computersystemresource.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="49fed-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49fed-125">Requirements</span></span>



| <span data-ttu-id="49fed-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="49fed-126">Requirement</span></span> | <span data-ttu-id="49fed-127">Wert</span><span class="sxs-lookup"><span data-stu-id="49fed-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49fed-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="49fed-128">Minimum supported client</span></span><br/> | <span data-ttu-id="49fed-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="49fed-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="49fed-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="49fed-130">Minimum supported server</span></span><br/> | <span data-ttu-id="49fed-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="49fed-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="49fed-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="49fed-132">Namespace</span></span><br/>                | <span data-ttu-id="49fed-133">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="49fed-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="49fed-134">MOF</span><span class="sxs-lookup"><span data-stu-id="49fed-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="49fed-135"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="49fed-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="49fed-136">DLL</span><span class="sxs-lookup"><span data-stu-id="49fed-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49fed-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49fed-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49fed-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49fed-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49fed-139">**CIM \_ computersystemresource**</span><span class="sxs-lookup"><span data-stu-id="49fed-139">**CIM\_ComputerSystemResource**</span></span>](cim-computersystemresource.md)
</dt> <dt>

[<span data-ttu-id="49fed-140">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="49fed-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
