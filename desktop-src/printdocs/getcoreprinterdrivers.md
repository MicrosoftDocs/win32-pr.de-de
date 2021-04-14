---
description: Ruft die GUID, die Version und das Datum der angegebenen Haupt Druckertreiber und den Pfad zu ihren Paketen ab.
ms.assetid: 98acad48-cd42-4d2b-be58-81c1366f6912
title: Getcoreprinterdrivers-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCorePrinterDrivers
- GetCorePrinterDriversA
- GetCorePrinterDriversW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 5bdebc3f4b716a21c56c9ec756ff56c02765d1a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345288"
---
# <a name="getcoreprinterdrivers-function"></a><span data-ttu-id="e25aa-103">Getcoreprinterdrivers-Funktion</span><span class="sxs-lookup"><span data-stu-id="e25aa-103">GetCorePrinterDrivers function</span></span>

<span data-ttu-id="e25aa-104">Ruft die GUID, die Version und das Datum der angegebenen Haupt Druckertreiber und den Pfad zu ihren Paketen ab.</span><span class="sxs-lookup"><span data-stu-id="e25aa-104">Retrieves GUID, version, and date of the specified core printer drivers and the path to their packages.</span></span>

## <a name="syntax"></a><span data-ttu-id="e25aa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e25aa-105">Syntax</span></span>


```C++
HRESULT GetCorePrinterDrivers(
  _In_  LPCTSTR              pszServer,
  _In_  LPCTSTR              pszEnvironment,
  _In_  LPCTSTR              pszzCoreDriverDependencies,
  _In_  DWORD                cCorePrinterDrivers,
  _Out_ PCORE_PRINTER_DRIVER pCorePrinterDrivers
);
```



## <a name="parameters"></a><span data-ttu-id="e25aa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e25aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e25aa-107">*pszserver* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e25aa-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e25aa-108">Ein Zeiger auf eine Konstante, auf NULL abschließende Zeichenfolge, die den Namen des Drucker Servers angibt.</span><span class="sxs-lookup"><span data-stu-id="e25aa-108">A pointer to a constant, null-terminated string that specifies the name of the print server.</span></span> <span data-ttu-id="e25aa-109">Verwenden Sie für den lokalen Computer **null** .</span><span class="sxs-lookup"><span data-stu-id="e25aa-109">Use **NULL** for the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="e25aa-110">*pszenvironment* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e25aa-110">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e25aa-111">Ein Zeiger auf eine Konstante, auf NULL abschließende Zeichenfolge, die die Prozessorarchitektur angibt (z. b. Windows NT x86).</span><span class="sxs-lookup"><span data-stu-id="e25aa-111">A pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="e25aa-112">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="e25aa-112">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e25aa-113">*pszzcoredriverdependen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e25aa-113">*pszzCoreDriverDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e25aa-114">Ein Zeiger auf eine mit NULL endenden Multizeichenfolge, die die GUIDs der Haupt Druckertreiber angibt.</span><span class="sxs-lookup"><span data-stu-id="e25aa-114">A pointer to a null-terminated multi-string that specifies the GUIDs of the core printer drivers.</span></span>

</dd> <dt>

<span data-ttu-id="e25aa-115">*ccoreprinterdrivers* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e25aa-115">*cCorePrinterDrivers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e25aa-116">Die Anzahl der Zeichen folgen in *pszzcoredriverdependen.*</span><span class="sxs-lookup"><span data-stu-id="e25aa-116">The number of strings in *pszzCoreDriverDependencies*.</span></span>

</dd> <dt>

<span data-ttu-id="e25aa-117">*pcoreprinterdrivers* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e25aa-117">*pCorePrinterDrivers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e25aa-118">Ein Zeiger auf ein Array aus mindestens einer [**Kern \_ Drucker \_ Treiber**](core-printer-driver.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="e25aa-118">A pointer to an array of one or more [**CORE\_PRINTER\_DRIVER**](core-printer-driver.md) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e25aa-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e25aa-119">Return value</span></span>

<span data-ttu-id="e25aa-120">Wenn der Vorgang erfolgreich ist, ist der Rückgabewert S \_ OK; andernfalls enthält das **HRESULT** einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="e25aa-120">If the operation succeeds, the return value is S\_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="e25aa-121">Weitere Informationen zu COM-Fehlercodes finden Sie unter [Fehlerbehandlung](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="e25aa-121">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e25aa-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e25aa-122">Remarks</span></span>

<span data-ttu-id="e25aa-123">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e25aa-123">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="e25aa-124">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="e25aa-124">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="e25aa-125">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="e25aa-125">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

## <a name="requirements"></a><span data-ttu-id="e25aa-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e25aa-126">Requirements</span></span>



| <span data-ttu-id="e25aa-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e25aa-127">Requirement</span></span> | <span data-ttu-id="e25aa-128">Wert</span><span class="sxs-lookup"><span data-stu-id="e25aa-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e25aa-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e25aa-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e25aa-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e25aa-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="e25aa-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e25aa-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e25aa-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e25aa-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e25aa-133">Header</span><span class="sxs-lookup"><span data-stu-id="e25aa-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="e25aa-134"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e25aa-134"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e25aa-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e25aa-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="e25aa-136"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e25aa-136"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="e25aa-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e25aa-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e25aa-138"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e25aa-138"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="e25aa-139">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="e25aa-139">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e25aa-140">**Getcoreprinterdriversw** (Unicode) und **getcoreprinterdriversa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e25aa-140">**GetCorePrinterDriversW** (Unicode) and **GetCorePrinterDriversA** (ANSI)</span></span><br/>                     |



## <a name="see-also"></a><span data-ttu-id="e25aa-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e25aa-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e25aa-142">Drucken</span><span class="sxs-lookup"><span data-stu-id="e25aa-142">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e25aa-143">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="e25aa-143">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

