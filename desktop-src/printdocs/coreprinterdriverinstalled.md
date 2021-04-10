---
description: Die coreprinterdriverinstallierte-Funktion meldet, ob ein Kern Druckertreiber mit der angegebenen GUID, dem angegebenen Datum und der angegebenen Version installiert ist.
ms.assetid: fb859aca-bb7b-495d-bd38-16ffa084c240
title: Coreprinterdriverinstallierte-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CorePrinterDriverInstalled
- CorePrinterDriverInstalledA
- CorePrinterDriverInstalledW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 2e4f7033e5ca15a892a208621049c2f500873d73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042634"
---
# <a name="coreprinterdriverinstalled-function"></a><span data-ttu-id="35393-103">Coreprinterdriverinstallierte-Funktion</span><span class="sxs-lookup"><span data-stu-id="35393-103">CorePrinterDriverInstalled function</span></span>

<span data-ttu-id="35393-104">Die **coreprinterdriverinstallierte** -Funktion meldet, ob ein Kern Druckertreiber mit der angegebenen GUID, dem angegebenen Datum und der angegebenen Version installiert ist.</span><span class="sxs-lookup"><span data-stu-id="35393-104">The **CorePrinterDriverInstalled** function reports whether a core printer driver with a specified GUID, date, and version is installed.</span></span>

## <a name="syntax"></a><span data-ttu-id="35393-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="35393-105">Syntax</span></span>


```C++
HRESULT CorePrinterDriverInstalled(
  _In_  LPCTSTR   pszServer,
  _In_  LPCTSTR   pszEnvironment,
  _In_  GUID      CoreDriverGUID,
  _In_  FILETIME  ftDriverDate,
  _In_  DWORDLONG dwlDriverVersion,
  _Out_ BOOL      *pbDriverInstalled
);
```



## <a name="parameters"></a><span data-ttu-id="35393-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="35393-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35393-107">*pszserver* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35393-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35393-108">Zeiger auf eine Konstante, auf NULL abschließende Zeichenfolge, die den Namen des Drucker Servers angibt.</span><span class="sxs-lookup"><span data-stu-id="35393-108">Pointer to a constant, null-terminated string that specifies the name of the print server.</span></span> <span data-ttu-id="35393-109">Verwenden Sie für den lokalen Computer **null** .</span><span class="sxs-lookup"><span data-stu-id="35393-109">Use **NULL** for the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="35393-110">*pszenvironment* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35393-110">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35393-111">Zeiger auf eine Konstante, auf NULL abschließende Zeichenfolge, die die Prozessorarchitektur angibt (z. b. Windows NT x86).</span><span class="sxs-lookup"><span data-stu-id="35393-111">Pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="35393-112">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="35393-112">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="35393-113">*Coredriverguid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35393-113">*CoreDriverGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35393-114">Die GUID des Haupt Druckertreibers.</span><span class="sxs-lookup"><span data-stu-id="35393-114">The GUID of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="35393-115">*ftdriverdate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35393-115">*ftDriverDate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35393-116">Das Datum des Haupt Druckertreibers.</span><span class="sxs-lookup"><span data-stu-id="35393-116">The date of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="35393-117">*dwldriverversion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35393-117">*dwlDriverVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35393-118">Die Version des Haupt Druckertreibers.</span><span class="sxs-lookup"><span data-stu-id="35393-118">The version of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="35393-119">*pbdriverinstalliert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="35393-119">*pbDriverInstalled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35393-120">Ein Zeiger auf **true** , wenn der Treiber oder eine neuere Version installiert ist, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="35393-120">A pointer to **TRUE** if the driver, or a newer version, is installed, **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35393-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="35393-121">Return value</span></span>

<span data-ttu-id="35393-122">Wenn der Vorgang erfolgreich ist, ist der Rückgabewert S \_ OK; andernfalls enthält das **HRESULT** einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="35393-122">If the operation succeeds, the return value is S\_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="35393-123">Weitere Informationen zu COM-Fehlercodes finden Sie unter [Fehlerbehandlung](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="35393-123">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="35393-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="35393-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="35393-125">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="35393-125">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="35393-126">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="35393-126">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="35393-127">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="35393-127">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="35393-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="35393-128">Requirements</span></span>



| <span data-ttu-id="35393-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35393-129">Requirement</span></span> | <span data-ttu-id="35393-130">Wert</span><span class="sxs-lookup"><span data-stu-id="35393-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35393-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="35393-131">Minimum supported client</span></span><br/> | <span data-ttu-id="35393-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="35393-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="35393-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="35393-133">Minimum supported server</span></span><br/> | <span data-ttu-id="35393-134">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="35393-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="35393-135">Header</span><span class="sxs-lookup"><span data-stu-id="35393-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="35393-136"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="35393-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="35393-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="35393-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="35393-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="35393-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="35393-139">DLL</span><span class="sxs-lookup"><span data-stu-id="35393-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35393-140"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35393-140"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="35393-141">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="35393-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="35393-142">**Coreprinterdriverinstalledw** (Unicode) und **coreprinterdriverinstalleda** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="35393-142">**CorePrinterDriverInstalledW** (Unicode) and **CorePrinterDriverInstalledA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="35393-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35393-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35393-144">Drucken</span><span class="sxs-lookup"><span data-stu-id="35393-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="35393-145">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="35393-145">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

