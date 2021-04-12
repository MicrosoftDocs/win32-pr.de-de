---
description: Die Funktion deletePort zeigt ein Dialogfeld an, in dem der Benutzer einen Portnamen löschen kann.
ms.assetid: 5f5788c2-c781-4106-abd2-98556d0a22de
title: DeletePort-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePort
- DeletePortA
- DeletePortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: fa0e3d4b0b5fd43d946d0b6a96b96d0494997a3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216873"
---
# <a name="deleteport-function"></a><span data-ttu-id="b08c9-103">DeletePort-Funktion</span><span class="sxs-lookup"><span data-stu-id="b08c9-103">DeletePort function</span></span>

<span data-ttu-id="b08c9-104">Die Funktion **deletePort** zeigt ein Dialogfeld an, in dem der Benutzer einen Portnamen löschen kann.</span><span class="sxs-lookup"><span data-stu-id="b08c9-104">The **DeletePort** function displays a dialog box that allows the user to delete a port name.</span></span>

## <a name="syntax"></a><span data-ttu-id="b08c9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b08c9-105">Syntax</span></span>


```C++
BOOL DeletePort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pPortName
);
```



## <a name="parameters"></a><span data-ttu-id="b08c9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b08c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b08c9-107">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b08c9-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b08c9-108">Ein Zeiger auf eine mit NULL endende Zeichenfolge, die den Namen des Servers angibt, für den der Port gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="b08c9-108">A pointer to a zero-terminated string that specifies the name of the server for which the port should be deleted.</span></span> <span data-ttu-id="b08c9-109">Wenn dieser Parameter **null** ist, wird ein lokaler Port gelöscht.</span><span class="sxs-lookup"><span data-stu-id="b08c9-109">If this parameter is **NULL**, a local port is deleted.</span></span>

</dd> <dt>

<span data-ttu-id="b08c9-110">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b08c9-110">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b08c9-111">Ein Handle für das übergeordnete Fenster des Dialog Felds zum Löschen von Port.</span><span class="sxs-lookup"><span data-stu-id="b08c9-111">A handle to the parent window of the port-deletion dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="b08c9-112">*pportname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b08c9-112">*pPortName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b08c9-113">Ein Zeiger auf eine mit NULL endende Zeichenfolge, die den Namen des Ports angibt, der gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="b08c9-113">A pointer to a zero-terminated string that specifies the name of the port that should be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b08c9-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b08c9-114">Return value</span></span>

<span data-ttu-id="b08c9-115">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="b08c9-115">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="b08c9-116">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="b08c9-116">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b08c9-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b08c9-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b08c9-118">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b08c9-118">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="b08c9-119">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="b08c9-119">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="b08c9-120">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="b08c9-120">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="b08c9-121">Eine Anwendung kann die Namen gültiger Ports abrufen, indem die [**enumports**](enumports.md) -Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b08c9-121">An application can retrieve the names of valid ports by calling the [**EnumPorts**](enumports.md) function.</span></span>

<span data-ttu-id="b08c9-122">Die **deletePort** -Funktion gibt einen Fehler zurück, wenn zurzeit ein Drucker mit dem angegebenen Port verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="b08c9-122">The **DeletePort** function returns an error if a printer is currently connected to the specified port.</span></span>

<span data-ttu-id="b08c9-123">Der Aufrufer der **deletePort** -Funktion muss über Server \_ Zugriffsberechtigungen \_ für den Server verfügen, mit dem der Port verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="b08c9-123">The caller of the **DeletePort** function must have SERVER\_ACCESS\_ADMINISTER access to the server to which the port is connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="b08c9-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b08c9-124">Requirements</span></span>



| <span data-ttu-id="b08c9-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b08c9-125">Requirement</span></span> | <span data-ttu-id="b08c9-126">Wert</span><span class="sxs-lookup"><span data-stu-id="b08c9-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b08c9-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b08c9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b08c9-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b08c9-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b08c9-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b08c9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b08c9-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b08c9-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b08c9-131">Header</span><span class="sxs-lookup"><span data-stu-id="b08c9-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="b08c9-132"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b08c9-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="b08c9-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b08c9-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="b08c9-134"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b08c9-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="b08c9-135">DLL</span><span class="sxs-lookup"><span data-stu-id="b08c9-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b08c9-136"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="b08c9-136"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="b08c9-137">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="b08c9-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b08c9-138">**Deleteportw** (Unicode) und **deleteporta** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b08c9-138">**DeletePortW** (Unicode) and **DeletePortA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="b08c9-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b08c9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b08c9-140">Drucken</span><span class="sxs-lookup"><span data-stu-id="b08c9-140">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="b08c9-141">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="b08c9-141">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="b08c9-142">**AddPort**</span><span class="sxs-lookup"><span data-stu-id="b08c9-142">**AddPort**</span></span>](addport.md)
</dt> <dt>

[<span data-ttu-id="b08c9-143">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="b08c9-143">**EnumPorts**</span></span>](enumports.md)
</dt> </dl>

 

 




