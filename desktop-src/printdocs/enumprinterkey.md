---
description: Die enumprinterkey-Funktion Listet die Unterschlüssel eines angegebenen Schlüssels für einen angegebenen Drucker auf.
ms.assetid: 721b1d23-a594-4439-b8f9-9b11be5fe874
title: Enumprinterkey-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterKey
- EnumPrinterKeyA
- EnumPrinterKeyW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: d9af6a9ef26612385cee68eba9733c148cd36b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347498"
---
# <a name="enumprinterkey-function"></a><span data-ttu-id="f39d2-103">Enumprinterkey-Funktion</span><span class="sxs-lookup"><span data-stu-id="f39d2-103">EnumPrinterKey function</span></span>

<span data-ttu-id="f39d2-104">Die **enumprinterkey** -Funktion Listet die Unterschlüssel eines angegebenen Schlüssels für einen angegebenen Drucker auf.</span><span class="sxs-lookup"><span data-stu-id="f39d2-104">The **EnumPrinterKey** function enumerates the subkeys of a specified key for a specified printer.</span></span>

<span data-ttu-id="f39d2-105">Druckerdaten werden in der Registrierung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f39d2-105">Printer data is stored in the registry.</span></span> <span data-ttu-id="f39d2-106">Wenn Sie Druckerdaten auflisten, dürfen Sie keine Registrierungsfunktionen aufzurufen, die die Daten möglicherweise ändern.</span><span class="sxs-lookup"><span data-stu-id="f39d2-106">While enumerating printer data, do not call registry functions that might change the data.</span></span>

## <a name="syntax"></a><span data-ttu-id="f39d2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f39d2-107">Syntax</span></span>


```C++
DWORD EnumPrinterKey(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _Out_ LPTSTR  pSubkey,
  _In_  DWORD   cbSubkey,
  _Out_ LPDWORD pcbSubkey
);
```



## <a name="parameters"></a><span data-ttu-id="f39d2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f39d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f39d2-109">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f39d2-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f39d2-110">Ein Handle für den Drucker, für den die-Funktion Unterschlüssel auflistet.</span><span class="sxs-lookup"><span data-stu-id="f39d2-110">A handle to the printer for which the function enumerates subkeys.</span></span> <span data-ttu-id="f39d2-111">Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.</span><span class="sxs-lookup"><span data-stu-id="f39d2-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="f39d2-112">*pkeyname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f39d2-112">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f39d2-113">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Schlüssel mit den unter Schlüsseln angibt, die aufgelistet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f39d2-113">A pointer to a null-terminated string that specifies the key containing the subkeys to enumerate.</span></span> <span data-ttu-id="f39d2-114">Verwenden Sie den umgekehrten Schrägstrich ' \\ ' als Trennzeichen, um einen Pfad mit einem oder mehreren unter Schlüsseln anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f39d2-114">Use the backslash '\\' character as a delimiter to specify a path with one or more subkeys.</span></span> <span data-ttu-id="f39d2-115">**Enumprinterkey** listet alle Unterschlüssel des Schlüssels auf, listet aber nicht die untergeordneten Schlüssel dieser Unterschlüssel auf.</span><span class="sxs-lookup"><span data-stu-id="f39d2-115">**EnumPrinterKey** enumerates all subkeys of the key, but does not enumerate the subkeys of those subkeys.</span></span>

<span data-ttu-id="f39d2-116">Wenn " *pkeyname* " eine leere Zeichenfolge ("") ist, listet " **enumprinterkey** " den Schlüssel der obersten Ebene für den Drucker auf.</span><span class="sxs-lookup"><span data-stu-id="f39d2-116">If *pKeyName* is an empty string (""), **EnumPrinterKey** enumerates the top-level key for the printer.</span></span> <span data-ttu-id="f39d2-117">Wenn *pkeyname* **null** ist, gibt **enumprinterkey** einen \_ ungültigen \_ Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="f39d2-117">If *pKeyName* is **NULL**, **EnumPrinterKey** returns ERROR\_INVALID\_PARAMETER.</span></span>

</dd> <dt>

<span data-ttu-id="f39d2-118">*psubkey* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f39d2-118">*pSubkey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f39d2-119">Ein Zeiger auf einen Puffer, der ein Array von auf NULL endenden Unterschlüssel Namen empfängt.</span><span class="sxs-lookup"><span data-stu-id="f39d2-119">A pointer to a buffer that receives an array of null-terminated subkey names.</span></span> <span data-ttu-id="f39d2-120">Das Array wird mit zwei NULL-Zeichen beendet.</span><span class="sxs-lookup"><span data-stu-id="f39d2-120">The array is terminated by two null characters.</span></span>

</dd> <dt>

<span data-ttu-id="f39d2-121">*cbsubkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f39d2-121">*cbSubkey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f39d2-122">Die Größe (in Bytes) des Puffers, auf den *psubkey* zeigt.</span><span class="sxs-lookup"><span data-stu-id="f39d2-122">The size, in bytes, of the buffer pointed to by *pSubkey*.</span></span> <span data-ttu-id="f39d2-123">Wenn Sie *cbsubkey* auf NULL festlegen, gibt der *pcbsubkey* -Parameter die erforderliche Puffergröße zurück.</span><span class="sxs-lookup"><span data-stu-id="f39d2-123">If you set *cbSubkey* to zero, the *pcbSubkey* parameter returns the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="f39d2-124">*pcbsubkey* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f39d2-124">*pcbSubkey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f39d2-125">Ein Zeiger auf eine Variable, die die Anzahl von Bytes empfängt, die im *psubkey* -Puffer abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="f39d2-125">A pointer to a variable that receives the number of bytes retrieved in the *pSubkey* buffer.</span></span> <span data-ttu-id="f39d2-126">Wenn die von *cbsubkey* angegebene Puffergröße zu klein ist, gibt die Funktion Fehler \_ Weitere \_ Daten zurück, und *pcbsubkey* gibt die erforderliche Puffergröße an.</span><span class="sxs-lookup"><span data-stu-id="f39d2-126">If the buffer size specified by *cbSubkey* is too small, the function returns ERROR\_MORE\_DATA and *pcbSubkey* indicates the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f39d2-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f39d2-127">Return value</span></span>

<span data-ttu-id="f39d2-128">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f39d2-128">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="f39d2-129">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Systemfehler Code.</span><span class="sxs-lookup"><span data-stu-id="f39d2-129">If the function fails, the return value is a system error code.</span></span> <span data-ttu-id="f39d2-130">Wenn " *pkeyname* " nicht vorhanden ist, lautet der Rückgabewert "Fehler \_ Datei \_ nicht \_ gefunden".</span><span class="sxs-lookup"><span data-stu-id="f39d2-130">If *pKeyName* does not exist, the return value is ERROR\_FILE\_NOT\_FOUND.</span></span>

## <a name="remarks"></a><span data-ttu-id="f39d2-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f39d2-131">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f39d2-132">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f39d2-132">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="f39d2-133">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="f39d2-133">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="f39d2-134">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="f39d2-134">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f39d2-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f39d2-135">Requirements</span></span>



| <span data-ttu-id="f39d2-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f39d2-136">Requirement</span></span> | <span data-ttu-id="f39d2-137">Wert</span><span class="sxs-lookup"><span data-stu-id="f39d2-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f39d2-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f39d2-138">Minimum supported client</span></span><br/> | <span data-ttu-id="f39d2-139">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f39d2-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f39d2-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f39d2-140">Minimum supported server</span></span><br/> | <span data-ttu-id="f39d2-141">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f39d2-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f39d2-142">Header</span><span class="sxs-lookup"><span data-stu-id="f39d2-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="f39d2-143"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f39d2-143"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f39d2-144">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f39d2-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="f39d2-145"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f39d2-145"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="f39d2-146">DLL</span><span class="sxs-lookup"><span data-stu-id="f39d2-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f39d2-147"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="f39d2-147"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="f39d2-148">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="f39d2-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f39d2-149">**Enumprinterkeyw** (Unicode) und **enumprinterkeya** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f39d2-149">**EnumPrinterKeyW** (Unicode) and **EnumPrinterKeyA** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="f39d2-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f39d2-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f39d2-151">Drucken</span><span class="sxs-lookup"><span data-stu-id="f39d2-151">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f39d2-152">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="f39d2-152">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="f39d2-153">**Deleteprinterdataex**</span><span class="sxs-lookup"><span data-stu-id="f39d2-153">**DeletePrinterDataEx**</span></span>](deleteprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="f39d2-154">**Getprinterdataex**</span><span class="sxs-lookup"><span data-stu-id="f39d2-154">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="f39d2-155">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="f39d2-155">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="f39d2-156">**Setprinterdataex**</span><span class="sxs-lookup"><span data-stu-id="f39d2-156">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

 




