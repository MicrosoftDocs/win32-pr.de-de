---
description: Die Funktion "Konfigurations Bericht" zeigt das Dialogfeld Port-Konfiguration für einen Port auf dem angegebenen Server an.
ms.assetid: a65e9876-d6af-48c2-9e6b-8bd8695db130
title: Funktion "Konfiguration Report" (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurePort
- ConfigurePortA
- ConfigurePortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 64f9b3f2e0b0896afdc878477c6e45f8916268a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959703"
---
# <a name="configureport-function"></a><span data-ttu-id="e83b3-103">Funktion "Konfigurations Bericht"</span><span class="sxs-lookup"><span data-stu-id="e83b3-103">ConfigurePort function</span></span>

<span data-ttu-id="e83b3-104">Die Funktion " **Konfigurations Bericht** " zeigt das Dialogfeld Port-Konfiguration für einen Port auf dem angegebenen Server an.</span><span class="sxs-lookup"><span data-stu-id="e83b3-104">The **ConfigurePort** function displays the port-configuration dialog box for a port on the specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="e83b3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e83b3-105">Syntax</span></span>


```C++
BOOL ConfigurePort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pPortName
);
```



## <a name="parameters"></a><span data-ttu-id="e83b3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e83b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e83b3-107">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e83b3-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e83b3-108">Ein Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen des Servers angibt, auf dem der angegebene Port vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e83b3-108">Pointer to a null-terminated string that specifies the name of the server on which the specified port exists.</span></span> <span data-ttu-id="e83b3-109">Wenn dieser Parameter **null** ist, ist der Port local.</span><span class="sxs-lookup"><span data-stu-id="e83b3-109">If this parameter is **NULL**, the port is local.</span></span>

</dd> <dt>

<span data-ttu-id="e83b3-110">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e83b3-110">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e83b3-111">Handle für das übergeordnete Fenster des Dialog Felds Port-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e83b3-111">Handle to the parent window of the port-configuration dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="e83b3-112">*pportname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e83b3-112">*pPortName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e83b3-113">Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des zu konfigurierenden Ports angibt.</span><span class="sxs-lookup"><span data-stu-id="e83b3-113">Pointer to a null-terminated string that specifies the name of the port to be configured.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e83b3-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e83b3-114">Return value</span></span>

<span data-ttu-id="e83b3-115">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="e83b3-115">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="e83b3-116">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="e83b3-116">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e83b3-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e83b3-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e83b3-118">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e83b3-118">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="e83b3-119">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="e83b3-119">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="e83b3-120">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="e83b3-120">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="e83b3-121">Vor dem Aufrufen der Funktion " **Konfigurations Bericht** " sollte eine Anwendung die Funktion " [**enumports**](enumports.md) " aufrufen, um gültige Portnamen zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="e83b3-121">Before calling the **ConfigurePort** function, an application should call the [**EnumPorts**](enumports.md) function to determine valid port names.</span></span>

## <a name="requirements"></a><span data-ttu-id="e83b3-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e83b3-122">Requirements</span></span>



| <span data-ttu-id="e83b3-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e83b3-123">Requirement</span></span> | <span data-ttu-id="e83b3-124">Wert</span><span class="sxs-lookup"><span data-stu-id="e83b3-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e83b3-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e83b3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e83b3-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e83b3-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e83b3-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e83b3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e83b3-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e83b3-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e83b3-129">Header</span><span class="sxs-lookup"><span data-stu-id="e83b3-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="e83b3-130"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e83b3-130"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e83b3-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e83b3-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="e83b3-132"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e83b3-132"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="e83b3-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e83b3-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e83b3-134"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="e83b3-134"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="e83b3-135">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="e83b3-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e83b3-136">" **Konfiguriertem Report w** (Unicode)" und " **konfigurier konfigurieren** " (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e83b3-136">**ConfigurePortW** (Unicode) and **ConfigurePortA** (ANSI)</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="e83b3-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e83b3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e83b3-138">Drucken</span><span class="sxs-lookup"><span data-stu-id="e83b3-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e83b3-139">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="e83b3-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="e83b3-140">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="e83b3-140">**EnumPorts**</span></span>](enumports.md)
</dt> </dl>

 

 




