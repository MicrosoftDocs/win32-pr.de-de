---
description: Die Treiber \_ Info \_ 2-Struktur identifiziert einen Druckertreiber, die Treiber Versionsnummer, die Umgebung, für die der Treiber geschrieben wurde, den Namen der Datei, in der der Treiber gespeichert ist, usw.
ms.assetid: cca1227d-69b9-44df-8dac-384c2f8843ae
title: DRIVER_INFO_2 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_2
- _DRIVER_INFO_2A
- _DRIVER_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: a88caf5aa10828b81dccefbe8118b3a57aebce97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350201"
---
# <a name="driver_info_2-structure"></a><span data-ttu-id="fa3fc-103">Struktur der Treiber \_ Info \_ 2</span><span class="sxs-lookup"><span data-stu-id="fa3fc-103">DRIVER\_INFO\_2 structure</span></span>

<span data-ttu-id="fa3fc-104">Die **Treiber \_ Info \_ 2** -Struktur identifiziert einen Druckertreiber, die Treiber Versionsnummer, die Umgebung, für die der Treiber geschrieben wurde, den Namen der Datei, in der der Treiber gespeichert ist, usw.</span><span class="sxs-lookup"><span data-stu-id="fa3fc-104">The **DRIVER\_INFO\_2** structure identifies a printer driver, the driver version number, the environment for which the driver was written, the name of the file in which the driver is stored, and so on.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa3fc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa3fc-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_2 {
  DWORD  cVersion;
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDriverPath;
  LPTSTR pDataFile;
  LPTSTR pConfigFile;
} DRIVER_INFO_2, *PDRIVER_INFO_2;
```



## <a name="members"></a><span data-ttu-id="fa3fc-106">Member</span><span class="sxs-lookup"><span data-stu-id="fa3fc-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="fa3fc-107">**cversion**</span><span class="sxs-lookup"><span data-stu-id="fa3fc-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="fa3fc-108">Die Betriebssystemversion, für die der Treiber geschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="fa3fc-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="fa3fc-109">Der unterstützte Wert ist 3.</span><span class="sxs-lookup"><span data-stu-id="fa3fc-109">The supported value is 3.</span></span>

</dd> <dt>

<span data-ttu-id="fa3fc-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="fa3fc-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="fa3fc-111">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Treibers angibt (z. b. "QMS 810").</span><span class="sxs-lookup"><span data-stu-id="fa3fc-111">A pointer to a null-terminated string that specifies the name of the driver (for example, "QMS 810").</span></span>

</dd> <dt>

<span data-ttu-id="fa3fc-112">**nach-oben**</span><span class="sxs-lookup"><span data-stu-id="fa3fc-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="fa3fc-113">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die Umgebung angibt, für die der Treiber geschrieben wurde (z. b. Windows x86, Windows ia64 und Windows x64).</span><span class="sxs-lookup"><span data-stu-id="fa3fc-113">A pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64).</span></span>

</dd> <dt>

<span data-ttu-id="fa3fc-114">**pdriverpath**</span><span class="sxs-lookup"><span data-stu-id="fa3fc-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="fa3fc-115">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die einen Dateinamen, einen vollständigen Pfad und einen Dateinamen für die Datei angibt, die den Gerätetreiber enthält (z. b. "c: \\ Drivers \\pscript.dll").</span><span class="sxs-lookup"><span data-stu-id="fa3fc-115">A pointer to null-terminated string that specifies a file name or full path and file name for the file that contains the device driver (for example, "c:\\drivers\\pscript.dll").</span></span>

</dd> <dt>

<span data-ttu-id="fa3fc-116">**pdatafile**</span><span class="sxs-lookup"><span data-stu-id="fa3fc-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="fa3fc-117">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Datei angibt, die Treiber Daten enthält (z. b. "c: \\ Drivers \\ Qms810. PPD").</span><span class="sxs-lookup"><span data-stu-id="fa3fc-117">A pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, "c:\\drivers\\Qms810.ppd").</span></span>

</dd> <dt>

<span data-ttu-id="fa3fc-118">**pconfigfile**</span><span class="sxs-lookup"><span data-stu-id="fa3fc-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="fa3fc-119">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Configuration. dll des Gerätetreibers angibt (z. b. "c: \\ Drivers \\Pscrptui.dll").</span><span class="sxs-lookup"><span data-stu-id="fa3fc-119">A pointer to a null-terminated string that specifies a file name or a full path and file name for the device-driver's configuration .dll (for example, "c:\\drivers\\Pscrptui.dll").</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fa3fc-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fa3fc-120">Requirements</span></span>



| <span data-ttu-id="fa3fc-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fa3fc-121">Requirement</span></span> | <span data-ttu-id="fa3fc-122">Wert</span><span class="sxs-lookup"><span data-stu-id="fa3fc-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa3fc-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fa3fc-123">Minimum supported client</span></span><br/> | <span data-ttu-id="fa3fc-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fa3fc-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fa3fc-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fa3fc-125">Minimum supported server</span></span><br/> | <span data-ttu-id="fa3fc-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fa3fc-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fa3fc-127">Header</span><span class="sxs-lookup"><span data-stu-id="fa3fc-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa3fc-128"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fa3fc-128"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="fa3fc-129">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="fa3fc-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fa3fc-130">**\_ Treiber \_ Informationen \_ 2W** (Unicode) und **\_ Treiber \_ Info \_ 2a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="fa3fc-130">**\_DRIVER\_INFO\_2W** (Unicode) and **\_DRIVER\_INFO\_2A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="fa3fc-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa3fc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa3fc-132">Drucken</span><span class="sxs-lookup"><span data-stu-id="fa3fc-132">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="fa3fc-133">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="fa3fc-133">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="fa3fc-134">**Addprinterdriver**</span><span class="sxs-lookup"><span data-stu-id="fa3fc-134">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="fa3fc-135">**Getprinterdriver**</span><span class="sxs-lookup"><span data-stu-id="fa3fc-135">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

 




