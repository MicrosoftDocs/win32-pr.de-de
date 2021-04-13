---
description: Enthält Druckertreiber Informationen.
ms.assetid: 6237def2-ffd4-4d93-b3a4-56f225793457
title: DRIVER_INFO_8 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_8
- _DRIVER_INFO_8A
- _DRIVER_INFO_8W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 3cc174fdc8617a8ff59afc5a12740eaba715114f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349089"
---
# <a name="driver_info_8-structure"></a><span data-ttu-id="5ed5a-103">Treiber \_ Info \_ 8-Struktur</span><span class="sxs-lookup"><span data-stu-id="5ed5a-103">DRIVER\_INFO\_8 structure</span></span>

<span data-ttu-id="5ed5a-104">Enthält Druckertreiber Informationen.</span><span class="sxs-lookup"><span data-stu-id="5ed5a-104">Contains printer driver information.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ed5a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ed5a-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_8 {
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
  LPTSTR    pszPrintProcessor;
  LPTSTR    pszVendorSetup;
  LPTSTR    pszzColorProfiles;
  LPTSTR    pszInfPath;
  DWORD     dwPrinterDriverAttributes;
  LPTSTR    pszzCoreDriverDependencies;
  FILETIME  ftMinInboxDriverVerDate;
  DWORDLONG dwlMinInboxDriverVerVersion;
} DRIVER_INFO_8, *PDRIVER_INFO_8, *LPDRIVER_INFO_8;
```



## <a name="members"></a><span data-ttu-id="5ed5a-106">Member</span><span class="sxs-lookup"><span data-stu-id="5ed5a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5ed5a-107">**cversion**</span><span class="sxs-lookup"><span data-stu-id="5ed5a-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="5ed5a-108">Die Betriebssystemversion, für die der Treiber geschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="5ed5a-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="5ed5a-109">Der unterstützte Wert ist 3.</span><span class="sxs-lookup"><span data-stu-id="5ed5a-109">The supported value is 3.</span></span>

</dd> <dt>

<span data-ttu-id="5ed5a-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="5ed5a-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="5ed5a-111">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Treibers angibt (z. b. QMS 810).</span><span class="sxs-lookup"><span data-stu-id="5ed5a-111">A pointer to a null-terminated string that specifies the name of the driver (for example, QMS 810).</span></span>

</dd> <dt>

<span data-ttu-id="5ed5a-112">**nach-oben**</span><span class="sxs-lookup"><span data-stu-id="5ed5a-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="5ed5a-113">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die Umgebung angibt, für die der Treiber geschrieben wurde (z. b. Windows x86, Windows ia64 und Windows x64).</span><span class="sxs-lookup"><span data-stu-id="5ed5a-113">A pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64.</span></span>

</dd> <dt>

<span data-ttu-id="5ed5a-114">**pdriverpath**</span><span class="sxs-lookup"><span data-stu-id="5ed5a-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="5ed5a-115">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Datei angibt, die den Gerätetreiber enthält (z. b. C: \\ Drivers \\Pscript.dll).</span><span class="sxs-lookup"><span data-stu-id="5ed5a-115">A pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains the device driver (for example, C:\\DRIVERS\\Pscript.dll).</span></span>

</dd> <dt>

<span data-ttu-id="5ed5a-116">**pdatafile**</span><span class="sxs-lookup"><span data-stu-id="5ed5a-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="5ed5a-117">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Datei angibt, die Treiber Daten enthält (z. b. C: \\ Drivers \\ Qms810. PPD).</span><span class="sxs-lookup"><span data-stu-id="5ed5a-117">A pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, C:\\DRIVERS\\Qms810.ppd).</span></span>

</dd> <dt>

<span data-ttu-id="5ed5a-118">**pconfigfile**</span><span class="sxs-lookup"><span data-stu-id="5ed5a-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="5ed5a-119">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Konfigurations-Dynamic Link Library des Gerätetreibers angibt (z. b. C: \\ Drivers \\Pscrptui.dll).</span><span class="sxs-lookup"><span data-stu-id="5ed5a-119">A pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, C:\\DRIVERS\\Pscrptui.dll).</span></span>

</dd> <dt>

<span data-ttu-id="5ed5a-120">**phelpfile**</span><span class="sxs-lookup"><span data-stu-id="5ed5a-120">**pHelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="5ed5a-121">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die einen Dateinamen oder einen vollständigen Pfad und Dateinamen für die Hilfedatei des Gerätetreibers angibt (z. b. C: \\ Drivers \\ PSCRPTUI. hlp).</span><span class="sxs-lookup"><span data-stu-id="5ed5a-121">A pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's help file (for example, C:\\DRIVERS\\Pscrptui.hlp).</span></span>

</dd> <dt>

<span data-ttu-id="5ed5a-122">**pdependentfiles**</span><span class="sxs-lookup"><span data-stu-id="5ed5a-122">**pDependentFiles**</span></span>
</dt> <dd>

<span data-ttu-id="5ed5a-123">Ein Zeiger auf einen MultiSZ-Puffer, der eine Sequenz von null-terminierten Zeichen folgen enthält.</span><span class="sxs-lookup"><span data-stu-id="5ed5a-123">A pointer to a MultiSZ buffer that contains a sequence of null-terminated strings.</span></span> <span data-ttu-id="5ed5a-124">Jede mit NULL endenden Zeichenfolge im Puffer enthält den Namen einer Datei, von der der Treiber abhängt.</span><span class="sxs-lookup"><span data-stu-id="5ed5a-124">Each null-terminated string in the buffer contains the name of a file the driver depends on.</span></span> <span data-ttu-id="5ed5a-125">Die Sequenz von Zeichen folgen wird durch eine leere Zeichenfolge der Länge 0 (null) beendet.</span><span class="sxs-lookup"><span data-stu-id="5ed5a-125">The sequence of strings is terminated by an empty, zero-length string.</span></span> <span data-ttu-id="5ed5a-126">Wenn **pdependentfiles** nicht **null** ist und keine Dateinamen enthält, wird auf einen Puffer mit zwei leeren Zeichen folgen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5ed5a-126">If **pDependentFiles** is not **NULL** and does not contain any file names, it will point to a buffer that contains two empty strings.</span></span>

</dd> <dt>

<span data-ttu-id="5ed5a-127">**pmonitorname**</span><span class="sxs-lookup"><span data-stu-id="5ed5a-127">**pMonitorName**</span></span>
</dt> <dd>

<span data-ttu-id="5ed5a-128">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die einen sprach Monitor angibt (z. b. "PJL-Monitor").</span><span class="sxs-lookup"><span data-stu-id="5ed5a-128">A pointer to a null-terminated string that specifies a language monitor (for example, "PJL monitor").</span></span> <span data-ttu-id="5ed5a-129">Dieser Member kann **null** sein und sollte nur für Drucker angegeben werden, die bidirektionale Kommunikation unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5ed5a-129">This member can be **NULL** and should be specified only for printers capable of bidirectional communication.</span></span>

</dd> <dt>

<span data-ttu-id="5ed5a-130">**pdefaultdatatype**</span><span class="sxs-lookup"><span data-stu-id="5ed5a-130">**pDefaultDataType**</span></span>
</dt> <dd>

<span data-ttu-id="5ed5a-131">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Standard Datentyp des Druckauftrags angibt (z. b. "EMF").</span><span class="sxs-lookup"><span data-stu-id="5ed5a-131">A pointer to a null-terminated string that specifies the default data type of the print job (for example, "EMF").</span></span>

</dd> <dt>

<span data-ttu-id="5ed5a-132">**pszzpreviousnames**</span><span class="sxs-lookup"><span data-stu-id="5ed5a-132">**pszzPreviousNames**</span></span>
</dt> <dd>

<span data-ttu-id="5ed5a-133">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die vorherige Druckertreiber Namen angibt, die mit diesem Treiber kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="5ed5a-133">A pointer to a null-terminated string that specifies previous printer driver names that are compatible with this driver.</span></span> <span data-ttu-id="5ed5a-134">Beispiel: OldName1 \\ 0oldname2 \\ 0 \\ 0.</span><span class="sxs-lookup"><span data-stu-id="5ed5a-134">For example, OldName1\\0OldName2\\0\\0.</span></span>

</dd> <dt>

<span data-ttu-id="5ed5a-135">**ftdriverdate**</span><span class="sxs-lookup"><span data-stu-id="5ed5a-135">**ftDriverDate**</span></span>
</dt> <dd>

<span data-ttu-id="5ed5a-136">Das Datum des Treiber Pakets, das in den Treiberdateien codiert ist.</span><span class="sxs-lookup"><span data-stu-id="5ed5a-136">The date of the driver package, as coded in the driver files.</span></span>

</dd> <dt>

<span data-ttu-id="5ed5a-137">**dwldriverversion**</span><span class="sxs-lookup"><span data-stu-id="5ed5a-137">**dwlDriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="5ed5a-138">Die Versionsnummer des Treibers.</span><span class="sxs-lookup"><span data-stu-id="5ed5a-138">The version number of the driver.</span></span> <span data-ttu-id="5ed5a-139">Dies ergibt sich aus der Versions Struktur des Treibers.</span><span class="sxs-lookup"><span data-stu-id="5ed5a-139">This comes from the version structure of the driver.</span></span>

</dd> <dt>

<span data-ttu-id="5ed5a-140">**pszmf-Name**</span><span class="sxs-lookup"><span data-stu-id="5ed5a-140">**pszMfgName**</span></span>
</dt> <dd>

<span data-ttu-id="5ed5a-141">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Herstellers angibt.</span><span class="sxs-lookup"><span data-stu-id="5ed5a-141">A pointer to a null-terminated string that specifies the manufacturer's name.</span></span>

</dd> <dt>

<span data-ttu-id="5ed5a-142">**pszoemurl**</span><span class="sxs-lookup"><span data-stu-id="5ed5a-142">**pszOEMUrl**</span></span>
</dt> <dd>

<span data-ttu-id="5ed5a-143">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die URL für den Hersteller angibt.</span><span class="sxs-lookup"><span data-stu-id="5ed5a-143">A pointer to a null-terminated string that specifies the URL for the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="5ed5a-144">**pszhardwareid**</span><span class="sxs-lookup"><span data-stu-id="5ed5a-144">**pszHardwareID**</span></span>
</dt> <dd>

<span data-ttu-id="5ed5a-145">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die Hardware-ID für den Druckertreiber angibt.</span><span class="sxs-lookup"><span data-stu-id="5ed5a-145">A pointer to a null-terminated string that specifies the hardware ID for the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="5ed5a-146">**pszprovider**</span><span class="sxs-lookup"><span data-stu-id="5ed5a-146">**pszProvider**</span></span>
</dt> <dd>

<span data-ttu-id="5ed5a-147">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Anbieter des Druckertreibers angibt (z. b. "Microsoft Windows 2000").</span><span class="sxs-lookup"><span data-stu-id="5ed5a-147">A pointer to a null-terminated string that specifies the provider of the printer driver (for example, "Microsoft Windows 2000").</span></span>

</dd> <dt>

<span data-ttu-id="5ed5a-148">**pszprintprocessor**</span><span class="sxs-lookup"><span data-stu-id="5ed5a-148">**pszPrintProcessor**</span></span>
</dt> <dd>

<span data-ttu-id="5ed5a-149">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Druck Prozessor angibt (z. b. "WinPrint").</span><span class="sxs-lookup"><span data-stu-id="5ed5a-149">A pointer to a null-terminated string that specifies the print processor (for example, "WinPrint").</span></span>

</dd> <dt>

<span data-ttu-id="5ed5a-150">**pszvendorsetup**</span><span class="sxs-lookup"><span data-stu-id="5ed5a-150">**pszVendorSetup**</span></span>
</dt> <dd>

<span data-ttu-id="5ed5a-151">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die Treiber-Setup-DLL und den Einstiegspunkt des Anbieters angibt.</span><span class="sxs-lookup"><span data-stu-id="5ed5a-151">A pointer to a null-terminated string that specifies the vendor's driver setup DLL and entry point.</span></span>

</dd> <dt>

<span data-ttu-id="5ed5a-152">**pszzcolorprofiles**</span><span class="sxs-lookup"><span data-stu-id="5ed5a-152">**pszzColorProfiles**</span></span>
</dt> <dd>

<span data-ttu-id="5ed5a-153">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die Farbprofile angibt, die dem Treiber zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="5ed5a-153">A pointer to a null-terminated string that specifies the color profiles associated with the driver.</span></span>

</dd> <dt>

<span data-ttu-id="5ed5a-154">**pszinfpath**</span><span class="sxs-lookup"><span data-stu-id="5ed5a-154">**pszInfPath**</span></span>
</dt> <dd>

<span data-ttu-id="5ed5a-155">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Pfad zur INF-Datei des Treibers im Treiber Speicher angibt.</span><span class="sxs-lookup"><span data-stu-id="5ed5a-155">A pointer to a null-terminated string that specifies the path to the driver's .inf file in the driver store.</span></span> <span data-ttu-id="5ed5a-156">(Siehe Hinweise.) Dieser Wert muss **null** sein, wenn die Treiber \_ Informationen \_ 8 an [**addprinterdriver**](addprinterdriver.md) oder [**addprinterdriverex**](addprinterdriverex.md)übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="5ed5a-156">(See Remarks.) This must be **NULL** if the DRIVER\_INFO\_8 is being passed to [**AddPrinterDriver**](addprinterdriver.md) or [**AddPrinterDriverEx**](addprinterdriverex.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ed5a-157">**dwprinterdriverattribute**</span><span class="sxs-lookup"><span data-stu-id="5ed5a-157">**dwPrinterDriverAttributes**</span></span>
</dt> <dd>

<span data-ttu-id="5ed5a-158">Attributflags für Druckertreiber.</span><span class="sxs-lookup"><span data-stu-id="5ed5a-158">Attribute flags for printer drivers.</span></span> <span data-ttu-id="5ed5a-159">Dieser Wert muss 0 sein, wenn die Treiber \_ Informationen \_ 8 an [**addprinterdriver**](addprinterdriver.md) oder [**addprinterdriverex**](addprinterdriverex.md)übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="5ed5a-159">This must be 0 if the DRIVER\_INFO\_8 is being passed to [**AddPrinterDriver**](addprinterdriver.md) or [**AddPrinterDriverEx**](addprinterdriverex.md).</span></span> <span data-ttu-id="5ed5a-160">Andernfalls kann es sich um eine beliebige Kombination der folgenden Flags handeln:</span><span class="sxs-lookup"><span data-stu-id="5ed5a-160">Otherwise, it can be any combination of the following flags:</span></span>



| <span data-ttu-id="5ed5a-161">FlagName/-Wert</span><span class="sxs-lookup"><span data-stu-id="5ed5a-161">Flag name/value</span></span>                                                         | <span data-ttu-id="5ed5a-162">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5ed5a-162">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="5ed5a-163">Minimaler Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="5ed5a-163">Minimum OS</span></span>                                             |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="5ed5a-164">Drucker \_ Treiber \_ Paket \_</span><span class="sxs-lookup"><span data-stu-id="5ed5a-164">PRINTER\_DRIVER\_PACKAGE\_AWARE</span></span><br/> <span data-ttu-id="5ed5a-165">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5ed5a-165">0x00000001</span></span><br/>        | <span data-ttu-id="5ed5a-166">Der Druckertreiber ist Teil eines Treiber Pakets.</span><span class="sxs-lookup"><span data-stu-id="5ed5a-166">The printer driver is part of a driver package.</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="5ed5a-167">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5ed5a-167">Windows Vista</span></span>                                          |
| <span data-ttu-id="5ed5a-168">Drucker \_ Treiber- \_ XPS</span><span class="sxs-lookup"><span data-stu-id="5ed5a-168">PRINTER\_DRIVER\_XPS</span></span><br/> <span data-ttu-id="5ed5a-169">0x00000002</span><span class="sxs-lookup"><span data-stu-id="5ed5a-169">0x00000002</span></span><br/>                   | <span data-ttu-id="5ed5a-170">Der Druckertreiber unterstützt das Microsoft XPS-Format, das in [XML Paper Specification: Overview (Übersicht](/previous-versions/windows/hardware/design/dn641615(v=vs.85))) und auch in [Product Behavior, Abschnitt <27>beschrieben wird ](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43).</span><span class="sxs-lookup"><span data-stu-id="5ed5a-170">The printer driver supports the Microsoft XPS format described in the [XML Paper Specification: Overview](/previous-versions/windows/hardware/design/dn641615(v=vs.85)), and also in [Product Behavior, section <27>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43).</span></span>                        | <span data-ttu-id="5ed5a-171">Windows 8</span><span class="sxs-lookup"><span data-stu-id="5ed5a-171">Windows 8</span></span><br/> <span data-ttu-id="5ed5a-172">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5ed5a-172">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="5ed5a-173">Drucker \_ Treiber- \_ Sandkasten \_ aktiviert</span><span class="sxs-lookup"><span data-stu-id="5ed5a-173">PRINTER\_DRIVER\_SANDBOX\_ENABLED</span></span><br/> <span data-ttu-id="5ed5a-174">0x00000004</span><span class="sxs-lookup"><span data-stu-id="5ed5a-174">0x00000004</span></span><br/>      | <span data-ttu-id="5ed5a-175">Der Druckertreiber ist mit der [Druckertreiber Isolation](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24)kompatibel.</span><span class="sxs-lookup"><span data-stu-id="5ed5a-175">The printer driver is compatible with [printer driver isolation](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span> <span data-ttu-id="5ed5a-176">Weitere Informationen finden Sie unter [Product Behavior, Section <28>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43).</span><span class="sxs-lookup"><span data-stu-id="5ed5a-176">For more information, see [Product Behavior, section <28>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43).</span></span> | <span data-ttu-id="5ed5a-177">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5ed5a-177">Windows 7</span></span><br/> <span data-ttu-id="5ed5a-178">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5ed5a-178">Windows Server 2008 R2</span></span><br/> |
| <span data-ttu-id="5ed5a-179">Drucker \_ Treiber \_ Klasse</span><span class="sxs-lookup"><span data-stu-id="5ed5a-179">PRINTER\_DRIVER\_CLASS</span></span><br/> <span data-ttu-id="5ed5a-180">0x00000008</span><span class="sxs-lookup"><span data-stu-id="5ed5a-180">0x00000008</span></span><br/>                 | <span data-ttu-id="5ed5a-181">Der Druckertreiber ist ein [Klassen Druckertreiber](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span><span class="sxs-lookup"><span data-stu-id="5ed5a-181">The printer driver is a [class printer driver](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                                       | <span data-ttu-id="5ed5a-182">Windows 8</span><span class="sxs-lookup"><span data-stu-id="5ed5a-182">Windows 8</span></span><br/> <span data-ttu-id="5ed5a-183">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5ed5a-183">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="5ed5a-184">\_ \_ abgeleiteter Druckertreiber</span><span class="sxs-lookup"><span data-stu-id="5ed5a-184">PRINTER\_DRIVER\_DERIVED</span></span><br/> <span data-ttu-id="5ed5a-185">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5ed5a-185">0x00000010</span></span><br/>               | <span data-ttu-id="5ed5a-186">Der Druckertreiber ist ein [abgeleiteter Druckertreiber](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span><span class="sxs-lookup"><span data-stu-id="5ed5a-186">The printer driver is a [derived printer driver](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                                   | <span data-ttu-id="5ed5a-187">Windows 8</span><span class="sxs-lookup"><span data-stu-id="5ed5a-187">Windows 8</span></span><br/> <span data-ttu-id="5ed5a-188">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5ed5a-188">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="5ed5a-189">Drucker \_ Treiber \_ nicht \_ share fähig</span><span class="sxs-lookup"><span data-stu-id="5ed5a-189">PRINTER\_DRIVER\_NOT\_SHAREABLE</span></span><br/> <span data-ttu-id="5ed5a-190">0x00000020</span><span class="sxs-lookup"><span data-stu-id="5ed5a-190">0x00000020</span></span><br/>        | <span data-ttu-id="5ed5a-191">Drucker, die diesen Druckertreiber verwenden, können nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5ed5a-191">Printers using this printer driver cannot be shared.</span></span>                                                                                                                                                                                                                                                                                                | <span data-ttu-id="5ed5a-192">Windows 8</span><span class="sxs-lookup"><span data-stu-id="5ed5a-192">Windows 8</span></span><br/> <span data-ttu-id="5ed5a-193">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5ed5a-193">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="5ed5a-194">Drucker \_ Treiber \_ Kategorie \_ Fax</span><span class="sxs-lookup"><span data-stu-id="5ed5a-194">PRINTER\_DRIVER\_CATEGORY\_FAX</span></span><br/> <span data-ttu-id="5ed5a-195">0x00000040</span><span class="sxs-lookup"><span data-stu-id="5ed5a-195">0x00000040</span></span><br/>         | <span data-ttu-id="5ed5a-196">Der Druckertreiber ist für die Verwendung mit [Faxdruckern](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24)vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="5ed5a-196">The printer driver is intended for use with [fax printers](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                                    | <span data-ttu-id="5ed5a-197">Windows 8</span><span class="sxs-lookup"><span data-stu-id="5ed5a-197">Windows 8</span></span><br/> <span data-ttu-id="5ed5a-198">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5ed5a-198">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="5ed5a-199">Drucker \_ Treiber \_ - \_ kategoriedatei</span><span class="sxs-lookup"><span data-stu-id="5ed5a-199">PRINTER\_DRIVER\_CATEGORY\_FILE</span></span><br/> <span data-ttu-id="5ed5a-200">0x00000080</span><span class="sxs-lookup"><span data-stu-id="5ed5a-200">0x00000080</span></span><br/>        | <span data-ttu-id="5ed5a-201">Der Druckertreiber ist für die Verwendung mit [Datei Druckern](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24)vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="5ed5a-201">The printer driver is intended for use with [file printers](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                                  | <span data-ttu-id="5ed5a-202">Windows 8</span><span class="sxs-lookup"><span data-stu-id="5ed5a-202">Windows 8</span></span><br/> <span data-ttu-id="5ed5a-203">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5ed5a-203">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="5ed5a-204">Drucker \_ Treiber \_ Kategorie \_ virtuell</span><span class="sxs-lookup"><span data-stu-id="5ed5a-204">PRINTER\_DRIVER\_CATEGORY\_VIRTUAL</span></span><br/> <span data-ttu-id="5ed5a-205">0x00000100</span><span class="sxs-lookup"><span data-stu-id="5ed5a-205">0x00000100</span></span><br/>     | <span data-ttu-id="5ed5a-206">Der Druckertreiber ist für die Verwendung mit [virtuellen Druckern](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24)vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="5ed5a-206">The printer driver is intended for use with [virtual printers](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                            | <span data-ttu-id="5ed5a-207">Windows 8</span><span class="sxs-lookup"><span data-stu-id="5ed5a-207">Windows 8</span></span><br/> <span data-ttu-id="5ed5a-208">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5ed5a-208">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="5ed5a-209">\_ \_ Kategorie \_ Dienst für Druckertreiber</span><span class="sxs-lookup"><span data-stu-id="5ed5a-209">PRINTER\_DRIVER\_CATEGORY\_SERVICE</span></span><br/> <span data-ttu-id="5ed5a-210">0x00000200</span><span class="sxs-lookup"><span data-stu-id="5ed5a-210">0x00000200</span></span><br/>     | <span data-ttu-id="5ed5a-211">Der Druckertreiber ist für die Verwendung mit [Dienst Druckern](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24)vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="5ed5a-211">The printer driver is intended for use with [service printers](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                            | <span data-ttu-id="5ed5a-212">Windows 8</span><span class="sxs-lookup"><span data-stu-id="5ed5a-212">Windows 8</span></span><br/> <span data-ttu-id="5ed5a-213">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5ed5a-213">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="5ed5a-214">Drucker \_ Treiber- \_ Soft \_ Reset \_ erforderlich</span><span class="sxs-lookup"><span data-stu-id="5ed5a-214">PRINTER\_DRIVER\_SOFT\_RESET\_REQUIRED</span></span><br/> <span data-ttu-id="5ed5a-215">0x00000400</span><span class="sxs-lookup"><span data-stu-id="5ed5a-215">0x00000400</span></span><br/> | <span data-ttu-id="5ed5a-216">Drucker, die diesen Druckertreiber verwenden, sollten den in der Definition der USB-Geräteklasse beschriebenen Richtlinien folgen.</span><span class="sxs-lookup"><span data-stu-id="5ed5a-216">Printers that use this printer driver should follow the guidelines outlined in the USB Device Class Definition.</span></span> <span data-ttu-id="5ed5a-217">Weitere Informationen finden Sie unter [Product Behavior, Section <36>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43)</span><span class="sxs-lookup"><span data-stu-id="5ed5a-217">For more information, see [Product Behavior, section <36>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43)</span></span>                                                                      | <span data-ttu-id="5ed5a-218">Windows 8</span><span class="sxs-lookup"><span data-stu-id="5ed5a-218">Windows 8</span></span><br/> <span data-ttu-id="5ed5a-219">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5ed5a-219">Windows Server 2012</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="5ed5a-220">**pszzcoredriverdependen**</span><span class="sxs-lookup"><span data-stu-id="5ed5a-220">**pszzCoreDriverDependencies**</span></span>
</dt> <dd>

<span data-ttu-id="5ed5a-221">Ein Zeiger auf eine mit NULL endenden Multizeichenfolge, die alle Kern Druckertreiber angibt, von denen der Treiber abhängt.</span><span class="sxs-lookup"><span data-stu-id="5ed5a-221">A pointer to a null-terminated multi-string that specifies all the core printer drivers that the driver depends on.</span></span> <span data-ttu-id="5ed5a-222">Dieser Wert muss **null** sein, wenn die **Treiber \_ Informationen \_ 8** an [**addprinterdriver**](addprinterdriver.md) oder [**addprinterdriverex**](addprinterdriverex.md)übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="5ed5a-222">This must be **NULL** if the **DRIVER\_INFO\_8** is being passed to [**AddPrinterDriver**](addprinterdriver.md) or [**AddPrinterDriverEx**](addprinterdriverex.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ed5a-223">**ftmininboxdriververdate**</span><span class="sxs-lookup"><span data-stu-id="5ed5a-223">**ftMinInboxDriverVerDate**</span></span>
</dt> <dd>

<span data-ttu-id="5ed5a-224">Das früheste zulässige Datum aller Treiber, die mit Windows ausgeliefert wurden und von denen dieser Treiber abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="5ed5a-224">The earliest allowed date of any drivers that shipped with Windows and on which this driver depends.</span></span>

</dd> <dt>

<span data-ttu-id="5ed5a-225">**dwlmininboxdriververversion**</span><span class="sxs-lookup"><span data-stu-id="5ed5a-225">**dwlMinInboxDriverVerVersion**</span></span>
</dt> <dd>

<span data-ttu-id="5ed5a-226">Die früheste zulässige Version aller Treiber, die mit Windows ausgeliefert wurden und von denen dieser Treiber abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="5ed5a-226">The earliest allowed version of any drivers that shipped with Windows and on which this driver depends.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5ed5a-227">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ed5a-227">Remarks</span></span>

<span data-ttu-id="5ed5a-228">Die Zeichen folgen für diese Member sind in der INF-Datei enthalten, die verwendet wird, um den Treiber hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="5ed5a-228">The strings for these members are contained in the .inf file that is used to add the driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ed5a-229">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ed5a-229">Requirements</span></span>



| <span data-ttu-id="5ed5a-230">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ed5a-230">Requirement</span></span> | <span data-ttu-id="5ed5a-231">Wert</span><span class="sxs-lookup"><span data-stu-id="5ed5a-231">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed5a-232">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5ed5a-232">Minimum supported client</span></span><br/> | <span data-ttu-id="5ed5a-233">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ed5a-233">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="5ed5a-234">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5ed5a-234">Minimum supported server</span></span><br/> | <span data-ttu-id="5ed5a-235">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ed5a-235">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5ed5a-236">Header</span><span class="sxs-lookup"><span data-stu-id="5ed5a-236">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ed5a-237"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ed5a-237"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="5ed5a-238">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="5ed5a-238">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5ed5a-239">**\_ Treiber \_ Info \_ 8W** (Unicode) und **\_ Treiber \_ Info \_ 8a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5ed5a-239">**\_DRIVER\_INFO\_8W** (Unicode) and **\_DRIVER\_INFO\_8A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="5ed5a-240">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ed5a-240">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ed5a-241">Drucken</span><span class="sxs-lookup"><span data-stu-id="5ed5a-241">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="5ed5a-242">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="5ed5a-242">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="5ed5a-243">**Addprinterdriver**</span><span class="sxs-lookup"><span data-stu-id="5ed5a-243">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="5ed5a-244">**Addprinterdriverex**</span><span class="sxs-lookup"><span data-stu-id="5ed5a-244">**AddPrinterDriverEx**</span></span>](addprinterdriverex.md)
</dt> </dl>

 

