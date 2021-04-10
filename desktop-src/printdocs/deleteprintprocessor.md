---
description: Die deleteprintprocessor-Funktion entfernt einen von der addprintprocessor-Funktion hinzugefügten Druck Prozessor.
ms.assetid: 65c77874-aa2c-4b4c-b218-fad361270a3e
title: Deleteprintprocessor-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrintProcessor
- DeletePrintProcessorA
- DeletePrintProcessorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 241efaad91e1587209f2ef2a905bc0e095c6b40c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215861"
---
# <a name="deleteprintprocessor-function"></a><span data-ttu-id="865b0-103">Deleteprintprocessor-Funktion</span><span class="sxs-lookup"><span data-stu-id="865b0-103">DeletePrintProcessor function</span></span>

<span data-ttu-id="865b0-104">Die **deleteprintprocessor** -Funktion entfernt einen von der [**addprintprocessor**](addprintprocessor.md) -Funktion hinzugefügten Druck Prozessor.</span><span class="sxs-lookup"><span data-stu-id="865b0-104">The **DeletePrintProcessor** function removes a print processor added by the [**AddPrintProcessor**](addprintprocessor.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="865b0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="865b0-105">Syntax</span></span>


```C++
BOOL DeletePrintProcessor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pPrintProcessorName
);
```



## <a name="parameters"></a><span data-ttu-id="865b0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="865b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="865b0-107">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="865b0-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="865b0-108">Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Servers angibt, von dem der Prozessor entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="865b0-108">A pointer to a null-terminated string that specifies the name of the server from which the processor is to be removed.</span></span> <span data-ttu-id="865b0-109">Wenn dieser Parameter **null** ist, wird der Drucker Prozessor lokal entfernt.</span><span class="sxs-lookup"><span data-stu-id="865b0-109">If this parameter is **NULL**, the printer processor is removed locally.</span></span>

</dd> <dt>

<span data-ttu-id="865b0-110">nach-oben  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="865b0-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="865b0-111">Ein Zeiger auf eine auf NULL endende Zeichenfolge, die die Umgebung angibt, aus der der Prozessor entfernt werden soll (z. b. Windows NT x86, Windows ia64 oder Windows x64).</span><span class="sxs-lookup"><span data-stu-id="865b0-111">A pointer to a null-terminated string that specifies the environment from which the processor is to be removed (for example, Windows NT x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="865b0-112">Wenn dieser Parameter **null** ist, wird der Prozessor aus der aktuellen Umgebung der aufrufenden Anwendung und des Client Computers (nicht der Zielanwendung und des Druck Servers) entfernt.</span><span class="sxs-lookup"><span data-stu-id="865b0-112">If this parameter is **NULL**, the processor is removed from the current environment of the calling application and client machine (not of the destination application and print server).</span></span> <span data-ttu-id="865b0-113">**Null** ist der empfohlene Wert, da er eine maximale Portabilität ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="865b0-113">**NULL** is the recommended value, as it provides maximum portability.</span></span>

</dd> <dt>

<span data-ttu-id="865b0-114">*pprintprocessorname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="865b0-114">*pPrintProcessorName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="865b0-115">Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des zu entfernenden Prozessors angibt.</span><span class="sxs-lookup"><span data-stu-id="865b0-115">A pointer to a null-terminated string that specifies the name of the processor to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="865b0-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="865b0-116">Return value</span></span>

<span data-ttu-id="865b0-117">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="865b0-117">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="865b0-118">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="865b0-118">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="865b0-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="865b0-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="865b0-120">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="865b0-120">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="865b0-121">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="865b0-121">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="865b0-122">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="865b0-122">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="865b0-123">Der [Aufrufer muss über die SeLoadDriverPrivilege-Berechtigung](/windows/desktop/SecAuthZ/authorization-constants)verfügen.</span><span class="sxs-lookup"><span data-stu-id="865b0-123">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

## <a name="requirements"></a><span data-ttu-id="865b0-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="865b0-124">Requirements</span></span>



| <span data-ttu-id="865b0-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="865b0-125">Requirement</span></span> | <span data-ttu-id="865b0-126">Wert</span><span class="sxs-lookup"><span data-stu-id="865b0-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="865b0-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="865b0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="865b0-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="865b0-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="865b0-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="865b0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="865b0-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="865b0-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="865b0-131">Header</span><span class="sxs-lookup"><span data-stu-id="865b0-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="865b0-132"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="865b0-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="865b0-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="865b0-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="865b0-134"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="865b0-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="865b0-135">DLL</span><span class="sxs-lookup"><span data-stu-id="865b0-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="865b0-136"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="865b0-136"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="865b0-137">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="865b0-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="865b0-138">**Deleteprintprocessorw** (Unicode) und **deleteprintprocessora** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="865b0-138">**DeletePrintProcessorW** (Unicode) and **DeletePrintProcessorA** (ANSI)</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="865b0-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="865b0-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="865b0-140">Drucken</span><span class="sxs-lookup"><span data-stu-id="865b0-140">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="865b0-141">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="865b0-141">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="865b0-142">**Addprintprocessor**</span><span class="sxs-lookup"><span data-stu-id="865b0-142">**AddPrintProcessor**</span></span>](addprintprocessor.md)
</dt> </dl>

 

