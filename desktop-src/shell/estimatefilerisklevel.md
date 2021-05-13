---
description: Schätzt das Risiko der Ausführung von unbekanntem Code, wenn ein Handler für eine bestimmte Datei aufgerufen wird. Dieses Risiko basiert auf einem Verständnis des Handlers und des Codeinhalts der Datei.
title: EstimateFileRiskLevel-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EstimateFileRiskLevel
api_type:
- DllExport
api_location:
- Winshfhc.dll
ms.assetid: 33a5589a-201b-4d94-afbf-5965a39e2748
ms.openlocfilehash: 2def6cb5bc2ed59a98e9e513aba1b5b578cd8681
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841431"
---
# <a name="estimatefilerisklevel-function"></a><span data-ttu-id="81839-104">EstimateFileRiskLevel-Funktion</span><span class="sxs-lookup"><span data-stu-id="81839-104">EstimateFileRiskLevel function</span></span>

<span data-ttu-id="81839-105">\[Diese Funktion ist unter Windows XP mit Service Pack 2 (SP2) über Windows Vista verfügbar.</span><span class="sxs-lookup"><span data-stu-id="81839-105">\[This function is available on Windows XP with Service Pack 2 (SP2) through Windows Vista.</span></span> <span data-ttu-id="81839-106">Sie kann in nachfolgenden Versionen von Windows geändert oder nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="81839-106">It might be altered or unavailable in subsequent versions of Windows.</span></span> <span data-ttu-id="81839-107">Clientanwendungen sollten stattdessen [**IAttachmentExecute**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute) verwenden, um eine Benutzerumgebung zu präsentieren, die einen sicheren Download und Austausch von Dateien über E-Mail- und Messaginganlagen ermöglicht.\]</span><span class="sxs-lookup"><span data-stu-id="81839-107">Client applications instead should use [**IAttachmentExecute**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute) to present a user environment that provides safe download and exchange of files through email and messaging attachments.\]</span></span>

<span data-ttu-id="81839-108">Schätzt das Risiko der Ausführung von unbekanntem Code, wenn ein Handler für eine bestimmte Datei aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="81839-108">Estimates the risk of executing unknown code when a handler is called on a given file.</span></span> <span data-ttu-id="81839-109">Dieses Risiko basiert auf einem Verständnis des Handlers und des Codeinhalts der Datei.</span><span class="sxs-lookup"><span data-stu-id="81839-109">This risk is based on an understanding of the handler and the code content of the file.</span></span>

## <a name="syntax"></a><span data-ttu-id="81839-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="81839-110">Syntax</span></span>


```C++
HRESULT EstimateFileRiskLevel(
  _In_  LPCWSTR         pszFilePath,
  _In_  LPCWSTR         pszExt,
  _In_  LPCWSTR         pszHandler,
  _Out_ FILE_RISK_LEVEL *pfrlEstimate
);
```



## <a name="parameters"></a><span data-ttu-id="81839-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="81839-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81839-112">*pszFilePath* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="81839-112">*pszFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81839-113">Typ: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="81839-113">Type: **LPCWSTR**</span></span>

<span data-ttu-id="81839-114">Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Pfad der Datei enthält, die für den Handler überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="81839-114">A pointer to a null-terminated string that contains the path of the file that is being checked against the handler.</span></span>

</dd> <dt>

<span data-ttu-id="81839-115">*pszExt* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="81839-115">*pszExt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81839-116">Typ: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="81839-116">Type: **LPCWSTR**</span></span>

<span data-ttu-id="81839-117">Ein Zeiger auf eine mit NULL endende Zeichenfolge, die die Erweiterung der zu überprüfenden Datei enthält, entweder mit oder ohne führenden Punkt.</span><span class="sxs-lookup"><span data-stu-id="81839-117">A pointer to a null-terminated string that contains the extension of the file that is being checked, either with or without its leading period.</span></span> <span data-ttu-id="81839-118">Beispiel: ".txt" oder "txt".</span><span class="sxs-lookup"><span data-stu-id="81839-118">For instance, ".txt" or "txt".</span></span>

</dd> <dt>

<span data-ttu-id="81839-119">*pszHandler* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="81839-119">*pszHandler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81839-120">Typ: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="81839-120">Type: **LPCWSTR**</span></span>

<span data-ttu-id="81839-121">Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Pfad des Handlers für die Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="81839-121">A pointer to a null-terminated string that contains the path of the handler for the file.</span></span>

</dd> <dt>

<span data-ttu-id="81839-122">*pfrlEstimate* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="81839-122">*pfrlEstimate* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81839-123">Typ: **\_ \_ DATEIRISIKOSTUFE \***</span><span class="sxs-lookup"><span data-stu-id="81839-123">Type: **FILE\_RISK\_LEVEL\***</span></span>

<span data-ttu-id="81839-124">Enthält nach erfolgreicher Rückgabe dieser Funktion einen Zeiger auf einen der folgenden Werte, der das geschätzte Risiko angibt.</span><span class="sxs-lookup"><span data-stu-id="81839-124">When this function returns successfully, contains a pointer to one of the following values that state the estimated risk.</span></span>

<dt>

<span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>

<span data-ttu-id="81839-125"><span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>**FRL \_ KEINE \_ MEINUNG** (0)</span><span class="sxs-lookup"><span data-stu-id="81839-125"><span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>**FRL\_NO\_OPINION** (0)</span></span>


</dt> <dd>

<span data-ttu-id="81839-126">Das Format der Datei wird nicht identifiziert, oder der Handler wird nicht identifiziert.</span><span class="sxs-lookup"><span data-stu-id="81839-126">The format of the file is not identified or the handler is not identified.</span></span> <span data-ttu-id="81839-127">Für eine aussagekräftige Antwort sind nicht genügend Informationen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="81839-127">Insufficient information available for a meaningful answer.</span></span>

</dd> <dt>

<span id="FRL_LOW"></span><span id="frl_low"></span>

<span data-ttu-id="81839-128"><span id="FRL_LOW"></span><span id="frl_low"></span>**FRL \_ LOW** (1)</span><span class="sxs-lookup"><span data-stu-id="81839-128"><span id="FRL_LOW"></span><span id="frl_low"></span>**FRL\_LOW** (1)</span></span>


</dt> <dd>

<span data-ttu-id="81839-129">Das Format der Datei ist vollständig verständlich, der Handler ist bekannt, und es ist sehr sicher, dass kein überflüssiger Code ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="81839-129">The format of the file is completely understood, the handler is known, and there is high confidence that no extraneous code will be executed.</span></span>

</dd> <dt>

<span id="FRL_MODERATE"></span><span id="frl_moderate"></span>

<span data-ttu-id="81839-130"><span id="FRL_MODERATE"></span><span id="frl_moderate"></span>**FRL \_ MODERATE** (2)</span><span class="sxs-lookup"><span data-stu-id="81839-130"><span id="FRL_MODERATE"></span><span id="frl_moderate"></span>**FRL\_MODERATE** (2)</span></span>


</dt> <dd>

<span data-ttu-id="81839-131">Das Format der Datei wird identifiziert, aber es ist nicht ausreichend verstanden, um als ein hohes oder niedriges Risiko zu bezeichnen.</span><span class="sxs-lookup"><span data-stu-id="81839-131">The format of the file is identified, but it is not sufficiently understood to label as either a high or low risk.</span></span>

</dd> <dt>

<span id="FRL_HIGH"></span><span id="frl_high"></span>

<span data-ttu-id="81839-132"><span id="FRL_HIGH"></span><span id="frl_high"></span>**FRL \_ HIGH** (3)</span><span class="sxs-lookup"><span data-stu-id="81839-132"><span id="FRL_HIGH"></span><span id="frl_high"></span>**FRL\_HIGH** (3)</span></span>


</dt> <dd>

<span data-ttu-id="81839-133">Das Dateiformat wird verstanden, und es wurden erhöhte Risikofaktoren identifiziert.</span><span class="sxs-lookup"><span data-stu-id="81839-133">The file format is understood and elevated risk factors have been identified.</span></span>

</dd> <dt>

<span id="FRL_BLOCK"></span><span id="frl_block"></span>

<span data-ttu-id="81839-134"><span id="FRL_BLOCK"></span><span id="frl_block"></span>**FRL \_ BLOCK** (4)</span><span class="sxs-lookup"><span data-stu-id="81839-134"><span id="FRL_BLOCK"></span><span id="frl_block"></span>**FRL\_BLOCK** (4)</span></span>


</dt> <dd>

<span data-ttu-id="81839-135">Das Dateiformat wird speziell für diesen Handler blockiert.</span><span class="sxs-lookup"><span data-stu-id="81839-135">The file format is specifically blocked for this handler.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81839-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="81839-136">Return value</span></span>

<span data-ttu-id="81839-137">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="81839-137">Type: **HRESULT**</span></span>

<span data-ttu-id="81839-138">Wenn diese Funktion erfolgreich ausgeführt wird, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="81839-138">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="81839-139">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="81839-139">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="81839-140">Hinweise</span><span class="sxs-lookup"><span data-stu-id="81839-140">Remarks</span></span>

<span data-ttu-id="81839-141">Diese Funktion ist nicht in einem öffentlichen Header deklariert oder in einer Bibliotheksdatei enthalten.</span><span class="sxs-lookup"><span data-stu-id="81839-141">This function is not declared in a public header or included in a library file.</span></span> <span data-ttu-id="81839-142">Um sie zu verwenden, müssen Sie sie direkt aus Winshfhc.dll von Ordnungszahl 101 laden.</span><span class="sxs-lookup"><span data-stu-id="81839-142">To use it you must load it directly from Winshfhc.dll by ordinal 101.</span></span>

## <a name="requirements"></a><span data-ttu-id="81839-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81839-143">Requirements</span></span>



| <span data-ttu-id="81839-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="81839-144">Requirement</span></span> | <span data-ttu-id="81839-145">Wert</span><span class="sxs-lookup"><span data-stu-id="81839-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81839-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="81839-146">Minimum supported client</span></span><br/> | <span data-ttu-id="81839-147">Nur Windows XP mit \[ SP2-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="81839-147">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="81839-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="81839-148">Minimum supported server</span></span><br/> | <span data-ttu-id="81839-149">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="81839-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="81839-150">DLL</span><span class="sxs-lookup"><span data-stu-id="81839-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81839-151"><dt>Winshfhc.dll (Version 5.1 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="81839-151"><dt>Winshfhc.dll (version 5.1 or later)</dt></span></span> </dl> |



 

 




