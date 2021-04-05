---
description: Die enumprinterdataex-Funktion Listet alle Wertnamen und-Daten für einen angegebenen Drucker und Schlüssel auf.
ms.assetid: bc5ecc46-24a4-4b54-9431-0eaf6446e2d6
title: Enumprinterdataex-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterDataEx
- EnumPrinterDataExA
- EnumPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 517d480d1c831627cadb289c41f99d24b1025ef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757854"
---
# <a name="enumprinterdataex-function"></a><span data-ttu-id="9b958-103">Enumprinterdataex-Funktion</span><span class="sxs-lookup"><span data-stu-id="9b958-103">EnumPrinterDataEx function</span></span>

<span data-ttu-id="9b958-104">Die **enumprinterdataex** -Funktion Listet alle Wertnamen und-Daten für einen angegebenen Drucker und Schlüssel auf.</span><span class="sxs-lookup"><span data-stu-id="9b958-104">The **EnumPrinterDataEx** function enumerates all value names and data for a specified printer and key.</span></span>

<span data-ttu-id="9b958-105">Druckerdaten werden in der Registrierung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9b958-105">Printer data is stored in the registry.</span></span> <span data-ttu-id="9b958-106">Wenn Sie Druckerdaten auflisten, dürfen Sie keine Registrierungsfunktionen aufzurufen, die die Daten möglicherweise ändern.</span><span class="sxs-lookup"><span data-stu-id="9b958-106">While enumerating printer data, do not call registry functions that might change the data.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b958-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b958-107">Syntax</span></span>


```C++
DWORD EnumPrinterDataEx(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _Out_ LPBYTE  pEnumValues,
  _In_  DWORD   cbEnumValues,
  _Out_ LPDWORD pcbEnumValues,
  _Out_ LPDWORD pnEnumValues
);
```



## <a name="parameters"></a><span data-ttu-id="9b958-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b958-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b958-109">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b958-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b958-110">Ein Handle für den Drucker, für den die Funktion Konfigurationsdaten abruft.</span><span class="sxs-lookup"><span data-stu-id="9b958-110">A handle to the printer for which the function retrieves configuration data.</span></span> <span data-ttu-id="9b958-111">Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.</span><span class="sxs-lookup"><span data-stu-id="9b958-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="9b958-112">*pkeyname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b958-112">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b958-113">Ein Zeiger auf eine mit NULL endenden Zeichenfolge, die den Schlüssel angibt, der die aufzuzählenden Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="9b958-113">A pointer to a null-terminated string that specifies the key containing the values to enumerate.</span></span> <span data-ttu-id="9b958-114">Verwenden Sie den umgekehrten Schrägstrich ( \\ ) als Trennzeichen, um einen Pfad mit einem oder mehreren unter Schlüsseln anzugeben.</span><span class="sxs-lookup"><span data-stu-id="9b958-114">Use the backslash ( \\ ) character as a delimiter to specify a path with one or more subkeys.</span></span> <span data-ttu-id="9b958-115">**Enumprinterdataex** listet alle Werte des Schlüssels auf, listet jedoch keine Werte der untergeordneten Schlüssel des angegebenen Schlüssels auf.</span><span class="sxs-lookup"><span data-stu-id="9b958-115">**EnumPrinterDataEx** enumerates all values of the key, but does not enumerate values of subkeys of the specified key.</span></span> <span data-ttu-id="9b958-116">Verwenden Sie die [**enumprinterkey**](enumprinterkey.md) -Funktion, um Unterschlüssel aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="9b958-116">Use the [**EnumPrinterKey**](enumprinterkey.md) function to enumerate subkeys.</span></span>

<span data-ttu-id="9b958-117">Wenn *pkeyname* **null** oder eine leere Zeichenfolge ist, gibt **enumprinterdataex** einen \_ ungültigen \_ Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="9b958-117">If *pKeyName* is **NULL** or an empty string, **EnumPrinterDataEx** returns ERROR\_INVALID\_PARAMETER.</span></span>

</dd> <dt>

<span data-ttu-id="9b958-118">" *Pum Values* \[ " vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9b958-118">*pEnumValues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b958-119">Ein Zeiger auf einen Puffer, der ein Array von [**druckerenumerationswert \_ \_**](printer-enum-values.md) -Strukturen empfängt.</span><span class="sxs-lookup"><span data-stu-id="9b958-119">A pointer to a buffer that receives an array of [**PRINTER\_ENUM\_VALUES**](printer-enum-values.md) structures.</span></span> <span data-ttu-id="9b958-120">Jede Struktur enthält den Wertnamen, den Typ, die Daten und die Größe eines Werts unter dem Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="9b958-120">Each structure contains the value name, type, data, and sizes of a value under the key.</span></span>

</dd> <dt>

<span data-ttu-id="9b958-121">*cbenumschlag-Werte* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b958-121">*cbEnumValues* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b958-122">Die Größe (in Bytes) des Puffers, auf den *pcbenumschlag Values* zeigt.</span><span class="sxs-lookup"><span data-stu-id="9b958-122">The size, in bytes, of the buffer pointed to by *pcbEnumValues*.</span></span> <span data-ttu-id="9b958-123">Wenn Sie " *cbenenumvalues* " auf NULL festlegen, gibt der Parameter " *pcbenumschlag Values* " die erforderliche Puffergröße zurück.</span><span class="sxs-lookup"><span data-stu-id="9b958-123">If you set *cbEnumValues* to zero, the *pcbEnumValues* parameter returns the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="9b958-124">*pcbenumschlag Values* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9b958-124">*pcbEnumValues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b958-125">Ein Zeiger auf eine Variable, die die Größe der abgerufenen Konfigurationsdaten in Bytes empfängt.</span><span class="sxs-lookup"><span data-stu-id="9b958-125">A pointer to a variable that receives the size, in bytes, of the retrieved configuration data.</span></span> <span data-ttu-id="9b958-126">Wenn die von *cbenumschlag Values* angegebene Puffergröße zu klein ist, gibt die Funktion Fehler \_ Weitere \_ Daten zurück, und *pcbenumschlag Values* gibt die erforderliche Puffergröße an.</span><span class="sxs-lookup"><span data-stu-id="9b958-126">If the buffer size specified by *cbEnumValues* is too small, the function returns ERROR\_MORE\_DATA and *pcbEnumValues* indicates the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="9b958-127">*pnenumvalues* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9b958-127">*pnEnumValues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b958-128">Ein Zeiger auf eine Variable, die die Anzahl der in " *pumvalues*" zurückgegebenen Strukturen der [**druckerenumerationswerte \_ \_**](printer-enum-values.md) empfängt.</span><span class="sxs-lookup"><span data-stu-id="9b958-128">A pointer to a variable that receives the number of [**PRINTER\_ENUM\_VALUES**](printer-enum-values.md) structures returned in *pEnumValues*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b958-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9b958-129">Return value</span></span>

<span data-ttu-id="9b958-130">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="9b958-130">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="9b958-131">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Systemfehler Code.</span><span class="sxs-lookup"><span data-stu-id="9b958-131">If the function fails, the return value is a system error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b958-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b958-132">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9b958-133">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9b958-133">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="9b958-134">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="9b958-134">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="9b958-135">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="9b958-135">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="9b958-136">**Enumprinterdataex** Ruft die Drucker Konfigurationsdaten ab, die von den Funktionen [**setprinterdataex**](setprinterdataex.md) und [**setprinterdata**](setprinterdata.md) festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="9b958-136">**EnumPrinterDataEx** retrieves printer configuration data set by the [**SetPrinterDataEx**](setprinterdataex.md) and [**SetPrinterData**](setprinterdata.md) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b958-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9b958-137">Requirements</span></span>



| <span data-ttu-id="9b958-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9b958-138">Requirement</span></span> | <span data-ttu-id="9b958-139">Wert</span><span class="sxs-lookup"><span data-stu-id="9b958-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b958-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9b958-140">Minimum supported client</span></span><br/> | <span data-ttu-id="9b958-141">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9b958-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9b958-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9b958-142">Minimum supported server</span></span><br/> | <span data-ttu-id="9b958-143">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9b958-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9b958-144">Header</span><span class="sxs-lookup"><span data-stu-id="9b958-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b958-145"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9b958-145"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="9b958-146">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9b958-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="9b958-147"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b958-147"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="9b958-148">DLL</span><span class="sxs-lookup"><span data-stu-id="9b958-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b958-149"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="9b958-149"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="9b958-150">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="9b958-150">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9b958-151">**Enumprinterdataexw** (Unicode) und **enumprinterdataexa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9b958-151">**EnumPrinterDataExW** (Unicode) and **EnumPrinterDataExA** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="9b958-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b958-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b958-153">Drucken</span><span class="sxs-lookup"><span data-stu-id="9b958-153">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="9b958-154">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="9b958-154">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="9b958-155">**Deleteprinterdataex**</span><span class="sxs-lookup"><span data-stu-id="9b958-155">**DeletePrinterDataEx**</span></span>](deleteprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="9b958-156">**Enumprinterkey**</span><span class="sxs-lookup"><span data-stu-id="9b958-156">**EnumPrinterKey**</span></span>](enumprinterkey.md)
</dt> <dt>

[<span data-ttu-id="9b958-157">**Getprinterdataex**</span><span class="sxs-lookup"><span data-stu-id="9b958-157">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="9b958-158">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="9b958-158">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="9b958-159">**druckerenumerationswerte \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9b958-159">**PRINTER\_ENUM\_VALUES**</span></span>](printer-enum-values.md)
</dt> <dt>

[<span data-ttu-id="9b958-160">**Setprinterdata**</span><span class="sxs-lookup"><span data-stu-id="9b958-160">**SetPrinterData**</span></span>](setprinterdata.md)
</dt> <dt>

[<span data-ttu-id="9b958-161">**Setprinterdataex**</span><span class="sxs-lookup"><span data-stu-id="9b958-161">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

 




