---
description: Die \_ WMI-Klasse "Win32 systemnetworkconnections Association" bezieht sich auf eine Netzwerkverbindung und das Computersystem, auf dem Sie sich befindet.
ms.assetid: 7c47f653-74a9-4729-a72c-94930181f8c9
ms.tgt_platform: multiple
title: Win32_SystemNetworkConnections-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemNetworkConnections
- Win32_SystemNetworkConnections.GroupComponent
- Win32_SystemNetworkConnections.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e90562dd4f98a00cf848fb83a9e3051b387241e4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127612"
---
# <a name="win32_systemnetworkconnections-class"></a><span data-ttu-id="81fe5-103">Win32 \_ systemnetworkconnections-Klasse</span><span class="sxs-lookup"><span data-stu-id="81fe5-103">Win32\_SystemNetworkConnections class</span></span>

<span data-ttu-id="81fe5-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) " **Win32 \_ systemnetworkconnections** Association" bezieht sich auf eine Netzwerkverbindung und das Computersystem, auf dem Sie sich befindet.</span><span class="sxs-lookup"><span data-stu-id="81fe5-104">The **Win32\_SystemNetworkConnections** association [WMI class](../wmisdk/retrieving-a-class.md) relates a network connection and the computer system on which it resides.</span></span>

<span data-ttu-id="81fe5-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="81fe5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="81fe5-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="81fe5-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="81fe5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="81fe5-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemNetworkConnections : CIM_SystemComponent
{
  Win32_ComputerSystem    REF GroupComponent;
  Win32_NetworkConnection REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="81fe5-108">Member</span><span class="sxs-lookup"><span data-stu-id="81fe5-108">Members</span></span>

<span data-ttu-id="81fe5-109">Die **Win32- \_ systemnetworkconnections** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="81fe5-109">The **Win32\_SystemNetworkConnections** class has these types of members:</span></span>

-   [<span data-ttu-id="81fe5-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="81fe5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="81fe5-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="81fe5-111">Properties</span></span>

<span data-ttu-id="81fe5-112">Die **Win32- \_ systemnetworkconnections** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="81fe5-112">The **Win32\_SystemNetworkConnections** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="81fe5-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="81fe5-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81fe5-114">Datentyp: **Win32 \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="81fe5-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="81fe5-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81fe5-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81fe5-116">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Computersystem")</span><span class="sxs-lookup"><span data-stu-id="81fe5-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="81fe5-117">Verweis auf die-Instanz, die das Computersystem darstellt, das mit dem Netzwerk verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="81fe5-117">Reference to the instance representing the computer system connected to the network.</span></span>

</dd> <dt>

<span data-ttu-id="81fe5-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="81fe5-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81fe5-119">Datentyp: **Win32 \_ Network Connection**</span><span class="sxs-lookup"><span data-stu-id="81fe5-119">Data type: **Win32\_NetworkConnection**</span></span>
</dt> <dt>

<span data-ttu-id="81fe5-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81fe5-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81fe5-121">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Network Connection")</span><span class="sxs-lookup"><span data-stu-id="81fe5-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkConnection")</span></span>
</dt> </dl>

<span data-ttu-id="81fe5-122">Verweis auf die-Instanz, die die Netzwerkverbindung mit diesem Computersystem darstellt.</span><span class="sxs-lookup"><span data-stu-id="81fe5-122">Reference to the instance representing the network connection to this computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="81fe5-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="81fe5-123">Remarks</span></span>

<span data-ttu-id="81fe5-124">Die **Win32- \_ systemnetworkconnections** -Klasse wird von [**CIM \_ SystemComponent**](cim-systemcomponent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="81fe5-124">The **Win32\_SystemNetworkConnections** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="81fe5-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81fe5-125">Requirements</span></span>



| <span data-ttu-id="81fe5-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="81fe5-126">Requirement</span></span> | <span data-ttu-id="81fe5-127">Wert</span><span class="sxs-lookup"><span data-stu-id="81fe5-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81fe5-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="81fe5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="81fe5-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="81fe5-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="81fe5-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="81fe5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="81fe5-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81fe5-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="81fe5-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="81fe5-132">Namespace</span></span><br/>                | <span data-ttu-id="81fe5-133">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="81fe5-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="81fe5-134">MOF</span><span class="sxs-lookup"><span data-stu-id="81fe5-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81fe5-135"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="81fe5-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="81fe5-136">DLL</span><span class="sxs-lookup"><span data-stu-id="81fe5-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81fe5-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81fe5-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81fe5-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81fe5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81fe5-139">**CIM- \_ SystemComponent**</span><span class="sxs-lookup"><span data-stu-id="81fe5-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="81fe5-140">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="81fe5-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
