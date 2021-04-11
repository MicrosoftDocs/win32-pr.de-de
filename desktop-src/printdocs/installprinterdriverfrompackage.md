---
description: Installiert einen Druckertreiber aus einem Treiber Paket, das sich im Treiber Speicher des Drucker Servers befindet.
ms.assetid: 5906d9c6-9fbf-4ec6-81ce-112a9ef6d7c0
title: Installprinterdriverfrompackage-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallPrinterDriverFromPackage
- InstallPrinterDriverFromPackageA
- InstallPrinterDriverFromPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: f817f5e73537f6a71d8236ad9532acdf02a53552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218220"
---
# <a name="installprinterdriverfrompackage-function"></a><span data-ttu-id="9d606-103">Installprinterdriverfrompackage-Funktion</span><span class="sxs-lookup"><span data-stu-id="9d606-103">InstallPrinterDriverFromPackage function</span></span>

<span data-ttu-id="9d606-104">Installiert einen Druckertreiber aus einem Treiber Paket, das sich im Treiber Speicher des Druck Servers befindet.</span><span class="sxs-lookup"><span data-stu-id="9d606-104">Installs a printer driver from a driver package that is in the print server's driver store.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d606-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d606-105">Syntax</span></span>


```C++
HRESULT InstallPrinterDriverFromPackage(
  _In_ LPCTSTR pszServer,
  _In_ LPCTSTR pszInfPath,
  _In_ LPCTSTR pszDriverName,
  _In_ LPCTSTR pszEnvironment,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="9d606-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d606-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d606-107">*pszserver* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d606-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d606-108">Ein Zeiger auf eine Konstante, auf NULL abschließende Zeichenfolge, die den Namen des Drucker Servers angibt.</span><span class="sxs-lookup"><span data-stu-id="9d606-108">A pointer to a constant, null-terminated string that specifies the name of the print server.</span></span> <span data-ttu-id="9d606-109">**Null** bedeutet, dass der lokale Computer ist.</span><span class="sxs-lookup"><span data-stu-id="9d606-109">**NULL** means the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="9d606-110">*pszinfpath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d606-110">*pszInfPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d606-111">Ein Zeiger auf eine Konstante, auf NULL abschließende Zeichenfolge, die den Treiber Speicherpfad zur INF-Datei des Druckertreibers angibt.</span><span class="sxs-lookup"><span data-stu-id="9d606-111">A pointer to a constant, null-terminated string that specifies the driver store path to the print driver's .inf file.</span></span> <span data-ttu-id="9d606-112">**Null** bedeutet, dass sich der Treiber in einer INF-Datei befindet, die mit Windows ausgeliefert wird.</span><span class="sxs-lookup"><span data-stu-id="9d606-112">**NULL** means the driver is in an inf file that shipped with Windows.</span></span>

</dd> <dt>

<span data-ttu-id="9d606-113">*pszdrivername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d606-113">*pszDriverName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d606-114">Ein Zeiger auf eine Konstante, auf NULL abschließende Zeichenfolge, die den Namen des Treibers angibt.</span><span class="sxs-lookup"><span data-stu-id="9d606-114">A pointer to a constant, null-terminated string that specifies the name of the driver.</span></span>

</dd> <dt>

<span data-ttu-id="9d606-115">*pszenvironment* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d606-115">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d606-116">Ein Zeiger auf eine Konstante, auf NULL abschließende Zeichenfolge, die die Prozessorarchitektur angibt (z. b. Windows NT x86).</span><span class="sxs-lookup"><span data-stu-id="9d606-116">A pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="9d606-117">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="9d606-117">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9d606-118">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d606-118">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d606-119">Dies kann nur 0 sein oder alle Dateien durch ipdfp \_ kopieren \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9d606-119">This can only be 0 or IPDFP\_COPY\_ALL\_FILES.</span></span> <span data-ttu-id="9d606-120">Der Wert 0 bedeutet, dass der Druckertreiber hinzugefügt werden muss und alle Dateien im Druckertreiber Verzeichnis, die neuer als die derzeit verwendeten Dateien sind, kopiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="9d606-120">A value of 0 means that the printer driver must be added and any files in the printer driver directory that are newer than corresponding files currently in use must be copied.</span></span> <span data-ttu-id="9d606-121">Der Wert ipdfp \_ \_ alle Dateien kopieren \_ bedeutet, dass der Druckertreiber und alle Dateien im Druckertreiber Verzeichnis hinzugefügt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="9d606-121">A value of IPDFP\_COPY\_ALL\_FILES means the printer driver and all the files in the printer driver directory must be added.</span></span> <span data-ttu-id="9d606-122">Die Zeitstempel der Datei werden ignoriert, wenn *dwFlags* den Wert ipdfp \_ \_ alle Dateien kopieren hat \_ .</span><span class="sxs-lookup"><span data-stu-id="9d606-122">The file time stamps are ignored when *dwFlags* has a value of IPDFP\_COPY\_ALL\_FILES.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d606-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9d606-123">Return value</span></span>

<span data-ttu-id="9d606-124">Wenn der Vorgang erfolgreich ist, ist der Rückgabewert S \_ OK; andernfalls enthält das **HRESULT** einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="9d606-124">If the operation succeeds, the return value is S\_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="9d606-125">Weitere Informationen zu COM-Fehlercodes finden Sie unter [Fehlerbehandlung](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="9d606-125">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9d606-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d606-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9d606-127">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9d606-127">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="9d606-128">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="9d606-128">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="9d606-129">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="9d606-129">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="9d606-130">Der Treiber Speicher ist in der Regel entweder% windir% \\ INF oder% windir% \\ system32 \\ DriverStore \\ FileRepository.</span><span class="sxs-lookup"><span data-stu-id="9d606-130">The driver store is typically either %windir%\\inf or %windir%\\System32\\DriverStore\\FileRepository.</span></span>

<span data-ttu-id="9d606-131">**Installprinterdriverfrompackage** installiert auch andere Dateien im Paket, z. b. Farbprofile und Druck Prozessoren.</span><span class="sxs-lookup"><span data-stu-id="9d606-131">**InstallPrinterDriverFromPackage** also installs other files in the package, such as color profiles and print processors.</span></span>

<span data-ttu-id="9d606-132">Benutzer müssen über Drucker Administratorrechte verfügen, um entweder auf einem Remote Computer oder auf dem lokalen Computer zu installieren, wenn der Benutzer mit Terminal Diensten angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="9d606-132">Users must have printer administration rights to install either on a remote computer or on the local computer when the user is logged in with Terminal Services.</span></span>

<span data-ttu-id="9d606-133">Nur signierte Pakete können auf einem Remote Computer installiert werden.</span><span class="sxs-lookup"><span data-stu-id="9d606-133">Only signed packages can be installed on a remote computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d606-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d606-134">Requirements</span></span>



| <span data-ttu-id="9d606-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d606-135">Requirement</span></span> | <span data-ttu-id="9d606-136">Wert</span><span class="sxs-lookup"><span data-stu-id="9d606-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d606-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9d606-137">Minimum supported client</span></span><br/> | <span data-ttu-id="9d606-138">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d606-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="9d606-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9d606-139">Minimum supported server</span></span><br/> | <span data-ttu-id="9d606-140">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d606-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9d606-141">Header</span><span class="sxs-lookup"><span data-stu-id="9d606-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d606-142"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9d606-142"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="9d606-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9d606-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="9d606-144"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9d606-144"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="9d606-145">DLL</span><span class="sxs-lookup"><span data-stu-id="9d606-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d606-146"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d606-146"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="9d606-147">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="9d606-147">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9d606-148">**Installprinterdriverfrompackagew** (Unicode) und **installprinterdriverfrompackagea** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9d606-148">**InstallPrinterDriverFromPackageW** (Unicode) and **InstallPrinterDriverFromPackageA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9d606-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d606-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d606-150">Drucken</span><span class="sxs-lookup"><span data-stu-id="9d606-150">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="9d606-151">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="9d606-151">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

