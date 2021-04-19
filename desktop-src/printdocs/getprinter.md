---
description: Die GetPrinter-Funktion Ruft Informationen zu einem angegebenen Drucker ab.
ms.assetid: f162edbb-83ee-40c3-8710-9c867301d652
title: GetPrinter-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinter
- GetPrinterA
- GetPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-0.dll
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: e99b3574762b84b830845da8149b0406664b6da7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350117"
---
# <a name="getprinter-function"></a><span data-ttu-id="95d7b-103">GetPrinter-Funktion</span><span class="sxs-lookup"><span data-stu-id="95d7b-103">GetPrinter function</span></span>

<span data-ttu-id="95d7b-104">Die **GetPrinter** -Funktion Ruft Informationen zu einem angegebenen Drucker ab.</span><span class="sxs-lookup"><span data-stu-id="95d7b-104">The **GetPrinter** function retrieves information about a specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="95d7b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="95d7b-105">Syntax</span></span>


```C++
BOOL GetPrinter(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrinter,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="95d7b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="95d7b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95d7b-107">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95d7b-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95d7b-108">Ein Handle für den Drucker, für den die Funktion Informationen abruft.</span><span class="sxs-lookup"><span data-stu-id="95d7b-108">A handle to the printer for which the function retrieves information.</span></span> <span data-ttu-id="95d7b-109">Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.</span><span class="sxs-lookup"><span data-stu-id="95d7b-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="95d7b-110">*Ebene* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95d7b-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95d7b-111">Die Ebene oder der Typ der Struktur, die die Funktion in dem Puffer speichert, auf den *pprinter* zeigt.</span><span class="sxs-lookup"><span data-stu-id="95d7b-111">The level or type of structure that the function stores into the buffer pointed to by *pPrinter*.</span></span>

<span data-ttu-id="95d7b-112">Dieser Wert kann 1, 2, 3, 4, 5, 6, 7, 8 oder 9 sein.</span><span class="sxs-lookup"><span data-stu-id="95d7b-112">This value can be 1, 2, 3, 4, 5, 6, 7, 8 or 9.</span></span>

</dd> <dt>

<span data-ttu-id="95d7b-113">*pprinter* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="95d7b-113">*pPrinter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95d7b-114">Ein Zeiger auf einen Puffer, der eine-Struktur mit Informationen über den angegebenen Drucker empfängt.</span><span class="sxs-lookup"><span data-stu-id="95d7b-114">A pointer to a buffer that receives a structure containing information about the specified printer.</span></span> <span data-ttu-id="95d7b-115">Der Puffer muss groß genug sein, um die Struktur und alle Zeichen folgen oder andere Daten zu empfangen, auf die die Strukturmember zeigen.</span><span class="sxs-lookup"><span data-stu-id="95d7b-115">The buffer must be large enough to receive the structure and any strings or other data to which the structure members point.</span></span> <span data-ttu-id="95d7b-116">Wenn der Puffer zu klein ist, gibt der Parameter *pcbrequired* die erforderliche Puffergröße zurück.</span><span class="sxs-lookup"><span data-stu-id="95d7b-116">If the buffer is too small, the *pcbNeeded* parameter returns the required buffer size.</span></span>

<span data-ttu-id="95d7b-117">Der Typ der Struktur wird durch den Wert der *Ebene* bestimmt.</span><span class="sxs-lookup"><span data-stu-id="95d7b-117">The type of structure is determined by the value of *Level*.</span></span>



| <span data-ttu-id="95d7b-118">Ebene</span><span class="sxs-lookup"><span data-stu-id="95d7b-118">Level</span></span>                                                                                                | <span data-ttu-id="95d7b-119">Struktur</span><span class="sxs-lookup"><span data-stu-id="95d7b-119">Structure</span></span>                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="95d7b-120"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="95d7b-120"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="95d7b-121">Eine Struktur von [**Drucker Informationen \_ \_ 1**](printer-info-1.md) , die allgemeine Drucker Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="95d7b-121">A [**PRINTER\_INFO\_1**](printer-info-1.md) structure containing general printer information.</span></span><br/>                                                                                                        |
| <span id="2"></span><dl> <span data-ttu-id="95d7b-122"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="95d7b-122"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="95d7b-123">Eine " [**Printer \_ Info \_ 2**](printer-info-2.md) "-Struktur, die ausführliche Informationen über den Drucker enthält.</span><span class="sxs-lookup"><span data-stu-id="95d7b-123">A [**PRINTER\_INFO\_2**](printer-info-2.md) structure containing detailed information about the printer.</span></span><br/>                                                                                             |
| <span id="3"></span><dl> <span data-ttu-id="95d7b-124"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="95d7b-124"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="95d7b-125">Eine [**Drucker \_ Info \_ 3**](printer-info-3.md) -Struktur, die die Sicherheitsinformationen des Druckers enthält.</span><span class="sxs-lookup"><span data-stu-id="95d7b-125">A [**PRINTER\_INFO\_3**](printer-info-3.md) structure containing the printer's security information.</span></span><br/>                                                                                                 |
| <span id="4"></span><dl> <span data-ttu-id="95d7b-126"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="95d7b-126"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="95d7b-127">Eine [**Drucker \_ Info \_ 4**](printer-info-4.md) -Struktur, die die minimalen Drucker Informationen enthält, einschließlich des Drucker namens, des Server namens und der Angabe, ob der Drucker Remote oder lokal ist.</span><span class="sxs-lookup"><span data-stu-id="95d7b-127">A [**PRINTER\_INFO\_4**](printer-info-4.md) structure containing minimal printer information, including the name of the printer, the name of the server, and whether the printer is remote or local.</span></span><br/> |
| <span id="5"></span><dl> <span data-ttu-id="95d7b-128"><dt>**5**</dt></span><span class="sxs-lookup"><span data-stu-id="95d7b-128"><dt>**5**</dt></span></span> </dl> | <span data-ttu-id="95d7b-129">Eine [**Drucker \_ Info \_ 5**](printer-info-5.md) -Struktur, die Drucker Informationen enthält, wie z. b. Drucker Attribute und Timeout Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="95d7b-129">A [**PRINTER\_INFO\_5**](printer-info-5.md) structure containing printer information such as printer attributes and time-out settings.</span></span><br/>                                                               |
| <span id="6"></span><dl> <span data-ttu-id="95d7b-130"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="95d7b-130"><dt>**6**</dt></span></span> </dl> | <span data-ttu-id="95d7b-131">Eine [**Drucker \_ Info \_ 6**](printer-info-6.md) -Struktur, die den Statuswert eines Druckers angibt.</span><span class="sxs-lookup"><span data-stu-id="95d7b-131">A [**PRINTER\_INFO\_6**](printer-info-6.md) structure specifying the status value of a printer.</span></span><br/>                                                                                                      |
| <span id="7"></span><dl> <span data-ttu-id="95d7b-132"><dt>**7**</dt></span><span class="sxs-lookup"><span data-stu-id="95d7b-132"><dt>**7**</dt></span></span> </dl> | <span data-ttu-id="95d7b-133">Eine [**Drucker \_ Info \_ 7**](printer-info-7.md) -Struktur, die angibt, ob der Drucker im Verzeichnisdienst veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="95d7b-133">A [**PRINTER\_INFO\_7**](printer-info-7.md) structure that indicates whether the printer is published in the directory service.</span></span><br/>                                                                      |
| <span id="8"></span><dl> <span data-ttu-id="95d7b-134"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="95d7b-134"><dt>**8**</dt></span></span> </dl> | <span data-ttu-id="95d7b-135">Eine [**Drucker \_ Info \_ 8**](printer-info-8.md) -Struktur, die die globalen Standarddrucker Einstellungen angibt.</span><span class="sxs-lookup"><span data-stu-id="95d7b-135">A [**PRINTER\_INFO\_8**](printer-info-8.md) structure specifying the global default printer settings.</span></span><br/>                                                                                                |
| <span id="9"></span><dl> <span data-ttu-id="95d7b-136"><dt>**9**</dt></span><span class="sxs-lookup"><span data-stu-id="95d7b-136"><dt>**9**</dt></span></span> </dl> | <span data-ttu-id="95d7b-137">Eine [**Drucker \_ Info \_ 9**](printer-info-9.md) -Struktur, die die Standarddrucker Einstellungen pro Benutzer angibt.</span><span class="sxs-lookup"><span data-stu-id="95d7b-137">A [**PRINTER\_INFO\_9**](printer-info-9.md) structure specifying the per-user default printer settings.</span></span><br/>                                                                                              |



 

</dd> <dt>

<span data-ttu-id="95d7b-138">*cbbuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95d7b-138">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95d7b-139">Die Größe (in Bytes) des Puffers, auf den *pprinter* zeigt.</span><span class="sxs-lookup"><span data-stu-id="95d7b-139">The size, in bytes, of the buffer pointed to by *pPrinter*.</span></span>

</dd> <dt>

<span data-ttu-id="95d7b-140">*pcbbenötigte* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="95d7b-140">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95d7b-141">Ein Zeiger auf eine Variable, die von der Funktion auf die Größe (in Bytes) der Drucker Informationen festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="95d7b-141">A pointer to a variable that the function sets to the size, in bytes, of the printer information.</span></span> <span data-ttu-id="95d7b-142">Wenn *cbbuf* kleiner ist als dieser Wert, schlägt **GetPrinter** fehl, und der Wert stellt die erforderliche Puffergröße dar.</span><span class="sxs-lookup"><span data-stu-id="95d7b-142">If *cbBuf* is smaller than this value, **GetPrinter** fails, and the value represents the required buffer size.</span></span> <span data-ttu-id="95d7b-143">Wenn *cbbuf* größer oder gleich diesem Wert ist, ist **GetPrinter** erfolgreich, und der Wert stellt die Anzahl von Bytes dar, die im Puffer gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="95d7b-143">If *cbBuf* is equal to or greater than this value, **GetPrinter** succeeds, and the value represents the number of bytes stored in the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95d7b-144">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95d7b-144">Return value</span></span>

<span data-ttu-id="95d7b-145">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="95d7b-145">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="95d7b-146">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="95d7b-146">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="95d7b-147">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95d7b-147">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="95d7b-148">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="95d7b-148">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="95d7b-149">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="95d7b-149">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="95d7b-150">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="95d7b-150">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="95d7b-151">Der **pdevmode** -Member in den Strukturen [**Printer \_ Info \_ 2**](printer-info-2.md), [**Printer \_ Info \_ 8**](printer-info-8.md)und [**Printer \_ Info \_ 9**](printer-info-9.md) kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="95d7b-151">The **pDevMode** member in the [**PRINTER\_INFO\_2**](printer-info-2.md), [**PRINTER\_INFO\_8**](printer-info-8.md), and [**PRINTER\_INFO\_9**](printer-info-9.md) structures can be **NULL**.</span></span> <span data-ttu-id="95d7b-152">Wenn dies der Fall ist, kann der Drucker erst wieder verwendet werden, wenn der Treiber erfolgreich erneut installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="95d7b-152">When this happens, the printer is unusable until the driver is reinstalled successfully.</span></span>

<span data-ttu-id="95d7b-153">Für die [**Drucker \_ Info \_ 2**](printer-info-2.md) -und [**Printer \_ Info \_ 3**](printer-info-3.md) -Strukturen, die einen Zeiger auf eine Sicherheits Beschreibung enthalten, ruft die Funktion nur die Komponenten der Sicherheits Beschreibung ab, für die der Aufrufer über Leseberechtigung verfügt.</span><span class="sxs-lookup"><span data-stu-id="95d7b-153">For the [**PRINTER\_INFO\_2**](printer-info-2.md) and [**PRINTER\_INFO\_3**](printer-info-3.md) structures that contain a pointer to a security descriptor, the function retrieves only those components of the security descriptor that the caller has permission to read.</span></span> <span data-ttu-id="95d7b-154">Zum Abrufen bestimmter sicherheitsbeschreibungkomponenten müssen Sie die erforderlichen Zugriffsrechte angeben, wenn Sie die [**OpenPrinter**](openprinter.md) -Funktion aufrufen, um ein Handle für den Drucker abzurufen.</span><span class="sxs-lookup"><span data-stu-id="95d7b-154">To retrieve particular security descriptor components, you must specify the necessary access rights when you call the [**OpenPrinter**](openprinter.md) function to retrieve a handle to the printer.</span></span> <span data-ttu-id="95d7b-155">In der folgenden Tabelle sind die zum Lesen der verschiedenen sicherheitsbeschreibungkomponenten erforderlichen Zugriffsrechte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="95d7b-155">The following table shows the access rights required to read the various security descriptor components.</span></span>



| <span data-ttu-id="95d7b-156">Zugriffsrecht</span><span class="sxs-lookup"><span data-stu-id="95d7b-156">Access Right</span></span>                        | <span data-ttu-id="95d7b-157">Sicherheitsbeschreibungerkomponente</span><span class="sxs-lookup"><span data-stu-id="95d7b-157">Security Descriptor Component</span></span>                                                                 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="95d7b-158">Lese \_ Steuerelement</span><span class="sxs-lookup"><span data-stu-id="95d7b-158">READ\_CONTROL</span></span><br/>            | <span data-ttu-id="95d7b-159">Besitzer</span><span class="sxs-lookup"><span data-stu-id="95d7b-159">Owner</span></span><br/> <span data-ttu-id="95d7b-160">Primäre Gruppe</span><span class="sxs-lookup"><span data-stu-id="95d7b-160">Primary group</span></span><br/> <span data-ttu-id="95d7b-161">Freigegebene Zugriffs Steuerungs Liste (DACL)</span><span class="sxs-lookup"><span data-stu-id="95d7b-161">Discretionary access-control list (DACL)</span></span><br/> |
| <span data-ttu-id="95d7b-162">Zugreifen auf die \_ System \_ Sicherheit</span><span class="sxs-lookup"><span data-stu-id="95d7b-162">ACCESS\_SYSTEM\_SECURITY</span></span><br/> | <span data-ttu-id="95d7b-163">System Zugriffs Steuerungs Liste (SACL)</span><span class="sxs-lookup"><span data-stu-id="95d7b-163">System access-control list (SACL)</span></span><br/>                                                  |



 

<span data-ttu-id="95d7b-164">Wenn Sie Ebene 7 angeben, gibt das **dwAction** -Mitglied von [**Printer \_ Info \_ 7**](printer-info-7.md) einen der folgenden Werte zurück, um anzugeben, ob der Drucker im Verzeichnisdienst veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="95d7b-164">If you specify level 7, the **dwAction** member of [**PRINTER\_INFO\_7**](printer-info-7.md) returns one of the following values to indicate whether the printer is published in the directory service.</span></span>



| <span data-ttu-id="95d7b-165">dwAction-Wert</span><span class="sxs-lookup"><span data-stu-id="95d7b-165">dwAction value</span></span>     | <span data-ttu-id="95d7b-166">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="95d7b-166">Meaning</span></span>                                                                                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95d7b-167">dsprint- \_ Veröffentlichung</span><span class="sxs-lookup"><span data-stu-id="95d7b-167">DSPRINT\_PUBLISH</span></span>   | <span data-ttu-id="95d7b-168">Der Drucker wird veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="95d7b-168">The printer is published.</span></span> <span data-ttu-id="95d7b-169">Das **pszobjectguid** -Element enthält die GUID des Verzeichnisdienste-druckwarteschlangenobjekts, das dem Drucker zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="95d7b-169">The **pszObjectGUID** member contains the GUID of the directory services print queue object associated with the printer.</span></span>                                                                                                       |
| <span data-ttu-id="95d7b-170">dsprint- \_ Veröffentlichung aufheben</span><span class="sxs-lookup"><span data-stu-id="95d7b-170">DSPRINT\_UNPUBLISH</span></span> | <span data-ttu-id="95d7b-171">Der Drucker ist nicht veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="95d7b-171">The printer is not published.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="95d7b-172">dsprint \_ Ausstehend</span><span class="sxs-lookup"><span data-stu-id="95d7b-172">DSPRINT\_PENDING</span></span>   | <span data-ttu-id="95d7b-173">Gibt an, dass das System versucht, einen Veröffentlichungs-oder unveröffentlichungsvorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="95d7b-173">Indicates that the system is attempting to complete a publish or unpublish operation.</span></span> <span data-ttu-id="95d7b-174">Wenn ein [**SetPrinter**](setprinter.md) -Rückruf einen Drucker nicht veröffentlichen oder nicht veröffentlichen kann, werden im Hintergrund weitere Versuche unternommen, den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="95d7b-174">If a [**SetPrinter**](setprinter.md) call fails to publish or unpublish a printer, the system makes further attempts to complete the operation in the background.</span></span> |



 

<span data-ttu-id="95d7b-175">Ab Windows Vista werden die von **GetPrinter** zurückgegebenen Druckerdaten aus einem lokalen Cache abgerufen, wenn sich *hprinter* auf einen Drucker bezieht, der von einem Druckserver gehostet wird, und mindestens eine offene Verbindung zum Druckserver vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="95d7b-175">Starting with Windows Vista, the printer data returned by **GetPrinter** is retrieved from a local cache when *hPrinter* refers to a printer hosted by a print server and there is at least one open connection to the print server.</span></span> <span data-ttu-id="95d7b-176">In allen anderen Konfigurationen werden die Druckerdaten vom Druckserver abgefragt.</span><span class="sxs-lookup"><span data-stu-id="95d7b-176">In all other configurations, the printer data is queried from the print server.</span></span>

## <a name="requirements"></a><span data-ttu-id="95d7b-177">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95d7b-177">Requirements</span></span>



| <span data-ttu-id="95d7b-178">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95d7b-178">Requirement</span></span> | <span data-ttu-id="95d7b-179">Wert</span><span class="sxs-lookup"><span data-stu-id="95d7b-179">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95d7b-180">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="95d7b-180">Minimum supported client</span></span><br/> | <span data-ttu-id="95d7b-181">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95d7b-181">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="95d7b-182">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="95d7b-182">Minimum supported server</span></span><br/> | <span data-ttu-id="95d7b-183">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95d7b-183">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="95d7b-184">Header</span><span class="sxs-lookup"><span data-stu-id="95d7b-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="95d7b-185"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="95d7b-185"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="95d7b-186">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="95d7b-186">Library</span></span><br/>                  | <dl> <span data-ttu-id="95d7b-187"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95d7b-187"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="95d7b-188">DLL</span><span class="sxs-lookup"><span data-stu-id="95d7b-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95d7b-189"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="95d7b-189"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="95d7b-190">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="95d7b-190">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="95d7b-191">**Getprinterw** (Unicode) und **getprintera** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="95d7b-191">**GetPrinterW** (Unicode) and **GetPrinterA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="95d7b-192">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95d7b-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95d7b-193">Drucken</span><span class="sxs-lookup"><span data-stu-id="95d7b-193">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="95d7b-194">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="95d7b-194">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="95d7b-195">**Abbruch Drucker**</span><span class="sxs-lookup"><span data-stu-id="95d7b-195">**AbortPrinter**</span></span>](abortprinter.md)
</dt> <dt>

[<span data-ttu-id="95d7b-196">**AddPrinter**</span><span class="sxs-lookup"><span data-stu-id="95d7b-196">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="95d7b-197">**Closeprinter**</span><span class="sxs-lookup"><span data-stu-id="95d7b-197">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="95d7b-198">**Deleteprinter**</span><span class="sxs-lookup"><span data-stu-id="95d7b-198">**DeletePrinter**</span></span>](deleteprinter.md)
</dt> <dt>

[<span data-ttu-id="95d7b-199">**Enumdrucker**</span><span class="sxs-lookup"><span data-stu-id="95d7b-199">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="95d7b-200">**Drucker \_ Informationen \_ 1**</span><span class="sxs-lookup"><span data-stu-id="95d7b-200">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="95d7b-201">**Drucker \_ Informationen \_ 2**</span><span class="sxs-lookup"><span data-stu-id="95d7b-201">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="95d7b-202">**Drucker \_ Informationen \_ 3**</span><span class="sxs-lookup"><span data-stu-id="95d7b-202">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="95d7b-203">**Drucker \_ Info \_ 4**</span><span class="sxs-lookup"><span data-stu-id="95d7b-203">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="95d7b-204">**Drucker \_ Informationen \_ 5**</span><span class="sxs-lookup"><span data-stu-id="95d7b-204">**PRINTER\_INFO\_5**</span></span>](printer-info-5.md)
</dt> <dt>

[<span data-ttu-id="95d7b-205">**Drucker \_ Info \_ 7**</span><span class="sxs-lookup"><span data-stu-id="95d7b-205">**PRINTER\_INFO\_7**</span></span>](printer-info-7.md)
</dt> <dt>

[<span data-ttu-id="95d7b-206">**Drucker \_ Informationen \_ 8**</span><span class="sxs-lookup"><span data-stu-id="95d7b-206">**PRINTER\_INFO\_8**</span></span>](printer-info-8.md)
</dt> <dt>

[<span data-ttu-id="95d7b-207">**Drucker \_ Informationen \_ 9**</span><span class="sxs-lookup"><span data-stu-id="95d7b-207">**PRINTER\_INFO\_9**</span></span>](printer-info-9.md)
</dt> <dt>

[<span data-ttu-id="95d7b-208">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="95d7b-208">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="95d7b-209">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="95d7b-209">**SetPrinter**</span></span>](setprinter.md)
</dt> </dl>

 

 




