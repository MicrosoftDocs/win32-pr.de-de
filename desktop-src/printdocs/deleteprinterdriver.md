---
description: Die deleteprinterdriver-Funktion entfernt den angegebenen Druckertreiber Namen aus der Liste der Namen unterstützter Treiber auf einem Server.
ms.assetid: b159bd8b-3416-44a5-91bf-c0447ed6b465
title: Deleteprinterdriver-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriver
- DeletePrinterDriverA
- DeletePrinterDriverW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 9e84730be0d20100c2da42aa357f35c08cfb0727
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106363441"
---
# <a name="deleteprinterdriver-function"></a><span data-ttu-id="5052f-103">Deleteprinterdriver-Funktion</span><span class="sxs-lookup"><span data-stu-id="5052f-103">DeletePrinterDriver function</span></span>

<span data-ttu-id="5052f-104">Die **deleteprinterdriver** -Funktion entfernt den angegebenen Druckertreiber Namen aus der Liste der Namen unterstützter Treiber auf einem Server.</span><span class="sxs-lookup"><span data-stu-id="5052f-104">The **DeletePrinterDriver** function removes the specified printer-driver name from the list of names of supported drivers on a server.</span></span>

<span data-ttu-id="5052f-105">Um die dem Treiber zugeordneten Dateien zu löschen und den angegebenen Druckertreiber Namen aus der Liste der Namen unterstützter Treiber für einen Server zu entfernen, verwenden Sie die Funktion [**deleteprinterdriverex**](deleteprinterdriverex.md) .</span><span class="sxs-lookup"><span data-stu-id="5052f-105">To delete the files associated with the driver in addition to removing the specified printer-driver name from the list of names of supported drivers for a server, use the [**DeletePrinterDriverEx**](deleteprinterdriverex.md) function.</span></span>

<span data-ttu-id="5052f-106">**Deleteprinterdriver** löscht einen Treiber nur dann, wenn keine Version des Treibers für die angegebene Umgebung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5052f-106">**DeletePrinterDriver** deletes a driver only if no version of the driver is in use for the specified environment.</span></span> <span data-ttu-id="5052f-107">[**Deleteprinterdriverex**](deleteprinterdriverex.md) kann bestimmte Versionen des Treibers löschen.</span><span class="sxs-lookup"><span data-stu-id="5052f-107">[**DeletePrinterDriverEx**](deleteprinterdriverex.md) can delete specific versions of the driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="5052f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5052f-108">Syntax</span></span>


```C++
BOOL DeletePrinterDriver(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pDriverName
);
```



## <a name="parameters"></a><span data-ttu-id="5052f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5052f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5052f-110">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5052f-110">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5052f-111">Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Servers angibt, von dem der Treiber gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="5052f-111">A pointer to a null-terminated string that specifies the name of the server from which the driver is to be deleted.</span></span> <span data-ttu-id="5052f-112">Wenn dieser Parameter **null** ist, wird der Name des Druckertreibers lokal entfernt.</span><span class="sxs-lookup"><span data-stu-id="5052f-112">If this parameter is **NULL**, the printer-driver name will be removed locally.</span></span>

</dd> <dt>

<span data-ttu-id="5052f-113">nach-oben  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5052f-113">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5052f-114">Ein Zeiger auf eine auf NULL endende Zeichenfolge, die die Umgebung angibt, aus der der Treiber gelöscht werden soll (z. b. Windows x86, Windows ia64 oder Windows x64).</span><span class="sxs-lookup"><span data-stu-id="5052f-114">A pointer to a null-terminated string that specifies the environment from which the driver is to be deleted (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="5052f-115">Wenn dieser Parameter **null** ist, wird der Treiber Name aus der aktuellen Umgebung der aufrufenden Anwendung und des Client Computers (nicht der Zielanwendung und des Druck Servers) gelöscht.</span><span class="sxs-lookup"><span data-stu-id="5052f-115">If this parameter is **NULL**, the driver name is deleted from the current environment of the calling application and client machine (not of the destination application and print server).</span></span>

</dd> <dt>

<span data-ttu-id="5052f-116">*pdrivername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5052f-116">*pDriverName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5052f-117">Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Treibers angibt, der gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="5052f-117">A pointer to a null-terminated string specifying the name of the driver that should be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5052f-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5052f-118">Return value</span></span>

<span data-ttu-id="5052f-119">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="5052f-119">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="5052f-120">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="5052f-120">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5052f-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5052f-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5052f-122">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5052f-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="5052f-123">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="5052f-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="5052f-124">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="5052f-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="5052f-125">Der [Aufrufer muss über die SeLoadDriverPrivilege-Berechtigung](/windows/desktop/SecAuthZ/authorization-constants)verfügen.</span><span class="sxs-lookup"><span data-stu-id="5052f-125">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="5052f-126">Die **deleteprinterdriver** -Funktion löscht die zugeordneten Dateien nicht, sondern entfernt lediglich den Treiber Namen aus der Liste, die von der [**enumprinterdrivers**](enumprinterdrivers.md) -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5052f-126">The **DeletePrinterDriver** function does not delete the associated files, it merely removes the driver name from the list returned by the [**EnumPrinterDrivers**](enumprinterdrivers.md) function.</span></span>

<span data-ttu-id="5052f-127">Vor dem Aufrufen von **deleteprinterdriver** müssen Sie alle Drucker Objekte löschen, die den Druckertreiber verwenden.</span><span class="sxs-lookup"><span data-stu-id="5052f-127">Before calling **DeletePrinterDriver**, you must delete all printer objects that use the printer driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="5052f-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5052f-128">Requirements</span></span>



| <span data-ttu-id="5052f-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5052f-129">Requirement</span></span> | <span data-ttu-id="5052f-130">Wert</span><span class="sxs-lookup"><span data-stu-id="5052f-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5052f-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5052f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5052f-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5052f-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5052f-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5052f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5052f-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5052f-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5052f-135">Header</span><span class="sxs-lookup"><span data-stu-id="5052f-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="5052f-136"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5052f-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="5052f-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5052f-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="5052f-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5052f-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="5052f-139">DLL</span><span class="sxs-lookup"><span data-stu-id="5052f-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5052f-140"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="5052f-140"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="5052f-141">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="5052f-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5052f-142">**Deleteprinterdriverw** (Unicode) und **deleteprinterdrivera** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5052f-142">**DeletePrinterDriverW** (Unicode) and **DeletePrinterDriverA** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="5052f-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5052f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5052f-144">Drucken</span><span class="sxs-lookup"><span data-stu-id="5052f-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="5052f-145">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="5052f-145">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="5052f-146">**Deleteprinterdriverex**</span><span class="sxs-lookup"><span data-stu-id="5052f-146">**DeletePrinterDriverEx**</span></span>](deleteprinterdriverex.md)
</dt> <dt>

[<span data-ttu-id="5052f-147">**Enumprinterdrivers**</span><span class="sxs-lookup"><span data-stu-id="5052f-147">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> </dl>

 

