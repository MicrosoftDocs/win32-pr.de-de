---
description: Die connecttoprinterdlg-Funktion zeigt ein Dialogfeld an, mit dem Benutzer in einem Netzwerk nach Druckern suchen und eine Verbindung mit Ihnen herstellen können.
ms.assetid: 7cb9108b-8b65-4af3-88c8-a69771ed8e3f
title: Connecttoprinterdlg-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConnectToPrinterDlg
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: 9af428533d111300d31f6529a0a030fc3b81ee7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366178"
---
# <a name="connecttoprinterdlg-function"></a><span data-ttu-id="5f643-103">Connecttoprinterdlg-Funktion</span><span class="sxs-lookup"><span data-stu-id="5f643-103">ConnectToPrinterDlg function</span></span>

<span data-ttu-id="5f643-104">Die **connecttoprinterdlg** -Funktion zeigt ein Dialogfeld an, mit dem Benutzer in einem Netzwerk nach Druckern suchen und eine Verbindung mit Ihnen herstellen können.</span><span class="sxs-lookup"><span data-stu-id="5f643-104">The **ConnectToPrinterDlg** function displays a dialog box that lets users browse and connect to printers on a network.</span></span> <span data-ttu-id="5f643-105">Wenn der Benutzer einen Drucker auswählt, versucht die Funktion, eine Verbindung damit herzustellen. Wenn ein geeigneter Treiber nicht auf dem Server installiert ist, erhält der Benutzer die Möglichkeit, einen Drucker lokal zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5f643-105">If the user selects a printer, the function attempts to create a connection to it; if a suitable driver is not installed on the server, the user is given the option of creating a printer locally.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f643-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f643-106">Syntax</span></span>


```C++
HANDLE ConnectToPrinterDlg(
  _In_ HWND  hwnd,
  _In_ DWORD Flags
);
```



## <a name="parameters"></a><span data-ttu-id="5f643-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f643-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f643-108">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5f643-108">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f643-109">Gibt das übergeordnete Fenster des Dialog Felds an.</span><span class="sxs-lookup"><span data-stu-id="5f643-109">Specifies the parent window of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="5f643-110">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="5f643-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f643-111">Dieser Parameter ist reserviert und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="5f643-111">This parameter is reserved and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f643-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5f643-112">Return value</span></span>

<span data-ttu-id="5f643-113">Wenn die Funktion erfolgreich ausgeführt wird und der Benutzer einen Drucker auswählt, ist der Rückgabewert ein Handle für den ausgewählten Drucker.</span><span class="sxs-lookup"><span data-stu-id="5f643-113">If the function succeeds and the user selects a printer, the return value is a handle to the selected printer.</span></span>

<span data-ttu-id="5f643-114">Wenn die Funktion fehlschlägt oder der Benutzer das Dialogfeld abbricht, ohne einen Drucker auszuwählen, ist der Rückgabewert **null**.</span><span class="sxs-lookup"><span data-stu-id="5f643-114">If the function fails, or the user cancels the dialog box without selecting a printer, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f643-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f643-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5f643-116">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5f643-116">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="5f643-117">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="5f643-117">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="5f643-118">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="5f643-118">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="5f643-119">Die **connecttoprinterdlg** -Funktion versucht, eine Verbindung mit dem ausgewählten Drucker herzustellen.</span><span class="sxs-lookup"><span data-stu-id="5f643-119">The **ConnectToPrinterDlg** function attempts to create a connection to the selected printer.</span></span> <span data-ttu-id="5f643-120">Wenn auf dem Server, auf dem der Drucker residiert, jedoch kein geeigneter Treiber installiert ist, bietet die Funktion dem Benutzer die Möglichkeit, einen Drucker lokal zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5f643-120">However, if the server on which the printer resides does not have a suitable driver installed, the function offers the user the option of creating a printer locally.</span></span> <span data-ttu-id="5f643-121">Eine aufrufenden Anwendung kann ermitteln, ob die Funktion einen Drucker lokal erstellt hat, indem Sie [**GetPrinter**](getprinter.md) mit einer [**Drucker \_ Info \_ 2**](printer-info-2.md) -Struktur aufgerufen hat, und dann den **Attributmember** der Struktur untersucht.</span><span class="sxs-lookup"><span data-stu-id="5f643-121">A calling application can determine whether the function has created a printer locally by calling [**GetPrinter**](getprinter.md) with a [**PRINTER\_INFO\_2**](printer-info-2.md) structure, then examining that structure's **Attributes** member.</span></span>

<span data-ttu-id="5f643-122">Eine Anwendung sollte [**deleteprinter**](deleteprinter.md) aufrufen, um einen lokalen Drucker zu löschen.</span><span class="sxs-lookup"><span data-stu-id="5f643-122">An application should call [**DeletePrinter**](deleteprinter.md) to delete a local printer.</span></span> <span data-ttu-id="5f643-123">Eine Anwendung sollte [**deleteprinterconnection**](deleteprinterconnection.md) aufrufen, um eine Verbindung mit einem Drucker zu löschen.</span><span class="sxs-lookup"><span data-stu-id="5f643-123">An application should call [**DeletePrinterConnection**](deleteprinterconnection.md) to delete a connection to a printer.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f643-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f643-124">Requirements</span></span>



| <span data-ttu-id="5f643-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f643-125">Requirement</span></span> | <span data-ttu-id="5f643-126">Wert</span><span class="sxs-lookup"><span data-stu-id="5f643-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f643-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5f643-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5f643-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5f643-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5f643-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5f643-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5f643-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5f643-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5f643-131">Header</span><span class="sxs-lookup"><span data-stu-id="5f643-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f643-132"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5f643-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="5f643-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5f643-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="5f643-134"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f643-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="5f643-135">DLL</span><span class="sxs-lookup"><span data-stu-id="5f643-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f643-136"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="5f643-136"><dt>WinSpool.drv</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="5f643-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f643-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f643-138">Drucken</span><span class="sxs-lookup"><span data-stu-id="5f643-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="5f643-139">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="5f643-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="5f643-140">**"AddPrinterConnection"**</span><span class="sxs-lookup"><span data-stu-id="5f643-140">**AddPrinterConnection**</span></span>](addprinterconnection.md)
</dt> <dt>

[<span data-ttu-id="5f643-141">**Closeprinter**</span><span class="sxs-lookup"><span data-stu-id="5f643-141">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="5f643-142">**Deleteprinter**</span><span class="sxs-lookup"><span data-stu-id="5f643-142">**DeletePrinter**</span></span>](deleteprinter.md)
</dt> <dt>

[<span data-ttu-id="5f643-143">**Deleteprinterconnection**</span><span class="sxs-lookup"><span data-stu-id="5f643-143">**DeletePrinterConnection**</span></span>](deleteprinterconnection.md)
</dt> <dt>

[<span data-ttu-id="5f643-144">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="5f643-144">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="5f643-145">**Drucker \_ Informationen \_ 2**</span><span class="sxs-lookup"><span data-stu-id="5f643-145">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> </dl>

 

 




