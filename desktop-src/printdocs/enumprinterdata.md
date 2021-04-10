---
description: Die enumprinterdata-Funktion Listet Konfigurationsdaten für einen angegebenen Drucker auf.
ms.assetid: 0a4c8436-46fe-4e21-8d55-c5031a3d1b38
title: Enumprinterdata-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterData
- EnumPrinterDataA
- EnumPrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: d7c175b0c90853a592e0ff979095d41432c16b38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215855"
---
# <a name="enumprinterdata-function"></a><span data-ttu-id="8c3c4-103">Enumprinterdata-Funktion</span><span class="sxs-lookup"><span data-stu-id="8c3c4-103">EnumPrinterData function</span></span>

<span data-ttu-id="8c3c4-104">Die **enumprinterdata** -Funktion Listet Konfigurationsdaten für einen angegebenen Drucker auf.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-104">The **EnumPrinterData** function enumerates configuration data for a specified printer.</span></span>

<span data-ttu-id="8c3c4-105">Um die Konfigurationsdaten in einem einzelnen-Befehl abzurufen, verwenden Sie die [**enumprinterdataex**](enumprinterdataex.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-105">To retrieve the configuration data in a single call, use the [**EnumPrinterDataEx**](enumprinterdataex.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c3c4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c3c4-106">Syntax</span></span>


```C++
DWORD EnumPrinterData(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   dwIndex,
  _Out_ LPTSTR  pValueName,
  _In_  DWORD   cbValueName,
  _Out_ LPDWORD pcbValueName,
  _Out_ LPDWORD pType,
  _Out_ LPBYTE  pData,
  _In_  DWORD   cbData,
  _Out_ LPDWORD pcbData
);
```



## <a name="parameters"></a><span data-ttu-id="8c3c4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c3c4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c3c4-108">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c3c4-108">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c3c4-109">Ein Handle für den Drucker, dessen Konfigurationsdaten abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-109">A handle to the printer whose configuration data is to be obtained.</span></span> <span data-ttu-id="8c3c4-110">Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-110">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="8c3c4-111">*dwIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c3c4-111">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c3c4-112">Ein Indexwert, der den abzurufenden Konfigurationsdaten Wert angibt.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-112">An index value that specifies the configuration data value to retrieve.</span></span>

<span data-ttu-id="8c3c4-113">Legen Sie diesen Parameter auf 0 (null) für den ersten **enumprinterdata** -Aufrufwert für ein bestimmtes Drucker Handle fest.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-113">Set this parameter to zero for the first call to **EnumPrinterData** for a specified printer handle.</span></span> <span data-ttu-id="8c3c4-114">Erhöhen Sie den Parameter dann um einen für nachfolgende Aufrufe, die denselben Drucker betreffen, bis die Funktion Fehler \_ ohne \_ Weitere Elemente zurückgibt \_ .</span><span class="sxs-lookup"><span data-stu-id="8c3c4-114">Then increment the parameter by one for subsequent calls involving the same printer, until the function returns ERROR\_NO\_MORE\_ITEMS.</span></span> <span data-ttu-id="8c3c4-115">Weitere Informationen finden Sie im folgenden Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="8c3c4-115">See the following Remarks section for further information.</span></span>

<span data-ttu-id="8c3c4-116">Wenn Sie das in den Beschreibungen der Parameter *cbvaluename* und *cbData* erwähnte Verfahren verwenden, um geeignete Puffergrößen Werte zu erhalten, wobei beide Parameter beim ersten **Aufzählen von enumprinterdata** für ein angegebenes Drucker Handle auf 0 (null) festgelegt werden, ist der Wert von *dwIndex* für diesen Befehl nicht von Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-116">If you use the technique mentioned in the descriptions of the *cbValueName* and *cbData* parameters to obtain adequate buffer size values, setting both those parameters to zero in a first call to **EnumPrinterData** for a specified printer handle, the value of *dwIndex* does not matter for that call.</span></span> <span data-ttu-id="8c3c4-117">Legen Sie *dwIndex* beim nächsten Aufzählung von **enumprinterdata** auf NULL fest, um den eigentlichen enumerationsprozess zu starten.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-117">Set *dwIndex* to zero in the next call to **EnumPrinterData** to start the actual enumeration process.</span></span>

<span data-ttu-id="8c3c4-118">Konfigurationsdaten Werte sind nicht geordnet.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-118">Configuration data values are not ordered.</span></span> <span data-ttu-id="8c3c4-119">Neue Werte haben einen beliebigen Index.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-119">New values will have an arbitrary index.</span></span> <span data-ttu-id="8c3c4-120">Dies bedeutet, dass die **enumprinterdata** -Funktion Werte in beliebiger Reihenfolge zurückgeben kann.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-120">This means that the **EnumPrinterData** function may return values in any order.</span></span>

</dd> <dt>

<span data-ttu-id="8c3c4-121">*pvaluename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8c3c4-121">*pValueName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c3c4-122">Ein Zeiger auf einen Puffer, der den Namen des Konfigurationsdaten Werts einschließlich eines abschließenden NULL-Zeichens empfängt.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-122">A pointer to a buffer that receives the name of the configuration data value, including a terminating null character.</span></span>

</dd> <dt>

<span data-ttu-id="8c3c4-123">*cbvaluename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c3c4-123">*cbValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c3c4-124">Die Größe (in Bytes) des Puffers, auf den *pvaluename* zeigt.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-124">The size, in bytes, of the buffer pointed to by *pValueName*.</span></span>

<span data-ttu-id="8c3c4-125">Wenn Sie möchten, dass das Betriebssystem eine angemessene Puffergröße bereitstellt, legen Sie für den ersten **enumprinterdata** -aufzurufenden Parameter sowohl diesen Parameter als auch den *cbData* -Parameter auf 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-125">If you want to have the operating system supply an adequate buffer size, set both this parameter and the *cbData* parameter to zero for the first call to **EnumPrinterData** for a specified printer handle.</span></span> <span data-ttu-id="8c3c4-126">Wenn die Funktion zurückgegeben wird, enthält die Variable, auf die von *pcbvaluename* verwiesen wird, eine Puffergröße, die groß genug ist, um alle Namen von Konfigurationsdaten für den Drucker erfolgreich aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-126">When the function returns, the variable pointed to by *pcbValueName* will contain a buffer size that is large enough to successfully enumerate all of the printer's configuration data value names.</span></span>

</dd> <dt>

<span data-ttu-id="8c3c4-127">*pcbvaluename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8c3c4-127">*pcbValueName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c3c4-128">Ein Zeiger auf eine Variable, die die Anzahl der Bytes empfängt, die im Puffer gespeichert werden, auf die von *pvaluename* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-128">A pointer to a variable that receives the number of bytes stored into the buffer pointed to by *pValueName*.</span></span>

</dd> <dt>

<span data-ttu-id="8c3c4-129">*pType* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8c3c4-129">*pType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c3c4-130">Ein Zeiger auf eine Variable, die einen Code empfängt, der den Typ der im angegebenen Wert gespeicherten Daten angibt.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-130">A pointer to a variable that receives a code indicating the type of data stored in the specified value.</span></span> <span data-ttu-id="8c3c4-131">Eine Liste der möglichen Typcodes finden Sie unter [Registrierungs Werttypen](/windows/desktop/SysInfo/registry-value-types).</span><span class="sxs-lookup"><span data-stu-id="8c3c4-131">For a list of the possible type codes, see [Registry Value Types](/windows/desktop/SysInfo/registry-value-types).</span></span> <span data-ttu-id="8c3c4-132">Der *pType* -Parameter kann **null** sein, wenn der Typcode nicht erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-132">The *pType* parameter can be **NULL** if the type code is not required.</span></span>

</dd> <dt>

<span data-ttu-id="8c3c4-133">*pData* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8c3c4-133">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c3c4-134">Ein Zeiger auf einen Puffer, der den Konfigurationsdaten Wert empfängt.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-134">A pointer to a buffer that receives the configuration data value.</span></span>

<span data-ttu-id="8c3c4-135">Dieser Parameter kann **null** sein, wenn der Wert für die Konfigurationsdaten nicht erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-135">This parameter can be **NULL** if the configuration data value is not required.</span></span>

</dd> <dt>

<span data-ttu-id="8c3c4-136">*cbData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c3c4-136">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c3c4-137">Die Größe (in Bytes) des Puffers, auf den *pData* zeigt.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-137">The size, in bytes, of the buffer pointed to by *pData*.</span></span>

<span data-ttu-id="8c3c4-138">Wenn Sie möchten, dass das Betriebssystem eine angemessene Puffergröße bereitstellt, legen Sie für den ersten **enumprinterdata** -aufzurufenden Parameter sowohl diesen Parameter als auch den *cbvaluename* -Parameter auf 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-138">If you want to have the operating system supply an adequate buffer size, set both this parameter and the *cbValueName* parameter to zero for the first call to **EnumPrinterData** for a specified printer handle.</span></span> <span data-ttu-id="8c3c4-139">Wenn die Funktion zurückgegeben wird, enthält die Variable, auf die von *pcbData* verwiesen wird, eine Puffergröße, die groß genug ist, um alle Namen von Konfigurationsdaten für den Drucker erfolgreich aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-139">When the function returns, the variable pointed to by *pcbData* will contain a buffer size that is large enough to successfully enumerate all of the printer's configuration data value names.</span></span>

</dd> <dt>

<span data-ttu-id="8c3c4-140">*pcbData* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8c3c4-140">*pcbData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c3c4-141">Ein Zeiger auf eine Variable, die die Anzahl der Bytes empfängt, die im Puffer gespeichert werden, auf die *pData* verweist.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-141">A pointer to a variable that receives the number of bytes stored into the buffer pointed to by *pData*.</span></span>

<span data-ttu-id="8c3c4-142">Dieser Parameter kann **null** sein, wenn *pData* **null** ist.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-142">This parameter can be **NULL** if *pData* is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c3c4-143">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8c3c4-143">Return value</span></span>

<span data-ttu-id="8c3c4-144">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-144">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="8c3c4-145">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Systemfehler Code.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-145">If the function fails, the return value is a system error code.</span></span>

<span data-ttu-id="8c3c4-146">Die Funktion gibt \_ einen Fehler ohne \_ Weitere Elemente zurück \_ , wenn keine weiteren Konfigurationsdaten Werte für ein angegebenes Drucker handle vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-146">The function returns ERROR\_NO\_MORE\_ITEMS when there are no more configuration data values to retrieve for a specified printer handle.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c3c4-147">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8c3c4-147">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8c3c4-148">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-148">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="8c3c4-149">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-149">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="8c3c4-150">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-150">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="8c3c4-151">**Enumprinterdata** Ruft das von der [**setprinterdata**](setprinterdata.md) -Funktion festgelegte Drucker Konfigurations DataSet ab.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-151">**EnumPrinterData** retrieves printer configuration data set by the [**SetPrinterData**](setprinterdata.md) function.</span></span> <span data-ttu-id="8c3c4-152">Die Konfigurationsdaten eines Druckers bestehen aus einem Satz von benannten und typisierten Werten.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-152">A printer's configuration data consists of a set of named and typed values.</span></span> <span data-ttu-id="8c3c4-153">Die **enumprinterdata** -Funktion Ruft bei jedem Aufruf einen dieser Werte und ihren Namen sowie einen Typcode ab.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-153">The **EnumPrinterData** function obtains one of these values, and its name and a type code, each time you call it.</span></span> <span data-ttu-id="8c3c4-154">Rufen Sie die **enumprinterdata** -Funktion mehrmals nacheinander auf, um alle Konfigurationsdaten Werte eines Druckers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-154">Call the **EnumPrinterData** function several times in succession to obtain all of a printer's configuration data values.</span></span>

<span data-ttu-id="8c3c4-155">Die Drucker Konfigurationsdaten werden in der Registrierung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-155">Printer configuration data is stored in the registry.</span></span> <span data-ttu-id="8c3c4-156">Beim Auflisten von Drucker Konfigurationsdaten sollten Sie keine Registrierungsfunktionen aufrufen, die diese Daten möglicherweise ändern.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-156">While enumerating printer configuration data, you should avoid calling registry functions that might change that data.</span></span>

<span data-ttu-id="8c3c4-157">Wenn Sie möchten, dass das Betriebssystem eine angemessene Puffergröße bereitstellt, müssen Sie zuerst **enumprinterdata** mit den Parametern *cbvaluename* und *cbData* auf NULL festlegen, wie zuvor im Abschnitt Parameters angegeben.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-157">If you want to have the operating system supply an adequate buffer size, first call **EnumPrinterData** with both the *cbValueName* and *cbData* parameters set to zero, as noted earlier in the Parameters section.</span></span> <span data-ttu-id="8c3c4-158">Der Wert von *dwIndex* ist für diesen-Befehl nicht von Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-158">The value of *dwIndex* does not matter for this call.</span></span> <span data-ttu-id="8c3c4-159">Wenn die Funktion zurückgegeben \* wird, enthalten *pcbvaluename* und \* *pcbData* Puffergrößen, die groß genug sind, um alle Namen und Werte der Konfigurationsdaten des Drucker aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-159">When the function returns, \**pcbValueName* and \**pcbData* will contain buffer sizes that are large enough to enumerate all of the printer's configuration data value names and values.</span></span> <span data-ttu-id="8c3c4-160">Beim nächsten-Befehl werden Werte Name und Datenpuffer zugewiesen, *cbvaluename* und *cbData* auf die Größen in Bytes der zugeordneten Puffer festgelegt, und *dwIndex* wird auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-160">On the next call, allocate value name and data buffers, set *cbValueName* and *cbData* to the sizes in bytes of the allocated buffers, and set *dwIndex* to zero.</span></span> <span data-ttu-id="8c3c4-161">Setzen Sie anschließend die **enumprinterdata** -Funktion fort, und erhöhen Sie *dwIndex* jedes Mal um 1, bis die Funktion Fehler \_ ohne \_ Weitere \_ Elemente zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="8c3c4-161">Thereafter, continue to call the **EnumPrinterData** function, incrementing *dwIndex* by one each time, until the function returns ERROR\_NO\_MORE\_ITEMS.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c3c4-162">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c3c4-162">Requirements</span></span>



| <span data-ttu-id="8c3c4-163">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8c3c4-163">Requirement</span></span> | <span data-ttu-id="8c3c4-164">Wert</span><span class="sxs-lookup"><span data-stu-id="8c3c4-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c3c4-165">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8c3c4-165">Minimum supported client</span></span><br/> | <span data-ttu-id="8c3c4-166">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8c3c4-166">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8c3c4-167">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8c3c4-167">Minimum supported server</span></span><br/> | <span data-ttu-id="8c3c4-168">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8c3c4-168">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8c3c4-169">Header</span><span class="sxs-lookup"><span data-stu-id="8c3c4-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c3c4-170"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8c3c4-170"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="8c3c4-171">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8c3c4-171">Library</span></span><br/>                  | <dl> <span data-ttu-id="8c3c4-172"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c3c4-172"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="8c3c4-173">DLL</span><span class="sxs-lookup"><span data-stu-id="8c3c4-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c3c4-174"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="8c3c4-174"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="8c3c4-175">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="8c3c4-175">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8c3c4-176">**Enumprinterdataw** (Unicode) und **enumprinterdataa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8c3c4-176">**EnumPrinterDataW** (Unicode) and **EnumPrinterDataA** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="8c3c4-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c3c4-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c3c4-178">Drucken</span><span class="sxs-lookup"><span data-stu-id="8c3c4-178">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="8c3c4-179">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="8c3c4-179">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="8c3c4-180">**Deleteprinterdata**</span><span class="sxs-lookup"><span data-stu-id="8c3c4-180">**DeletePrinterData**</span></span>](deleteprinterdata.md)
</dt> <dt>

[<span data-ttu-id="8c3c4-181">**Enumprinterdataex**</span><span class="sxs-lookup"><span data-stu-id="8c3c4-181">**EnumPrinterDataEx**</span></span>](enumprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="8c3c4-182">**Getprinterdata**</span><span class="sxs-lookup"><span data-stu-id="8c3c4-182">**GetPrinterData**</span></span>](getprinterdata.md)
</dt> <dt>

[<span data-ttu-id="8c3c4-183">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="8c3c4-183">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="8c3c4-184">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="8c3c4-184">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="8c3c4-185">**Setprinterdata**</span><span class="sxs-lookup"><span data-stu-id="8c3c4-185">**SetPrinterData**</span></span>](setprinterdata.md)
</dt> </dl>

 

