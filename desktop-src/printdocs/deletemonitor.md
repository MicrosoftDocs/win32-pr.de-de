---
description: Die deletemonitor-Funktion entfernt einen von der addmonitor-Funktion hinzugefügten Port Monitor.
ms.assetid: 32548d4f-830a-471d-8a72-c0f62f43ffa2
title: Deletemonitor-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteMonitor
- DeleteMonitorA
- DeleteMonitorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 0f11504be516f79610200d4f7da9d571ae1cab9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347558"
---
# <a name="deletemonitor-function"></a><span data-ttu-id="9adb0-103">Deletemonitor-Funktion</span><span class="sxs-lookup"><span data-stu-id="9adb0-103">DeleteMonitor function</span></span>

<span data-ttu-id="9adb0-104">Die **deletemonitor** -Funktion entfernt einen von der [**addmonitor**](addmonitor.md) -Funktion hinzugefügten Port Monitor.</span><span class="sxs-lookup"><span data-stu-id="9adb0-104">The **DeleteMonitor** function removes a port monitor added by the [**AddMonitor**](addmonitor.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="9adb0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9adb0-105">Syntax</span></span>


```C++
BOOL DeleteMonitor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pMonitorName
);
```



## <a name="parameters"></a><span data-ttu-id="9adb0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9adb0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9adb0-107">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9adb0-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9adb0-108">Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Servers angibt, von dem der Monitor entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9adb0-108">A pointer to a null-terminated string that specifies the name of the server from which the monitor is to be removed.</span></span> <span data-ttu-id="9adb0-109">Wenn dieser Parameter **null** ist, wird der Port Monitor lokal entfernt.</span><span class="sxs-lookup"><span data-stu-id="9adb0-109">If this parameter is **NULL**, the port monitor is removed locally.</span></span>

</dd> <dt>

<span data-ttu-id="9adb0-110">nach-oben  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9adb0-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9adb0-111">Ein Zeiger auf eine auf NULL endende Zeichenfolge, die die Umgebung angibt, aus der der Monitor entfernt werden soll (z. b. Windows x86, Windows ia64 oder Windows x64).</span><span class="sxs-lookup"><span data-stu-id="9adb0-111">A pointer to a null-terminated string that specifies the environment from which the monitor is to be removed (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="9adb0-112">Wenn dieser Parameter **null** ist, wird der Monitor aus der aktuellen Umgebung der aufrufenden Anwendung und des Client Computers (nicht der Zielanwendung und des Druck Servers) entfernt.</span><span class="sxs-lookup"><span data-stu-id="9adb0-112">If this parameter is **NULL**, the monitor is removed from the current environment of the calling application and client machine (not of the destination application and print server).</span></span>

</dd> <dt>

<span data-ttu-id="9adb0-113">*pmonitorname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9adb0-113">*pMonitorName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9adb0-114">Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des zu entfernenden Monitors angibt.</span><span class="sxs-lookup"><span data-stu-id="9adb0-114">A pointer to a null-terminated string that specifies the name of the monitor to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9adb0-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9adb0-115">Return value</span></span>

<span data-ttu-id="9adb0-116">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="9adb0-116">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="9adb0-117">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="9adb0-117">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9adb0-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9adb0-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9adb0-119">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9adb0-119">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="9adb0-120">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="9adb0-120">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="9adb0-121">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="9adb0-121">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="9adb0-122">Der [Aufrufer muss über SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants)verfügen.</span><span class="sxs-lookup"><span data-stu-id="9adb0-122">The caller must have [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

## <a name="requirements"></a><span data-ttu-id="9adb0-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9adb0-123">Requirements</span></span>



| <span data-ttu-id="9adb0-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9adb0-124">Requirement</span></span> | <span data-ttu-id="9adb0-125">Wert</span><span class="sxs-lookup"><span data-stu-id="9adb0-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9adb0-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9adb0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9adb0-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9adb0-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9adb0-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9adb0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9adb0-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9adb0-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9adb0-130">Header</span><span class="sxs-lookup"><span data-stu-id="9adb0-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="9adb0-131"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9adb0-131"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="9adb0-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9adb0-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="9adb0-133"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9adb0-133"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="9adb0-134">DLL</span><span class="sxs-lookup"><span data-stu-id="9adb0-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9adb0-135"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="9adb0-135"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="9adb0-136">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="9adb0-136">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9adb0-137">**Deletemonitorw** (Unicode) und **deletemonitora** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9adb0-137">**DeleteMonitorW** (Unicode) and **DeleteMonitorA** (ANSI)</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="9adb0-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9adb0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9adb0-139">Drucken</span><span class="sxs-lookup"><span data-stu-id="9adb0-139">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="9adb0-140">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="9adb0-140">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="9adb0-141">**Addmonitor**</span><span class="sxs-lookup"><span data-stu-id="9adb0-141">**AddMonitor**</span></span>](addmonitor.md)
</dt> </dl>

 

