---
description: Die Funktion findnextprinterchangenotifiruft Informationen über die aktuellste Änderungs Benachrichtigung für ein Änderungs Benachrichtigungs Objekt ab, das einem Drucker oder Druckserver zugeordnet ist.
ms.assetid: ea7774ae-361f-41e4-bbc6-3f100028b22a
title: Findnextprinterchangenotifi-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindNextPrinterChangeNotification
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: ef3ece0d4831409d79e2152cf7b6a37d6bbdc8b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866180"
---
# <a name="findnextprinterchangenotification-function"></a><span data-ttu-id="dd70d-103">Findnextprinterchangenotifi-Funktion</span><span class="sxs-lookup"><span data-stu-id="dd70d-103">FindNextPrinterChangeNotification function</span></span>

<span data-ttu-id="dd70d-104">Die Funktion **findnextprinterchangenotifiruft** Informationen über die aktuellste Änderungs Benachrichtigung für ein Änderungs Benachrichtigungs Objekt ab, das einem Drucker oder Druckserver zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="dd70d-104">The **FindNextPrinterChangeNotification** function retrieves information about the most recent change notification for a change notification object associated with a printer or print server.</span></span> <span data-ttu-id="dd70d-105">Diese Funktion wird aufgerufen, wenn ein warte Vorgang für das Änderungs Benachrichtigungs Objekt erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="dd70d-105">Call this function when a wait operation on the change notification object is satisfied.</span></span>

<span data-ttu-id="dd70d-106">Die-Funktion setzt auch das Änderungs Benachrichtigungs Objekt auf den nicht signalisierten Zustand zurück.</span><span class="sxs-lookup"><span data-stu-id="dd70d-106">The function also resets the change notification object to the not-signaled state.</span></span> <span data-ttu-id="dd70d-107">Anschließend können Sie das Objekt in einem anderen warte Vorgang verwenden, um die Überwachung des Druckers oder des Druck Servers fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="dd70d-107">You can then use the object in another wait operation to continue monitoring the printer or print server.</span></span> <span data-ttu-id="dd70d-108">Das Betriebssystem legt das Objekt auf den signalisierten Zustand fest, wenn ein bestimmter Satz von Änderungen für den Drucker oder den Druckserver das nächste Mal ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dd70d-108">The operating system will set the object to the signaled state the next time one of a specified set of changes occurs to the printer or print server.</span></span> <span data-ttu-id="dd70d-109">Die Funktion [**findfirstprinterchangenotifierstellt**](findfirstprinterchangenotification.md) das Änderungs Benachrichtigungs Objekt und gibt die Gruppe der zu überwachenden Änderungen an.</span><span class="sxs-lookup"><span data-stu-id="dd70d-109">The [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function creates the change notification object and specifies the set of changes to be monitored.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd70d-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd70d-110">Syntax</span></span>


```C++
BOOL FindNextPrinterChangeNotification(
  _In_      HANDLE hChange,
  _Out_opt_ PDWORD pdwChange,
  _In_opt_  LPVOID pPrinterNotifyOptions,
  _Out_opt_ LPVOID *ppPrinterNotifyInfo
);
```



## <a name="parameters"></a><span data-ttu-id="dd70d-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd70d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd70d-112">*hchange* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dd70d-112">*hChange* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd70d-113">Ein Handle für ein Änderungs Benachrichtigungs Objekt, das einem Drucker oder Druckserver zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="dd70d-113">A handle to a change notification object associated with a printer or print server.</span></span> <span data-ttu-id="dd70d-114">Sie erhalten ein solches handle, indem Sie die [**findfirstprinterchangenotifizierungsfunktion**](findfirstprinterchangenotification.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="dd70d-114">You obtain such a handle by calling the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function.</span></span> <span data-ttu-id="dd70d-115">Das Betriebssystem legt dieses Änderungs Benachrichtigungs Objekt auf den signalisierten Zustand fest, wenn eine der im Änderungs Benachrichtigungs Filter des Objekts angegebenen Änderungen erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="dd70d-115">The operating system sets this change notification object to the signaled state when it detects one of the changes specified in the object's change notification filter.</span></span>

</dd> <dt>

<span data-ttu-id="dd70d-116">*pdwchange* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="dd70d-116">*pdwChange* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dd70d-117">Ein Zeiger auf eine Variable, deren Bits festgelegt ist, um die Änderungen anzugeben, die aufgetreten sind, um die letzte Benachrichtigung zu verursachen.</span><span class="sxs-lookup"><span data-stu-id="dd70d-117">A pointer to a variable whose bits are set to indicate the changes that occurred to cause the most recent notification.</span></span> <span data-ttu-id="dd70d-118">Die Bitflags, die festgelegt werden können, entsprechen den Werten, die im *fdwfilter* -Parameter des [**findfirstprinterchangenotifizierungsaufrufes**](findfirstprinterchangenotification.md) angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="dd70d-118">The bit flags that might be set correspond to those specified in the *fdwFilter* parameter of the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) call.</span></span> <span data-ttu-id="dd70d-119">Das System legt mindestens eines der folgenden Bitflags fest.</span><span class="sxs-lookup"><span data-stu-id="dd70d-119">The system sets one or more of the following bit flags.</span></span>



| <span data-ttu-id="dd70d-120">Wert</span><span class="sxs-lookup"><span data-stu-id="dd70d-120">Value</span></span>                                                                                                                                                                                                                                             | <span data-ttu-id="dd70d-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="dd70d-121">Meaning</span></span>                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="PRINTER_CHANGE_ADD_FORM"></span><span id="printer_change_add_form"></span><dl> <span data-ttu-id="dd70d-122"><dt>**Formular "Drucker \_ Änderung \_ Hinzufügen" \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dd70d-122"><dt>**PRINTER\_CHANGE\_ADD\_FORM**</dt></span></span> </dl>                                                     | <span data-ttu-id="dd70d-123">Dem Server wurde ein Formular hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="dd70d-123">A form was added to the server.</span></span><br/>                |
| <span id="PRINTER_CHANGE_ADD_JOB"></span><span id="printer_change_add_job"></span><dl> <span data-ttu-id="dd70d-124"><dt>**Drucker \_ Änderung \_ Auftrag hinzufügen \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dd70d-124"><dt>**PRINTER\_CHANGE\_ADD\_JOB**</dt></span></span> </dl>                                                        | <span data-ttu-id="dd70d-125">Ein Druckauftrag wurde an den Drucker gesendet.</span><span class="sxs-lookup"><span data-stu-id="dd70d-125">A print job was sent to the printer.</span></span><br/>           |
| <span id="PRINTER_CHANGE_ADD_PORT"></span><span id="printer_change_add_port"></span><dl> <span data-ttu-id="dd70d-126"><dt>**Drucker \_ Änderung \_ " \_ Port hinzufügen"**</dt></span><span class="sxs-lookup"><span data-stu-id="dd70d-126"><dt>**PRINTER\_CHANGE\_ADD\_PORT**</dt></span></span> </dl>                                                     | <span data-ttu-id="dd70d-127">Dem Server wurde ein Port oder Monitor hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="dd70d-127">A port or monitor was added to the server.</span></span><br/>     |
| <span id="PRINTER_CHANGE_ADD_PRINT_PROCESSOR"></span><span id="printer_change_add_print_processor"></span><dl> <span data-ttu-id="dd70d-128"><dt>**Drucker \_ Änderung \_ Hinzufügen eines \_ Druck \_ Prozessors**</dt></span><span class="sxs-lookup"><span data-stu-id="dd70d-128"><dt>**PRINTER\_CHANGE\_ADD\_PRINT\_PROCESSOR**</dt></span></span> </dl>                   | <span data-ttu-id="dd70d-129">Ein Druck Prozessor wurde dem Server hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="dd70d-129">A print processor was added to the server.</span></span><br/>     |
| <span id="PRINTER_CHANGE_ADD_PRINTER"></span><span id="printer_change_add_printer"></span><dl> <span data-ttu-id="dd70d-130"><dt>**Drucker \_ Änderung \_ Drucker hinzufügen \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dd70d-130"><dt>**PRINTER\_CHANGE\_ADD\_PRINTER**</dt></span></span> </dl>                                            | <span data-ttu-id="dd70d-131">Ein Drucker wurde dem Server hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="dd70d-131">A printer was added to the server.</span></span><br/>             |
| <span id="PRINTER_CHANGE_ADD_PRINTER_DRIVER"></span><span id="printer_change_add_printer_driver"></span><dl> <span data-ttu-id="dd70d-132"><dt>**Drucker \_ Änderung \_ Drucker \_ Treiber hinzufügen \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dd70d-132"><dt>**PRINTER\_CHANGE\_ADD\_PRINTER\_DRIVER**</dt></span></span> </dl>                      | <span data-ttu-id="dd70d-133">Ein Druckertreiber wurde dem Server hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="dd70d-133">A printer driver was added to the server.</span></span><br/>      |
| <span id="PRINTER_CHANGE_CONFIGURE_PORT"></span><span id="printer_change_configure_port"></span><dl> <span data-ttu-id="dd70d-134"><dt>**Port für die Drucker \_ Änderung \_ konfigurieren \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dd70d-134"><dt>**PRINTER\_CHANGE\_CONFIGURE\_PORT**</dt></span></span> </dl>                                   | <span data-ttu-id="dd70d-135">Auf dem Server wurde ein Port konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="dd70d-135">A port was configured on the server.</span></span><br/>           |
| <span id="PRINTER_CHANGE_DELETE_FORM"></span><span id="printer_change_delete_form"></span><dl> <span data-ttu-id="dd70d-136"><dt>**Formular für das Löschen von Drucker \_ Änderungen \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dd70d-136"><dt>**PRINTER\_CHANGE\_DELETE\_FORM**</dt></span></span> </dl>                                            | <span data-ttu-id="dd70d-137">Ein Formular wurde vom Server gelöscht.</span><span class="sxs-lookup"><span data-stu-id="dd70d-137">A form was deleted from the server.</span></span><br/>            |
| <span id="PRINTER_CHANGE_DELETE_JOB"></span><span id="printer_change_delete_job"></span><dl> <span data-ttu-id="dd70d-138"><dt>**Auftrag zum Löschen der Drucker \_ Änderung \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dd70d-138"><dt>**PRINTER\_CHANGE\_DELETE\_JOB**</dt></span></span> </dl>                                               | <span data-ttu-id="dd70d-139">Ein Auftrag wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="dd70d-139">A job was deleted.</span></span><br/>                             |
| <span id="PRINTER_CHANGE_DELETE_PORT"></span><span id="printer_change_delete_port"></span><dl> <span data-ttu-id="dd70d-140"><dt>**\_druckeränderungsport \_ Löschen \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dd70d-140"><dt>**PRINTER\_CHANGE\_DELETE\_PORT**</dt></span></span> </dl>                                            | <span data-ttu-id="dd70d-141">Ein Port oder Monitor wurde vom Server gelöscht.</span><span class="sxs-lookup"><span data-stu-id="dd70d-141">A port or monitor was deleted from the server.</span></span><br/> |
| <span id="PRINTER_CHANGE_DELETE_PRINT_PROCESSOR"></span><span id="printer_change_delete_print_processor"></span><dl> <span data-ttu-id="dd70d-142"><dt>**Drucker \_ Änderung \_ Delete- \_ Druck \_ Prozessor**</dt></span><span class="sxs-lookup"><span data-stu-id="dd70d-142"><dt>**PRINTER\_CHANGE\_DELETE\_PRINT\_PROCESSOR**</dt></span></span> </dl>          | <span data-ttu-id="dd70d-143">Ein Druck Prozessor wurde vom Server gelöscht.</span><span class="sxs-lookup"><span data-stu-id="dd70d-143">A print processor was deleted from the server.</span></span><br/> |
| <span id="PRINTER_CHANGE_DELETE_PRINTER"></span><span id="printer_change_delete_printer"></span><dl> <span data-ttu-id="dd70d-144"><dt>**Drucker \_ Änderung Drucker \_ Löschen \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dd70d-144"><dt>**PRINTER\_CHANGE\_DELETE\_PRINTER**</dt></span></span> </dl>                                   | <span data-ttu-id="dd70d-145">Ein Drucker wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="dd70d-145">A printer was deleted.</span></span><br/>                         |
| <span id="PRINTER_CHANGE_DELETE_PRINTER_DRIVER"></span><span id="printer_change_delete_printer_driver"></span><dl> <span data-ttu-id="dd70d-146"><dt>**Drucker \_ Änderung zum \_ Löschen des \_ Drucker \_ Treibers**</dt></span><span class="sxs-lookup"><span data-stu-id="dd70d-146"><dt>**PRINTER\_CHANGE\_DELETE\_PRINTER\_DRIVER**</dt></span></span> </dl>             | <span data-ttu-id="dd70d-147">Ein Druckertreiber wurde vom Server gelöscht.</span><span class="sxs-lookup"><span data-stu-id="dd70d-147">A printer driver was deleted from the server.</span></span><br/>  |
| <span id="PRINTER_CHANGE_FAILED_CONNECTION_PRINTER"></span><span id="printer_change_failed_connection_printer"></span><dl> <span data-ttu-id="dd70d-148"><dt>**Fehler beim Drucker \_ Änderungs \_ \_ Verbindungs \_ Drucker.**</dt></span><span class="sxs-lookup"><span data-stu-id="dd70d-148"><dt>**PRINTER\_CHANGE\_FAILED\_CONNECTION\_PRINTER**</dt></span></span> </dl> | <span data-ttu-id="dd70d-149">Fehler bei einer Druckerverbindung.</span><span class="sxs-lookup"><span data-stu-id="dd70d-149">A printer connection has failed.</span></span><br/>               |
| <span id="PRINTER_CHANGE_SET_FORM"></span><span id="printer_change_set_form"></span><dl> <span data-ttu-id="dd70d-150"><dt>**Formular für den Drucker \_ Änderungs \_ Satz \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dd70d-150"><dt>**PRINTER\_CHANGE\_SET\_FORM**</dt></span></span> </dl>                                                     | <span data-ttu-id="dd70d-151">Auf dem Server wurde ein Formular festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dd70d-151">A form was set on the server.</span></span><br/>                  |
| <span id="PRINTER_CHANGE_SET_JOB"></span><span id="printer_change_set_job"></span><dl> <span data-ttu-id="dd70d-152"><dt>**Auftrag für Drucker \_ Änderungs \_ Satz \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dd70d-152"><dt>**PRINTER\_CHANGE\_SET\_JOB**</dt></span></span> </dl>                                                        | <span data-ttu-id="dd70d-153">Ein Auftrag wurde festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dd70d-153">A job was set.</span></span><br/>                                 |
| <span id="PRINTER_CHANGE_SET_PRINTER"></span><span id="printer_change_set_printer"></span><dl> <span data-ttu-id="dd70d-154"><dt>**Drucker \_ Änderungs \_ Satz- \_ Drucker**</dt></span><span class="sxs-lookup"><span data-stu-id="dd70d-154"><dt>**PRINTER\_CHANGE\_SET\_PRINTER**</dt></span></span> </dl>                                            | <span data-ttu-id="dd70d-155">Ein Drucker wurde festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dd70d-155">A printer was set.</span></span><br/>                             |
| <span id="PRINTER_CHANGE_SET_PRINTER_DRIVER"></span><span id="printer_change_set_printer_driver"></span><dl> <span data-ttu-id="dd70d-156"><dt>**Drucker \_ \_ Treiber- \_ Drucker \_ Treiber**</dt></span><span class="sxs-lookup"><span data-stu-id="dd70d-156"><dt>**PRINTER\_CHANGE\_SET\_PRINTER\_DRIVER**</dt></span></span> </dl>                      | <span data-ttu-id="dd70d-157">Ein Druckertreiber wurde festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dd70d-157">A printer driver was set.</span></span><br/>                      |
| <span id="PRINTER_CHANGE_WRITE_JOB"></span><span id="printer_change_write_job"></span><dl> <span data-ttu-id="dd70d-158"><dt>**\_ \_ Schreib \_ Auftrag für Drucker Änderung**</dt></span><span class="sxs-lookup"><span data-stu-id="dd70d-158"><dt>**PRINTER\_CHANGE\_WRITE\_JOB**</dt></span></span> </dl>                                                  | <span data-ttu-id="dd70d-159">Es wurden Auftragsdaten geschrieben.</span><span class="sxs-lookup"><span data-stu-id="dd70d-159">Job data was written.</span></span><br/>                          |
| <span id="PRINTER_CHANGE_TIMEOUT"></span><span id="printer_change_timeout"></span><dl> <span data-ttu-id="dd70d-160"><dt>**Drucker \_ Änderungs \_ Timeout**</dt></span><span class="sxs-lookup"><span data-stu-id="dd70d-160"><dt>**PRINTER\_CHANGE\_TIMEOUT**</dt></span></span> </dl>                                                         | <span data-ttu-id="dd70d-161">Timeout des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="dd70d-161">The job timed out.</span></span><br/>                             |
| <span id="PRINTER_CHANGE_SERVER"></span><span id="printer_change_server"></span><dl> <span data-ttu-id="dd70d-162"><dt>**Drucker \_ Änderungs \_ Server**</dt></span><span class="sxs-lookup"><span data-stu-id="dd70d-162"><dt>**PRINTER\_CHANGE\_SERVER**</dt></span></span> </dl>                                                            | <span data-ttu-id="dd70d-163">Windows 7: auf dem Server ist eine Änderung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="dd70d-163">Windows 7: A change occurred on the server.</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="dd70d-164">*pprinternotifyoptions* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="dd70d-164">*pPrinterNotifyOptions* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dd70d-165">Ein Zeiger auf die Struktur der [**Drucker \_ Benachrichtigungs \_ Optionen**](printer-notify-options.md) .</span><span class="sxs-lookup"><span data-stu-id="dd70d-165">A pointer to a [**PRINTER\_NOTIFY\_OPTIONS**](printer-notify-options.md) structure.</span></span> <span data-ttu-id="dd70d-166">Legen Sie den **Flags** -Member dieser Struktur auf **Drucker \_ Benachrichtigungs \_ Optionen \_ Aktualisieren** fest, damit die Funktion die aktuellen Daten für alle überwachten Drucker Informationsfelder zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="dd70d-166">Set the **Flags** member of this structure to **PRINTER\_NOTIFY\_OPTIONS\_REFRESH**, to cause the function to return the current data for all monitored printer information fields.</span></span> <span data-ttu-id="dd70d-167">Die-Funktion ignoriert alle anderen Member der-Struktur.</span><span class="sxs-lookup"><span data-stu-id="dd70d-167">The function ignores all other members of the structure.</span></span> <span data-ttu-id="dd70d-168">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="dd70d-168">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="dd70d-169">*ppprinternotifyinfo* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="dd70d-169">*ppPrinterNotifyInfo* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dd70d-170">Ein Zeiger auf eine Zeiger Variable, die einen Zeiger auf einen vom System zugewiesenen, schreibgeschützten Puffer empfängt.</span><span class="sxs-lookup"><span data-stu-id="dd70d-170">A pointer to a pointer variable that receives a pointer to a system-allocated, read-only buffer.</span></span> <span data-ttu-id="dd70d-171">Wenn Sie damit fertig sind, können Sie die [**freeprinternotifyinfo**](freeprinternotifyinfo.md) -Funktion aufzurufen, um den Puffer freizugeben.</span><span class="sxs-lookup"><span data-stu-id="dd70d-171">Call the [**FreePrinterNotifyInfo**](freeprinternotifyinfo.md) function to free the buffer when you are finished with it.</span></span> <span data-ttu-id="dd70d-172">Dieser Parameter kann **null** sein, wenn keine Informationen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="dd70d-172">This parameter can be **NULL** if no information is required.</span></span>

<span data-ttu-id="dd70d-173">Der Puffer enthält eine [**Drucker \_ Benachrichtigungs \_**](printer-notify-info.md) Struktur, die ein Array von [**Informationen zur \_ Drucker \_ Benachrichtigung \_**](printer-notify-info-data.md) enthält.</span><span class="sxs-lookup"><span data-stu-id="dd70d-173">The buffer contains a [**PRINTER\_NOTIFY\_INFO**](printer-notify-info.md) structure, which contains an array of [**PRINTER\_NOTIFY\_INFO\_DATA**](printer-notify-info-data.md) structures.</span></span> <span data-ttu-id="dd70d-174">Jedes Element des Arrays enthält Informationen zu einem der Felder, die im *pprinternotifyoptions* -Parameter des [**findfirstprinterchangenotifizierungsaufrufes**](findfirstprinterchangenotification.md) angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="dd70d-174">Each element of the array contains information about one of the fields specified in the *pPrinterNotifyOptions* parameter of the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) call.</span></span> <span data-ttu-id="dd70d-175">In der Regel stellt die Funktion Daten nur für die Felder bereit, die geändert wurden, um die letzte Benachrichtigung zu verursachen.</span><span class="sxs-lookup"><span data-stu-id="dd70d-175">Typically, the function provides data only for the fields that changed to cause the most recent notification.</span></span> <span data-ttu-id="dd70d-176">Wenn jedoch die Struktur, auf die der *pprinternotifyoptions* -Parameter verweist, die **\_ Option zur \_ \_ Aktualisierung von Drucker Benachrichtigungen** angibt, stellt die Funktion Daten für alle überwachten Felder bereit.</span><span class="sxs-lookup"><span data-stu-id="dd70d-176">However, if the structure pointed to by the *pPrinterNotifyOptions* parameter specifies **PRINTER\_NOTIFY\_OPTIONS\_REFRESH**, the function provides data for all monitored fields.</span></span>

<span data-ttu-id="dd70d-177">Wenn das **\_ \_ \_ verworfene** Element für den Drucker Benachrichtigen in der **Flags** - [**Information der \_ Drucker \_ Informations**](printer-notify-info.md) Struktur festgelegt ist, ist ein Überlauf oder Fehler aufgetreten, und die Benachrichtigungen sind möglicherweise verloren gegangen.</span><span class="sxs-lookup"><span data-stu-id="dd70d-177">If the **PRINTER\_NOTIFY\_INFO\_DISCARDED** bit is set in the **Flags** member of the [**PRINTER\_NOTIFY\_INFO**](printer-notify-info.md) structure, an overflow or error occurred, and notifications may have been lost.</span></span> <span data-ttu-id="dd70d-178">In diesem Fall werden keine weiteren Benachrichtigungen gesendet, bis Sie einen zweiten **findnextprinterchangenotifizierungsbefehl** ausführen, der die **Aktualisierung der Drucker \_ Benachrichtigungs \_ Optionen \_** angibt.</span><span class="sxs-lookup"><span data-stu-id="dd70d-178">In this case, no additional notifications will be sent until you make a second **FindNextPrinterChangeNotification** call that specifies **PRINTER\_NOTIFY\_OPTIONS\_REFRESH**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd70d-179">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dd70d-179">Return value</span></span>

<span data-ttu-id="dd70d-180">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="dd70d-180">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="dd70d-181">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="dd70d-181">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd70d-182">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dd70d-182">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="dd70d-183">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="dd70d-183">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="dd70d-184">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="dd70d-184">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="dd70d-185">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="dd70d-185">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="dd70d-186">Rufen Sie die Funktion " **findnextprinterchangenotifitifitifitifitifitifitifitifitifitifitifitifitifiup** " auf, nachdem ein warte Vorgang für ein von [**findfirstprinterchangenotifi**](findfirstprinterchangenotification.md)</span><span class="sxs-lookup"><span data-stu-id="dd70d-186">Call the **FindNextPrinterChangeNotification** function after a wait operation on a notification object created by [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) has been satisfied.</span></span> <span data-ttu-id="dd70d-187">Durch Aufrufen von **findnextprinterchangenotifikönnen** Sie Informationen zu der Änderung abrufen, die den warte Vorgang erfüllt hat, und das Benachrichtigungs Objekt zurücksetzen, damit es signalisiert werden kann, wenn die nächste Änderung auftritt.</span><span class="sxs-lookup"><span data-stu-id="dd70d-187">Calling **FindNextPrinterChangeNotification** lets you obtain information about the change that satisfied the wait operation, and resets the notification object so it can be signaled when the next change occurs.</span></span>

<span data-ttu-id="dd70d-188">Rufen Sie die **findnextprinterchangenotifi-** Funktion mit einer Ausnahme nicht auf, wenn sich das Änderungs Benachrichtigungs Objekt nicht im signalisierten Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="dd70d-188">With one exception, do not call the **FindNextPrinterChangeNotification** function if the change notification object is not in the signaled state.</span></span> <span data-ttu-id="dd70d-189">Wenn eine wait-Funktion den **\_ Timeout** Wert der Wartezeit zurückgibt, befindet sich das Änderungs Objekt nicht im signalisierten Zustand.</span><span class="sxs-lookup"><span data-stu-id="dd70d-189">If a wait function returns the value **WAIT\_TIMEOUT**, the change object is not in the signaled state.</span></span> <span data-ttu-id="dd70d-190">Rufen Sie die Funktion " **findnextprinterchangenotifitifitifitifitifitifitifitifitifitifitifitifitifitifi"** nur auf Eine Ausnahme bildet die Verwendung von **findnextprinterchangenotifizierung** mit dem im Parameter *pprinternotifyoptions* festgelegten **\_ \_ \_ Refresh** -Bit für die Drucker Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="dd70d-190">Call the **FindNextPrinterChangeNotification** function only if the wait function succeeds without timing out. The exception is when **FindNextPrinterChangeNotification** is called with the **PRINTER\_NOTIFY\_OPTIONS\_REFRESH** bit set in the *pPrinterNotifyOptions* parameter.</span></span> <span data-ttu-id="dd70d-191">Beachten Sie, dass auch dann, wenn dieses Flag festgelegt ist, das Flag für das **\_ \_ \_ verworfene Drucker Benachrichtigen** weiterhin im *ppprinternotifyinfo* -Parameter festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="dd70d-191">Note that even when this flag is set, it is still possible for the **PRINTER\_NOTIFY\_INFO\_DISCARDED** flag to be set in the *ppPrinterNotifyInfo* parameter.</span></span>

<span data-ttu-id="dd70d-192">Wenn Sie die Überwachung des Druckers oder des Druck Servers fortsetzen möchten, wiederholen Sie den Vorgang, indem Sie eine der [Wait-Funktionen](/windows/desktop/Sync/wait-functions) aufrufen und dann die **findnextprinterchangenotifi-** Funktion aufrufen, um die Änderung zu überprüfen und das Benachrichtigungs Objekt zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="dd70d-192">To continue monitoring the printer or print server for changes, repeat the cycle of calling one of the [wait functions](/windows/desktop/Sync/wait-functions) , and then calling the **FindNextPrinterChangeNotification** function to examine the change and reset the notification object.</span></span>

<span data-ttu-id="dd70d-193">**Findnextprinterchangenotifizierung** kann mehrere Änderungen am gleichen Drucker Informationsfeld in einer einzelnen Benachrichtigung kombinieren.</span><span class="sxs-lookup"><span data-stu-id="dd70d-193">**FindNextPrinterChangeNotification** may combine multiple changes to the same printer information field into a single notification.</span></span> <span data-ttu-id="dd70d-194">In diesem Fall reduziert die Funktion in der Regel alle Änderungen für das Feld in einem einzelnen Eintrag im Array der [**Drucker \_ \_ Info- \_ Daten**](printer-notify-info-data.md) Strukturen, die in *ppprinternotifyinfo* angezeigt werden. der einzige Eintrag meldet nur die aktuellsten Informationen.</span><span class="sxs-lookup"><span data-stu-id="dd70d-194">When this occurs, the function typically collapses all changes for the field into a single entry in the array of [**PRINTER\_NOTIFY\_INFO\_DATA**](printer-notify-info-data.md) structures in *ppPrinterNotifyInfo*; the single entry reports only the most current information.</span></span> <span data-ttu-id="dd70d-195">Für einige Auftrags-und Drucker Informationsfelder kann die Funktion jedoch mehrere Array Einträge für dasselbe Feld zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="dd70d-195">However, for some job and printer information fields, the function can return multiple array entries for the same field.</span></span> <span data-ttu-id="dd70d-196">In diesem Fall meldet der letzte Array Eintrag für das Feld die aktuellen Daten, und die früheren Einträge enthalten die Daten für die Zwischenstufen.</span><span class="sxs-lookup"><span data-stu-id="dd70d-196">In this case, the last array entry for the field reports the current data, and the earlier entries contain the data for the intermediate stages.</span></span>

<span data-ttu-id="dd70d-197">Wenn das Änderungs Benachrichtigungs Objekt nicht mehr benötigt wird, schließen Sie es, indem Sie die [**findcloseprinterchangenotifi-**](findcloseprinterchangenotification.md) Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="dd70d-197">When you no longer need the change notification object, close it by calling the [**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="dd70d-198">In Windows XP mit Service Pack 2 (SP2) und höher blockiert die Internetverbindungs Firewall (ICF) standardmäßig Drucker Anschlüsse, eine Ausnahme für die Datei-und Druckfreigabe kann jedoch aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="dd70d-198">In Windows XP with Service Pack 2 (SP2) and later, the Internet Connection Firewall (ICF) blocks printer ports by default, but an exception for File and Print Sharing can be enabled.</span></span> <span data-ttu-id="dd70d-199">Wenn ein Benutzer eine Druckerverbindung mit einem anderen Computer herstellt und die Ausnahme nicht aktiviert ist, empfängt der Benutzer keine Drucker Änderungs Benachrichtigungen vom Server.</span><span class="sxs-lookup"><span data-stu-id="dd70d-199">If a user makes a printer connection to another machine, and the exception is not enabled, then the user will not receive printer change notifications from the server.</span></span> <span data-ttu-id="dd70d-200">Ein Computer Administrator muss die Ausnahme aktivieren.</span><span class="sxs-lookup"><span data-stu-id="dd70d-200">A machine admin will have to enable exception.</span></span>

 

## <a name="examples"></a><span data-ttu-id="dd70d-201">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dd70d-201">Examples</span></span>

<span data-ttu-id="dd70d-202">Im folgenden Codebeispiel wird veranschaulicht, wie Sie den Druckerstatus mithilfe dieser Funktionen überwachen können.</span><span class="sxs-lookup"><span data-stu-id="dd70d-202">The following code sample illustrates how you might monitor printer status by using these functions.</span></span>


```C++
// Get change notification handle for the printer   
chgObject = FindFirstPrinterChangeNotification( 
                hPrinter, 
                PRINTER_CHANGE_JOB, 
                0, 
                NULL); 

if (chgObject != INVALID_HANDLE_VALUE) {
    while (bKeepMonitoring) {
        // Wait for the change notification 
        WaitForSingleObject(chgObject, INFINITE);

        fcnreturn = FindNextPrinterChangeNotification(
                        chgObject, 
                        pdwChange, 
                        NULL, 
                        NULL);

        if (fcnreturn) {
            // Check value of *pdwChange and 
            //  deal with the indicated change 
        }
        // Insert some mechanism to stop monitoring
        //  such as: 
        //
        // if (something happens) {
        //     bKeepMonitoring = false; 
        // }
        //
    }
    // Close Printer Change Notification handle when finished. 
    FindClosePrinterChangeNotification(chgObject);
} else {
    // Unable to open printer change notification handle 
    dwStatus = GetLastError();
}
```



## <a name="requirements"></a><span data-ttu-id="dd70d-203">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dd70d-203">Requirements</span></span>



| <span data-ttu-id="dd70d-204">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dd70d-204">Requirement</span></span> | <span data-ttu-id="dd70d-205">Wert</span><span class="sxs-lookup"><span data-stu-id="dd70d-205">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd70d-206">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dd70d-206">Minimum supported client</span></span><br/> | <span data-ttu-id="dd70d-207">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dd70d-207">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="dd70d-208">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dd70d-208">Minimum supported server</span></span><br/> | <span data-ttu-id="dd70d-209">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dd70d-209">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="dd70d-210">Header</span><span class="sxs-lookup"><span data-stu-id="dd70d-210">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd70d-211"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dd70d-211"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="dd70d-212">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dd70d-212">Library</span></span><br/>                  | <dl> <span data-ttu-id="dd70d-213"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd70d-213"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="dd70d-214">DLL</span><span class="sxs-lookup"><span data-stu-id="dd70d-214">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd70d-215"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd70d-215"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="dd70d-216">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd70d-216">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd70d-217">Drucken</span><span class="sxs-lookup"><span data-stu-id="dd70d-217">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="dd70d-218">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="dd70d-218">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="dd70d-219">**Findcloseprinterchangenotifizierung**</span><span class="sxs-lookup"><span data-stu-id="dd70d-219">**FindClosePrinterChangeNotification**</span></span>](findcloseprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="dd70d-220">**Findfirstprinterchangenotifizierung**</span><span class="sxs-lookup"><span data-stu-id="dd70d-220">**FindFirstPrinterChangeNotification**</span></span>](findfirstprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="dd70d-221">**Drucker \_ Benachrichtigungs \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="dd70d-221">**PRINTER\_NOTIFY\_INFO**</span></span>](printer-notify-info.md)
</dt> <dt>

[<span data-ttu-id="dd70d-222">**\_ \_ Info \_ Daten für Drucker Benachrichtigen**</span><span class="sxs-lookup"><span data-stu-id="dd70d-222">**PRINTER\_NOTIFY\_INFO\_DATA**</span></span>](printer-notify-info-data.md)
</dt> <dt>

[<span data-ttu-id="dd70d-223">**Drucker \_ Benachrichtigungs \_ Optionen**</span><span class="sxs-lookup"><span data-stu-id="dd70d-223">**PRINTER\_NOTIFY\_OPTIONS**</span></span>](printer-notify-options.md)
</dt> </dl>

 

