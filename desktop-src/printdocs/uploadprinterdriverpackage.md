---
description: Lädt einen Druckertreiber in den Drucker Server-Treiber Speicher hoch, damit er durch Aufrufen von installprinterdriverfrompackage installiert werden kann.
ms.assetid: dd3b3a3b-8ded-44ae-85dd-e630bc62e898
title: Uploadprinterdriverpackage-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UploadPrinterDriverPackage
- UploadPrinterDriverPackageA
- UploadPrinterDriverPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: f616c4f731d3a416806f499a513f48466263f441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217837"
---
# <a name="uploadprinterdriverpackage-function"></a><span data-ttu-id="a2be5-103">Uploadprinterdriverpackage-Funktion</span><span class="sxs-lookup"><span data-stu-id="a2be5-103">UploadPrinterDriverPackage function</span></span>

<span data-ttu-id="a2be5-104">Lädt einen Druckertreiber in den Treiber Speicher des Druck Servers hoch, sodass er durch Aufrufen von [**installprinterdriverfrompackage**](installprinterdriverfrompackage.md)installiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a2be5-104">Uploads a printer driver to the print server's driver store so that it can be installed by calling [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a2be5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2be5-105">Syntax</span></span>


```C++
HRESULT UploadPrinterDriverPackage(
  _In_    LPCTSTR pszServer,
  _In_    LPCTSTR pszInfPath,
  _In_    LPCTSTR pszEnvironment,
  _In_    DWORD   dwFlags,
  _In_    HWND    hwnd,
  _Out_   LPTSTR  pszDestInfPath,
  _Inout_ PULONG  pcchDestInfPath
);
```



## <a name="parameters"></a><span data-ttu-id="a2be5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2be5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2be5-107">*pszserver* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2be5-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2be5-108">Ein Zeiger auf eine Konstante, auf NULL abschließende Zeichenfolge, die den Namen des Drucker Servers angibt.</span><span class="sxs-lookup"><span data-stu-id="a2be5-108">A pointer to a constant, null-terminated string that specifies the name of the print server.</span></span> <span data-ttu-id="a2be5-109">Verwenden Sie **null** , wenn der Server der lokale Computer ist.</span><span class="sxs-lookup"><span data-stu-id="a2be5-109">Use **NULL** if the server is the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="a2be5-110">*pszinfpath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2be5-110">*pszInfPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2be5-111">Ein Zeiger auf eine Konstante, auf NULL abschließende Zeichenfolge, die den Quellpfad zur INF-Datei des Treibers angibt.</span><span class="sxs-lookup"><span data-stu-id="a2be5-111">A pointer to a constant ,null-terminated string that specifies the source path to the driver's .inf file.</span></span>

</dd> <dt>

<span data-ttu-id="a2be5-112">*pszenvironment* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2be5-112">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2be5-113">Ein Zeiger auf eine Konstante, auf NULL abschließende Zeichenfolge, die die Prozessorarchitektur des Servers angibt (z. b. Windows NT x86).</span><span class="sxs-lookup"><span data-stu-id="a2be5-113">A pointer to a constant, null-terminated string that specifies the server's processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="a2be5-114">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="a2be5-114">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a2be5-115">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2be5-115">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2be5-116">Dabei kann es sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="a2be5-116">This can be any of the following values:</span></span>



| <span data-ttu-id="a2be5-117">Wert</span><span class="sxs-lookup"><span data-stu-id="a2be5-117">Value</span></span>                                                                                                                                                                                     | <span data-ttu-id="a2be5-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a2be5-118">Meaning</span></span>                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UPDP_SILENT_UPLOAD"></span><span id="updp_silent_upload"></span><dl> <span data-ttu-id="a2be5-119"><dt>**UPDP_SILENT_UPLOAD**</dt></span><span class="sxs-lookup"><span data-stu-id="a2be5-119"><dt>**UPDP_SILENT_UPLOAD**</dt></span></span> </dl>             | <span data-ttu-id="a2be5-120">Die Benutzeroberfläche wird während des Uploads nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a2be5-120">The UI will not be shown during the upload.</span></span><br/>                                                                                                             |
| <span id="UPDP_UPLOAD_ALWAYS"></span><span id="updp_upload_always"></span><dl> <span data-ttu-id="a2be5-121"><dt>**UPDP_UPLOAD_ALWAYS**</dt></span><span class="sxs-lookup"><span data-stu-id="a2be5-121"><dt>**UPDP_UPLOAD_ALWAYS**</dt></span></span> </dl>             | <span data-ttu-id="a2be5-122">Die Dateien werden auch dann hochgeladen, wenn das Paket bereits im Treiber Speicher des Servers vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a2be5-122">The files will be uploaded even if the package is already in the server's driver store.</span></span><br/>                                                                 |
| <span id="UPDP_CHECK_DRIVERSTORE"></span><span id="updp_check_driverstore"></span><dl> <span data-ttu-id="a2be5-123"><dt>**UPDP_CHECK_DRIVERSTORE**</dt></span><span class="sxs-lookup"><span data-stu-id="a2be5-123"><dt>**UPDP_CHECK_DRIVERSTORE**</dt></span></span> </dl> | <span data-ttu-id="a2be5-124">Der Treiber Speicher des Servers wird vor dem Hochladen geprüft, um festzustellen, ob das Paket bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a2be5-124">The server's driver store will be checked before upload to see if the package is already there.</span></span> <span data-ttu-id="a2be5-125">Diese Einstellung wird ignoriert, wenn UPDP_UPLOAD_ALWAYS festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a2be5-125">This setting is ignored if UPDP_UPLOAD_ALWAYS is set.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a2be5-126">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2be5-126">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2be5-127">Ein Handle für die kopierende Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="a2be5-127">A handle to the copying user interface.</span></span>

</dd> <dt>

<span data-ttu-id="a2be5-128">*pszdestinfpath* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a2be5-128">*pszDestInfPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a2be5-129">Ein Zeiger auf den Zielpfad im Treiber Speicher, in den die INF-Datei des Treibers kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a2be5-129">A pointer to the destination path, in the driver store, to which the driver's .inf file was copied.</span></span>

</dd> <dt>

<span data-ttu-id="a2be5-130">*pcchdestinfpath* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a2be5-130">*pcchDestInfPath* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a2be5-131">Gibt bei der Eingabe die Größe des *pszdestinfpath* -Puffers in Zeichen an.</span><span class="sxs-lookup"><span data-stu-id="a2be5-131">On input, specifies the size, in characters, of the *pszDestInfPath* buffer.</span></span> <span data-ttu-id="a2be5-132">Bei der Ausgabe empfängt die Größe der Pfad Zeichenfolge in Zeichen, einschließlich des abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="a2be5-132">On output, receives the size, in characters, of the path string, including the terminating null character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2be5-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a2be5-133">Return value</span></span>

<span data-ttu-id="a2be5-134">Wenn der Vorgang erfolgreich ist, wird der Rückgabewert S_OK, andernfalls enthält das **HRESULT** einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="a2be5-134">If the operation succeeds, the return value is S_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="a2be5-135">Weitere Informationen zu COM-Fehlercodes finden Sie unter [Fehlerbehandlung](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="a2be5-135">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a2be5-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a2be5-136">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a2be5-137">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a2be5-137">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="a2be5-138">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="a2be5-138">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="a2be5-139">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="a2be5-139">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="a2be5-140">Der Treiber Speicher ist in der Regel entweder% windir% \\ INF oder% windir% \\ system32 \\ DriverStore \\ FileRepository.</span><span class="sxs-lookup"><span data-stu-id="a2be5-140">The driver store is typically either %windir%\\inf or %windir%\\System32\\DriverStore\\FileRepository.</span></span>

<span data-ttu-id="a2be5-141">Es kann immer nur jeweils ein Paket hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="a2be5-141">Only one package at a time can be uploaded.</span></span> <span data-ttu-id="a2be5-142">Wenn ein Paket von anderen abhängig ist, müssen diese separat hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="a2be5-142">If a package is dependent on others, they must be uploaded separately.</span></span>

<span data-ttu-id="a2be5-143">Nur signierte Treiber Pakete können hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="a2be5-143">Only signed driver packages can be uploaded.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2be5-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2be5-144">Requirements</span></span>



| <span data-ttu-id="a2be5-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a2be5-145">Requirement</span></span> | <span data-ttu-id="a2be5-146">Wert</span><span class="sxs-lookup"><span data-stu-id="a2be5-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2be5-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a2be5-147">Minimum supported client</span></span><br/> | <span data-ttu-id="a2be5-148">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2be5-148">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="a2be5-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a2be5-149">Minimum supported server</span></span><br/> | <span data-ttu-id="a2be5-150">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2be5-150">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a2be5-151">Header</span><span class="sxs-lookup"><span data-stu-id="a2be5-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2be5-152"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a2be5-152"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="a2be5-153">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a2be5-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="a2be5-154"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a2be5-154"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="a2be5-155">DLL</span><span class="sxs-lookup"><span data-stu-id="a2be5-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2be5-156"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2be5-156"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="a2be5-157">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="a2be5-157">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a2be5-158">**UploadPrinterDriverPackageW** (Unicode) und **UploadPrinterDriverPackageA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a2be5-158">**UploadPrinterDriverPackageW** (Unicode) and **UploadPrinterDriverPackageA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="a2be5-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2be5-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2be5-160">Drucken</span><span class="sxs-lookup"><span data-stu-id="a2be5-160">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="a2be5-161">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="a2be5-161">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

