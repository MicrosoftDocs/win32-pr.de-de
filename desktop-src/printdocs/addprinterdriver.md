---
description: Mit der addprinterdriver-Funktion wird ein lokaler oder Remote Druckertreiber installiert, und die Konfigurations-, Daten-und Treiberdateien werden zugeordnet.
ms.assetid: 0f762800-f5a5-40ea-8be1-7fd8bda23788
title: Addprinterdriver-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterDriver
- AddPrinterDriverA
- AddPrinterDriverW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: de5a9e9d16a47dfe8b9620edc9acdc5c5fd4d552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757860"
---
# <a name="addprinterdriver-function"></a><span data-ttu-id="cf99f-103">Addprinterdriver-Funktion</span><span class="sxs-lookup"><span data-stu-id="cf99f-103">AddPrinterDriver function</span></span>

<span data-ttu-id="cf99f-104">Mit der **addprinterdriver** -Funktion wird ein lokaler oder Remote Druckertreiber installiert, und die Konfigurations-, Daten-und Treiberdateien werden zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="cf99f-104">The **AddPrinterDriver** function installs a local or remote printer driver and associates the configuration, data, and driver files.</span></span>

<span data-ttu-id="cf99f-105">Wenn Sie Druckertreiber installieren oder aktualisieren, können Sie die [**addprinterdriverex**](addprinterdriverex.md) -Funktion verwenden, da Sie strikte Upgrades, strikte Downgrade, das Kopieren von neueren Dateien und das Kopieren aller Dateien (unabhängig von den Dateizeitstempeln) zulässt.</span><span class="sxs-lookup"><span data-stu-id="cf99f-105">For more flexibility in installing or upgrading printer drivers, use the [**AddPrinterDriverEx**](addprinterdriverex.md) function because it allows strict upgrade, strict downgrade, copying of newer files only, and copying of all files (regardless of the file time stamps).</span></span>

> [!Note]  
> <span data-ttu-id="cf99f-106">Das Installieren eines Druckertreibers ohne Treiber Paket wird nicht mehr empfohlen.</span><span class="sxs-lookup"><span data-stu-id="cf99f-106">Installing a printer driver without a driver package is no longer recommended.</span></span> <span data-ttu-id="cf99f-107">Verwenden Sie stattdessen " [**installprinterdriverfrompackage**](installprinterdriverfrompackage.md) ".</span><span class="sxs-lookup"><span data-stu-id="cf99f-107">Use [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) instead.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="cf99f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf99f-108">Syntax</span></span>


```C++
BOOL AddPrinterDriver(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pDriverInfo
);
```



## <a name="parameters"></a><span data-ttu-id="cf99f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf99f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf99f-110">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf99f-110">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf99f-111">Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Servers angibt, auf dem der Treiber installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cf99f-111">A pointer to a null-terminated string that specifies the name of the server on which the driver should be installed.</span></span>

<span data-ttu-id="cf99f-112">Wenn *PName* **null** ist, wird der Treiber lokal installiert.</span><span class="sxs-lookup"><span data-stu-id="cf99f-112">If *pName* is **NULL**, the driver will be installed locally.</span></span>

</dd> <dt>

<span data-ttu-id="cf99f-113">*Ebene* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf99f-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf99f-114">Die Version der-Struktur, auf die *pdriverinfo* verweist.</span><span class="sxs-lookup"><span data-stu-id="cf99f-114">The version of the structure to which *pDriverInfo* points.</span></span>

<span data-ttu-id="cf99f-115">Dieser Wert kann 2, 3, 4, 6 oder 8 sein.</span><span class="sxs-lookup"><span data-stu-id="cf99f-115">This value can be 2, 3, 4, 6, or 8.</span></span>

</dd> <dt>

<span data-ttu-id="cf99f-116">*pdriverinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf99f-116">*pDriverInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf99f-117">Ein Zeiger auf eine-Struktur, die Druckertreiber Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="cf99f-117">A pointer to a structure containing printer driver information.</span></span> <span data-ttu-id="cf99f-118">Dies hängt vom Wert der- *Ebene* ab.</span><span class="sxs-lookup"><span data-stu-id="cf99f-118">This depends on the value of *Level*.</span></span>



| <span data-ttu-id="cf99f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="cf99f-119">Value</span></span> | <span data-ttu-id="cf99f-120">Drucker Laufwerks Struktur</span><span class="sxs-lookup"><span data-stu-id="cf99f-120">Printer Drive Structure</span></span>                  |
|-------|------------------------------------------|
| <span data-ttu-id="cf99f-121">2</span><span class="sxs-lookup"><span data-stu-id="cf99f-121">2</span></span>     | [<span data-ttu-id="cf99f-122">**Treiber \_ Informationen \_ 2**</span><span class="sxs-lookup"><span data-stu-id="cf99f-122">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md) |
| <span data-ttu-id="cf99f-123">3</span><span class="sxs-lookup"><span data-stu-id="cf99f-123">3</span></span>     | [<span data-ttu-id="cf99f-124">**Treiber \_ Info \_ 3**</span><span class="sxs-lookup"><span data-stu-id="cf99f-124">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md) |
| <span data-ttu-id="cf99f-125">4</span><span class="sxs-lookup"><span data-stu-id="cf99f-125">4</span></span>     | [<span data-ttu-id="cf99f-126">**Treiber \_ Info \_ 4**</span><span class="sxs-lookup"><span data-stu-id="cf99f-126">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md) |
| <span data-ttu-id="cf99f-127">6</span><span class="sxs-lookup"><span data-stu-id="cf99f-127">6</span></span>     | [<span data-ttu-id="cf99f-128">**Treiber \_ Info \_ 6**</span><span class="sxs-lookup"><span data-stu-id="cf99f-128">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md) |
| <span data-ttu-id="cf99f-129">8</span><span class="sxs-lookup"><span data-stu-id="cf99f-129">8</span></span>     | [<span data-ttu-id="cf99f-130">**Treiber \_ Informationen \_ 8**</span><span class="sxs-lookup"><span data-stu-id="cf99f-130">**DRIVER\_INFO\_8**</span></span>](driver-info-8.md) |



 

<span data-ttu-id="cf99f-131">Wenn der " **pvironment** "-Member der Struktur, auf die von *pdriverinfo* verwiesen wird, **null** ist, wird die aktuelle Umgebung des Aufrufers bzw. des Clients (nicht des Ziels/Servers) verwendet.</span><span class="sxs-lookup"><span data-stu-id="cf99f-131">If the **pEnvironment** member of the structure pointed to by *pDriverInfo* is **NULL**, the current environment of the caller/client (not of the destination/server) is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf99f-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf99f-132">Return value</span></span>

<span data-ttu-id="cf99f-133">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="cf99f-133">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="cf99f-134">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="cf99f-134">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf99f-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf99f-135">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cf99f-136">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cf99f-136">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="cf99f-137">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="cf99f-137">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="cf99f-138">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="cf99f-138">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="cf99f-139">Der [Aufrufer muss über die SeLoadDriverPrivilege-Berechtigung](/windows/desktop/SecAuthZ/authorization-constants)verfügen.</span><span class="sxs-lookup"><span data-stu-id="cf99f-139">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="cf99f-140">Bevor eine Anwendung die **addprinterdriver** -Funktion aufruft, müssen alle Dateien, die für den Treiber erforderlich sind, in das Druckertreiber Verzeichnis des Systems kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="cf99f-140">Before an application calls the **AddPrinterDriver** function, all files required by the driver must be copied to the system's printer-driver directory.</span></span> <span data-ttu-id="cf99f-141">Eine Anwendung kann den Namen dieses Verzeichnisses abrufen, indem Sie die [**getprinterdriverdirectory**](getprinterdriverdirectory.md) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="cf99f-141">An application can retrieve the name of this directory by calling the [**GetPrinterDriverDirectory**](getprinterdriverdirectory.md) function.</span></span>

<span data-ttu-id="cf99f-142">Eine Anwendung kann ermitteln, welche Druckertreiber zurzeit durch Aufrufen der Funktion " [**enumprinterdrivers**](enumprinterdrivers.md) " installiert werden.</span><span class="sxs-lookup"><span data-stu-id="cf99f-142">An application can determine which printer drivers are currently installed by calling the [**EnumPrinterDrivers**](enumprinterdrivers.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf99f-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf99f-143">Requirements</span></span>



| <span data-ttu-id="cf99f-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf99f-144">Requirement</span></span> | <span data-ttu-id="cf99f-145">Wert</span><span class="sxs-lookup"><span data-stu-id="cf99f-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf99f-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cf99f-146">Minimum supported client</span></span><br/> | <span data-ttu-id="cf99f-147">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf99f-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cf99f-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cf99f-148">Minimum supported server</span></span><br/> | <span data-ttu-id="cf99f-149">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf99f-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cf99f-150">Header</span><span class="sxs-lookup"><span data-stu-id="cf99f-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf99f-151"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cf99f-151"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="cf99f-152">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cf99f-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="cf99f-153"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf99f-153"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="cf99f-154">DLL</span><span class="sxs-lookup"><span data-stu-id="cf99f-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf99f-155"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="cf99f-155"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="cf99f-156">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="cf99f-156">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="cf99f-157">**Addprinterdriverw** (Unicode) und **addprinterdrivera** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="cf99f-157">**AddPrinterDriverW** (Unicode) and **AddPrinterDriverA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="cf99f-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf99f-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf99f-159">Drucken</span><span class="sxs-lookup"><span data-stu-id="cf99f-159">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="cf99f-160">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="cf99f-160">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="cf99f-161">**Addprinterdriverex**</span><span class="sxs-lookup"><span data-stu-id="cf99f-161">**AddPrinterDriverEx**</span></span>](addprinterdriverex.md)
</dt> <dt>

[<span data-ttu-id="cf99f-162">**Treiber \_ Informationen \_ 2**</span><span class="sxs-lookup"><span data-stu-id="cf99f-162">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)
</dt> <dt>

[<span data-ttu-id="cf99f-163">**Treiber \_ Info \_ 3**</span><span class="sxs-lookup"><span data-stu-id="cf99f-163">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)
</dt> <dt>

[<span data-ttu-id="cf99f-164">**Treiber \_ Info \_ 4**</span><span class="sxs-lookup"><span data-stu-id="cf99f-164">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)
</dt> <dt>

[<span data-ttu-id="cf99f-165">**Treiber \_ Info \_ 6**</span><span class="sxs-lookup"><span data-stu-id="cf99f-165">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)
</dt> <dt>

[<span data-ttu-id="cf99f-166">**Enumprinterdrivers**</span><span class="sxs-lookup"><span data-stu-id="cf99f-166">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="cf99f-167">**Getprinterdriverdirectory**</span><span class="sxs-lookup"><span data-stu-id="cf99f-167">**GetPrinterDriverDirectory**</span></span>](getprinterdriverdirectory.md)
</dt> </dl>

 

