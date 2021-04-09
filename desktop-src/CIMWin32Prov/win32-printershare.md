---
description: Die \_ WMI-Klasse von Win32 printershare Association verknüpft einen lokalen Drucker und die Freigabe, die ihn darstellt, wie er über ein Netzwerk angezeigt wird.
ms.assetid: 9ac99e52-5e8f-4329-960f-7bd1fd229e37
ms.tgt_platform: multiple
title: Win32_PrinterShare-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterShare
- Win32_PrinterShare.Antecedent
- Win32_PrinterShare.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 57bc15fc5d3db78179335b039851d7d3b7cbf8a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861496"
---
# <a name="win32_printershare-class"></a><span data-ttu-id="afed8-103">Win32- \_ Klasse "printershare"</span><span class="sxs-lookup"><span data-stu-id="afed8-103">Win32\_PrinterShare class</span></span>

<span data-ttu-id="afed8-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) von **Win32 \_ printershare** Association verknüpft einen lokalen Drucker und die Freigabe, die ihn darstellt, wie er über ein Netzwerk angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="afed8-104">The **Win32\_PrinterShare** association [WMI class](../wmisdk/retrieving-a-class.md) relates a local printer and the share that represents it as it is viewed over a network.</span></span>

<span data-ttu-id="afed8-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="afed8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="afed8-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="afed8-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="afed8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="afed8-107">Syntax</span></span>

``` syntax
class Win32_PrinterShare : CIM_Dependency
{
  Win32_Printer REF Antecedent;
  Win32_Share   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="afed8-108">Member</span><span class="sxs-lookup"><span data-stu-id="afed8-108">Members</span></span>

<span data-ttu-id="afed8-109">Die Win32-Klasse " **\_ printershare** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="afed8-109">The **Win32\_PrinterShare** class has these types of members:</span></span>

-   [<span data-ttu-id="afed8-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="afed8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="afed8-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="afed8-111">Properties</span></span>

<span data-ttu-id="afed8-112">Die **Win32-Klasse \_ printershare** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="afed8-112">The **Win32\_PrinterShare** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="afed8-113">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="afed8-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afed8-114">Datentyp: **Win32- \_ Drucker**</span><span class="sxs-lookup"><span data-stu-id="afed8-114">Data type: **Win32\_Printer**</span></span>
</dt> <dt>

<span data-ttu-id="afed8-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="afed8-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afed8-116">Qualifizierer: [ **Schlüssel**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="afed8-116">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="afed8-117">Verweis auf die-Instanz, die den in dieser Zuordnung freigegebenen lokalen Drucker darstellt.</span><span class="sxs-lookup"><span data-stu-id="afed8-117">Reference to the instance representing the local printer shared in this association.</span></span>

</dd> <dt>

<span data-ttu-id="afed8-118">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="afed8-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afed8-119">Datentyp: **Win32- \_ Freigabe**</span><span class="sxs-lookup"><span data-stu-id="afed8-119">Data type: **Win32\_Share**</span></span>
</dt> <dt>

<span data-ttu-id="afed8-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="afed8-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afed8-121">Qualifizierer: [ **Schlüssel**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="afed8-121">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="afed8-122">Verweis auf die-Instanz, die die Freigabe des Druckers in dieser Zuordnung darstellt.</span><span class="sxs-lookup"><span data-stu-id="afed8-122">Reference to the instance representing the share of the printer in this association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="afed8-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="afed8-123">Remarks</span></span>

<span data-ttu-id="afed8-124">Die **Win32-Klasse \_ printershare** ist von [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="afed8-124">The **Win32\_PrinterShare** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="afed8-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="afed8-125">Requirements</span></span>



| <span data-ttu-id="afed8-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="afed8-126">Requirement</span></span> | <span data-ttu-id="afed8-127">Wert</span><span class="sxs-lookup"><span data-stu-id="afed8-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="afed8-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="afed8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="afed8-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="afed8-129">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="afed8-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="afed8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="afed8-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="afed8-131">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="afed8-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="afed8-132">Namespace</span></span><br/>                | <span data-ttu-id="afed8-133">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="afed8-133">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="afed8-134">MOF</span><span class="sxs-lookup"><span data-stu-id="afed8-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="afed8-135"><dt>Win32 \_ Printer. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="afed8-135"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="afed8-136">DLL</span><span class="sxs-lookup"><span data-stu-id="afed8-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afed8-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afed8-137"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="afed8-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="afed8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afed8-139">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="afed8-139">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
