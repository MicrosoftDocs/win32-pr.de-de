---
description: Die Treiber \_ Info \_ 3-Struktur enthält Druckertreiber Informationen.
ms.assetid: ccf87319-0bcf-4f71-8de3-0190459d2b0e
title: DRIVER_INFO_3 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_3
- _DRIVER_INFO_3A
- _DRIVER_INFO_3W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 64509977a85bc33cb13dac4e6ba2817502c06cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352283"
---
# <a name="driver_info_3-structure"></a><span data-ttu-id="e320f-103">Treiber \_ Info \_ 3-Struktur</span><span class="sxs-lookup"><span data-stu-id="e320f-103">DRIVER\_INFO\_3 structure</span></span>

<span data-ttu-id="e320f-104">Die **Treiber \_ Info \_ 3** -Struktur enthält Druckertreiber Informationen.</span><span class="sxs-lookup"><span data-stu-id="e320f-104">The **DRIVER\_INFO\_3** structure contains printer driver information.</span></span>

## <a name="syntax"></a><span data-ttu-id="e320f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e320f-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_3 {
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
} DRIVER_INFO_3, *PDRIVER_INFO_3;
```



## <a name="members"></a><span data-ttu-id="e320f-106">Member</span><span class="sxs-lookup"><span data-stu-id="e320f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e320f-107">**cversion**</span><span class="sxs-lookup"><span data-stu-id="e320f-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="e320f-108">Die Betriebssystemversion, für die der Treiber geschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="e320f-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="e320f-109">Die unterstützten Werte sind 3 und 4, die jeweils die V3-und v4-Treiber darstellen.</span><span class="sxs-lookup"><span data-stu-id="e320f-109">The supported values are 3 and 4, which represent the V3 and V4 drivers, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="e320f-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="e320f-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="e320f-111">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Treibers angibt (z. b. "QMS 810").</span><span class="sxs-lookup"><span data-stu-id="e320f-111">A pointer to a null-terminated string that specifies the name of the driver (for example, "QMS 810").</span></span>

</dd> <dt>

<span data-ttu-id="e320f-112">**nach-oben**</span><span class="sxs-lookup"><span data-stu-id="e320f-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="e320f-113">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die Umgebung angibt, für die der Treiber geschrieben wurde (z. b. Windows x86, Windows ia64 und Windows x64).</span><span class="sxs-lookup"><span data-stu-id="e320f-113">A pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64).</span></span>

</dd> <dt>

<span data-ttu-id="e320f-114">**pdriverpath**</span><span class="sxs-lookup"><span data-stu-id="e320f-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="e320f-115">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die einen Dateinamen, einen vollständigen Pfad und einen Dateinamen für die Datei angibt, die den Gerätetreiber enthält (z. b. "C: \\ Drivers \\Pscript.dll").</span><span class="sxs-lookup"><span data-stu-id="e320f-115">A pointer to a null-terminated string that specifies a file name or full path and file name for the file that contains the device driver (for example, "C:\\DRIVERS\\Pscript.dll").</span></span>

</dd> <dt>

<span data-ttu-id="e320f-116">**pdatafile**</span><span class="sxs-lookup"><span data-stu-id="e320f-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="e320f-117">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Datei angibt, die Treiber Daten enthält (z. b. "C: \\ Drivers \\ Qms810. PPD").</span><span class="sxs-lookup"><span data-stu-id="e320f-117">A pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, "C:\\DRIVERS\\Qms810.ppd").</span></span>

</dd> <dt>

<span data-ttu-id="e320f-118">**pconfigfile**</span><span class="sxs-lookup"><span data-stu-id="e320f-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="e320f-119">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Konfigurations-Dynamic Link Library des Gerätetreibers angibt (z. b. "C: \\ Drivers \\Pscrptui.dll").</span><span class="sxs-lookup"><span data-stu-id="e320f-119">A pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, "C:\\DRIVERS\\Pscrptui.dll").</span></span>

</dd> <dt>

<span data-ttu-id="e320f-120">**phelpfile**</span><span class="sxs-lookup"><span data-stu-id="e320f-120">**pHelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="e320f-121">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Hilfedatei des Gerätetreibers angibt.</span><span class="sxs-lookup"><span data-stu-id="e320f-121">A pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's help file.</span></span>

</dd> <dt>

<span data-ttu-id="e320f-122">**pdependentfiles**</span><span class="sxs-lookup"><span data-stu-id="e320f-122">**pDependentFiles**</span></span>
</dt> <dd>

<span data-ttu-id="e320f-123">Ein Zeiger auf einen MultiSZ-Puffer, der eine Sequenz von null-terminierten Zeichen folgen enthält.</span><span class="sxs-lookup"><span data-stu-id="e320f-123">A pointer to a MultiSZ buffer that contains a sequence of null-terminated strings.</span></span> <span data-ttu-id="e320f-124">Jede mit NULL endenden Zeichenfolge im Puffer enthält den Namen einer Datei, von der der Treiber abhängt.</span><span class="sxs-lookup"><span data-stu-id="e320f-124">Each null-terminated string in the buffer contains the name of a file the driver depends on.</span></span> <span data-ttu-id="e320f-125">Die Sequenz von Zeichen folgen wird durch eine leere Zeichenfolge der Länge 0 (null) beendet.</span><span class="sxs-lookup"><span data-stu-id="e320f-125">The sequence of strings is terminated by an empty, zero-length string.</span></span> <span data-ttu-id="e320f-126">Wenn **pdependentfiles** nicht **null** ist und keine Dateinamen enthält, wird auf einen Puffer mit zwei leeren Zeichen folgen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e320f-126">If **pDependentFiles** is not **NULL** and does not contain any file names, it will point to a buffer that contains two empty strings.</span></span>

</dd> <dt>

<span data-ttu-id="e320f-127">**pmonitorname**</span><span class="sxs-lookup"><span data-stu-id="e320f-127">**pMonitorName**</span></span>
</dt> <dd>

<span data-ttu-id="e320f-128">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die einen sprach Monitor angibt (z. b. "PJL-Monitor").</span><span class="sxs-lookup"><span data-stu-id="e320f-128">A pointer to a null-terminated string that specifies a language monitor (for example, "PJL monitor").</span></span> <span data-ttu-id="e320f-129">Dieser Member kann **null** sein und sollte nur für Drucker angegeben werden, die bidirektionale Kommunikation unterstützen.</span><span class="sxs-lookup"><span data-stu-id="e320f-129">This member can be **NULL** and should be specified only for printers capable of bidirectional communication.</span></span>

</dd> <dt>

<span data-ttu-id="e320f-130">**pdefaultdatatype**</span><span class="sxs-lookup"><span data-stu-id="e320f-130">**pDefaultDataType**</span></span>
</dt> <dd>

<span data-ttu-id="e320f-131">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Standard Datentyp des Druckauftrags angibt (z. b. "EMF").</span><span class="sxs-lookup"><span data-stu-id="e320f-131">A pointer to a null-terminated string that specifies the default data type of the print job (for example, "EMF").</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e320f-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e320f-132">Requirements</span></span>



| <span data-ttu-id="e320f-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e320f-133">Requirement</span></span> | <span data-ttu-id="e320f-134">Wert</span><span class="sxs-lookup"><span data-stu-id="e320f-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e320f-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e320f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e320f-136">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e320f-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e320f-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e320f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e320f-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e320f-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e320f-139">Header</span><span class="sxs-lookup"><span data-stu-id="e320f-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="e320f-140"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e320f-140"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e320f-141">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="e320f-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e320f-142">**\_ Treiber \_ Info \_ 3W** (Unicode) und **\_ Treiber \_ Info \_ 3a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e320f-142">**\_DRIVER\_INFO\_3W** (Unicode) and **\_DRIVER\_INFO\_3A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="e320f-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e320f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e320f-144">Drucken</span><span class="sxs-lookup"><span data-stu-id="e320f-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e320f-145">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="e320f-145">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="e320f-146">**Addprinterdriver**</span><span class="sxs-lookup"><span data-stu-id="e320f-146">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="e320f-147">**Enumprinterdrivers**</span><span class="sxs-lookup"><span data-stu-id="e320f-147">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="e320f-148">**Getprinterdriver**</span><span class="sxs-lookup"><span data-stu-id="e320f-148">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

 




