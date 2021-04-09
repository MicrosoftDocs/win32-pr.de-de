---
description: Die Funktion AddPort fügt der Liste der unterstützten Ports den Namen eines Ports hinzu. Die Funktion AddPort wird vom Port Monitor exportiert.
ms.assetid: 9191d507-9167-4488-a4b4-286590a8a62a
title: AddPort-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPort
- AddPortA
- AddPortW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 00e589b59b15c898887090b12348f23fac57fda3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868344"
---
# <a name="addport-function"></a><span data-ttu-id="73887-104">AddPort-Funktion</span><span class="sxs-lookup"><span data-stu-id="73887-104">AddPort function</span></span>

<span data-ttu-id="73887-105">Die Funktion **AddPort** fügt der Liste der unterstützten Ports den Namen eines Ports hinzu.</span><span class="sxs-lookup"><span data-stu-id="73887-105">The **AddPort** function adds the name of a port to the list of supported ports.</span></span> <span data-ttu-id="73887-106">Die Funktion **AddPort** wird vom Port Monitor exportiert.</span><span class="sxs-lookup"><span data-stu-id="73887-106">The **AddPort** function is exported by the port monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="73887-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="73887-107">Syntax</span></span>


```C++
BOOL AddPort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pMonitorName
);
```



## <a name="parameters"></a><span data-ttu-id="73887-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="73887-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73887-109">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73887-109">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73887-110">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Servers angibt, mit dem der Port verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="73887-110">A pointer to a zero-terminated string that specifies the name of the server to which the port is connected.</span></span> <span data-ttu-id="73887-111">Wenn dieser Parameter **null** ist, ist der Port local.</span><span class="sxs-lookup"><span data-stu-id="73887-111">If this parameter is **NULL**, the port is local.</span></span>

</dd> <dt>

<span data-ttu-id="73887-112">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73887-112">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73887-113">Ein Handle für das übergeordnete Fenster des Dialog Felds **AddPort** .</span><span class="sxs-lookup"><span data-stu-id="73887-113">A handle to the parent window of the **AddPort** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="73887-114">*pmonitorname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73887-114">*pMonitorName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73887-115">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den dem Port zugeordneten Monitor angibt.</span><span class="sxs-lookup"><span data-stu-id="73887-115">A pointer to a zero-terminated string that specifies the monitor associated with the port.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73887-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="73887-116">Return value</span></span>

<span data-ttu-id="73887-117">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="73887-117">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="73887-118">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="73887-118">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="73887-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73887-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="73887-120">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="73887-120">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="73887-121">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="73887-121">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="73887-122">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="73887-122">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="73887-123">Die **AddPort** -Funktion durchsucht das Netzwerk, um vorhandene Ports zu suchen, und zeigt ein Dialogfeld für den Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="73887-123">The **AddPort** function browses the network to find existing ports, and displays a dialog box for the user.</span></span> <span data-ttu-id="73887-124">Die **AddPort** -Funktion muss den vom Benutzer eingegebenen Portnamen durch Aufrufen von [**enumports**](enumports.md) überprüfen, um sicherzustellen, dass keine doppelten Namen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="73887-124">The **AddPort** function should validate the port name entered by the user by calling [**EnumPorts**](enumports.md) to ensure that no duplicate names exist.</span></span>

<span data-ttu-id="73887-125">Der Aufrufer der **AddPort** -Funktion muss über Server \_ Zugriffsberechtigungen \_ für den Server verfügen, mit dem der Port verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="73887-125">The caller of the **AddPort** function must have SERVER\_ACCESS\_ADMINISTER access to the server to which the port is connected.</span></span>

<span data-ttu-id="73887-126">Um einen Port hinzuzufügen, ohne ein Dialogfeld anzuzeigen, müssen Sie die **XcvData** -Funktion anstelle von **AddPort** aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="73887-126">To add a port without displaying a dialog box, call the **XcvData** function instead of **AddPort**.</span></span> <span data-ttu-id="73887-127">Weitere Informationen zu **XcvData** finden Sie im Microsoft Windows Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="73887-127">For more information about **XcvData**, see the Microsoft Windows Driver Development Kit (DDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="73887-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73887-128">Requirements</span></span>



| <span data-ttu-id="73887-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="73887-129">Requirement</span></span> | <span data-ttu-id="73887-130">Wert</span><span class="sxs-lookup"><span data-stu-id="73887-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73887-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="73887-131">Minimum supported client</span></span><br/> | <span data-ttu-id="73887-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73887-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="73887-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="73887-133">Minimum supported server</span></span><br/> | <span data-ttu-id="73887-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73887-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="73887-135">Header</span><span class="sxs-lookup"><span data-stu-id="73887-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="73887-136"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="73887-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="73887-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="73887-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="73887-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="73887-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="73887-139">DLL</span><span class="sxs-lookup"><span data-stu-id="73887-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73887-140"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73887-140"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="73887-141">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="73887-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="73887-142">**Addportw** (Unicode) und **addporta** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="73887-142">**AddPortW** (Unicode) and **AddPortA** (ANSI)</span></span><br/>                                                 |



## <a name="see-also"></a><span data-ttu-id="73887-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73887-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73887-144">Drucken</span><span class="sxs-lookup"><span data-stu-id="73887-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="73887-145">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="73887-145">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="73887-146">**DeletePort**</span><span class="sxs-lookup"><span data-stu-id="73887-146">**DeletePort**</span></span>](deleteport.md)
</dt> <dt>

[<span data-ttu-id="73887-147">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="73887-147">**EnumPorts**</span></span>](enumports.md)
</dt> <dt>

[<span data-ttu-id="73887-148">**SetPort**</span><span class="sxs-lookup"><span data-stu-id="73887-148">**SetPort**</span></span>](setport.md)
</dt> </dl>

 

 




