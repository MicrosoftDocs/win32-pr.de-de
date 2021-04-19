---
description: Löscht ein Druckertreiber Paket aus dem Treiber Speicher.
ms.assetid: a43a94d1-097e-457c-bce9-d4c434ecfa93
title: Deleteprinterdriverpackage-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriverPackage
- DeletePrinterDriverPackageA
- DeletePrinterDriverPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 54d1cda53795f4feab60e397ce7e38402f22374f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355687"
---
# <a name="deleteprinterdriverpackage-function"></a><span data-ttu-id="349de-103">Deleteprinterdriverpackage-Funktion</span><span class="sxs-lookup"><span data-stu-id="349de-103">DeletePrinterDriverPackage function</span></span>

<span data-ttu-id="349de-104">Löscht ein Druckertreiber Paket aus dem Treiber Speicher.</span><span class="sxs-lookup"><span data-stu-id="349de-104">Deletes a printer driver package from the driver store.</span></span>

## <a name="syntax"></a><span data-ttu-id="349de-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="349de-105">Syntax</span></span>


```C++
HRESULT DeletePrinterDriverPackage(
  _In_ LPCTSTR pszServer,
  _In_ LPCTSTR pszInfPath,
  _In_ LPCTSTR pszEnvironment
);
```



## <a name="parameters"></a><span data-ttu-id="349de-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="349de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="349de-107">*pszserver* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="349de-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="349de-108">Ein Zeiger auf eine Konstante, auf NULL abschließende Zeichenfolge, die den Namen des Drucker Servers angibt, von dem das Treiber Paket gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="349de-108">A pointer to a constant, null-terminated string that specifies the name of the print server from which the driver package is being deleted.</span></span> <span data-ttu-id="349de-109">Ein **null** -Zeiger Wert bedeutet den lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="349de-109">A **NULL** pointer value means the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="349de-110">*pszinfpath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="349de-110">*pszInfPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="349de-111">Ein Zeiger auf eine Konstante, auf NULL abschließende Zeichenfolge, die den Pfad zur INF-Datei des Treibers angibt \* .</span><span class="sxs-lookup"><span data-stu-id="349de-111">A pointer to a constant, null-terminated string that specifies the path to the driver's \*.inf file.</span></span>

</dd> <dt>

<span data-ttu-id="349de-112">*pszenvironment* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="349de-112">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="349de-113">Ein Zeiger auf eine Konstante, auf NULL abschließende Zeichenfolge, die die Prozessorarchitektur angibt (z. b. Windows NT x86).</span><span class="sxs-lookup"><span data-stu-id="349de-113">A pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="349de-114">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="349de-114">This can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="349de-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="349de-115">Return value</span></span>

<span data-ttu-id="349de-116">S \_ OK, wenn der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="349de-116">S\_OK, if the operation succeeds.</span></span>

<span data-ttu-id="349de-117">E \_ AccessDenied, wenn das Paket mit Windows ausgeliefert wurde.</span><span class="sxs-lookup"><span data-stu-id="349de-117">E\_ACCESSDENIED, if the package was shipped with Windows.</span></span>

<span data-ttu-id="349de-118">HRESULT- \_ Code (Fehler \_ Druck \_ Treiber Paket wird \_ \_ \_ verwendet), wenn das Paket verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="349de-118">HRESULT\_CODE(ERROR\_PRINT\_DRIVER\_PACKAGE\_IN\_USE), if the package is being used.</span></span>

<span data-ttu-id="349de-119">Andernfalls enthält das **HRESULT** einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="349de-119">Otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="349de-120">Weitere Informationen zu COM-Fehlercodes finden Sie unter [Fehlerbehandlung](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="349de-120">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="349de-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="349de-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="349de-122">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="349de-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="349de-123">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="349de-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="349de-124">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="349de-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="349de-125">Der Treiber Speicher ist in der Regel% windir% \\ INF oder% windir% \\ system32 \\ DriverStore \\ FileRepository.</span><span class="sxs-lookup"><span data-stu-id="349de-125">The driver store is typically %windir%\\inf or %windir%\\System32\\DriverStore\\FileRepository.</span></span>

<span data-ttu-id="349de-126">Ein Treiber Paket, das mit Windows ausgeliefert wurde, kann mit dieser Funktion nicht entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="349de-126">A driver package that shipped with Windows cannot be removed with this function.</span></span>

<span data-ttu-id="349de-127">Der Benutzer muss über Administrator Berechtigungen für die Druckerverwaltung verfügen.</span><span class="sxs-lookup"><span data-stu-id="349de-127">The user must have printer administration privileges.</span></span>

## <a name="requirements"></a><span data-ttu-id="349de-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="349de-128">Requirements</span></span>



| <span data-ttu-id="349de-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="349de-129">Requirement</span></span> | <span data-ttu-id="349de-130">Wert</span><span class="sxs-lookup"><span data-stu-id="349de-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="349de-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="349de-131">Minimum supported client</span></span><br/> | <span data-ttu-id="349de-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="349de-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="349de-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="349de-133">Minimum supported server</span></span><br/> | <span data-ttu-id="349de-134">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="349de-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="349de-135">Header</span><span class="sxs-lookup"><span data-stu-id="349de-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="349de-136"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="349de-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="349de-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="349de-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="349de-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="349de-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="349de-139">DLL</span><span class="sxs-lookup"><span data-stu-id="349de-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="349de-140"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="349de-140"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="349de-141">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="349de-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="349de-142">**DeletePrinterDriverPackageW** (Unicode) und **DeletePrinterDriverPackageA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="349de-142">**DeletePrinterDriverPackageW** (Unicode) and **DeletePrinterDriverPackageA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="349de-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="349de-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="349de-144">Drucken</span><span class="sxs-lookup"><span data-stu-id="349de-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="349de-145">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="349de-145">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

