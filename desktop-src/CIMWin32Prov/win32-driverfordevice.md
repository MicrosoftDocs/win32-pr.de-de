---
description: Die \_ WMI-Klasse "Win32 driverfordevice Association" verknüpft eine Drucker Instanz mit einer Druckertreiber Instanz.
ms.assetid: 56ff74b2-31ba-4d8e-b389-9f962932aa03
ms.tgt_platform: multiple
title: Win32_DriverForDevice-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DriverForDevice
- Win32_DriverForDevice.Antecedent
- Win32_DriverForDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b5fb384eed80c6a614af448477c50be3204d3080
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341149"
---
# <a name="win32_driverfordevice-class"></a><span data-ttu-id="c693d-103">Win32- \_ Klasse "driverfordevice"</span><span class="sxs-lookup"><span data-stu-id="c693d-103">Win32\_DriverForDevice class</span></span>

<span data-ttu-id="c693d-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) " **Win32 \_ driverfordevice** Association" verknüpft eine Drucker Instanz mit einer Druckertreiber Instanz.</span><span class="sxs-lookup"><span data-stu-id="c693d-104">The **Win32\_DriverForDevice** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a printer instance to a printer driver instance.</span></span>

<span data-ttu-id="c693d-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c693d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="c693d-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c693d-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c693d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c693d-107">Syntax</span></span>

``` syntax
class Win32_DriverForDevice : CIM_Dependency
{
  Win32_Printer       REF Antecedent;
  Win32_PrinterDriver REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="c693d-108">Member</span><span class="sxs-lookup"><span data-stu-id="c693d-108">Members</span></span>

<span data-ttu-id="c693d-109">Die Win32-Klasse " **\_ driverfordevice** " enthält diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c693d-109">The **Win32\_DriverForDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="c693d-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c693d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c693d-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c693d-111">Properties</span></span>

<span data-ttu-id="c693d-112">Die Win32-Klasse " **\_ driverfordevice** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c693d-112">The **Win32\_DriverForDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c693d-113">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="c693d-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c693d-114">Datentyp: **Win32- \_ Drucker**</span><span class="sxs-lookup"><span data-stu-id="c693d-114">Data type: **Win32\_Printer**</span></span>
</dt> <dt>

<span data-ttu-id="c693d-115">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c693d-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c693d-116">Verweis auf die [**Win32- \_ Drucker**](win32-printer.md) Instanz, die den Drucker darstellt.</span><span class="sxs-lookup"><span data-stu-id="c693d-116">Reference to the [**Win32\_Printer**](win32-printer.md) instance that represents the printer.</span></span>

<span data-ttu-id="c693d-117">Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c693d-117">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> <dt>

<span data-ttu-id="c693d-118">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="c693d-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c693d-119">Datentyp: **Win32 \_ PrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="c693d-119">Data type: **Win32\_PrinterDriver**</span></span>
</dt> <dt>

<span data-ttu-id="c693d-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c693d-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c693d-121">Verweis auf die [**Win32- \_ PrinterDriver**](win32-printerdriver.md) -Instanz, die den Druckertreiber für den Drucker darstellt.</span><span class="sxs-lookup"><span data-stu-id="c693d-121">Reference to the [**Win32\_PrinterDriver**](win32-printerdriver.md) instance that represents the printer driver for the printer.</span></span>

<span data-ttu-id="c693d-122">Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c693d-122">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c693d-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c693d-123">Remarks</span></span>

<span data-ttu-id="c693d-124">Die Win32-Klasse " **\_ driverfordevice** " wird von [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c693d-124">The **Win32\_DriverForDevice** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c693d-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c693d-125">Requirements</span></span>



| <span data-ttu-id="c693d-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c693d-126">Requirement</span></span> | <span data-ttu-id="c693d-127">Wert</span><span class="sxs-lookup"><span data-stu-id="c693d-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c693d-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c693d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c693d-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c693d-129">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="c693d-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c693d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c693d-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c693d-131">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="c693d-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="c693d-132">Namespace</span></span><br/>                | <span data-ttu-id="c693d-133">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c693d-133">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="c693d-134">MOF</span><span class="sxs-lookup"><span data-stu-id="c693d-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c693d-135"><dt>Win32 \_ Printer. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c693d-135"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="c693d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c693d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c693d-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c693d-137"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="c693d-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c693d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c693d-139">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="c693d-139">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

