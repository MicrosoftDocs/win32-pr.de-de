---
description: Die Treiber \_ Info \_ 4-Struktur enthält Druckertreiber Informationen.
ms.assetid: 63000de6-74e7-4427-98d7-7bbd2dd61080
title: DRIVER_INFO_4 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_4
- _DRIVER_INFO_4A
- _DRIVER_INFO_4W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b737947b19e93a6b8de0563128a0f1be412101ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215856"
---
# <a name="driver_info_4-structure"></a><span data-ttu-id="96b09-103">Treiber \_ Info \_ 4-Struktur</span><span class="sxs-lookup"><span data-stu-id="96b09-103">DRIVER\_INFO\_4 structure</span></span>

<span data-ttu-id="96b09-104">Die **Treiber \_ Info \_ 4** -Struktur enthält Druckertreiber Informationen.</span><span class="sxs-lookup"><span data-stu-id="96b09-104">The **DRIVER\_INFO\_4** structure contains printer driver information.</span></span>

## <a name="syntax"></a><span data-ttu-id="96b09-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="96b09-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_4 {
  DWORD  cVersion;
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDriverPath;
  LPTSTR pDataFile;
  LPTSTR pConfigFile;
  LPTSTR pHelpFile;
  LPTSTR pDependentFiles;
  LPTSTR pMonitorName;
  LPTSTR pDefaultDataType;
  LPTSTR pszzPreviousNames;
} DRIVER_INFO_4, *PDRIVER_INFO_4;
```



## <a name="members"></a><span data-ttu-id="96b09-106">Member</span><span class="sxs-lookup"><span data-stu-id="96b09-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="96b09-107">**cversion**</span><span class="sxs-lookup"><span data-stu-id="96b09-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="96b09-108">Die Betriebssystemversion, für die der Treiber geschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="96b09-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="96b09-109">Der unterstützte Wert ist 3.</span><span class="sxs-lookup"><span data-stu-id="96b09-109">The supported value is 3.</span></span>

</dd> <dt>

<span data-ttu-id="96b09-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="96b09-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="96b09-111">Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen des Treibers angibt (z. b. "QMS 810").</span><span class="sxs-lookup"><span data-stu-id="96b09-111">Pointer to a null-terminated string that specifies the name of the driver (for example, "QMS 810").</span></span>

</dd> <dt>

<span data-ttu-id="96b09-112">**nach-oben**</span><span class="sxs-lookup"><span data-stu-id="96b09-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="96b09-113">Zeiger auf eine mit NULL endenden Zeichenfolge, die die Umgebung angibt, für die der Treiber geschrieben wurde (z. b. Windows x86, Windows ia64 und Windows x64).</span><span class="sxs-lookup"><span data-stu-id="96b09-113">Pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64).</span></span>

</dd> <dt>

<span data-ttu-id="96b09-114">**pdriverpath**</span><span class="sxs-lookup"><span data-stu-id="96b09-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="96b09-115">Zeiger auf eine mit NULL endenden Zeichenfolge, die einen Dateinamen oder vollständigen Pfad und Dateinamen für die Datei angibt, die den Gerätetreiber enthält (z. b. C: \\ Drivers \\Pscript.dll).</span><span class="sxs-lookup"><span data-stu-id="96b09-115">Pointer to a null-terminated string that specifies a file name or full path and file name for the file that contains the device driver (for example, C:\\DRIVERS\\Pscript.dll).</span></span>

</dd> <dt>

<span data-ttu-id="96b09-116">**pdatafile**</span><span class="sxs-lookup"><span data-stu-id="96b09-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="96b09-117">Ein Zeiger auf eine mit NULL endenden Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Datei angibt, die Treiber Daten enthält (z. b. C: \\ Drivers \\ Qms810. PPD).</span><span class="sxs-lookup"><span data-stu-id="96b09-117">Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, C:\\DRIVERS\\Qms810.ppd).</span></span>

</dd> <dt>

<span data-ttu-id="96b09-118">**pconfigfile**</span><span class="sxs-lookup"><span data-stu-id="96b09-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="96b09-119">Ein Zeiger auf eine mit NULL endenden Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Konfigurations-Dynamic Link Library des Gerätetreibers angibt (z. b. C: \\ Drivers \\Pscrptui.dll).</span><span class="sxs-lookup"><span data-stu-id="96b09-119">Pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, C:\\DRIVERS\\Pscrptui.dll).</span></span>

</dd> <dt>

<span data-ttu-id="96b09-120">**phelpfile**</span><span class="sxs-lookup"><span data-stu-id="96b09-120">**pHelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="96b09-121">Zeiger auf eine mit NULL endenden Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Hilfedatei des Gerätetreibers angibt.</span><span class="sxs-lookup"><span data-stu-id="96b09-121">Pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's help file.</span></span>

</dd> <dt>

<span data-ttu-id="96b09-122">**pdependentfiles**</span><span class="sxs-lookup"><span data-stu-id="96b09-122">**pDependentFiles**</span></span>
</dt> <dd>

<span data-ttu-id="96b09-123">Ein Zeiger auf einen MultiSZ-Puffer, der eine Sequenz von null-terminierten Zeichen folgen enthält.</span><span class="sxs-lookup"><span data-stu-id="96b09-123">A pointer to a MultiSZ buffer that contains a sequence of null-terminated strings.</span></span> <span data-ttu-id="96b09-124">Jede mit NULL endenden Zeichenfolge im Puffer enthält den Namen einer Datei, von der der Treiber abhängt.</span><span class="sxs-lookup"><span data-stu-id="96b09-124">Each null-terminated string in the buffer contains the name of a file the driver depends on.</span></span> <span data-ttu-id="96b09-125">Die Sequenz von Zeichen folgen wird durch eine leere Zeichenfolge der Länge 0 (null) beendet.</span><span class="sxs-lookup"><span data-stu-id="96b09-125">The sequence of strings is terminated by an empty, zero-length string.</span></span> <span data-ttu-id="96b09-126">Wenn **pdependentfiles** nicht **null** ist und keine Dateinamen enthält, wird auf einen Puffer mit zwei leeren Zeichen folgen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="96b09-126">If **pDependentFiles** is not **NULL** and does not contain any file names, it will point to a buffer that contains two empty strings.</span></span>

</dd> <dt>

<span data-ttu-id="96b09-127">**pmonitorname**</span><span class="sxs-lookup"><span data-stu-id="96b09-127">**pMonitorName**</span></span>
</dt> <dd>

<span data-ttu-id="96b09-128">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die einen sprach Monitor angibt (z. b. PJL-Monitor).</span><span class="sxs-lookup"><span data-stu-id="96b09-128">A pointer to a null-terminated string that specifies a language monitor (for example, PJL monitor).</span></span> <span data-ttu-id="96b09-129">Dieser Member kann **null** sein und sollte nur für Drucker angegeben werden, die bidirektionale Kommunikation unterstützen.</span><span class="sxs-lookup"><span data-stu-id="96b09-129">This member can be **NULL** and should be specified only for printers capable of bidirectional communication.</span></span>

</dd> <dt>

<span data-ttu-id="96b09-130">**pdefaultdatatype**</span><span class="sxs-lookup"><span data-stu-id="96b09-130">**pDefaultDataType**</span></span>
</dt> <dd>

<span data-ttu-id="96b09-131">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Standard Datentyp des Druckauftrags angibt (z. b. EMF).</span><span class="sxs-lookup"><span data-stu-id="96b09-131">A pointer to a null-terminated string that specifies the default data type of the print job (for example, EMF).</span></span>

</dd> <dt>

<span data-ttu-id="96b09-132">**pszzpreviousnames**</span><span class="sxs-lookup"><span data-stu-id="96b09-132">**pszzPreviousNames**</span></span>
</dt> <dd>

<span data-ttu-id="96b09-133">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die vorherige Druckertreiber Namen angibt, die mit diesem Treiber kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="96b09-133">A pointer to a null-terminated string that specifies previous printer driver names that are compatible with this driver.</span></span> <span data-ttu-id="96b09-134">Beispiel: OldName1 \\ 0oldname2 \\ 0 \\ 0.</span><span class="sxs-lookup"><span data-stu-id="96b09-134">For example, OldName1\\0OldName2\\0\\0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="96b09-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96b09-135">Requirements</span></span>



| <span data-ttu-id="96b09-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="96b09-136">Requirement</span></span> | <span data-ttu-id="96b09-137">Wert</span><span class="sxs-lookup"><span data-stu-id="96b09-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96b09-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="96b09-138">Minimum supported client</span></span><br/> | <span data-ttu-id="96b09-139">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="96b09-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="96b09-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="96b09-140">Minimum supported server</span></span><br/> | <span data-ttu-id="96b09-141">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="96b09-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="96b09-142">Header</span><span class="sxs-lookup"><span data-stu-id="96b09-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="96b09-143"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="96b09-143"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="96b09-144">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="96b09-144">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="96b09-145">**\_ Treiber \_ Info \_ 4W** (Unicode) und **\_ Treiber \_ Info \_ 4a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="96b09-145">**\_DRIVER\_INFO\_4W** (Unicode) and **\_DRIVER\_INFO\_4A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="96b09-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="96b09-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96b09-147">Drucken</span><span class="sxs-lookup"><span data-stu-id="96b09-147">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="96b09-148">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="96b09-148">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="96b09-149">**Addprinterdriver**</span><span class="sxs-lookup"><span data-stu-id="96b09-149">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="96b09-150">**Enumprinterdrivers**</span><span class="sxs-lookup"><span data-stu-id="96b09-150">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="96b09-151">**Getprinterdriver**</span><span class="sxs-lookup"><span data-stu-id="96b09-151">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

 




