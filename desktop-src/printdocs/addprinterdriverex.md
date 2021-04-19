---
description: Die Funktion addprinterdriverex installiert einen lokalen oder Remote Druckertreiber und verknüpft die Konfigurations-, Daten-und Treiberdateien.
ms.assetid: 472adb7d-39cc-4c76-b96c-610ff9d276ad
title: Addprinterdriverex-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterDriverEx
- AddPrinterDriverExA
- AddPrinterDriverExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: c431d710ddad7f723d063fd5bf046bae08b77b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359016"
---
# <a name="addprinterdriverex-function"></a><span data-ttu-id="ae94d-103">Addprinterdriverex-Funktion</span><span class="sxs-lookup"><span data-stu-id="ae94d-103">AddPrinterDriverEx function</span></span>

<span data-ttu-id="ae94d-104">Die Funktion **addprinterdriverex** installiert einen lokalen oder Remote Druckertreiber und verknüpft die Konfigurations-, Daten-und Treiberdateien.</span><span class="sxs-lookup"><span data-stu-id="ae94d-104">The **AddPrinterDriverEx** function installs a local or remote printer driver and links the configuration, data, and driver files.</span></span> <span data-ttu-id="ae94d-105">Neben den Funktionen von [**addprinterdriver**](addprinterdriver.md)bietet es auch Optionen, die das strikte Upgrade, das strikte Downgrade, das Kopieren von neueren Dateien und das Kopieren aller Dateien (unabhängig von Dateizeitstempeln) ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="ae94d-105">Besides having the capabilities of [**AddPrinterDriver**](addprinterdriver.md), it also has options that permit strict upgrade, strict downgrade, copying of newer files only, and copying of all files (regardless of file time stamps).</span></span>

> [!Note]  
> <span data-ttu-id="ae94d-106">Das Installieren eines Druckertreibers ohne Treiber Paket wird nicht mehr empfohlen.</span><span class="sxs-lookup"><span data-stu-id="ae94d-106">Installing a printer driver without a driver package is no longer recommended.</span></span> <span data-ttu-id="ae94d-107">Verwenden Sie stattdessen " [**installprinterdriverfrompackage**](installprinterdriverfrompackage.md) ".</span><span class="sxs-lookup"><span data-stu-id="ae94d-107">Use [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) instead.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ae94d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae94d-108">Syntax</span></span>


```C++
BOOL AddPrinterDriverEx(
  _In_    LPTSTR pName,
  _In_    DWORD  Level,
  _Inout_ LPBYTE pDriverInfo,
  _In_    DWORD  dwFileCopyFlags
);
```



## <a name="parameters"></a><span data-ttu-id="ae94d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae94d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae94d-110">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae94d-110">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae94d-111">Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Servers angibt, auf dem der Treiber installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ae94d-111">A pointer to a null-terminated string that specifies the name of the server on which the driver should be installed.</span></span> <span data-ttu-id="ae94d-112">Wenn dieser Parameter **null** ist, wird der Treiber von der Funktion auf dem lokalen Computer installiert.</span><span class="sxs-lookup"><span data-stu-id="ae94d-112">If this parameter is **NULL**, the function installs the driver on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="ae94d-113">*Ebene* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae94d-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae94d-114">Die Version der-Struktur, auf die *pdriverinfo* verweist.</span><span class="sxs-lookup"><span data-stu-id="ae94d-114">The version of the structure to which *pDriverInfo* points.</span></span> <span data-ttu-id="ae94d-115">Dieser Wert kann 2, 3, 4, 6 oder 8 sein.</span><span class="sxs-lookup"><span data-stu-id="ae94d-115">This value can be 2, 3, 4, 6, or 8.</span></span>

</dd> <dt>

<span data-ttu-id="ae94d-116">*pdriverinfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ae94d-116">*pDriverInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae94d-117">Ein Zeiger auf eine-Struktur, die Druckertreiber Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="ae94d-117">A pointer to a structure containing printer driver information.</span></span> <span data-ttu-id="ae94d-118">Dies kann einer der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="ae94d-118">It can be one of the following.</span></span>



| <span data-ttu-id="ae94d-119">Wert der Ebene</span><span class="sxs-lookup"><span data-stu-id="ae94d-119">Value of Level</span></span>                                                                                       | <span data-ttu-id="ae94d-120">Treiber \_ Informations \_ \* Struktur</span><span class="sxs-lookup"><span data-stu-id="ae94d-120">DRIVER\_INFO\_\* Structure</span></span>                          |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="2"></span><dl> <span data-ttu-id="ae94d-121"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="ae94d-121"><dt>**2**</dt></span></span> </dl> | [<span data-ttu-id="ae94d-122">**Treiber \_ Informationen \_ 2**</span><span class="sxs-lookup"><span data-stu-id="ae94d-122">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <span data-ttu-id="ae94d-123"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="ae94d-123"><dt>**3**</dt></span></span> </dl> | [<span data-ttu-id="ae94d-124">**Treiber \_ Info \_ 3**</span><span class="sxs-lookup"><span data-stu-id="ae94d-124">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <span data-ttu-id="ae94d-125"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="ae94d-125"><dt>**4**</dt></span></span> </dl> | [<span data-ttu-id="ae94d-126">**Treiber \_ Info \_ 4**</span><span class="sxs-lookup"><span data-stu-id="ae94d-126">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)<br/> |
| <span id="6"></span><dl> <span data-ttu-id="ae94d-127"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="ae94d-127"><dt>**6**</dt></span></span> </dl> | [<span data-ttu-id="ae94d-128">**Treiber \_ Info \_ 6**</span><span class="sxs-lookup"><span data-stu-id="ae94d-128">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <span data-ttu-id="ae94d-129"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="ae94d-129"><dt>**8**</dt></span></span> </dl> | [<span data-ttu-id="ae94d-130">**Treiber \_ Informationen \_ 8**</span><span class="sxs-lookup"><span data-stu-id="ae94d-130">**DRIVER\_INFO\_8**</span></span>](driver-info-8.md)<br/> |



 

<span data-ttu-id="ae94d-131">Wenn der " **pvironment** "-Member der Struktur, auf die von *pdriverinfo* verwiesen wird, **null** ist, verwendet die Funktion die aktuelle Umgebung des Aufrufers bzw. des Clients, nicht die Umgebung des Ziels bzw. des Servers.</span><span class="sxs-lookup"><span data-stu-id="ae94d-131">If the **pEnvironment** member of the structure pointed to by *pDriverInfo* is **NULL**, the function uses the current environment of the caller/client, not the environment of the destination/server.</span></span>

</dd> <dt>

<span data-ttu-id="ae94d-132">*dwfilecopyflags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae94d-132">*dwFileCopyFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae94d-133">Die Optionen zum Kopieren der Treiberdateien.</span><span class="sxs-lookup"><span data-stu-id="ae94d-133">The options for copying the driver files.</span></span> <span data-ttu-id="ae94d-134">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="ae94d-134">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="ae94d-135">Wert</span><span class="sxs-lookup"><span data-stu-id="ae94d-135">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="ae94d-136">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ae94d-136">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APD_COPY_ALL_FILES"></span><span id="apd_copy_all_files"></span><dl> <span data-ttu-id="ae94d-137"><dt>**APD \_ \_ alle \_ Dateien kopieren**</dt></span><span class="sxs-lookup"><span data-stu-id="ae94d-137"><dt>**APD\_COPY\_ALL\_FILES**</dt></span></span> </dl>                | <span data-ttu-id="ae94d-138">Fügen Sie den Druckertreiber hinzu, und kopieren Sie alle Dateien im Druckertreiber Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="ae94d-138">Add the printer driver and copy all the files in the printer-driver directory.</span></span> <span data-ttu-id="ae94d-139">Die Zeitstempel der Datei werden bei dieser Option ignoriert.</span><span class="sxs-lookup"><span data-stu-id="ae94d-139">The file time stamps are ignored with this option.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="APD_COPY_FROM_DIRECTORY"></span><span id="apd_copy_from_directory"></span><dl> <span data-ttu-id="ae94d-140"><dt>**APD- \_ Kopie \_ aus \_ Verzeichnis**</dt></span><span class="sxs-lookup"><span data-stu-id="ae94d-140"><dt>**APD\_COPY\_FROM\_DIRECTORY**</dt></span></span> </dl> | <span data-ttu-id="ae94d-141">Fügen Sie den Druckertreiber mit den voll qualifizierten Dateinamen hinzu, die in der [**Treiber \_ Info \_ 6**](driver-info-6.md) -Struktur angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="ae94d-141">Add the printer driver using the fully qualified file names specified in the [**DRIVER\_INFO\_6**](driver-info-6.md) structure.</span></span> <span data-ttu-id="ae94d-142">Dieses Flag wird in Verbindung mit einem der anderen kopierflags angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ae94d-142">This flag is ORed in conjunction with one of the other copy flags.</span></span> <span data-ttu-id="ae94d-143">Wenn dieses Flag festgelegt ist, schlägt **addprinterdriverex** fehl, wenn die Dateien nicht vorhanden sind, wenn Sie in der **\_ Information \_ 6** -Struktur des Treibers vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="ae94d-143">If this flag is set, **AddPrinterDriverEx** will fail if the files do not exist where they are specified to exist by the **DRIVER\_INFO\_6** structure.</span></span> <span data-ttu-id="ae94d-144">Die Dateien müssen nicht in das Druckertreiber Verzeichnis des Systems kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="ae94d-144">The files do not need to be copied to the system's printer-driver directory.</span></span> <span data-ttu-id="ae94d-145">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="ae94d-145">See the Remarks.</span></span><br/> <span data-ttu-id="ae94d-146">**Windows 2000:** Dieses Flag wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ae94d-146">**Windows 2000:** This flag is not supported.</span></span><br/> |
| <span id="APD_COPY_NEW_FILES"></span><span id="apd_copy_new_files"></span><dl> <span data-ttu-id="ae94d-147"><dt>**APD \_ \_ neue \_ Dateien kopieren**</dt></span><span class="sxs-lookup"><span data-stu-id="ae94d-147"><dt>**APD\_COPY\_NEW\_FILES**</dt></span></span> </dl>                | <span data-ttu-id="ae94d-148">Fügen Sie den Druckertreiber hinzu, und kopieren Sie die Dateien in das Druckertreiber Verzeichnis, das neuer ist als alle entsprechenden Dateien, die zurzeit verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ae94d-148">Add the printer driver and copy the files in the printer-driver directory that are newer than any corresponding files that are currently in use.</span></span> <span data-ttu-id="ae94d-149">Dieses Flag emuliert das Verhalten von [**addprinterdriver**](addprinterdriver.md).</span><span class="sxs-lookup"><span data-stu-id="ae94d-149">This flag emulates the behavior of [**AddPrinterDriver**](addprinterdriver.md).</span></span><br/>                                                                                                                                                                                                                                                                                  |
| <span id="APD_STRICT_DOWNGRADE"></span><span id="apd_strict_downgrade"></span><dl> <span data-ttu-id="ae94d-150"><dt>**APD \_ Strict \_ Downgrade**</dt></span><span class="sxs-lookup"><span data-stu-id="ae94d-150"><dt>**APD\_STRICT\_DOWNGRADE**</dt></span></span> </dl>           | <span data-ttu-id="ae94d-151">Fügen Sie den Druckertreiber nur hinzu, wenn alle Dateien im Druckertreiber Verzeichnis älter sind als alle derzeit verwendeten Dateien.</span><span class="sxs-lookup"><span data-stu-id="ae94d-151">Add the printer driver only if all the files in the printer-driver directory are older than any corresponding files currently in use.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="APD_STRICT_UPGRADE"></span><span id="apd_strict_upgrade"></span><dl> <span data-ttu-id="ae94d-152"><dt>**APD \_ Strict- \_ Upgrade**</dt></span><span class="sxs-lookup"><span data-stu-id="ae94d-152"><dt>**APD\_STRICT\_UPGRADE**</dt></span></span> </dl>                 | <span data-ttu-id="ae94d-153">Fügen Sie den Druckertreiber nur hinzu, wenn alle Dateien im Druckertreiber Verzeichnis neuer als alle entsprechenden Dateien sind, die zurzeit verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ae94d-153">Add the printer driver only if all the files in the printer-driver directory are newer than any corresponding files currently in use.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae94d-154">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ae94d-154">Return value</span></span>

<span data-ttu-id="ae94d-155">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="ae94d-155">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="ae94d-156">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="ae94d-156">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="ae94d-157">Wenn der Druckertreiber Probleme beim Arbeiten mit dem Betriebssystem hat, schlägt **addprinterdriverex** mit einem der folgenden Fehlercodes fehl:</span><span class="sxs-lookup"><span data-stu-id="ae94d-157">If the printer driver is known to have problems working with the operating system, **AddPrinterDriverEx** will fail with one of the following error codes:</span></span>



| <span data-ttu-id="ae94d-158">Fehlercode</span><span class="sxs-lookup"><span data-stu-id="ae94d-158">Error Code</span></span>                      | <span data-ttu-id="ae94d-159">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ae94d-159">Meaning</span></span>                                                                                                                                                   |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae94d-160">Fehler \_ Drucker \_ Treiber \_ blockiert</span><span class="sxs-lookup"><span data-stu-id="ae94d-160">ERROR\_PRINTER\_DRIVER\_BLOCKED</span></span> | <span data-ttu-id="ae94d-161">Der Treiber funktioniert nicht auf dem Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="ae94d-161">The driver does not work on the operating system.</span></span>                                                                                                         |
| <span data-ttu-id="ae94d-162">Fehler \_ Drucker \_ Treiber \_ gewarnt</span><span class="sxs-lookup"><span data-stu-id="ae94d-162">ERROR\_PRINTER\_DRIVER\_WARNED</span></span>  | <span data-ttu-id="ae94d-163">Der Treiber ist auf dem Betriebssystem unzuverlässig.</span><span class="sxs-lookup"><span data-stu-id="ae94d-163">The driver is unreliable on the operating system.</span></span> <span data-ttu-id="ae94d-164">Wenn jedoch \_ \_ der angemahnte Treiber für die APD-Installation \_ angegeben ist, wird der Treiber installiert, und es wird keine Warnung ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="ae94d-164">However, if APD\_INSTALL\_WARNED\_DRIVER is specified, the driver is installed and no warning is given.</span></span> |



 

<span data-ttu-id="ae94d-165">Weitere Informationen finden Sie in den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="ae94d-165">For more information, see the Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae94d-166">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ae94d-166">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ae94d-167">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ae94d-167">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="ae94d-168">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="ae94d-168">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="ae94d-169">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="ae94d-169">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="ae94d-170">Der [Aufrufer muss über die SeLoadDriverPrivilege-Berechtigung](/windows/desktop/SecAuthZ/authorization-constants)verfügen.</span><span class="sxs-lookup"><span data-stu-id="ae94d-170">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="ae94d-171">Vor dem Aufrufen der **addprinterdriverex** -Funktion müssen alle Dateien, die für den Treiber erforderlich sind, in das Druckertreiber Verzeichnis des Systems kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="ae94d-171">Before calling the **AddPrinterDriverEx** function, all files required by the driver must be copied to the system's printer-driver directory.</span></span> <span data-ttu-id="ae94d-172">Um den Namen dieses Verzeichnisses abzurufen, rufen Sie die [**getprinterdriverdirectory**](getprinterdriverdirectory.md) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="ae94d-172">To retrieve the name of this directory, call the [**GetPrinterDriverDirectory**](getprinterdriverdirectory.md) function.</span></span>

<span data-ttu-id="ae94d-173">Um zu ermitteln, welche Druckertreiber derzeit installiert sind, müssen Sie die Funktion " [**enumprinterdrivers**](enumprinterdrivers.md) " aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="ae94d-173">To determine which printer drivers are currently installed, call the [**EnumPrinterDrivers**](enumprinterdrivers.md) function.</span></span>

<span data-ttu-id="ae94d-174">Wenn der Druckertreiber erfolgreich hinzugefügt wurde, ruft die Funktion die drvdriverevent (Treiber \_ Ereignis \_ Initialize, Level, Driver \_ Info \_ \* , LPARAM)-Funktion auf, damit der Treiber alle während der Installation eines Druckertreibers erforderlichen Initialisierungen ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="ae94d-174">If the printer driver has been successfully added, the function calls the DrvDriverEvent (DRIVER\_EVENT\_INITIALIZE, Level, DRIVER\_INFO\_\*, lparam ) function to allow the driver to perform any initializations required during the installation of a printer driver.</span></span> <span data-ttu-id="ae94d-175">Weitere Informationen zu **drvdriverevent** finden Sie im Microsoft Windows Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="ae94d-175">For more information about **DrvDriverEvent**, see the Microsoft Windows Driver Development Kit (DDK)</span></span>

<span data-ttu-id="ae94d-176">Der Treiber sollte während des Aufrufes **drvdriverevent** keinen UI-Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="ae94d-176">The driver should not use a UI call during the call to **DrvDriverEvent**.</span></span> <span data-ttu-id="ae94d-177">Zum Ausführen von UI-bezogenen Aufträgen sollte das Installationsprogramm entweder den vendorsetup-Eintrag in der INF-Datei des Druckers verwenden, oder für Plug & Play Geräte kann das Installationsprogramm einen gerätespezifischen Co-Installer verwenden.</span><span class="sxs-lookup"><span data-stu-id="ae94d-177">To do UI-related jobs, the installer should either use the VendorSetup entry in the printer's .inf file or, for Plug and Play devices, the installer can use a device-specific co-installer.</span></span> <span data-ttu-id="ae94d-178">Weitere Informationen zu vendorsetup finden Sie unter DDK.</span><span class="sxs-lookup"><span data-stu-id="ae94d-178">For more information about VendorSetup, see the DDK.</span></span>

<span data-ttu-id="ae94d-179">Die Dateien, auf die in der [**Driver \_ Info \_ 6**](driver-info-6.md) -Struktur verwiesen wird, müssen sich lokal auf dem Computer befinden, von dem aus der-Befehl aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ae94d-179">The files that are referenced in the [**DRIVER\_INFO\_6**](driver-info-6.md) structure must be local to the machine from which the call is made.</span></span> <span data-ttu-id="ae94d-180">Ein Dateiname kann ein UNC-Name sein, solange der UNC-Name der lokale Computer ist.</span><span class="sxs-lookup"><span data-stu-id="ae94d-180">A file name can be a UNC name as long as the UNC name is the local machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae94d-181">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae94d-181">Requirements</span></span>



| <span data-ttu-id="ae94d-182">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ae94d-182">Requirement</span></span> | <span data-ttu-id="ae94d-183">Wert</span><span class="sxs-lookup"><span data-stu-id="ae94d-183">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae94d-184">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ae94d-184">Minimum supported client</span></span><br/> | <span data-ttu-id="ae94d-185">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ae94d-185">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ae94d-186">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ae94d-186">Minimum supported server</span></span><br/> | <span data-ttu-id="ae94d-187">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ae94d-187">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ae94d-188">Header</span><span class="sxs-lookup"><span data-stu-id="ae94d-188">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae94d-189"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ae94d-189"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ae94d-190">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ae94d-190">Library</span></span><br/>                  | <dl> <span data-ttu-id="ae94d-191"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae94d-191"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="ae94d-192">DLL</span><span class="sxs-lookup"><span data-stu-id="ae94d-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae94d-193"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="ae94d-193"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="ae94d-194">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="ae94d-194">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ae94d-195">**Addprinterdriverexw** (Unicode) und **addprinterdriverexa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ae94d-195">**AddPrinterDriverExW** (Unicode) and **AddPrinterDriverExA** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="ae94d-196">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae94d-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae94d-197">Drucken</span><span class="sxs-lookup"><span data-stu-id="ae94d-197">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ae94d-198">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="ae94d-198">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="ae94d-199">**Addprinterdriver**</span><span class="sxs-lookup"><span data-stu-id="ae94d-199">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="ae94d-200">**Treiber \_ Informationen \_ 2**</span><span class="sxs-lookup"><span data-stu-id="ae94d-200">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)
</dt> <dt>

[<span data-ttu-id="ae94d-201">**Treiber \_ Info \_ 3**</span><span class="sxs-lookup"><span data-stu-id="ae94d-201">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)
</dt> <dt>

[<span data-ttu-id="ae94d-202">**Treiber \_ Info \_ 4**</span><span class="sxs-lookup"><span data-stu-id="ae94d-202">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)
</dt> <dt>

[<span data-ttu-id="ae94d-203">**Treiber \_ Info \_ 6**</span><span class="sxs-lookup"><span data-stu-id="ae94d-203">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)
</dt> <dt>

[<span data-ttu-id="ae94d-204">**Deleteprinterdriverex**</span><span class="sxs-lookup"><span data-stu-id="ae94d-204">**DeletePrinterDriverEx**</span></span>](deleteprinterdriverex.md)
</dt> <dt>

[<span data-ttu-id="ae94d-205">**Enumprinterdrivers**</span><span class="sxs-lookup"><span data-stu-id="ae94d-205">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="ae94d-206">**Getprinterdriverdirectory**</span><span class="sxs-lookup"><span data-stu-id="ae94d-206">**GetPrinterDriverDirectory**</span></span>](getprinterdriverdirectory.md)
</dt> </dl>

 

