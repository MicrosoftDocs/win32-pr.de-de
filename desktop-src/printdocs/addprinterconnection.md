---
description: Die addprconnection-Funktion fügt dem angegebenen Drucker für den aktuellen Benutzer eine Verbindung hinzu.
ms.assetid: 6decf89a-1411-4e7e-aa20-60e7068658c2
title: AddPrinterConnection-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterConnection
- AddPrinterConnectionA
- AddPrinterConnectionW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: dae1f823f89b69526218ab4c027642fb54e3cea5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866564"
---
# <a name="addprinterconnection-function"></a><span data-ttu-id="caacb-103">AddPrinterConnection-Funktion</span><span class="sxs-lookup"><span data-stu-id="caacb-103">AddPrinterConnection function</span></span>

<span data-ttu-id="caacb-104">Die **addprconnection** -Funktion fügt dem angegebenen Drucker für den aktuellen Benutzer eine Verbindung hinzu.</span><span class="sxs-lookup"><span data-stu-id="caacb-104">The **AddPrinterConnection** function adds a connection to the specified printer for the current user.</span></span>

## <a name="syntax"></a><span data-ttu-id="caacb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="caacb-105">Syntax</span></span>


```C++
BOOL AddPrinterConnection(
  _In_ LPTSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="caacb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="caacb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="caacb-107">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="caacb-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="caacb-108">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen eines Druckers angibt, mit dem der aktuelle Benutzer eine Verbindung herstellen möchte.</span><span class="sxs-lookup"><span data-stu-id="caacb-108">A pointer to a null-terminated string that specifies the name of a printer to which the current user wishes to establish a connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="caacb-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="caacb-109">Return value</span></span>

<span data-ttu-id="caacb-110">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="caacb-110">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="caacb-111">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="caacb-111">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="caacb-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="caacb-112">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="caacb-113">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="caacb-113">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="caacb-114">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="caacb-114">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="caacb-115">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="caacb-115">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="caacb-116">Wenn Windows eine Verbindung zu einem Drucker herstellt, müssen möglicherweise Druckertreiber Dateien auf den Server kopiert werden, an den der Drucker angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="caacb-116">When Windows makes a connection to a printer, it may need to copy printer driver files to the server to which the printer is attached.</span></span> <span data-ttu-id="caacb-117">Wenn der Benutzer nicht über die Berechtigung zum Kopieren von Dateien an den entsprechenden Speicherort verfügt, schlägt die **AddPrinterConnection** -Funktion fehl, und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den Fehler \_ Zugriff \_ verweigert zurück.</span><span class="sxs-lookup"><span data-stu-id="caacb-117">If the user does not have permission to copy files to the appropriate location, the **AddPrinterConnection** function fails, and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="caacb-118">Eine Druckerverbindung, die durch den Aufruf von **addprconnection** hergestellt wird, wird aufgelistet, wenn [**enumprinter**](enumprinters.md) aufgerufen wird, wobei *dwType* auf druckerenum-Verbindung festgelegt ist \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="caacb-118">A printer connection established by calling **AddPrinterConnection** will be enumerated when [**EnumPrinters**](enumprinters.md) is called with *dwType* set to PRINTER\_ENUM\_CONNECTION.</span></span>

## <a name="requirements"></a><span data-ttu-id="caacb-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="caacb-119">Requirements</span></span>



| <span data-ttu-id="caacb-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="caacb-120">Requirement</span></span> | <span data-ttu-id="caacb-121">Wert</span><span class="sxs-lookup"><span data-stu-id="caacb-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="caacb-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="caacb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="caacb-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="caacb-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="caacb-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="caacb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="caacb-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="caacb-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="caacb-126">Header</span><span class="sxs-lookup"><span data-stu-id="caacb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="caacb-127"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="caacb-127"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="caacb-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="caacb-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="caacb-129"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="caacb-129"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="caacb-130">DLL</span><span class="sxs-lookup"><span data-stu-id="caacb-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="caacb-131"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="caacb-131"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="caacb-132">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="caacb-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="caacb-133">**Addprinterconnectionw** (Unicode) und **addprinterconnectiona** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="caacb-133">**AddPrinterConnectionW** (Unicode) and **AddPrinterConnectionA** (ANSI)</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="caacb-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="caacb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caacb-135">Drucken</span><span class="sxs-lookup"><span data-stu-id="caacb-135">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="caacb-136">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="caacb-136">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="caacb-137">**Connecttoprinterdlg**</span><span class="sxs-lookup"><span data-stu-id="caacb-137">**ConnectToPrinterDlg**</span></span>](connecttoprinterdlg.md)
</dt> <dt>

[<span data-ttu-id="caacb-138">**Deleteprinterconnection**</span><span class="sxs-lookup"><span data-stu-id="caacb-138">**DeletePrinterConnection**</span></span>](deleteprinterconnection.md)
</dt> <dt>

[<span data-ttu-id="caacb-139">**Enumdrucker**</span><span class="sxs-lookup"><span data-stu-id="caacb-139">**EnumPrinters**</span></span>](enumprinters.md)
</dt> </dl>

 

