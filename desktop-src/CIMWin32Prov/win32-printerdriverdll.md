---
description: Die \_ WMI-Klasse für die Win32 printerdriverdll-Zuordnung bezieht sich auf einen lokalen Drucker und seine Treiberdatei.
ms.assetid: decbd1de-8091-47f7-94a1-42862070b920
ms.tgt_platform: multiple
title: Win32_PrinterDriverDll-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriverDll
- Win32_PrinterDriverDll.Antecedent
- Win32_PrinterDriverDll.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 41484c39d9e1b59efd79d7aee08719b3a241de97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483694"
---
# <a name="win32_printerdriverdll-class"></a><span data-ttu-id="325c9-103">Win32 \_ printerdriverdll-Klasse</span><span class="sxs-lookup"><span data-stu-id="325c9-103">Win32\_PrinterDriverDll class</span></span>

<span data-ttu-id="325c9-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) für die **Win32 \_ printerdriverdll** -Zuordnung bezieht sich auf einen lokalen Drucker und seine Treiberdatei.</span><span class="sxs-lookup"><span data-stu-id="325c9-104">The **Win32\_PrinterDriverDll** association [WMI class](../wmisdk/retrieving-a-class.md) relates a local printer and its driver file.</span></span>

<span data-ttu-id="325c9-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="325c9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="325c9-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="325c9-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="325c9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="325c9-107">Syntax</span></span>

``` syntax
class Win32_PrinterDriverDll : CIM_Dependency
{
  CIM_DataFile  REF Antecedent;
  Win32_Printer REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="325c9-108">Member</span><span class="sxs-lookup"><span data-stu-id="325c9-108">Members</span></span>

<span data-ttu-id="325c9-109">Die **Win32 \_ printerdriverdll** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="325c9-109">The **Win32\_PrinterDriverDll** class has these types of members:</span></span>

-   [<span data-ttu-id="325c9-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="325c9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="325c9-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="325c9-111">Properties</span></span>

<span data-ttu-id="325c9-112">Die **Win32 \_ printerdriverdll** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="325c9-112">The **Win32\_PrinterDriverDll** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="325c9-113">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="325c9-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="325c9-114">Datentyp: **CIM \_ DataFile**</span><span class="sxs-lookup"><span data-stu-id="325c9-114">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="325c9-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="325c9-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="325c9-116">Qualifizierer: [ **Schlüssel**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="325c9-116">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="325c9-117">Verweis auf die [**CIM- \_ DataFile**](cim-datafile.md) -Instanz, die die Treiberdatei für diesen Windows-basierten Drucker darstellt.</span><span class="sxs-lookup"><span data-stu-id="325c9-117">Reference to the [**CIM\_DataFile**](cim-datafile.md) instance representing the driver file for this Windows-based printer.</span></span>

<span data-ttu-id="325c9-118">Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="325c9-118">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> <dt>

<span data-ttu-id="325c9-119">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="325c9-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="325c9-120">Datentyp: **Win32- \_ Drucker**</span><span class="sxs-lookup"><span data-stu-id="325c9-120">Data type: **Win32\_Printer**</span></span>
</dt> <dt>

<span data-ttu-id="325c9-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="325c9-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="325c9-122">Qualifizierer: [ **Schlüssel**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="325c9-122">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="325c9-123">Verweis auf die [**Win32- \_ Drucker**](win32-printer.md) Instanz.</span><span class="sxs-lookup"><span data-stu-id="325c9-123">Reference to the [**Win32\_Printer**](win32-printer.md) instance.</span></span>

<span data-ttu-id="325c9-124">Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="325c9-124">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="325c9-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="325c9-125">Remarks</span></span>

<span data-ttu-id="325c9-126">Die **Win32-Klasse \_ printerdriverdll** wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="325c9-126">The **Win32\_PrinterDriverDll** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="325c9-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="325c9-127">Requirements</span></span>



| <span data-ttu-id="325c9-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="325c9-128">Requirement</span></span> | <span data-ttu-id="325c9-129">Wert</span><span class="sxs-lookup"><span data-stu-id="325c9-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="325c9-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="325c9-130">Minimum supported client</span></span><br/> | <span data-ttu-id="325c9-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="325c9-131">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="325c9-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="325c9-132">Minimum supported server</span></span><br/> | <span data-ttu-id="325c9-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="325c9-133">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="325c9-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="325c9-134">Namespace</span></span><br/>                | <span data-ttu-id="325c9-135">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="325c9-135">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="325c9-136">MOF</span><span class="sxs-lookup"><span data-stu-id="325c9-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="325c9-137"><dt>Win32 \_ Printer. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="325c9-137"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="325c9-138">DLL</span><span class="sxs-lookup"><span data-stu-id="325c9-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="325c9-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="325c9-139"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="325c9-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="325c9-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="325c9-141">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="325c9-141">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="325c9-142">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="325c9-142">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
