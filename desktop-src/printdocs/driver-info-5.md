---
description: Die Treiber \_ Info \_ 5-Struktur enthält Druckertreiber Informationen.
ms.assetid: 6fb63a9f-5227-46a3-97dc-8de1968e9d63
title: DRIVER_INFO_5 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_5
- _DRIVER_INFO_5A
- _DRIVER_INFO_5W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 11281e69b70b2d87d354138a6313c8bca6673944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355381"
---
# <a name="driver_info_5-structure"></a><span data-ttu-id="fbb74-103">Treiber \_ Info \_ 5-Struktur</span><span class="sxs-lookup"><span data-stu-id="fbb74-103">DRIVER\_INFO\_5 structure</span></span>

<span data-ttu-id="fbb74-104">Die **Treiber \_ Info \_ 5** -Struktur enthält Druckertreiber Informationen.</span><span class="sxs-lookup"><span data-stu-id="fbb74-104">The **DRIVER\_INFO\_5** structure contains printer driver information.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbb74-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fbb74-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_5 {
  DWORD  cVersion;
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDriverPath;
  LPTSTR pDataFile;
  LPTSTR pConfigFile;
  DWORD  dwDriverAttributes;
  DWORD  dwConfigVersion;
  DWORD  dwDriverVersion;
} DRIVER_INFO_5, *PDRIVER_INFO_5;
```



## <a name="members"></a><span data-ttu-id="fbb74-106">Member</span><span class="sxs-lookup"><span data-stu-id="fbb74-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="fbb74-107">**cversion**</span><span class="sxs-lookup"><span data-stu-id="fbb74-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="fbb74-108">Die Betriebssystemversion, für die der Treiber geschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="fbb74-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="fbb74-109">Der unterstützte Wert ist 3.</span><span class="sxs-lookup"><span data-stu-id="fbb74-109">The supported value is 3.</span></span>

</dd> <dt>

<span data-ttu-id="fbb74-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="fbb74-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="fbb74-111">Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen des Treibers angibt (z. b. QMS 810).</span><span class="sxs-lookup"><span data-stu-id="fbb74-111">Pointer to a null-terminated string that specifies the name of the driver (for example, QMS 810).</span></span>

</dd> <dt>

<span data-ttu-id="fbb74-112">**nach-oben**</span><span class="sxs-lookup"><span data-stu-id="fbb74-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="fbb74-113">Zeiger auf eine mit NULL endenden Zeichenfolge, die die Umgebung angibt, für die der Treiber geschrieben wurde (z. b. Windows x86, Windows ia64 und Windows x64).</span><span class="sxs-lookup"><span data-stu-id="fbb74-113">Pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64).</span></span>

</dd> <dt>

<span data-ttu-id="fbb74-114">**pdriverpath**</span><span class="sxs-lookup"><span data-stu-id="fbb74-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="fbb74-115">Zeiger auf eine mit NULL endenden Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Datei angibt, die den Gerätetreiber enthält (z. b. C: \\ Drivers \\Pscript.dll).</span><span class="sxs-lookup"><span data-stu-id="fbb74-115">Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains the device driver (for example, C:\\DRIVERS\\Pscript.dll).</span></span>

</dd> <dt>

<span data-ttu-id="fbb74-116">**pdatafile**</span><span class="sxs-lookup"><span data-stu-id="fbb74-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="fbb74-117">Ein Zeiger auf eine mit NULL endenden Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Datei angibt, die Treiber Daten enthält (z. b. C: \\ Drivers \\ Qms810. PPD).</span><span class="sxs-lookup"><span data-stu-id="fbb74-117">Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, C:\\DRIVERS\\Qms810.ppd).</span></span>

</dd> <dt>

<span data-ttu-id="fbb74-118">**pconfigfile**</span><span class="sxs-lookup"><span data-stu-id="fbb74-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="fbb74-119">Ein Zeiger auf eine mit NULL endenden Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Konfigurations-Dynamic Link Library des Gerätetreibers angibt (z. b. C: \\ Drivers \\Pscrptui.dll).</span><span class="sxs-lookup"><span data-stu-id="fbb74-119">Pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, C:\\DRIVERS\\Pscrptui.dll).</span></span>

</dd> <dt>

<span data-ttu-id="fbb74-120">**dwdriverattribute**</span><span class="sxs-lookup"><span data-stu-id="fbb74-120">**dwDriverAttributes**</span></span>
</dt> <dd>

<span data-ttu-id="fbb74-121">Treiber Attribute, wie z. b. umpd/kmpd.</span><span class="sxs-lookup"><span data-stu-id="fbb74-121">Driver attributes, like UMPD/KMPD.</span></span>

</dd> <dt>

<span data-ttu-id="fbb74-122">**dwconfigversion**</span><span class="sxs-lookup"><span data-stu-id="fbb74-122">**dwConfigVersion**</span></span>
</dt> <dd>

<span data-ttu-id="fbb74-123">Gibt an, wie oft die Konfigurationsdatei für diesen Treiber seit dem letzten Neustart des Spoolers aktualisiert oder herabgestuft wurde.</span><span class="sxs-lookup"><span data-stu-id="fbb74-123">Number of times the configuration file for this driver has been upgraded or downgraded since the last spooler restart.</span></span>

</dd> <dt>

<span data-ttu-id="fbb74-124">**dwdriverversion**</span><span class="sxs-lookup"><span data-stu-id="fbb74-124">**dwDriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="fbb74-125">Gibt an, wie oft die Treiberdatei für diesen Treiber seit dem letzten Neustart des Spoolers aktualisiert oder herabgestuft wurde.</span><span class="sxs-lookup"><span data-stu-id="fbb74-125">Number of times the driver file for this driver has been upgraded or downgraded since the last spooler restart.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fbb74-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fbb74-126">Requirements</span></span>



| <span data-ttu-id="fbb74-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fbb74-127">Requirement</span></span> | <span data-ttu-id="fbb74-128">Wert</span><span class="sxs-lookup"><span data-stu-id="fbb74-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbb74-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fbb74-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fbb74-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fbb74-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fbb74-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fbb74-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fbb74-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fbb74-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fbb74-133">Header</span><span class="sxs-lookup"><span data-stu-id="fbb74-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbb74-134"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fbb74-134"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="fbb74-135">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="fbb74-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fbb74-136">**\_ Treiber \_ Info \_ 5W** (Unicode) und **\_ Treiber \_ Info \_ 5A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="fbb74-136">**\_DRIVER\_INFO\_5W** (Unicode) and **\_DRIVER\_INFO\_5A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="fbb74-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fbb74-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbb74-138">Drucken</span><span class="sxs-lookup"><span data-stu-id="fbb74-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="fbb74-139">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="fbb74-139">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="fbb74-140">**Addprinterdriver**</span><span class="sxs-lookup"><span data-stu-id="fbb74-140">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="fbb74-141">**Enumprinterdrivers**</span><span class="sxs-lookup"><span data-stu-id="fbb74-141">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="fbb74-142">**Getprinterdriver**</span><span class="sxs-lookup"><span data-stu-id="fbb74-142">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

 




