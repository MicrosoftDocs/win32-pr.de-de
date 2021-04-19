---
description: Fügt dem angegebenen Drucker eine Verbindung für den aktuellen Benutzer hinzu und gibt Verbindungsdetails an.
ms.assetid: 5ae98157-5978-449e-beb1-4787110925fa
title: AddPrinterConnection2-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterConnection2
- AddPrinterConnection2W
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: b24d5ddb25a43fae8576a042c4be6da8fd7cfef7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347987"
---
# <a name="addprinterconnection2-function"></a><span data-ttu-id="b6685-103">AddPrinterConnection2-Funktion</span><span class="sxs-lookup"><span data-stu-id="b6685-103">AddPrinterConnection2 function</span></span>

<span data-ttu-id="b6685-104">Fügt dem angegebenen Drucker eine Verbindung für den aktuellen Benutzer hinzu und gibt Verbindungsdetails an.</span><span class="sxs-lookup"><span data-stu-id="b6685-104">Adds a connection to the specified printer for the current user and specifies connection details.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6685-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6685-105">Syntax</span></span>


```C++
BOOL AddPrinterConnection2(
  _In_ HWND    hWnd,
  _In_ LPCTSTR pszName,
       DWORD   dwLevel,
  _In_ PVOID   pConnectionInfo
);
```



## <a name="parameters"></a><span data-ttu-id="b6685-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6685-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6685-107">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6685-107">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6685-108">Ein Handle für das übergeordnete Fenster, in dem das Dialogfeld angezeigt wird, wenn das Drucksystem einen Druckertreiber vom Druckserver für diese Verbindung herunterladen muss.</span><span class="sxs-lookup"><span data-stu-id="b6685-108">A handle to the parent window in which the dialog box will be displayed if the print system must download a printer driver from the print server for this connection.</span></span>

</dd> <dt>

<span data-ttu-id="b6685-109">*pszName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6685-109">*pszName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6685-110">Ein Zeiger auf eine Konstante mit NULL endenden Zeichenfolge, die den Namen des Druckers angibt, mit dem der aktuelle Benutzer eine Verbindung herstellen möchte.</span><span class="sxs-lookup"><span data-stu-id="b6685-110">A pointer to a constant null-terminated string specifying the name of the printer to which the current user wishes to connect.</span></span>

</dd> <dt>

<span data-ttu-id="b6685-111">*dwlevel*</span><span class="sxs-lookup"><span data-stu-id="b6685-111">*dwLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="b6685-112">Die Version der Struktur, auf die von *pconnectioninfo* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="b6685-112">The version of the structure pointed to by *pConnectionInfo*.</span></span> <span data-ttu-id="b6685-113">Derzeit wird nur Ebene 1 definiert, sodass der Wert von *dwlevel* 1 lauten muss.</span><span class="sxs-lookup"><span data-stu-id="b6685-113">Currently, only level 1 is defined so the value of *dwLevel* must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="b6685-114">*pconnectioninfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6685-114">*pConnectionInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6685-115">Ein Zeiger auf die Struktur der [**Drucker \_ Verbindungs \_ Informationen \_ 1**](printer-connection-info-1.md) .</span><span class="sxs-lookup"><span data-stu-id="b6685-115">A pointer to a [**PRINTER\_CONNECTION\_INFO\_1**](printer-connection-info-1.md) structure.</span></span> <span data-ttu-id="b6685-116">Weitere Informationen zu diesem Parameter finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="b6685-116">See the Remarks section for more about this parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6685-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b6685-117">Return value</span></span>

<span data-ttu-id="b6685-118">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="b6685-118">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="b6685-119">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="b6685-119">If the function fails, the return value is zero.</span></span> <span data-ttu-id="b6685-120">Für erweiterte Fehlerinformationen aufrufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="b6685-120">For extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="b6685-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b6685-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b6685-122">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b6685-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="b6685-123">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="b6685-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="b6685-124">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="b6685-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="b6685-125">Wenn Windows Vista eine Verbindung zu einem Drucker herstellt, müssen möglicherweise Druckertreiber Dateien von dem Server, an den der Drucker angefügt ist, kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="b6685-125">When Windows Vista makes a connection to a printer, it may need to copy printer driver files from the server to which the printer is attached.</span></span> <span data-ttu-id="b6685-126">Wenn der Benutzer nicht über die Berechtigung zum Kopieren von Dateien an den entsprechenden Speicherort verfügt, schlägt die **AddPrinterConnection2** -Funktion fehl, und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den Fehler " \_ Zugriff verweigert" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="b6685-126">If the user does not have permission to copy files to the appropriate location, the **AddPrinterConnection2** function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="b6685-127">Wenn die Druckertreiber Dateien vom Druckserver kopiert werden müssen, aber nicht automatisch kopiert werden können, da die Gruppenrichtlinien wirksam sind und die Drucker \_ Verbindung \_ keine \_ Benutzeroberfläche in *pconnectioninfo->dwFlags* festgelegt ist, werden keine Dialogfelder angezeigt, und der Aufruf schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="b6685-127">If the printer driver files must be copied from the print server but cannot be copied silently due to the group policies that are in effect and PRINTER\_CONNECTION\_NO\_UI is set in *pConnectionInfo->dwFlags*, no dialog boxes will be displayed and the call will fail.</span></span>

<span data-ttu-id="b6685-128">Wenn der lokale Druckertreiber zum renderingdruck von Druckaufträgen für diesen Drucker verwendet werden kann und die Version des lokalen Treibers nicht mit der Version des Druckertreibers auf dem Server identisch ist, legen Sie \_ den Drucker Verbindungs Konflikt \_ in *pconnectioninfo->dwFlags* fest, und weisen Sie den Zeiger einer Zeichen folgen Variablen zu, die den Pfad des lokalen Druckertreibers zu *pconnectioninfo->pszdrivername* enthält.</span><span class="sxs-lookup"><span data-stu-id="b6685-128">If the local printer driver can be used to render print jobs for this printer and the version of the local driver must not match the version of the printer driver on the server, set PRINTER\_CONNECTION\_MISMATCH in *pConnectionInfo->dwFlags* and assign the pointer to a string variable that contains the path to the local printer driver to *pConnectionInfo->pszDriverName*.</span></span>

<span data-ttu-id="b6685-129">Eine Druckerverbindung, die durch den Aufruf von **AddPrinterConnection2** hergestellt wird, wird aufgezählt, wenn [**enumprinter**](enumprinters.md) aufgerufen wird, wobei *dwType* auf druckerenum-Verbindung festgelegt ist \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b6685-129">A printer connection that is established by calling **AddPrinterConnection2** will be enumerated when [**EnumPrinters**](enumprinters.md) is called with *dwType* set to PRINTER\_ENUM\_CONNECTION.</span></span>

<span data-ttu-id="b6685-130">Die ANSI-Version dieser Funktion, **AddPrinterConnection2A**, wird nicht unterstützt und gibt einen Fehler zurück, der **\_ nicht \_ unterstützt** wird.</span><span class="sxs-lookup"><span data-stu-id="b6685-130">The ANSI version of this function, **AddPrinterConnection2A**, is not supported and returns **ERROR\_NOT\_SUPPORTED**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6685-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6685-131">Requirements</span></span>



| <span data-ttu-id="b6685-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6685-132">Requirement</span></span> | <span data-ttu-id="b6685-133">Wert</span><span class="sxs-lookup"><span data-stu-id="b6685-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6685-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b6685-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b6685-135">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6685-135">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="b6685-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b6685-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b6685-137">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6685-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b6685-138">Header</span><span class="sxs-lookup"><span data-stu-id="b6685-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6685-139"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6685-139"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="b6685-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b6685-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="b6685-141"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6685-141"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="b6685-142">DLL</span><span class="sxs-lookup"><span data-stu-id="b6685-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6685-143"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="b6685-143"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="b6685-144">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="b6685-144">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b6685-145">**AddPrinterConnection2W** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="b6685-145">**AddPrinterConnection2W** (Unicode)</span></span><br/>                                                           |



## <a name="see-also"></a><span data-ttu-id="b6685-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6685-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6685-147">Drucken</span><span class="sxs-lookup"><span data-stu-id="b6685-147">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="b6685-148">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="b6685-148">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="b6685-149">**Connecttoprinterdlg**</span><span class="sxs-lookup"><span data-stu-id="b6685-149">**ConnectToPrinterDlg**</span></span>](connecttoprinterdlg.md)
</dt> <dt>

[<span data-ttu-id="b6685-150">**Enumdrucker**</span><span class="sxs-lookup"><span data-stu-id="b6685-150">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="b6685-151">**Deleteprinterconnection**</span><span class="sxs-lookup"><span data-stu-id="b6685-151">**DeletePrinterConnection**</span></span>](deleteprinterconnection.md)
</dt> </dl>

 

