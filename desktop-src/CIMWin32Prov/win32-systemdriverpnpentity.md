---
description: Die \_ WMI-Klasse "Win32 systemdriverpnptity" verknüpft ein Plug & Play-Gerät auf dem Computersystem, auf dem Windows ausgeführt wird, sowie den Treiber, der das Plug & Play Gerät unterstützt.
ms.assetid: 2696c8e5-3bc3-42e3-807b-a387607c7c09
ms.tgt_platform: multiple
title: Win32_SystemDriverPNPEntity-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriverPNPEntity
- Win32_SystemDriverPNPEntity.Antecedent
- Win32_SystemDriverPNPEntity.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8b5a7eedfbd7a545e37cb9cda38c19cf61308761
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523683"
---
# <a name="win32_systemdriverpnpentity-class"></a><span data-ttu-id="39726-103">Win32 \_ systemdriverpnptity-Klasse</span><span class="sxs-lookup"><span data-stu-id="39726-103">Win32\_SystemDriverPNPEntity class</span></span>

<span data-ttu-id="39726-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) " **Win32 \_ systemdriverpnptity** " verknüpft ein Plug & Play-Gerät auf dem Computersystem, auf dem Windows ausgeführt wird, sowie den Treiber, der das Plug & Play Gerät unterstützt.</span><span class="sxs-lookup"><span data-stu-id="39726-104">The **Win32\_SystemDriverPNPEntity** association [WMI class](../wmisdk/retrieving-a-class.md) relates a Plug and Play device on the computer system running Windows and the driver that supports the Plug and Play device.</span></span>

<span data-ttu-id="39726-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="39726-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="39726-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="39726-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="39726-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="39726-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0800F074-CB98-11d2-B35D-00104BC97924}"), AMENDMENT]
class Win32_SystemDriverPNPEntity : CIM_Dependency
{
  Win32_PNPEntity    REF Antecedent;
  Win32_SystemDriver REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="39726-108">Member</span><span class="sxs-lookup"><span data-stu-id="39726-108">Members</span></span>

<span data-ttu-id="39726-109">Die **Win32 \_ systemdriverpnptity** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="39726-109">The **Win32\_SystemDriverPNPEntity** class has these types of members:</span></span>

-   [<span data-ttu-id="39726-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="39726-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="39726-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="39726-111">Properties</span></span>

<span data-ttu-id="39726-112">Die **Win32 \_ systemdriverpnptity** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="39726-112">The **Win32\_SystemDriverPNPEntity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="39726-113">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="39726-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39726-114">Datentyp: **Win32 \_ pnptity**</span><span class="sxs-lookup"><span data-stu-id="39726-114">Data type: **Win32\_PNPEntity**</span></span>
</dt> <dt>

<span data-ttu-id="39726-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39726-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39726-116">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Vorgänger"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ pnptity")</span><span class="sxs-lookup"><span data-stu-id="39726-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PNPEntity")</span></span>
</dt> </dl>

<span data-ttu-id="39726-117">Stellt das vom Treiber gesteuerte Plug & Play Gerät dar.</span><span class="sxs-lookup"><span data-stu-id="39726-117">Represents the Plug and Play device controlled by the driver.</span></span>

</dd> <dt>

<span data-ttu-id="39726-118">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="39726-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39726-119">Datentyp: **Win32 \_ System Driver**</span><span class="sxs-lookup"><span data-stu-id="39726-119">Data type: **Win32\_SystemDriver**</span></span>
</dt> <dt>

<span data-ttu-id="39726-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39726-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39726-121">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ System Driver")</span><span class="sxs-lookup"><span data-stu-id="39726-121">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_SystemDriver")</span></span>
</dt> </dl>

<span data-ttu-id="39726-122">Ein [**Win32- \_ System Treiber**](win32-systemdriver.md) , der den Treiber darstellt, der das Plug & Play Gerät unterstützt.</span><span class="sxs-lookup"><span data-stu-id="39726-122">A [**Win32\_SystemDriver**](win32-systemdriver.md) that represents the driver that supports the Plug and Play device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39726-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39726-123">Remarks</span></span>

<span data-ttu-id="39726-124">Die **Win32- \_ systemdriverpnptity** -Klasse wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="39726-124">The **Win32\_SystemDriverPNPEntity** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="39726-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39726-125">Requirements</span></span>



| <span data-ttu-id="39726-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39726-126">Requirement</span></span> | <span data-ttu-id="39726-127">Wert</span><span class="sxs-lookup"><span data-stu-id="39726-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39726-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="39726-128">Minimum supported client</span></span><br/> | <span data-ttu-id="39726-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="39726-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="39726-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="39726-130">Minimum supported server</span></span><br/> | <span data-ttu-id="39726-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39726-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="39726-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="39726-132">Namespace</span></span><br/>                | <span data-ttu-id="39726-133">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="39726-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="39726-134">MOF</span><span class="sxs-lookup"><span data-stu-id="39726-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="39726-135"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="39726-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="39726-136">DLL</span><span class="sxs-lookup"><span data-stu-id="39726-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39726-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39726-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39726-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39726-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39726-139">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="39726-139">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="39726-140">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="39726-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
