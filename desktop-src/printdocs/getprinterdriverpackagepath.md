---
description: Ruft den Pfad zum angegebenen Druckertreiber Paket auf einem Druckserver ab.
ms.assetid: e88e984b-d2c0-43b4-8f70-b05ec202ab14
title: GetPrinterDriverPackagePath-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriverPackagePath
- GetPrinterDriverPackagePathA
- GetPrinterDriverPackagePathW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: ea355782df6cce7910f92a46af3cde320536106e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352558"
---
# <a name="getprinterdriverpackagepath-function"></a><span data-ttu-id="87327-103">GetPrinterDriverPackagePath-Funktion</span><span class="sxs-lookup"><span data-stu-id="87327-103">GetPrinterDriverPackagePath function</span></span>

<span data-ttu-id="87327-104">Ruft den Pfad zum angegebenen Druckertreiber Paket auf einem Druckserver ab.</span><span class="sxs-lookup"><span data-stu-id="87327-104">Retrieves the path to the specified printer driver package on a print server.</span></span>

## <a name="syntax"></a><span data-ttu-id="87327-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="87327-105">Syntax</span></span>


```C++
HRESULT GetPrinterDriverPackagePath(
  _In_    LPCTSTR pszServer,
  _In_    LPCTSTR pszEnvironment,
  _In_    LPCTSTR pszLanguage,
  _In_    LPCTSTR pszPackageID,
  _Inout_ LPTSTR  pszDriverPackageCab,
  _In_    DWORD   cchDriverPackageCab,
  _Out_   LPDWORD pcchRequiredSize
);
```



## <a name="parameters"></a><span data-ttu-id="87327-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="87327-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87327-107">*pszserver* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87327-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87327-108">Ein Zeiger auf eine Konstante, auf NULL abschließende Zeichenfolge, die den Namen des Drucker Servers angibt.</span><span class="sxs-lookup"><span data-stu-id="87327-108">A pointer to a constant, null-terminated string that specifies the name of the print server.</span></span> <span data-ttu-id="87327-109">Verwenden Sie für den lokalen Computer **null** .</span><span class="sxs-lookup"><span data-stu-id="87327-109">Use **NULL** for the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="87327-110">*pszenvironment* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87327-110">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87327-111">Ein Zeiger auf eine Konstante, auf NULL abschließende Zeichenfolge, die die Prozessorarchitektur angibt (z. b. Windows NT x86).</span><span class="sxs-lookup"><span data-stu-id="87327-111">A pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="87327-112">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="87327-112">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="87327-113">*pszlanguage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87327-113">*pszLanguage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87327-114">Ein Zeiger auf eine Konstante, auf NULL abschließende Zeichenfolge, die die [mehrsprachige Benutzeroberflächen](/windows/desktop/Intl/mui-resource-management) Sprache für den installierten Treiber angibt.</span><span class="sxs-lookup"><span data-stu-id="87327-114">A pointer to a constant, null-terminated string that specifies the [Multilingual User Interface](/windows/desktop/Intl/mui-resource-management) language for the driver being installed.</span></span> <span data-ttu-id="87327-115">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="87327-115">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="87327-116">*pszpackageid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87327-116">*pszPackageID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87327-117">Ein Zeiger auf eine Konstante, auf NULL abschließende Zeichenfolge, die die ID des Treiber Pakets angibt.</span><span class="sxs-lookup"><span data-stu-id="87327-117">A pointer to a constant, null-terminated string that specifies the ID of the driver package.</span></span>

</dd> <dt>

<span data-ttu-id="87327-118">*pszDriverPackageCab* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="87327-118">*pszDriverPackageCab* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="87327-119">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Pfad zur CAB-Datei für das Treiber Paket angibt.</span><span class="sxs-lookup"><span data-stu-id="87327-119">A pointer to a null-terminated string that specifies the path to the cabinet file for the driver package.</span></span> <span data-ttu-id="87327-120">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="87327-120">This can be **NULL**.</span></span> <span data-ttu-id="87327-121">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="87327-121">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="87327-122">*cchDriverPackageCab* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87327-122">*cchDriverPackageCab* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87327-123">Die Größe des *pszDriverPackageCab* -Puffers in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="87327-123">The size, in characters, of the *pszDriverPackageCab* buffer.</span></span> <span data-ttu-id="87327-124">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="87327-124">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="87327-125">*pcchrequirements dsize* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="87327-125">*pcchRequiredSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87327-126">Ein Zeiger auf die erforderliche Größe des *pszDriverPackageCab* -Puffers.</span><span class="sxs-lookup"><span data-stu-id="87327-126">A pointer to the required size of the *pszDriverPackageCab* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87327-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="87327-127">Return value</span></span>

<span data-ttu-id="87327-128">Wenn der Vorgang erfolgreich ist, ist der Rückgabewert S \_ OK; andernfalls enthält das **HRESULT** einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="87327-128">If the operation succeeds, the return value is S\_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="87327-129">Weitere Informationen zu COM-Fehlercodes finden Sie unter [Fehlerbehandlung](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="87327-129">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="87327-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="87327-130">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="87327-131">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="87327-131">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="87327-132">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="87327-132">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="87327-133">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="87327-133">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="87327-134">Um einen Wert für *cchDriverPackageCab* zu erhalten, rufen Sie die Funktion mit **null** als Wert von *pszDriverPackageCab* auf.</span><span class="sxs-lookup"><span data-stu-id="87327-134">To obtain a value for *cchDriverPackageCab*, call the function with **NULL** as the value of *pszDriverPackageCab*.</span></span> <span data-ttu-id="87327-135">Verwenden Sie den Wert, der in *pcchrequirements dsize* zurückgegeben wurde, als Wert von *cchDriverPackageCab* , und führen Sie die Funktion erneut aus.</span><span class="sxs-lookup"><span data-stu-id="87327-135">Use the value returned in *pcchRequiredSize* as the value of *cchDriverPackageCab* and call the function again.</span></span>

<span data-ttu-id="87327-136">*Pszpackageid* wird in der Regel von einem get-Befehl [**getcoreprinterdrivers**](getcoreprinterdrivers.md)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="87327-136">The *pszPackageID* is typically obtained from a call to [**GetCorePrinterDrivers**](getcoreprinterdrivers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="87327-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="87327-137">Requirements</span></span>



| <span data-ttu-id="87327-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="87327-138">Requirement</span></span> | <span data-ttu-id="87327-139">Wert</span><span class="sxs-lookup"><span data-stu-id="87327-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87327-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="87327-140">Minimum supported client</span></span><br/> | <span data-ttu-id="87327-141">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="87327-141">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="87327-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="87327-142">Minimum supported server</span></span><br/> | <span data-ttu-id="87327-143">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="87327-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="87327-144">Header</span><span class="sxs-lookup"><span data-stu-id="87327-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="87327-145"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="87327-145"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="87327-146">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="87327-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="87327-147"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="87327-147"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="87327-148">DLL</span><span class="sxs-lookup"><span data-stu-id="87327-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87327-149"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87327-149"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="87327-150">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="87327-150">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="87327-151">**GetPrinterDriverPackagePathW** (Unicode) und **GetPrinterDriverPackagePathA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="87327-151">**GetPrinterDriverPackagePathW** (Unicode) and **GetPrinterDriverPackagePathA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="87327-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87327-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87327-153">Drucken</span><span class="sxs-lookup"><span data-stu-id="87327-153">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="87327-154">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="87327-154">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

