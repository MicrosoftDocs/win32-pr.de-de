---
description: Die deleteprconnection-Funktion löscht eine Verbindung zu einem Drucker, der durch einen AddPrinterConnection-oder connecttoprinterdlg-Rückruf hergestellt wurde.
ms.assetid: 7b056eea-fbd9-4a08-a2dc-7326caeec387
title: Deleteprinterconnection-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterConnection
- DeletePrinterConnectionA
- DeletePrinterConnectionW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: c524e3bcc79efc2207839b3d3a95051e2eb8bae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352284"
---
# <a name="deleteprinterconnection-function"></a><span data-ttu-id="c56e5-103">Deleteprinterconnection-Funktion</span><span class="sxs-lookup"><span data-stu-id="c56e5-103">DeletePrinterConnection function</span></span>

<span data-ttu-id="c56e5-104">Die **deleteprconnection** -Funktion löscht eine Verbindung zu einem Drucker, der durch einen [**AddPrinterConnection**](addprinterconnection.md) -oder [**connecttoprinterdlg**](connecttoprinterdlg.md)-Rückruf hergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="c56e5-104">The **DeletePrinterConnection** function deletes a connection to a printer that was established by a call to [**AddPrinterConnection**](addprinterconnection.md) or [**ConnectToPrinterDlg**](connecttoprinterdlg.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c56e5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c56e5-105">Syntax</span></span>


```C++
BOOL DeletePrinterConnection(
  _In_ LPTSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="c56e5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c56e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c56e5-107">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c56e5-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c56e5-108">Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen der zu löschenden Druckerverbindung angibt.</span><span class="sxs-lookup"><span data-stu-id="c56e5-108">Pointer to a null-terminated string that specifies the name of the printer connection to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c56e5-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c56e5-109">Return value</span></span>

<span data-ttu-id="c56e5-110">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="c56e5-110">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="c56e5-111">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="c56e5-111">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c56e5-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c56e5-112">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c56e5-113">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c56e5-113">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="c56e5-114">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="c56e5-114">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="c56e5-115">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="c56e5-115">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="c56e5-116">Die **deleteprinterconnection** -Funktion löscht keine Druckertreiber Dateien, die auf den Server kopiert wurden, an den der Drucker angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="c56e5-116">The **DeletePrinterConnection** function does not delete any printer driver files that were copied to the server to which the printer is attached.</span></span>

## <a name="requirements"></a><span data-ttu-id="c56e5-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c56e5-117">Requirements</span></span>



| <span data-ttu-id="c56e5-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c56e5-118">Requirement</span></span> | <span data-ttu-id="c56e5-119">Wert</span><span class="sxs-lookup"><span data-stu-id="c56e5-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c56e5-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c56e5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c56e5-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c56e5-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c56e5-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c56e5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c56e5-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c56e5-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c56e5-124">Header</span><span class="sxs-lookup"><span data-stu-id="c56e5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c56e5-125"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c56e5-125"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="c56e5-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c56e5-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="c56e5-127"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c56e5-127"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="c56e5-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c56e5-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c56e5-129"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="c56e5-129"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="c56e5-130">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="c56e5-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c56e5-131">**Deleteprinterconnectionw** (Unicode) und **deleteprinterconnectiona** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c56e5-131">**DeletePrinterConnectionW** (Unicode) and **DeletePrinterConnectionA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="c56e5-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c56e5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c56e5-133">Drucken</span><span class="sxs-lookup"><span data-stu-id="c56e5-133">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c56e5-134">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="c56e5-134">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="c56e5-135">**"AddPrinterConnection"**</span><span class="sxs-lookup"><span data-stu-id="c56e5-135">**AddPrinterConnection**</span></span>](addprinterconnection.md)
</dt> <dt>

[<span data-ttu-id="c56e5-136">**AddPrinterConnection2**</span><span class="sxs-lookup"><span data-stu-id="c56e5-136">**AddPrinterConnection2**</span></span>](addprinterconnection2.md)
</dt> <dt>

[<span data-ttu-id="c56e5-137">**Connecttoprinterdlg**</span><span class="sxs-lookup"><span data-stu-id="c56e5-137">**ConnectToPrinterDlg**</span></span>](connecttoprinterdlg.md)
</dt> </dl>

 

 




