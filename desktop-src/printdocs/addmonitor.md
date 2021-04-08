---
description: Mit der addmonitor-Funktion wird ein lokaler Port Monitor installiert, und die Konfigurations-, Daten-und Überwachungs Dateien werden verknüpft.
ms.assetid: 6a556422-5360-42d2-b177-dba0498c06d8
title: Addmonitor-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddMonitor
- AddMonitorA
- AddMonitorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 40b45c4dc05580837a2cf4a001cf8d18e646e5cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050494"
---
# <a name="addmonitor-function"></a><span data-ttu-id="ec10d-103">Addmonitor-Funktion</span><span class="sxs-lookup"><span data-stu-id="ec10d-103">AddMonitor function</span></span>

<span data-ttu-id="ec10d-104">Mit der **addmonitor** -Funktion wird ein lokaler Port Monitor installiert, und die Konfigurations-, Daten-und Überwachungs Dateien werden verknüpft.</span><span class="sxs-lookup"><span data-stu-id="ec10d-104">The **AddMonitor** function installs a local port monitor and links the configuration, data, and monitor files.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec10d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec10d-105">Syntax</span></span>


```C++
BOOL AddMonitor(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pMonitors
);
```



## <a name="parameters"></a><span data-ttu-id="ec10d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec10d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec10d-107">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ec10d-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec10d-108">Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Servers angibt, auf dem der Monitor installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ec10d-108">A pointer to a null-terminated string that specifies the name of the server on which the monitor should be installed.</span></span> <span data-ttu-id="ec10d-109">Für Systeme, die nur die lokale Installation von Monitoren unterstützen, sollte diese Zeichenfolge **null** sein.</span><span class="sxs-lookup"><span data-stu-id="ec10d-109">For systems that support only local installation of monitors, this string should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ec10d-110">*Ebene* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ec10d-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec10d-111">Die Version der-Struktur, auf die *pmonitors* zeigt.</span><span class="sxs-lookup"><span data-stu-id="ec10d-111">The version of the structure to which *pMonitors* points.</span></span> <span data-ttu-id="ec10d-112">Dieser Wert muss 2 sein.</span><span class="sxs-lookup"><span data-stu-id="ec10d-112">This value must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="ec10d-113">*pmonitors* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ec10d-113">*pMonitors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec10d-114">Ein Zeiger auf eine [**Monitor \_ Info \_ 2**](monitor-info-2.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="ec10d-114">A pointer to a [**MONITOR\_INFO\_2**](monitor-info-2.md) structure.</span></span> <span data-ttu-id="ec10d-115">Wenn das Element " **pvironment** " der *pmonitors* -Struktur **null** ist, wird die aktuelle Umgebung des Aufrufers (Client) nicht des Ziels (Server) verwendet.</span><span class="sxs-lookup"><span data-stu-id="ec10d-115">If the **pEnvironment** member of the *pMonitors* structure is **NULL**, the current environment of the caller (client), not of the destination (server), is used.</span></span>

<span data-ttu-id="ec10d-116">Beachten Sie, dass der-Befehl fehlschlägt, wenn die Umgebung nicht der Umgebung des Servers entspricht, d. h., Sie können nur einen Monitor hinzufügen, der für die Architektur des Servers geschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="ec10d-116">Note that the call will fail if the environment does not match the environment of the server, that is, you can only add a monitor that was written for the architecture of the server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec10d-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ec10d-117">Return value</span></span>

<span data-ttu-id="ec10d-118">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="ec10d-118">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="ec10d-119">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="ec10d-119">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec10d-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ec10d-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ec10d-121">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ec10d-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="ec10d-122">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="ec10d-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="ec10d-123">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="ec10d-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="ec10d-124">Der [Aufrufer muss über die SeLoadDriverPrivilege-Berechtigung](/windows/desktop/SecAuthZ/authorization-constants)verfügen.</span><span class="sxs-lookup"><span data-stu-id="ec10d-124">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="ec10d-125">Bevor eine Anwendung die **addmonitor** -Funktion aufruft, müssen alle Dateien, die für den Monitor erforderlich sind, in das Verzeichnis System32 kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="ec10d-125">Before an application calls the **AddMonitor** function, all files required by the monitor must be copied to the SYSTEM32 directory.</span></span>

<span data-ttu-id="ec10d-126">Um die derzeit installierten Port Monitore zu ermitteln, müssen Sie die [**enummonitors**](enummonitors.md) -Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="ec10d-126">To determine the port monitors that are currently installed, call the [**EnumMonitors**](enummonitors.md) function.</span></span>

<span data-ttu-id="ec10d-127">Um einen von **addmonitor** hinzugefügten Monitor zu entfernen, müssen Sie die [**deletemonitor**](deletemonitor.md) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ec10d-127">To remove a monitor added by **AddMonitor**, call the [**DeleteMonitor**](deletemonitor.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec10d-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ec10d-128">Requirements</span></span>



| <span data-ttu-id="ec10d-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ec10d-129">Requirement</span></span> | <span data-ttu-id="ec10d-130">Wert</span><span class="sxs-lookup"><span data-stu-id="ec10d-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec10d-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ec10d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ec10d-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ec10d-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ec10d-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ec10d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ec10d-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ec10d-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ec10d-135">Header</span><span class="sxs-lookup"><span data-stu-id="ec10d-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec10d-136"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ec10d-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ec10d-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ec10d-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="ec10d-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ec10d-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="ec10d-139">DLL</span><span class="sxs-lookup"><span data-stu-id="ec10d-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec10d-140"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="ec10d-140"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="ec10d-141">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="ec10d-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ec10d-142">**Addmonitorw** (Unicode) und **addmonitora** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ec10d-142">**AddMonitorW** (Unicode) and **AddMonitorA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="ec10d-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec10d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec10d-144">Drucken</span><span class="sxs-lookup"><span data-stu-id="ec10d-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ec10d-145">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="ec10d-145">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="ec10d-146">**Deletemonitor**</span><span class="sxs-lookup"><span data-stu-id="ec10d-146">**DeleteMonitor**</span></span>](deletemonitor.md)
</dt> <dt>

[<span data-ttu-id="ec10d-147">**Enumüberwachungen**</span><span class="sxs-lookup"><span data-stu-id="ec10d-147">**EnumMonitors**</span></span>](enummonitors.md)
</dt> <dt>

[<span data-ttu-id="ec10d-148">**Überwachen von \_ Informationen \_ 2**</span><span class="sxs-lookup"><span data-stu-id="ec10d-148">**MONITOR\_INFO\_2**</span></span>](monitor-info-2.md)
</dt> </dl>

 

