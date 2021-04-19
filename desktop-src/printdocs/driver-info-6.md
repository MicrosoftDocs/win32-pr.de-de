---
description: Die Treiber \_ Info \_ 6-Struktur enthält Druckertreiber Informationen.
ms.assetid: 9771cbb5-caaa-4b7d-9a96-d24234440bac
title: DRIVER_INFO_6 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_6
- _DRIVER_INFO_6A
- _DRIVER_INFO_6W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 20edef2aca2c6948984f5195b16711b78112354a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348588"
---
# <a name="driver_info_6-structure"></a><span data-ttu-id="eb083-103">Treiber \_ Info \_ 6-Struktur</span><span class="sxs-lookup"><span data-stu-id="eb083-103">DRIVER\_INFO\_6 structure</span></span>

<span data-ttu-id="eb083-104">Die **Treiber \_ Info \_ 6** -Struktur enthält Druckertreiber Informationen.</span><span class="sxs-lookup"><span data-stu-id="eb083-104">The **DRIVER\_INFO\_6** structure contains printer driver information.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb083-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb083-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_6 {
  DWORD     cVersion;
  LPTSTR    pName;
  LPTSTR    pEnvironment;
  LPTSTR    pDriverPath;
  LPTSTR    pDataFile;
  LPTSTR    pConfigFile;
  LPTSTR    pHelpFile;
  LPTSTR    pDependentFiles;
  LPTSTR    pMonitorName;
  LPTSTR    pDefaultDataType;
  LPTSTR    pszzPreviousNames;
  FILETIME  ftDriverDate;
  DWORDLONG dwlDriverVersion;
  LPTSTR    pszMfgName;
  LPTSTR    pszOEMUrl;
  LPTSTR    pszHardwareID;
  LPTSTR    pszProvider;
} DRIVER_INFO_6, *PDRIVER_INFO_6, *LPDRIVER_INFO_6;
```



## <a name="members"></a><span data-ttu-id="eb083-106">Member</span><span class="sxs-lookup"><span data-stu-id="eb083-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="eb083-107">**cversion**</span><span class="sxs-lookup"><span data-stu-id="eb083-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="eb083-108">Die Betriebssystemversion, für die der Treiber geschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="eb083-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="eb083-109">Der unterstützte Wert ist 3.</span><span class="sxs-lookup"><span data-stu-id="eb083-109">The supported value is 3.</span></span>

</dd> <dt>

<span data-ttu-id="eb083-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="eb083-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="eb083-111">Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen des Treibers angibt (z. b. QMS 810).</span><span class="sxs-lookup"><span data-stu-id="eb083-111">Pointer to a null-terminated string that specifies the name of the driver (for example, QMS 810).</span></span>

</dd> <dt>

<span data-ttu-id="eb083-112">**nach-oben**</span><span class="sxs-lookup"><span data-stu-id="eb083-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="eb083-113">Zeiger auf eine mit NULL endenden Zeichenfolge, die die Umgebung angibt, für die der Treiber geschrieben wurde (z. b. Windows NT x86, Windows ia64 und Windows x64).</span><span class="sxs-lookup"><span data-stu-id="eb083-113">Pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows NT x86, Windows IA64, and Windows x64.</span></span>

</dd> <dt>

<span data-ttu-id="eb083-114">**pdriverpath**</span><span class="sxs-lookup"><span data-stu-id="eb083-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="eb083-115">Zeiger auf eine mit NULL endenden Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Datei angibt, die den Gerätetreiber enthält (z. b. C: \\ Drivers \\Pscript.dll).</span><span class="sxs-lookup"><span data-stu-id="eb083-115">Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains the device driver (for example, C:\\DRIVERS\\Pscript.dll).</span></span>

</dd> <dt>

<span data-ttu-id="eb083-116">**pdatafile**</span><span class="sxs-lookup"><span data-stu-id="eb083-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="eb083-117">Ein Zeiger auf eine mit NULL endenden Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Datei angibt, die Treiber Daten enthält (z. b. C: \\ Drivers \\ Qms810. PPD).</span><span class="sxs-lookup"><span data-stu-id="eb083-117">Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, C:\\DRIVERS\\Qms810.ppd).</span></span>

</dd> <dt>

<span data-ttu-id="eb083-118">**pconfigfile**</span><span class="sxs-lookup"><span data-stu-id="eb083-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="eb083-119">Ein Zeiger auf eine mit NULL endenden Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Konfigurations-Dynamic Link Library des Gerätetreibers angibt (z. b. C: \\ Drivers \\Pscrptui.dll).</span><span class="sxs-lookup"><span data-stu-id="eb083-119">Pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, C:\\DRIVERS\\Pscrptui.dll).</span></span>

</dd> <dt>

<span data-ttu-id="eb083-120">**phelpfile**</span><span class="sxs-lookup"><span data-stu-id="eb083-120">**pHelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="eb083-121">Zeiger auf eine mit NULL endenden Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Hilfedatei des Gerätetreibers angibt (z. b. C: \\ Drivers \\ PSCRPTUI. hlp).</span><span class="sxs-lookup"><span data-stu-id="eb083-121">Pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's help file (for example, C:\\DRIVERS\\Pscrptui.hlp).</span></span>

</dd> <dt>

<span data-ttu-id="eb083-122">**pdependentfiles**</span><span class="sxs-lookup"><span data-stu-id="eb083-122">**pDependentFiles**</span></span>
</dt> <dd>

<span data-ttu-id="eb083-123">Ein Zeiger auf einen MultiSZ-Puffer, der eine Sequenz von null-terminierten Zeichen folgen enthält.</span><span class="sxs-lookup"><span data-stu-id="eb083-123">A pointer to a MultiSZ buffer that contains a sequence of null-terminated strings.</span></span> <span data-ttu-id="eb083-124">Jede mit NULL endenden Zeichenfolge im Puffer enthält den Namen einer Datei, von der der Treiber abhängt.</span><span class="sxs-lookup"><span data-stu-id="eb083-124">Each null-terminated string in the buffer contains the name of a file the driver depends on.</span></span> <span data-ttu-id="eb083-125">Die Sequenz von Zeichen folgen wird durch eine leere Zeichenfolge der Länge 0 (null) beendet.</span><span class="sxs-lookup"><span data-stu-id="eb083-125">The sequence of strings is terminated by an empty, zero-length string.</span></span> <span data-ttu-id="eb083-126">Wenn **pdependentfiles** nicht **null** ist und keine Dateinamen enthält, wird auf einen Puffer mit zwei leeren Zeichen folgen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="eb083-126">If **pDependentFiles** is not **NULL** and does not contain any file names, it will point to a buffer that contains two empty strings.</span></span>

</dd> <dt>

<span data-ttu-id="eb083-127">**pmonitorname**</span><span class="sxs-lookup"><span data-stu-id="eb083-127">**pMonitorName**</span></span>
</dt> <dd>

<span data-ttu-id="eb083-128">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die einen sprach Monitor angibt (z. b. "PJL-Monitor").</span><span class="sxs-lookup"><span data-stu-id="eb083-128">A pointer to a null-terminated string that specifies a language monitor (for example, "PJL monitor").</span></span> <span data-ttu-id="eb083-129">Dieser Member kann **null** sein und sollte nur für Drucker angegeben werden, die bidirektionale Kommunikation unterstützen.</span><span class="sxs-lookup"><span data-stu-id="eb083-129">This member can be **NULL** and should be specified only for printers capable of bidirectional communication.</span></span>

</dd> <dt>

<span data-ttu-id="eb083-130">**pdefaultdatatype**</span><span class="sxs-lookup"><span data-stu-id="eb083-130">**pDefaultDataType**</span></span>
</dt> <dd>

<span data-ttu-id="eb083-131">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Standard Datentyp des Druckauftrags angibt (z. b. "EMF").</span><span class="sxs-lookup"><span data-stu-id="eb083-131">A pointer to a null-terminated string that specifies the default data type of the print job (for example, "EMF").</span></span>

</dd> <dt>

<span data-ttu-id="eb083-132">**pszzpreviousnames**</span><span class="sxs-lookup"><span data-stu-id="eb083-132">**pszzPreviousNames**</span></span>
</dt> <dd>

<span data-ttu-id="eb083-133">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die vorherige Druckertreiber Namen angibt, die mit diesem Treiber kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="eb083-133">A pointer to a null-terminated string that specifies previous printer driver names that are compatible with this driver.</span></span> <span data-ttu-id="eb083-134">Beispiel: OldName1 \\ 0oldname2 \\ 0 \\ 0.</span><span class="sxs-lookup"><span data-stu-id="eb083-134">For example, OldName1\\0OldName2\\0\\0.</span></span>

</dd> <dt>

<span data-ttu-id="eb083-135">**ftdriverdate**</span><span class="sxs-lookup"><span data-stu-id="eb083-135">**ftDriverDate**</span></span>
</dt> <dd>

<span data-ttu-id="eb083-136">Das Datum des Treiber Pakets, das in den Treiberdateien codiert ist.</span><span class="sxs-lookup"><span data-stu-id="eb083-136">The date of the driver package, as coded in the driver files.</span></span>

</dd> <dt>

<span data-ttu-id="eb083-137">**dwldriverversion**</span><span class="sxs-lookup"><span data-stu-id="eb083-137">**dwlDriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="eb083-138">Die Versionsnummer des Treibers.</span><span class="sxs-lookup"><span data-stu-id="eb083-138">Version number of the driver.</span></span> <span data-ttu-id="eb083-139">Dies ergibt sich aus der Versions Struktur des Treibers.</span><span class="sxs-lookup"><span data-stu-id="eb083-139">This comes out of the version structure of the driver.</span></span>

</dd> <dt>

<span data-ttu-id="eb083-140">**pszmf-Name**</span><span class="sxs-lookup"><span data-stu-id="eb083-140">**pszMfgName**</span></span>
</dt> <dd>

<span data-ttu-id="eb083-141">Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen des Herstellers angibt.</span><span class="sxs-lookup"><span data-stu-id="eb083-141">Pointer to a null-terminated string that specifies the manufacturer's name.</span></span>

</dd> <dt>

<span data-ttu-id="eb083-142">**pszoemurl**</span><span class="sxs-lookup"><span data-stu-id="eb083-142">**pszOEMUrl**</span></span>
</dt> <dd>

<span data-ttu-id="eb083-143">Zeiger auf eine mit NULL endenden Zeichenfolge, die die URL für den Hersteller angibt.</span><span class="sxs-lookup"><span data-stu-id="eb083-143">Pointer to a null-terminated string that specifies the URL for the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="eb083-144">**pszhardwareid**</span><span class="sxs-lookup"><span data-stu-id="eb083-144">**pszHardwareID**</span></span>
</dt> <dd>

<span data-ttu-id="eb083-145">Zeiger auf eine mit NULL endenden Zeichenfolge, die die Hardware-ID für den Druckertreiber angibt.</span><span class="sxs-lookup"><span data-stu-id="eb083-145">Pointer to a null-terminated string that specifies the hardware ID for the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="eb083-146">**pszprovider**</span><span class="sxs-lookup"><span data-stu-id="eb083-146">**pszProvider**</span></span>
</dt> <dd>

<span data-ttu-id="eb083-147">Zeiger auf eine mit NULL endenden Zeichenfolge, die den Anbieter des Druckertreibers angibt (z. b. "Microsoft Windows 2000")</span><span class="sxs-lookup"><span data-stu-id="eb083-147">Pointer to a null-terminated string that specifies the provider of the printer driver (for example, "Microsoft Windows 2000")</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb083-148">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb083-148">Remarks</span></span>

<span data-ttu-id="eb083-149">Die Zeichen folgen für diese Member sind in der INF-Datei enthalten, die verwendet wird, um den Treiber hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="eb083-149">The strings for these members are contained in the .inf file that is used to add the driver.</span></span>

<span data-ttu-id="eb083-150">Wenn Sie [**addprinterdriver**](addprinterdriver.md) oder [**addprinterdriverex**](addprinterdriverex.md) aufrufen, bei dem die *Ebene* nicht gleich 6 ist, wenn Sie [**getprinterdriver**](getprinterdriver.md) oder [**enumprinterdrivers**](enumprinterdrivers.md) mit einer *Ebene* gleich 6 aufrufen, wird die **Driver \_ Info \_ 6** -Struktur mit **pszmfgname**, **pszoemurl**, **pszhardwareid** und **pszprovider** auf **null**, **dwldriverversion** auf 0 und **ftdriverdate** auf (0,0) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="eb083-150">If you call [**AddPrinterDriver**](addprinterdriver.md) or [**AddPrinterDriverEx**](addprinterdriverex.md) with *Level* not equal to 6, and then you call [**GetPrinterDriver**](getprinterdriver.md) or [**EnumPrinterDrivers**](enumprinterdrivers.md) with *Level* equal to 6, the **DRIVER\_INFO\_6** structure is returned with **pszMfgName**, **pszOEMUrl**, **pszHardwareID**, and **pszProvider** set to **NULL**, **dwlDriverVersion** set to 0, and **ftDriverDate** set to (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="eb083-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb083-151">Requirements</span></span>



| <span data-ttu-id="eb083-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eb083-152">Requirement</span></span> | <span data-ttu-id="eb083-153">Wert</span><span class="sxs-lookup"><span data-stu-id="eb083-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb083-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eb083-154">Minimum supported client</span></span><br/> | <span data-ttu-id="eb083-155">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eb083-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="eb083-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eb083-156">Minimum supported server</span></span><br/> | <span data-ttu-id="eb083-157">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eb083-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="eb083-158">Header</span><span class="sxs-lookup"><span data-stu-id="eb083-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb083-159"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eb083-159"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="eb083-160">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="eb083-160">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="eb083-161">**\_ Treiber \_ Info \_ 6W** (Unicode) und **\_ Treiber \_ Info \_ 6a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="eb083-161">**\_DRIVER\_INFO\_6W** (Unicode) and **\_DRIVER\_INFO\_6A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="eb083-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb083-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb083-163">Drucken</span><span class="sxs-lookup"><span data-stu-id="eb083-163">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="eb083-164">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="eb083-164">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="eb083-165">**Addprinterdriver**</span><span class="sxs-lookup"><span data-stu-id="eb083-165">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="eb083-166">**Addprinterdriverex**</span><span class="sxs-lookup"><span data-stu-id="eb083-166">**AddPrinterDriverEx**</span></span>](addprinterdriverex.md)
</dt> <dt>

[<span data-ttu-id="eb083-167">**Enumprinterdrivers**</span><span class="sxs-lookup"><span data-stu-id="eb083-167">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="eb083-168">**Getprinterdriver**</span><span class="sxs-lookup"><span data-stu-id="eb083-168">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

 




