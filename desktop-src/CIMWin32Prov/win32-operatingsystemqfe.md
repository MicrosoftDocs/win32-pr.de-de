---
description: Die \_ WMI-Klasse "Win32 operatingsystemqfe Association" bezieht sich auf ein Betriebssystem und die in der Win32- \_ quickfixengineering dargestellten Produktupdates.
ms.assetid: 71985759-7e45-44df-82a9-f9a93e3b923e
ms.tgt_platform: multiple
title: Win32_OperatingSystemQFE-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystemQFE
- Win32_OperatingSystemQFE.Antecedent
- Win32_OperatingSystemQFE.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a3b357e3c6efb62217c137bc6c785185154ed984
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958542"
---
# <a name="win32_operatingsystemqfe-class"></a><span data-ttu-id="44dc8-103">Win32 \_ operatingsystemqfe-Klasse</span><span class="sxs-lookup"><span data-stu-id="44dc8-103">Win32\_OperatingSystemQFE class</span></span>

<span data-ttu-id="44dc8-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) " **Win32 \_ operatingsystemqfe** Association" bezieht sich auf ein Betriebssystem und die in der [**Win32- \_ quickfixengineering**](win32-quickfixengineering.md)dargestellten Produktupdates.</span><span class="sxs-lookup"><span data-stu-id="44dc8-104">The **Win32\_OperatingSystemQFE** association [WMI class](../wmisdk/retrieving-a-class.md) relates an operating system and the product updates applied as represented in [**Win32\_QuickFixEngineering**](win32-quickfixengineering.md).</span></span>

<span data-ttu-id="44dc8-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="44dc8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="44dc8-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="44dc8-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="44dc8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="44dc8-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{2CB2C452-C516-11D2-B364-00105A1F77A1}"), AMENDMENT]
class Win32_OperatingSystemQFE : CIM_Dependency
{
  Win32_OperatingSystem     REF Antecedent;
  Win32_QuickFixEngineering REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="44dc8-108">Member</span><span class="sxs-lookup"><span data-stu-id="44dc8-108">Members</span></span>

<span data-ttu-id="44dc8-109">Die **Win32 \_ operatingsystemqfe** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="44dc8-109">The **Win32\_OperatingSystemQFE** class has these types of members:</span></span>

-   [<span data-ttu-id="44dc8-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="44dc8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="44dc8-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="44dc8-111">Properties</span></span>

<span data-ttu-id="44dc8-112">Die **Win32 \_ operatingsystemqfe** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="44dc8-112">The **Win32\_OperatingSystemQFE** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="44dc8-113">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="44dc8-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44dc8-114">Datentyp: **Win32- \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="44dc8-114">Data type: **Win32\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="44dc8-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="44dc8-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44dc8-116">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Vorgänger"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ OperatingSystem")</span><span class="sxs-lookup"><span data-stu-id="44dc8-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_OperatingSystem")</span></span>
</dt> </dl>

<span data-ttu-id="44dc8-117">Verweis auf die-Instanz, die das System darstellt, das durch das Produkt Update in dieser Zuordnung betroffen ist.</span><span class="sxs-lookup"><span data-stu-id="44dc8-117">Reference to the instance representing the system affected by the product update in this association.</span></span>

</dd> <dt>

<span data-ttu-id="44dc8-118">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="44dc8-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44dc8-119">Datentyp: **Win32 \_ quickfixengineering**</span><span class="sxs-lookup"><span data-stu-id="44dc8-119">Data type: **Win32\_QuickFixEngineering**</span></span>
</dt> <dt>

<span data-ttu-id="44dc8-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="44dc8-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44dc8-121">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**Weak**](../wmisdk/standard-qualifiers.md), [**override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ quickfixengineering")</span><span class="sxs-lookup"><span data-stu-id="44dc8-121">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Weak**](../wmisdk/standard-qualifiers.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_QuickFixEngineering")</span></span>
</dt> </dl>

<span data-ttu-id="44dc8-122">Verweis auf die-Instanz, die die Objektinstanz darstellt, die in dieser Zuordnung auf das Betriebssystem angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="44dc8-122">Reference to the instance representing the object instance applied to the operating system in this association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="44dc8-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="44dc8-123">Remarks</span></span>

<span data-ttu-id="44dc8-124">Die **Win32- \_ operatingsystemqfe** -Klasse wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="44dc8-124">The **Win32\_OperatingSystemQFE** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="44dc8-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44dc8-125">Requirements</span></span>



| <span data-ttu-id="44dc8-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44dc8-126">Requirement</span></span> | <span data-ttu-id="44dc8-127">Wert</span><span class="sxs-lookup"><span data-stu-id="44dc8-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="44dc8-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="44dc8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="44dc8-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="44dc8-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="44dc8-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="44dc8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="44dc8-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="44dc8-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="44dc8-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="44dc8-132">Namespace</span></span><br/>                | <span data-ttu-id="44dc8-133">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="44dc8-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="44dc8-134">MOF</span><span class="sxs-lookup"><span data-stu-id="44dc8-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44dc8-135"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="44dc8-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="44dc8-136">DLL</span><span class="sxs-lookup"><span data-stu-id="44dc8-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44dc8-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44dc8-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44dc8-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44dc8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44dc8-139">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="44dc8-139">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="44dc8-140">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="44dc8-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
