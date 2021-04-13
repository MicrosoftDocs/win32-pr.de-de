---
description: Die deleteprintprovidor-Funktion entfernt einen von der addprintprovidor-Funktion hinzugefügten Druckanbieter.
ms.assetid: b7104f9a-111c-4904-a355-063bb4cc81f1
title: Deleteprintprovidor-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrintProvidor
- DeletePrintProvidorA
- DeletePrintProvidorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: e68e56f115bac8abb1d0999990f57067f791d76d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216872"
---
# <a name="deleteprintprovidor-function"></a><span data-ttu-id="ac4eb-103">Deleteprintprovidor-Funktion</span><span class="sxs-lookup"><span data-stu-id="ac4eb-103">DeletePrintProvidor function</span></span>

<span data-ttu-id="ac4eb-104">Die **deleteprintprovidor** -Funktion entfernt einen von der [**addprintprovidor**](addprintprovidor.md) -Funktion hinzugefügten Druckanbieter.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-104">The **DeletePrintProvidor** function removes a print provider added by the [**AddPrintProvidor**](addprintprovidor.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac4eb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac4eb-105">Syntax</span></span>


```C++
BOOL DeletePrintProvidor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pPrintProviderName
);
```



## <a name="parameters"></a><span data-ttu-id="ac4eb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac4eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac4eb-107">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac4eb-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac4eb-108">Bleiben muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-108">Reserved; must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ac4eb-109">nach-oben  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac4eb-109">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac4eb-110">Ein Zeiger auf eine auf NULL endende Zeichenfolge, die die Umgebung angibt, aus der der Anbieter entfernt werden soll (z. b. Windows NT x86, Windows ia64 oder Windows x64).</span><span class="sxs-lookup"><span data-stu-id="ac4eb-110">A pointer to a null-terminated string that specifies the environment from which the provider is to be removed (for example, Windows NT x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="ac4eb-111">Wenn dieser Parameter **null** ist, wird der Anbieter aus der aktuellen Umgebung der aufrufenden Anwendung und des Client Computers (nicht der Zielanwendung und des Druck Servers) entfernt.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-111">If this parameter is **NULL**, the provider is removed from the current environment of the calling application and client machine (not of the destination application and print server).</span></span> <span data-ttu-id="ac4eb-112">**Null** ist der empfohlene Wert, da er eine maximale Portabilität ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-112">**NULL** is the recommended value because it provides maximum portability.</span></span>

</dd> <dt>

<span data-ttu-id="ac4eb-113">*pprintprovidername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac4eb-113">*pPrintProviderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac4eb-114">Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des zu entfernenden Anbieters angibt.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-114">A pointer to a null-terminated string that specifies the name of the provider to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac4eb-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ac4eb-115">Return value</span></span>

<span data-ttu-id="ac4eb-116">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="ac4eb-116">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="ac4eb-117">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-117">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac4eb-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac4eb-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ac4eb-119">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-119">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="ac4eb-120">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-120">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="ac4eb-121">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-121">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ac4eb-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac4eb-122">Requirements</span></span>



| <span data-ttu-id="ac4eb-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac4eb-123">Requirement</span></span> | <span data-ttu-id="ac4eb-124">Wert</span><span class="sxs-lookup"><span data-stu-id="ac4eb-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac4eb-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ac4eb-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ac4eb-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac4eb-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ac4eb-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ac4eb-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ac4eb-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac4eb-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ac4eb-129">Header</span><span class="sxs-lookup"><span data-stu-id="ac4eb-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac4eb-130"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ac4eb-130"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ac4eb-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ac4eb-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="ac4eb-132"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac4eb-132"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="ac4eb-133">DLL</span><span class="sxs-lookup"><span data-stu-id="ac4eb-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac4eb-134"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="ac4eb-134"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="ac4eb-135">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="ac4eb-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ac4eb-136">**Deleteprintprovidorw** (Unicode) und **deleteprintprovidora** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ac4eb-136">**DeletePrintProvidorW** (Unicode) and **DeletePrintProvidorA** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="ac4eb-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac4eb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac4eb-138">Drucken</span><span class="sxs-lookup"><span data-stu-id="ac4eb-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ac4eb-139">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="ac4eb-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="ac4eb-140">**Addprintprovidor**</span><span class="sxs-lookup"><span data-stu-id="ac4eb-140">**AddPrintProvidor**</span></span>](addprintprovidor.md)
</dt> </dl>

 

 




