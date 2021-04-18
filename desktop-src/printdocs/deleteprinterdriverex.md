---
description: Mit der deleteprinterdriverex-Funktion wird der angegebene Druckertreiber Name aus der Liste mit den Namen unterstützter Treiber auf einem Server entfernt, und die dem Treiber zugeordneten Dateien werden gelöscht. Mit dieser Funktion können auch bestimmte Versionen des Treibers gelöscht werden.
ms.assetid: 1a3d7c7f-1d45-4877-a8f7-a77f40e3c319
title: Deleteprinterdriverex-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriverEx
- DeletePrinterDriverExA
- DeletePrinterDriverExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: b88ef38236961286875a1885dad9dde936887d13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347403"
---
# <a name="deleteprinterdriverex-function"></a><span data-ttu-id="a9440-104">Deleteprinterdriverex-Funktion</span><span class="sxs-lookup"><span data-stu-id="a9440-104">DeletePrinterDriverEx function</span></span>

<span data-ttu-id="a9440-105">Mit der **deleteprinterdriverex** -Funktion wird der angegebene Druckertreiber Name aus der Liste mit den Namen unterstützter Treiber auf einem Server entfernt, und die dem Treiber zugeordneten Dateien werden gelöscht.</span><span class="sxs-lookup"><span data-stu-id="a9440-105">The **DeletePrinterDriverEx** function removes the specified printer-driver name from the list of names of supported drivers on a server and deletes the files associated with the driver.</span></span> <span data-ttu-id="a9440-106">Mit dieser Funktion können auch bestimmte Versionen des Treibers gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="a9440-106">This function can also delete specific versions of the driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9440-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9440-107">Syntax</span></span>


```C++
BOOL DeletePrinterDriverEx(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pDriverName,
  _In_ DWORD  dwDeleteFlag,
  _In_ DWORD  dwVersionFlag
);
```



## <a name="parameters"></a><span data-ttu-id="a9440-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9440-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9440-109">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a9440-109">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9440-110">Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Servers angibt, von dem der Treiber gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="a9440-110">A pointer to a null-terminated string that specifies the name of the server from which the driver is to be deleted.</span></span> <span data-ttu-id="a9440-111">Wenn dieser Parameter **null** ist, löscht die Funktion den Druckertreiber auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="a9440-111">If this parameter is **NULL**, the function deletes the printer-driver from the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="a9440-112">nach-oben  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a9440-112">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9440-113">Ein Zeiger auf eine auf NULL endende Zeichenfolge, die die Umgebung angibt, aus der der Treiber gelöscht werden soll (z. b. Windows NT x86, Windows ia64 oder Windows x64).</span><span class="sxs-lookup"><span data-stu-id="a9440-113">A pointer to a null-terminated string that specifies the environment from which the driver is to be deleted (for example, Windows NT x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="a9440-114">Wenn dieser Parameter **null** ist, wird der Treiber Name aus der aktuellen Umgebung der aufrufenden Anwendung und des Client Computers (nicht der Zielanwendung und des Druck Servers) gelöscht.</span><span class="sxs-lookup"><span data-stu-id="a9440-114">If this parameter is **NULL**, the driver name is deleted from the current environment of the calling application and client computer (not of the destination application and print server).</span></span>

</dd> <dt>

<span data-ttu-id="a9440-115">*pdrivername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a9440-115">*pDriverName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9440-116">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des zu löschenden Treibers angibt.</span><span class="sxs-lookup"><span data-stu-id="a9440-116">A pointer to a null-terminated string specifying the name of the driver to delete.</span></span>

</dd> <dt>

<span data-ttu-id="a9440-117">*dwdeleteflag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a9440-117">*dwDeleteFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9440-118">Die Optionen zum Löschen von Dateien und Versionen des Treibers.</span><span class="sxs-lookup"><span data-stu-id="a9440-118">The options for deleting files and versions of the driver.</span></span> <span data-ttu-id="a9440-119">Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a9440-119">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="a9440-120">Wert</span><span class="sxs-lookup"><span data-stu-id="a9440-120">Value</span></span>                                                                                                                                                                                                     | <span data-ttu-id="a9440-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a9440-121">Meaning</span></span>                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DPD_DELETE_SPECIFIC_VERSION"></span><span id="dpd_delete_specific_version"></span><dl> <span data-ttu-id="a9440-122"><dt>**DPD \_ - \_ bestimmte \_ Version löschen**</dt></span><span class="sxs-lookup"><span data-stu-id="a9440-122"><dt>**DPD\_DELETE\_SPECIFIC\_VERSION**</dt></span></span> </dl> | <span data-ttu-id="a9440-123">Löscht die in *dwversionflag* angegebene Version.</span><span class="sxs-lookup"><span data-stu-id="a9440-123">Deletes the version specified in *dwVersionFlag*.</span></span> <span data-ttu-id="a9440-124">Dadurch wird nicht sichergestellt, dass der Treiber aus der Liste der unterstützten Treiber für den Server entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="a9440-124">This does not ensure that the driver will be removed from the list of supported drivers for the server.</span></span><br/>                  |
| <span id="DPD_DELETE_UNUSED_FILES"></span><span id="dpd_delete_unused_files"></span><dl> <span data-ttu-id="a9440-125"><dt>**DPD, nicht \_ \_ verwendete \_ Dateien löschen**</dt></span><span class="sxs-lookup"><span data-stu-id="a9440-125"><dt>**DPD\_DELETE\_UNUSED\_FILES**</dt></span></span> </dl>             | <span data-ttu-id="a9440-126">Entfernt alle nicht verwendeten Treiberdateien.</span><span class="sxs-lookup"><span data-stu-id="a9440-126">Removes any unused driver files.</span></span><br/>                                                                                                                                           |
| <span id="DPD_DELETE_ALL_FILES"></span><span id="dpd_delete_all_files"></span><dl> <span data-ttu-id="a9440-127"><dt>**DPD \_ \_ alle \_ Dateien löschen**</dt></span><span class="sxs-lookup"><span data-stu-id="a9440-127"><dt>**DPD\_DELETE\_ALL\_FILES**</dt></span></span> </dl>                      | <span data-ttu-id="a9440-128">Löscht den Treiber nur dann, wenn alle zugehörigen Dateien entfernt werden können.</span><span class="sxs-lookup"><span data-stu-id="a9440-128">Deletes the driver only if all its associated files can be removed.</span></span> <span data-ttu-id="a9440-129">Der Löschvorgang schlägt fehl, wenn eine der Treiberdateien von einem anderen installierten Treiber verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a9440-129">The delete operation fails if any of the driver's files are being used by some other installed driver.</span></span><br/> |



 

<span data-ttu-id="a9440-130">Wenn DPD \_ Delete \_ Specific \_ Version nicht angegeben ist, löscht die Funktion alle Versionen des Treibers, wenn keine dieser Versionen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a9440-130">If DPD\_DELETE\_SPECIFIC\_VERSION is not specified, the function deletes all versions of the driver if none of them is in use.</span></span> <span data-ttu-id="a9440-131">Wenn keines \_ der DPD \_ nicht verwendete Dateien löscht und keine DPD-Dateien gelöscht \_ \_ \_ \_ werden, werden die Treiberdateien von der Funktion nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="a9440-131">If neither DPD\_DELETE\_UNUSED\_FILES nor DPD\_DELETE\_ALL\_FILES is specified, the function does not delete driver files.</span></span>

</dd> <dt>

<span data-ttu-id="a9440-132">*dwversionflag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a9440-132">*dwVersionFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9440-133">Die Version des zu löschenden Treibers.</span><span class="sxs-lookup"><span data-stu-id="a9440-133">The version of the driver to be deleted.</span></span> <span data-ttu-id="a9440-134">Dieser Parameter kann 0, 1, 2 oder 3 sein.</span><span class="sxs-lookup"><span data-stu-id="a9440-134">This parameter can be 0, 1, 2 or 3.</span></span> <span data-ttu-id="a9440-135">Dieser Parameter wird nur verwendet, wenn *dwdeleteflag* das Flag für die DPD- \_ \_ spezifische \_ Version enthält.</span><span class="sxs-lookup"><span data-stu-id="a9440-135">This parameter is used only if *dwDeleteFlag* includes the DPD\_DELETE\_SPECIFIC\_VERSION flag.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9440-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a9440-136">Return value</span></span>

<span data-ttu-id="a9440-137">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="a9440-137">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="a9440-138">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="a9440-138">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9440-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a9440-139">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a9440-140">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a9440-140">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="a9440-141">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="a9440-141">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="a9440-142">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="a9440-142">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="a9440-143">Bevor die Funktion die Treiberdateien löscht, wird die **drvdriverevent** -Funktion des Treibers aufgerufen, sodass der Treiber alle privaten Dateien entfernen kann, die nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a9440-143">Before the function deletes the driver files, it calls the driver's **DrvDriverEvent** function, allowing the driver to remove any private files that are not used.</span></span> <span data-ttu-id="a9440-144">Weitere Informationen zu **drvdriverevent** finden Sie im Microsoft Windows Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="a9440-144">For more information about **DrvDriverEvent**, see the Microsoft Windows Driver Development Kit (DDK).</span></span>

<span data-ttu-id="a9440-145">Wenn die Treiberdateien zurzeit geladen sind, verschiebt die Funktion Sie in ein temporäres Verzeichnis und markiert Sie beim Neustart für das Löschen.</span><span class="sxs-lookup"><span data-stu-id="a9440-145">If the driver files are currently loaded, the function moves them to a temp directory and marks them for deletion on restart.</span></span>

<span data-ttu-id="a9440-146">Vor dem Aufrufen von **deleteprinterdriverex** müssen Sie alle Drucker Objekte löschen, die den Druckertreiber verwenden.</span><span class="sxs-lookup"><span data-stu-id="a9440-146">Before calling **DeletePrinterDriverEx**, you must delete all printer objects that use the printer driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9440-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9440-147">Requirements</span></span>



| <span data-ttu-id="a9440-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a9440-148">Requirement</span></span> | <span data-ttu-id="a9440-149">Wert</span><span class="sxs-lookup"><span data-stu-id="a9440-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9440-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a9440-150">Minimum supported client</span></span><br/> | <span data-ttu-id="a9440-151">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9440-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a9440-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a9440-152">Minimum supported server</span></span><br/> | <span data-ttu-id="a9440-153">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9440-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a9440-154">Header</span><span class="sxs-lookup"><span data-stu-id="a9440-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9440-155"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a9440-155"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="a9440-156">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a9440-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="a9440-157"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9440-157"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="a9440-158">DLL</span><span class="sxs-lookup"><span data-stu-id="a9440-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9440-159"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="a9440-159"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="a9440-160">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="a9440-160">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a9440-161">**Deleteprinterdriverexw** (Unicode) und **deleteprinterdriverexa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a9440-161">**DeletePrinterDriverExW** (Unicode) and **DeletePrinterDriverExA** (ANSI)</span></span><br/>                     |



## <a name="see-also"></a><span data-ttu-id="a9440-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9440-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9440-163">Drucken</span><span class="sxs-lookup"><span data-stu-id="a9440-163">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="a9440-164">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="a9440-164">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="a9440-165">**Addprinterdriverex**</span><span class="sxs-lookup"><span data-stu-id="a9440-165">**AddPrinterDriverEx**</span></span>](addprinterdriverex.md)
</dt> </dl>

 

 




