---
description: Die addprintprocessor-Funktion installiert einen Druck Prozessor auf dem angegebenen Server und fügt der Liste der unterstützten Druck Prozessoren den Druck Prozessor Namen hinzu.
ms.assetid: 99899cee-f74d-4405-8ea5-616e3769aba9
title: Addprintprocessor-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrintProcessor
- AddPrintProcessorA
- AddPrintProcessorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 871df9fee211ae13e1552978ce651840d7f542f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351492"
---
# <a name="addprintprocessor-function"></a><span data-ttu-id="70b49-103">Addprintprocessor-Funktion</span><span class="sxs-lookup"><span data-stu-id="70b49-103">AddPrintProcessor function</span></span>

<span data-ttu-id="70b49-104">Die **addprintprocessor** -Funktion installiert einen Druck Prozessor auf dem angegebenen Server und fügt der Liste der unterstützten Druck Prozessoren den Druck Prozessor Namen hinzu.</span><span class="sxs-lookup"><span data-stu-id="70b49-104">The **AddPrintProcessor** function installs a print processor on the specified server and adds the print-processor name to the list of supported print processors.</span></span>

## <a name="syntax"></a><span data-ttu-id="70b49-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="70b49-105">Syntax</span></span>


```C++
BOOL AddPrintProcessor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pPathName,
  _In_ LPTSTR pPrintProcessorName
);
```



## <a name="parameters"></a><span data-ttu-id="70b49-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="70b49-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70b49-107">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="70b49-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70b49-108">Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Servers angibt, auf dem der Druck Prozessor installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="70b49-108">A pointer to a null-terminated string that specifies the name of the server on which the print processor should be installed.</span></span> <span data-ttu-id="70b49-109">Wenn dieser Parameter **null** ist, wird der Druck Prozessor lokal installiert.</span><span class="sxs-lookup"><span data-stu-id="70b49-109">If this parameter is **NULL**, the print processor is installed locally.</span></span>

</dd> <dt>

<span data-ttu-id="70b49-110">nach-oben  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="70b49-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70b49-111">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die Umgebung angibt (z. b. Windows x86, Windows ia64 oder Windows x64).</span><span class="sxs-lookup"><span data-stu-id="70b49-111">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="70b49-112">Wenn dieser Parameter **null** ist, wird die aktuelle Umgebung des Aufrufers/Clients (nicht des Ziels/Servers) verwendet.</span><span class="sxs-lookup"><span data-stu-id="70b49-112">If this parameter is **NULL**, the current environment of the caller/client (not of the destination/server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="70b49-113">*ppathname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="70b49-113">*pPathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70b49-114">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen der Datei angibt, die den Druck Prozessor enthält.</span><span class="sxs-lookup"><span data-stu-id="70b49-114">A pointer to a null-terminated string that specifies the name of the file that contains the print processor.</span></span> <span data-ttu-id="70b49-115">Diese Datei muss sich im Systemdruck Prozessor Verzeichnis befinden.</span><span class="sxs-lookup"><span data-stu-id="70b49-115">This file must be in the system print-processor directory.</span></span>

</dd> <dt>

<span data-ttu-id="70b49-116">*pprintprocessorname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="70b49-116">*pPrintProcessorName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70b49-117">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Druck Prozessors angibt.</span><span class="sxs-lookup"><span data-stu-id="70b49-117">A pointer to a null-terminated string that specifies the name of the print processor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70b49-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="70b49-118">Return value</span></span>

<span data-ttu-id="70b49-119">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="70b49-119">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="70b49-120">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="70b49-120">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="70b49-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="70b49-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="70b49-122">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="70b49-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="70b49-123">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="70b49-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="70b49-124">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="70b49-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="70b49-125">Der [Aufrufer muss über die SeLoadDriverPrivilege-Berechtigung](/windows/desktop/SecAuthZ/authorization-constants)verfügen.</span><span class="sxs-lookup"><span data-stu-id="70b49-125">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="70b49-126">Vor dem Aufrufen der **addprintprocessor** -Funktion muss eine Anwendung überprüfen, ob die Datei, in der der Druck Prozessor enthalten ist, im Systemdruck Prozessor Verzeichnis gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="70b49-126">Before calling the **AddPrintProcessor** function, an application should verify that the file containing the print processor is stored in the system print-processor directory.</span></span> <span data-ttu-id="70b49-127">Eine Anwendung kann den Namen des Systemdruck Prozessor-Verzeichnisses abrufen, indem Sie die [**getprintprocessordirectory**](getprintprocessordirectory.md) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="70b49-127">An application can retrieve the name of the system print-processor directory by calling the [**GetPrintProcessorDirectory**](getprintprocessordirectory.md) function.</span></span>

<span data-ttu-id="70b49-128">Eine Anwendung kann den Namen vorhandener Druck Prozessoren ermitteln, indem die [**enumprintprocessor**](enumprintprocessors.md) -Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="70b49-128">An application can determine the name of existing print processors by calling the [**EnumPrintProcessors**](enumprintprocessors.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="70b49-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="70b49-129">Requirements</span></span>



| <span data-ttu-id="70b49-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="70b49-130">Requirement</span></span> | <span data-ttu-id="70b49-131">Wert</span><span class="sxs-lookup"><span data-stu-id="70b49-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70b49-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="70b49-132">Minimum supported client</span></span><br/> | <span data-ttu-id="70b49-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="70b49-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="70b49-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="70b49-134">Minimum supported server</span></span><br/> | <span data-ttu-id="70b49-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="70b49-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="70b49-136">Header</span><span class="sxs-lookup"><span data-stu-id="70b49-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="70b49-137"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="70b49-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="70b49-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="70b49-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="70b49-139"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70b49-139"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="70b49-140">DLL</span><span class="sxs-lookup"><span data-stu-id="70b49-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70b49-141"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="70b49-141"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="70b49-142">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="70b49-142">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="70b49-143">**Addprintprocessorw** (Unicode) und **addprintprocessora** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="70b49-143">**AddPrintProcessorW** (Unicode) and **AddPrintProcessorA** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="70b49-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70b49-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70b49-145">Drucken</span><span class="sxs-lookup"><span data-stu-id="70b49-145">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="70b49-146">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="70b49-146">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="70b49-147">**Enumprintprozessoren**</span><span class="sxs-lookup"><span data-stu-id="70b49-147">**EnumPrintProcessors**</span></span>](enumprintprocessors.md)
</dt> <dt>

[<span data-ttu-id="70b49-148">**Getprintprocessordirectory**</span><span class="sxs-lookup"><span data-stu-id="70b49-148">**GetPrintProcessorDirectory**</span></span>](getprintprocessordirectory.md)
</dt> </dl>

 

