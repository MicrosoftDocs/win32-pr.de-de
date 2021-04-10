---
description: Die DocumentProperties-Funktion ruft Drucker Initialisierungs Informationen ab oder ändert Sie oder zeigt ein Eigenschaften Blatt der Druckerkonfiguration für den angegebenen Drucker an.
ms.assetid: e89a2f6f-2bac-4369-b526-f8e15028698b
title: DocumentProperties-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DocumentProperties
- DocumentPropertiesA
- DocumentPropertiesW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 732cb6901b444117d0599a2899327ebcb749cf74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131909"
---
# <a name="documentproperties-function"></a><span data-ttu-id="d7f6f-103">DocumentProperties-Funktion</span><span class="sxs-lookup"><span data-stu-id="d7f6f-103">DocumentProperties function</span></span>

<span data-ttu-id="d7f6f-104">Die **DocumentProperties** -Funktion ruft Drucker Initialisierungs Informationen ab oder ändert Sie oder zeigt ein Eigenschaften Blatt der Druckerkonfiguration für den angegebenen Drucker an.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-104">The **DocumentProperties** function retrieves or modifies printer initialization information or displays a printer-configuration property sheet for the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7f6f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7f6f-105">Syntax</span></span>


```C++
LONG DocumentProperties(
  _In_  HWND     hWnd,
  _In_  HANDLE   hPrinter,
  _In_  LPTSTR   pDeviceName,
  _Out_ PDEVMODE pDevModeOutput,
  _In_  PDEVMODE pDevModeInput,
  _In_  DWORD    fMode
);
```



## <a name="parameters"></a><span data-ttu-id="d7f6f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7f6f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7f6f-107">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7f6f-107">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7f6f-108">Ein Handle für das übergeordnete Fenster des Druckerkonfigurations-Eigenschaften Blatts.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-108">A handle to the parent window of the printer-configuration property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="d7f6f-109">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7f6f-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7f6f-110">Ein Handle für ein Drucker Objekt.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-110">A handle to a printer object.</span></span> <span data-ttu-id="d7f6f-111">Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="d7f6f-112">*pdevicename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7f6f-112">*pDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7f6f-113">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Geräts angibt, für das das Eigenschaften Blatt "Druckerkonfiguration" angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-113">A pointer to a null-terminated string that specifies the name of the device for which the printer-configuration property sheet is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="d7f6f-114">*pdevmodeoutput* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d7f6f-114">*pDevModeOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7f6f-115">Ein Zeiger auf eine [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur, die die vom Benutzer angegebenen Drucker Konfigurationsdaten empfängt.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-115">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that receives the printer configuration data specified by the user.</span></span>

</dd> <dt>

<span data-ttu-id="d7f6f-116">*pdevmodeinput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7f6f-116">*pDevModeInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7f6f-117">Ein Zeiger auf eine [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur, die das Betriebssystem verwendet, um die Eigenschaften Blatt-Steuerelemente zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-117">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that the operating system uses to initialize the property sheet controls.</span></span>

<span data-ttu-id="d7f6f-118">Dieser Parameter wird nur verwendet, wenn das **DM \_ in- \_ pufferflag** im Parameter " *f Mode* " festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-118">This parameter is only used if the **DM\_IN\_BUFFER** flag is set in the *fMode* parameter.</span></span> <span data-ttu-id="d7f6f-119">Wenn **DM \_ im \_ Puffer** nicht festgelegt ist, verwendet das Betriebssystem den standardmäßigen [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)des Druckers.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-119">If **DM\_IN\_BUFFER** is not set, the operating system uses the printer's default [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea).</span></span>

</dd> <dt>

<span data-ttu-id="d7f6f-120">*f-Modus* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7f6f-120">*fMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7f6f-121">Die Vorgänge, die die Funktion ausführt.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-121">The operations the function performs.</span></span> <span data-ttu-id="d7f6f-122">Wenn dieser Parameter NULL ist, gibt die **DocumentProperties** -Funktion die Anzahl der Bytes zurück, die für die [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Datenstruktur des Druckertreibers erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-122">If this parameter is zero, the **DocumentProperties** function returns the number of bytes required by the printer driver's [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) data structure.</span></span> <span data-ttu-id="d7f6f-123">Verwenden Sie andernfalls mindestens eine der folgenden Konstanten, um einen Wert für diesen Parameter zu erstellen. Beachten Sie jedoch, dass eine Anwendung mindestens einen Eingabe Wert und einen Ausgabewert angeben muss, um die Druckeinstellungen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-123">Otherwise, use one or more of the following constants to construct a value for this parameter; note, however, that in order to change the print settings, an application must specify at least one input value and one output value.</span></span>



| <span data-ttu-id="d7f6f-124">Wert</span><span class="sxs-lookup"><span data-stu-id="d7f6f-124">Value</span></span>                                                                                                                                                          | <span data-ttu-id="d7f6f-125">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d7f6f-125">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DM_IN_BUFFER"></span><span id="dm_in_buffer"></span><dl> <span data-ttu-id="d7f6f-126"><dt>**DM \_ in \_ Puffer**</dt></span><span class="sxs-lookup"><span data-stu-id="d7f6f-126"><dt>**DM\_IN\_BUFFER**</dt></span></span> </dl>    | <span data-ttu-id="d7f6f-127">Der Eingabe Wert.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-127">Input value.</span></span> <span data-ttu-id="d7f6f-128">Vor dem aufrufen, kopieren oder aktualisieren führt die Funktion die aktuellen Druckeinstellungen des Druckertreibers mit den Einstellungen in der [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur zusammen, die durch den *pdevmodeinput* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-128">Before prompting, copying, or updating, the function merges the printer driver's current print settings with the settings in the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure specified by the *pDevModeInput* parameter.</span></span> <span data-ttu-id="d7f6f-129">Die-Funktion aktualisiert die-Struktur nur für die Elemente, die vom **dmFields** -Member der **DEVMODE** -Struktur angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-129">The function updates the structure only for those members specified by the **DEVMODE** structure's **dmFields** member.</span></span> <span data-ttu-id="d7f6f-130">Dieser Wert wird auch als **DM- \_ Änderung** definiert.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-130">This value is also defined as **DM\_MODIFY**.</span></span> <span data-ttu-id="d7f6f-131">Bei einem Konflikt während der Zusammenführung überschreiben die Einstellungen in der **DEVMODE** -Struktur, die von *pdevmodeinput* angegeben werden, die aktuellen Druckeinstellungen des Druckertreibers.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-131">In cases of conflict during the merge, the settings in the **DEVMODE** structure specified by *pDevModeInput* override the printer driver's current print settings.</span></span><br/> |
| <span id="DM_IN_PROMPT"></span><span id="dm_in_prompt"></span><dl> <span data-ttu-id="d7f6f-132"><dt>**DM \_ - \_ Eingabeaufforderung**</dt></span><span class="sxs-lookup"><span data-stu-id="d7f6f-132"><dt>**DM\_IN\_PROMPT**</dt></span></span> </dl>    | <span data-ttu-id="d7f6f-133">Der Eingabe Wert.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-133">Input value.</span></span> <span data-ttu-id="d7f6f-134">Die Funktion zeigt das Druck Setup-Eigenschaften Blatt des Druckertreibers an und ändert anschließend die Einstellungen in der [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Datenstruktur des Druckers auf die vom Benutzer angegebenen Werte.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-134">The function presents the printer driver's Print Setup property sheet and then changes the settings in the printer's [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) data structure to those values specified by the user.</span></span> <span data-ttu-id="d7f6f-135">Dieser Wert wird auch als **DM- \_ Eingabeaufforderung** definiert.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-135">This value is also defined as **DM\_PROMPT**.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <span id="DM_OUT_BUFFER"></span><span id="dm_out_buffer"></span><dl> <span data-ttu-id="d7f6f-136"><dt>**DM- \_ out- \_ Puffer**</dt></span><span class="sxs-lookup"><span data-stu-id="d7f6f-136"><dt>**DM\_OUT\_BUFFER**</dt></span></span> </dl> | <span data-ttu-id="d7f6f-137">Ausgabewert.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-137">Output value.</span></span> <span data-ttu-id="d7f6f-138">Die-Funktion schreibt die aktuellen Druckeinstellungen des Druckertreibers, einschließlich privater Daten, in die [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Datenstruktur, die durch den *pdevmodeoutput* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-138">The function writes the printer driver's current print settings, including private data, to the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) data structure specified by the *pDevModeOutput* parameter.</span></span> <span data-ttu-id="d7f6f-139">Der Aufrufer muss einen ausreichend großen Puffer zuordnen, um die Informationen zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-139">The caller must allocate a buffer sufficiently large to contain the information.</span></span> <span data-ttu-id="d7f6f-140">Wenn die Bit- **DM- \_ out- \_ Puffer** Sätze eindeutig sind, kann der *pdevmodeoutput* -Parameter **null** sein.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-140">If the bit **DM\_OUT\_BUFFER** sets is clear, the *pDevModeOutput* parameter can be **NULL**.</span></span> <span data-ttu-id="d7f6f-141">Dieser Wert wird auch als **DM- \_ Kopie** definiert.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-141">This value is also defined as **DM\_COPY**.</span></span><br/>                                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7f6f-142">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d7f6f-142">Return value</span></span>

<span data-ttu-id="d7f6f-143">Wenn der *fmode* -Parameter 0 (null) ist, ist der Rückgabewert die Größe des Puffers, der zum enthalten der Initialisierungs Daten für den Druckertreiber erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-143">If the *fMode* parameter is zero, the return value is the size of the buffer required to contain the printer driver initialization data.</span></span> <span data-ttu-id="d7f6f-144">Beachten Sie, dass dieser Puffer größer als eine [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur sein kann, wenn der Druckertreiber private Daten an die Struktur anfügt.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-144">Note that this buffer can be larger than a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure if the printer driver appends private data to the structure.</span></span>

<span data-ttu-id="d7f6f-145">Wenn die Funktion das Eigenschaften Blatt anzeigt, ist der Rückgabewert entweder **IDOK** oder **IDCANCEL**, abhängig von der Schaltfläche, die der Benutzer auswählt.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-145">If the function displays the property sheet, the return value is either **IDOK** or **IDCANCEL**, depending on which button the user selects.</span></span>

<span data-ttu-id="d7f6f-146">Wenn die Funktion das Eigenschaften Blatt nicht anzeigt und erfolgreich ist, lautet der Rückgabewert **IDOK**.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-146">If the function does not display the property sheet and is successful, the return value is **IDOK**.</span></span>

<span data-ttu-id="d7f6f-147">Wenn die Funktion fehlschlägt, ist der Rückgabewert kleiner als 0 (null).</span><span class="sxs-lookup"><span data-stu-id="d7f6f-147">If the function fails, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7f6f-148">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d7f6f-148">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d7f6f-149">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-149">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="d7f6f-150">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-150">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="d7f6f-151">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-151">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="d7f6f-152">Die Zeichenfolge, auf die der *pdevicename* -Parameter verweist, kann durch Aufrufen der [**GetPrinter**](getprinter.md) -Funktion abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-152">The string pointed to by the *pDeviceName* parameter can be obtained by calling the [**GetPrinter**](getprinter.md) function.</span></span>

<span data-ttu-id="d7f6f-153">Die [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur, die tatsächlich von einem Druckertreiber verwendet wird, enthält den geräteunabhängigen Teil (wie oben definiert), gefolgt von einem treiberspezifischen Teil, der in Größe und Inhalt mit den einzelnen Treiber-und Treiberversionen variiert.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-153">The [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure actually used by a printer driver contains the device-independent part (as defined above) followed by a driver-specific part that varies in size and content with each driver and driver version.</span></span> <span data-ttu-id="d7f6f-154">Aufgrund dieser Treiber Abhängigkeit ist es sehr wichtig, dass Anwendungen den Treiber nach der richtigen Größe der **DEVMODE** -Struktur Abfragen, bevor Sie einen Puffer dafür zuordnen.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-154">Because of this driver dependence, it is very important for applications to query the driver for the correct size of the **DEVMODE** structure before allocating a buffer for it.</span></span>

<span data-ttu-id="d7f6f-155">**Um Änderungen an den Druckeinstellungen vorzunehmen, die für eine Anwendung lokal sind, sollte eine Anwendung die folgenden Schritte ausführen:**</span><span class="sxs-lookup"><span data-stu-id="d7f6f-155">**To make changes to print settings that are local to an application, an application should follow these steps:**</span></span>

1.  <span data-ttu-id="d7f6f-156">Rufen Sie die Anzahl der Bytes ab, die für die vollständige [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur erforderlich sind, indem Sie **DocumentProperties** aufrufen und NULL im *fmode* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-156">Get the number of bytes required for the full [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure by calling **DocumentProperties** and specifying zero in the *fMode* parameter.</span></span>
2.  <span data-ttu-id="d7f6f-157">Zuweisen von Speicher für die vollständige [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-157">Allocate memory for the full [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure.</span></span>
3.  <span data-ttu-id="d7f6f-158">Rufen Sie die aktuellen Druckereinstellungen durch Aufrufen von **DocumentProperties** ab.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-158">Get the current printer settings by calling **DocumentProperties**.</span></span> <span data-ttu-id="d7f6f-159">Übergeben Sie einen Zeiger an die [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur, die in Schritt 2 als *pdevmodeoutput* -Parameter zugewiesen wurde, und geben Sie den Wert für **DM \_ out- \_ Puffer** an</span><span class="sxs-lookup"><span data-stu-id="d7f6f-159">Pass a pointer to the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure allocated in Step 2 as the *pDevModeOutput* parameter and specify the **DM\_OUT\_BUFFER** value.</span></span>
4.  <span data-ttu-id="d7f6f-160">Ändern Sie die entsprechenden Member der zurückgegebenen [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur, und geben Sie an, welche Elemente geändert wurden, indem Sie die entsprechenden Bits im **dmFields** -Member von **DEVMODE** festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-160">Modify the appropriate members of the returned [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure and indicate which members were changed by setting the corresponding bits in the **dmFields** member of the **DEVMODE**.</span></span>
5.  <span data-ttu-id="d7f6f-161">Verwenden Sie **DocumentProperties** , und übergeben Sie die geänderte [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur zurück als *pdevmodeinput* -Parameter und *pdevmodeoutput* -Parameter, und geben Sie sowohl den **DM \_ in \_ buffer** -als auch den **DM \_ out- \_ Puffer** Wert an (die mithilfe des OR-Operators kombiniert werden). Die **DEVMODE** -Struktur, die vom dritten **DocumentProperties** -Befehl zurückgegeben wird, kann als Argument in einem aufrufen [**der Funktion "**](/windows/desktop/api/wingdi/nf-wingdi-createdca) -Funktion" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-161">Call **DocumentProperties** and pass the modified [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure back as both the *pDevModeInput* and *pDevModeOutput* parameters and specify both the **DM\_IN\_BUFFER** and **DM\_OUT\_BUFFER** values (which are combined using the OR operator).The **DEVMODE** structure returned by the third call to **DocumentProperties** can be used as an argument in a call to the [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) function.</span></span>

<span data-ttu-id="d7f6f-162">Um mithilfe der aktuellen Druckereinstellungen ein Handle für einen Druckergerätekontext zu erstellen, müssen Sie die **DocumentProperties** -Eigenschaft wie oben beschrieben zweimal abrufen.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-162">To create a handle to a printer-device context using the current printer settings, you only need to call **DocumentProperties** twice, as described above.</span></span> <span data-ttu-id="d7f6f-163">Der erste-Befehl ruft die Größe des vollständigen [**DEVMODE-Ausdrucks**](/windows/win32/api/wingdi/ns-wingdi-devmodea) ab, und der zweite aufrufsinitialisiert den **DEVMODE** mit den aktuellen Druckereinstellungen.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-163">The first call gets the size of the full [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) and the second call initializes the **DEVMODE** with the current printer settings.</span></span> <span data-ttu-id="d7f6f-164">Übergeben Sie den initialisierten **DEVMODE** -Typ an " [**kreatedc**](/windows/desktop/api/wingdi/nf-wingdi-createdca) ", um das Handle für den Drucker Gerätekontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-164">Pass the initialized **DEVMODE** to [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) to obtain the handle to the printer device context.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7f6f-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d7f6f-165">Requirements</span></span>



| <span data-ttu-id="d7f6f-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d7f6f-166">Requirement</span></span> | <span data-ttu-id="d7f6f-167">Wert</span><span class="sxs-lookup"><span data-stu-id="d7f6f-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7f6f-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d7f6f-168">Minimum supported client</span></span><br/> | <span data-ttu-id="d7f6f-169">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d7f6f-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d7f6f-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d7f6f-170">Minimum supported server</span></span><br/> | <span data-ttu-id="d7f6f-171">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d7f6f-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d7f6f-172">Header</span><span class="sxs-lookup"><span data-stu-id="d7f6f-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7f6f-173"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d7f6f-173"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="d7f6f-174">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d7f6f-174">Library</span></span><br/>                  | <dl> <span data-ttu-id="d7f6f-175"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7f6f-175"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="d7f6f-176">DLL</span><span class="sxs-lookup"><span data-stu-id="d7f6f-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7f6f-177"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="d7f6f-177"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="d7f6f-178">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="d7f6f-178">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d7f6f-179">**Documentpropertiesw** (Unicode) und **documentpropertiesa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d7f6f-179">**DocumentPropertiesW** (Unicode) and **DocumentPropertiesA** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="d7f6f-180">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d7f6f-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7f6f-181">Drucken</span><span class="sxs-lookup"><span data-stu-id="d7f6f-181">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="d7f6f-182">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="d7f6f-182">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="d7f6f-183">**Advanceddocumentproperties**</span><span class="sxs-lookup"><span data-stu-id="d7f6f-183">**AdvancedDocumentProperties**</span></span>](advanceddocumentproperties.md)
</dt> <dt>

[<span data-ttu-id="d7f6f-184">**-**</span><span class="sxs-lookup"><span data-stu-id="d7f6f-184">**CreateDC**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-createdca)
</dt> <dt>

[<span data-ttu-id="d7f6f-185">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="d7f6f-185">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="d7f6f-186">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="d7f6f-186">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="d7f6f-187">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="d7f6f-187">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

