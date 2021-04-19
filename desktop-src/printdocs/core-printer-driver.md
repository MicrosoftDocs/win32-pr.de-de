---
description: Stellt einen Druckertreiber dar, von dem andere Druckertreiber abhängig sind.
ms.assetid: b03f9ac1-7ad2-4aee-b496-e1ee15ba7d38
title: CORE_PRINTER_DRIVER Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CORE_PRINTER_DRIVER
- _CORE_PRINTER_DRIVERA
- _CORE_PRINTER_DRIVERW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 786fa3491919659fca60700cfb086023c3fdef3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356149"
---
# <a name="core_printer_driver-structure"></a><span data-ttu-id="f307e-103">Struktur des Kern \_ Drucker \_ Treibers</span><span class="sxs-lookup"><span data-stu-id="f307e-103">CORE\_PRINTER\_DRIVER structure</span></span>

<span data-ttu-id="f307e-104">Stellt einen Druckertreiber dar, von dem andere Druckertreiber abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="f307e-104">Represents a printer driver on which other printer drivers depend.</span></span>

## <a name="syntax"></a><span data-ttu-id="f307e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f307e-105">Syntax</span></span>


```C++
typedef struct _CORE_PRINTER_DRIVER {
  GUID      CoreDriverGUID;
  FILETIME  ftDriverDate;
  DWORDLONG dwlDriverVersion;
  TCHAR     szPackageID[MAX_PATH];
} CORE_PRINTER_DRIVER, *PCORE_PRINTER_DRIVER;
```



## <a name="members"></a><span data-ttu-id="f307e-106">Member</span><span class="sxs-lookup"><span data-stu-id="f307e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f307e-107">**Coredriverguid**</span><span class="sxs-lookup"><span data-stu-id="f307e-107">**CoreDriverGUID**</span></span>
</dt> <dd>

<span data-ttu-id="f307e-108">Die GUID des Haupt Druckertreibers.</span><span class="sxs-lookup"><span data-stu-id="f307e-108">The GUID of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="f307e-109">**ftdriverdate**</span><span class="sxs-lookup"><span data-stu-id="f307e-109">**ftDriverDate**</span></span>
</dt> <dd>

<span data-ttu-id="f307e-110">Das Datum und die Uhrzeit der neuesten Version des Haupt Druckertreibers.</span><span class="sxs-lookup"><span data-stu-id="f307e-110">The date and time of the latest version of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="f307e-111">**dwldriverversion**</span><span class="sxs-lookup"><span data-stu-id="f307e-111">**dwlDriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="f307e-112">Die Versions-ID der neuesten Version des Haupt Druckertreibers.</span><span class="sxs-lookup"><span data-stu-id="f307e-112">The version ID of the latest version of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="f307e-113">**szpackageid, \[ maximaler \_ Pfad\]**</span><span class="sxs-lookup"><span data-stu-id="f307e-113">**szPackageID\[MAX\_PATH\]**</span></span>
</dt> <dd>

<span data-ttu-id="f307e-114">Der Pfad zum Treiber Paket, das den Kern Druckertreiber enthält.</span><span class="sxs-lookup"><span data-stu-id="f307e-114">The path to the driver package that contains the core printer driver.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f307e-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f307e-115">Remarks</span></span>

<span data-ttu-id="f307e-116">Diese Struktur kann den Basis Treiber eines Herstellers darstellen, von dem die Treiber für verschiedene Druckermodelle abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="f307e-116">This structure can represent a manufacturer's base driver on which the drivers for various printer models are dependent.</span></span>

## <a name="requirements"></a><span data-ttu-id="f307e-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f307e-117">Requirements</span></span>



| <span data-ttu-id="f307e-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f307e-118">Requirement</span></span> | <span data-ttu-id="f307e-119">Wert</span><span class="sxs-lookup"><span data-stu-id="f307e-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f307e-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f307e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f307e-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f307e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="f307e-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f307e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f307e-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f307e-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f307e-124">Header</span><span class="sxs-lookup"><span data-stu-id="f307e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f307e-125"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f307e-125"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f307e-126">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="f307e-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f307e-127">**\_ Core \_ Printer \_ driverw** (Unicode) und **\_ Core \_ Printer \_ drivera** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f307e-127">**\_CORE\_PRINTER\_DRIVERW** (Unicode) and **\_CORE\_PRINTER\_DRIVERA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="f307e-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f307e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f307e-129">Drucken</span><span class="sxs-lookup"><span data-stu-id="f307e-129">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f307e-130">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="f307e-130">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




