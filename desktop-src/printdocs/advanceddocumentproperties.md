---
description: Die advanceddocumentproperties-Funktion zeigt ein druckerkonfigurationsdialogfeld für den angegebenen Drucker an, sodass der Benutzer diesen Drucker konfigurieren kann.
ms.assetid: 29e33f34-f6ec-4989-b076-e1fef8eb5bc4
title: Advanceddocumentproperties-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AdvancedDocumentProperties
- AdvancedDocumentPropertiesA
- AdvancedDocumentPropertiesW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: da8754add6e3f5997354c940c303c41d4588c7b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759559"
---
# <a name="advanceddocumentproperties-function"></a><span data-ttu-id="f28d4-103">Advanceddocumentproperties-Funktion</span><span class="sxs-lookup"><span data-stu-id="f28d4-103">AdvancedDocumentProperties function</span></span>

<span data-ttu-id="f28d4-104">Die **advanceddocumentproperties** -Funktion zeigt ein druckerkonfigurationsdialogfeld für den angegebenen Drucker an, sodass der Benutzer diesen Drucker konfigurieren kann.</span><span class="sxs-lookup"><span data-stu-id="f28d4-104">The **AdvancedDocumentProperties** function displays a printer-configuration dialog box for the specified printer, allowing the user to configure that printer.</span></span>

<span data-ttu-id="f28d4-105">Diese Funktion ist ein Sonderfall der [**DocumentProperties**](documentproperties.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="f28d4-105">This function is a special case of the [**DocumentProperties**](documentproperties.md) function.</span></span> <span data-ttu-id="f28d4-106">Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="f28d4-106">For more details, see the Remarks section.</span></span>

## <a name="syntax"></a><span data-ttu-id="f28d4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f28d4-107">Syntax</span></span>


```C++
LONG AdvancedDocumentProperties(
  _In_  HWND     hWnd,
  _In_  HANDLE   hPrinter,
  _In_  LPTSTR   pDeviceName,
  _Out_ PDEVMODE pDevModeOutput,
  _In_  PDEVMODE pDevModeInput
);
```



## <a name="parameters"></a><span data-ttu-id="f28d4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f28d4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f28d4-109">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f28d4-109">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f28d4-110">Ein Handle für das übergeordnete Fenster des druckerkonfigurationsdialogfelds.</span><span class="sxs-lookup"><span data-stu-id="f28d4-110">A handle to the parent window of the printer-configuration dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="f28d4-111">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f28d4-111">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f28d4-112">Ein Handle für ein Drucker Objekt.</span><span class="sxs-lookup"><span data-stu-id="f28d4-112">A handle to a printer object.</span></span> <span data-ttu-id="f28d4-113">Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.</span><span class="sxs-lookup"><span data-stu-id="f28d4-113">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="f28d4-114">*pdevicename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f28d4-114">*pDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f28d4-115">Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Geräts angibt, für das ein Dialogfeld für die Druckerkonfiguration angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f28d4-115">A pointer to a null-terminated string specifying the name of the device for which a printer-configuration dialog box should be displayed.</span></span>

</dd> <dt>

<span data-ttu-id="f28d4-116">*pdevmodeoutput* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f28d4-116">*pDevModeOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f28d4-117">Ein Zeiger auf eine [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur, die die vom Benutzer angegebenen Konfigurationsdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="f28d4-117">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that will contain the configuration data specified by the user.</span></span>

</dd> <dt>

<span data-ttu-id="f28d4-118">*pdevmodeinput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f28d4-118">*pDevModeInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f28d4-119">Ein Zeiger auf eine [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur, die die Konfigurationsdaten enthält, die zum Initialisieren der Steuerelemente im Dialogfeld Druckerkonfiguration verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f28d4-119">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that contains the configuration data used to initialize the controls of the printer-configuration dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f28d4-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f28d4-120">Return value</span></span>

<span data-ttu-id="f28d4-121">Wenn die [**DocumentProperties**](documentproperties.md) -Funktion mit diesen Parametern erfolgreich ist, ist der Rückgabewert von **advanceddocumentproperties** 1.</span><span class="sxs-lookup"><span data-stu-id="f28d4-121">If the [**DocumentProperties**](documentproperties.md) function with these parameters is successful, the return value of **AdvancedDocumentProperties** is 1.</span></span> <span data-ttu-id="f28d4-122">Andernfalls ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="f28d4-122">Otherwise, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f28d4-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f28d4-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f28d4-124">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f28d4-124">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="f28d4-125">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="f28d4-125">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="f28d4-126">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="f28d4-126">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="f28d4-127">Diese Funktion kann nur das Dialogfeld Druckerkonfiguration anzeigen, sodass Sie von einem Benutzer konfiguriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="f28d4-127">This function can only display the printer-configuration dialog box so a user can configure it.</span></span> <span data-ttu-id="f28d4-128">Wenn Sie mehr Kontrolle haben, verwenden Sie [**DocumentProperties**](documentproperties.md).</span><span class="sxs-lookup"><span data-stu-id="f28d4-128">For more control, use [**DocumentProperties**](documentproperties.md).</span></span> <span data-ttu-id="f28d4-129">Die Eingabeparameter für diese Funktion werden direkt an **DocumentProperties** übermittelt, und der *fmode* -Wert wird in der \_ Puffer- \_ \| DM \_ in der \_ Eingabeaufforderung-DM- \| \_ \_ Puffer auf DM festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f28d4-129">The input parameters for this function are passed directly to **DocumentProperties** and the *fMode* value is set to DM\_IN\_BUFFER \| DM\_IN\_PROMPT \| DM\_OUT\_BUFFER.</span></span> <span data-ttu-id="f28d4-130">Im Gegensatz zu **DocumentProperties** gibt diese Funktion nur 1 oder 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="f28d4-130">Unlike **DocumentProperties**, this function only returns 1 or 0.</span></span> <span data-ttu-id="f28d4-131">Daher können Sie die erforderliche Größe von [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) nicht ermitteln, indem Sie *pdevmode* auf NULL festlegen.</span><span class="sxs-lookup"><span data-stu-id="f28d4-131">Thus, you cannot determine the required size of [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) by setting *pDevMode* to zero.</span></span>

<span data-ttu-id="f28d4-132">Eine Anwendung kann den Namen, auf den der *pdevicename* -Parameter verweist, abrufen, indem Sie die [**GetPrinter**](getprinter.md) -Funktion aufruft und dann den **pprintername** -Member der " [**Printer \_ Info \_ 2**](printer-info-2.md) "-Struktur untersucht.</span><span class="sxs-lookup"><span data-stu-id="f28d4-132">An application can obtain the name pointed to by the *pDeviceName* parameter by calling the [**GetPrinter**](getprinter.md) function and then examining the **pPrinterName** member of the [**PRINTER\_INFO\_2**](printer-info-2.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="f28d4-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f28d4-133">Requirements</span></span>



| <span data-ttu-id="f28d4-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f28d4-134">Requirement</span></span> | <span data-ttu-id="f28d4-135">Wert</span><span class="sxs-lookup"><span data-stu-id="f28d4-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f28d4-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f28d4-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f28d4-137">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f28d4-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f28d4-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f28d4-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f28d4-139">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f28d4-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f28d4-140">Header</span><span class="sxs-lookup"><span data-stu-id="f28d4-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="f28d4-141"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f28d4-141"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f28d4-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f28d4-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="f28d4-143"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f28d4-143"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="f28d4-144">DLL</span><span class="sxs-lookup"><span data-stu-id="f28d4-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f28d4-145"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="f28d4-145"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="f28d4-146">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="f28d4-146">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f28d4-147">**Advanceddocumentpropertiesw** (Unicode) und **advanceddocumentpropertiesa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f28d4-147">**AdvancedDocumentPropertiesW** (Unicode) and **AdvancedDocumentPropertiesA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="f28d4-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f28d4-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f28d4-149">Drucken</span><span class="sxs-lookup"><span data-stu-id="f28d4-149">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f28d4-150">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="f28d4-150">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="f28d4-151">**AddPrinter**</span><span class="sxs-lookup"><span data-stu-id="f28d4-151">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="f28d4-152">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="f28d4-152">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="f28d4-153">**DocumentProperties**</span><span class="sxs-lookup"><span data-stu-id="f28d4-153">**DocumentProperties**</span></span>](documentproperties.md)
</dt> <dt>

[<span data-ttu-id="f28d4-154">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="f28d4-154">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="f28d4-155">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="f28d4-155">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="f28d4-156">**Drucker \_ Informationen \_ 2**</span><span class="sxs-lookup"><span data-stu-id="f28d4-156">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> </dl>

 

 




