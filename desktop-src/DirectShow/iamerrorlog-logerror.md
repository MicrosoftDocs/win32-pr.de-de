---
description: Die LogError-Methode protokolliert einen Fehler. Anwendungen müssen diese Methode nicht aufzurufen. Sie wird intern als Reaktion auf Renderingfehler aufgerufen.
ms.assetid: 08765c8a-21ca-4c40-84a8-d13da87d9c5f
title: 'Iamerrorlog:: LogError-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMErrorLog.LogError
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dc94532639f325b53db850ebe8a5af489a8b3cf2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372329"
---
# <a name="iamerrorloglogerror-method"></a><span data-ttu-id="692d2-105">Iamerrorlog:: LogError-Methode</span><span class="sxs-lookup"><span data-stu-id="692d2-105">IAMErrorLog::LogError method</span></span>

> [!Note]  
> <span data-ttu-id="692d2-106">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="692d2-106">\[Deprecated.</span></span> <span data-ttu-id="692d2-107">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="692d2-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="692d2-108">Die **LogError** -Methode protokolliert einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="692d2-108">The **LogError** method logs an error.</span></span> <span data-ttu-id="692d2-109">Anwendungen müssen diese Methode nicht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="692d2-109">Applications do not need to call this method.</span></span> <span data-ttu-id="692d2-110">Sie wird intern als Reaktion auf Renderingfehler aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="692d2-110">It is called internally in response to rendering errors.</span></span>

## <a name="syntax"></a><span data-ttu-id="692d2-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="692d2-111">Syntax</span></span>


```C++
HRESULT LogError(
       LONG    Severity,
       BSTR    ErrorString,
       LONG    ErrorCode,
       HRESULT hresult,
  [in] VARIANT *pExtraInfo
);
```



## <a name="parameters"></a><span data-ttu-id="692d2-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="692d2-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="692d2-113">*Severity*</span><span class="sxs-lookup"><span data-stu-id="692d2-113">*Severity*</span></span> 
</dt> <dd>

<span data-ttu-id="692d2-114">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="692d2-114">Reserved.</span></span> <span data-ttu-id="692d2-115">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="692d2-115">Do not use.</span></span>

</dd> <dt>

<span data-ttu-id="692d2-116">*ErrorString*</span><span class="sxs-lookup"><span data-stu-id="692d2-116">*ErrorString*</span></span> 
</dt> <dd>

<span data-ttu-id="692d2-117">Ein Zeichen folgen Wert, der den Text des Fehlers enthält.</span><span class="sxs-lookup"><span data-stu-id="692d2-117">String value containing the text of the error.</span></span>

</dd> <dt>

<span data-ttu-id="692d2-118">*ErrorCode*</span><span class="sxs-lookup"><span data-stu-id="692d2-118">*ErrorCode*</span></span> 
</dt> <dd>

<span data-ttu-id="692d2-119">Fehlercode</span><span class="sxs-lookup"><span data-stu-id="692d2-119">Error code.</span></span>

</dd> <dt>

<span data-ttu-id="692d2-120">*HRESULT*</span><span class="sxs-lookup"><span data-stu-id="692d2-120">*hresult*</span></span> 
</dt> <dd>

<span data-ttu-id="692d2-121">Der HRESULT-Wert, der vom Methoden Aufrufwert zurückgegeben wurde, der den Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="692d2-121">The HRESULT value that was returned by the method call that caused the error.</span></span>

</dd> <dt>

<span data-ttu-id="692d2-122">*pextrainfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="692d2-122">*pExtraInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="692d2-123">Ein Zeiger auf eine Variante, die alle zusätzlichen Informationen über den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="692d2-123">Pointer to a VARIANT that contains any additional information about the error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="692d2-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="692d2-124">Return value</span></span>

<span data-ttu-id="692d2-125">Gibt den Wert des *HRESULT* -Parameters zurück.</span><span class="sxs-lookup"><span data-stu-id="692d2-125">Return the value of the *hresult* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="692d2-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="692d2-126">Remarks</span></span>

<span data-ttu-id="692d2-127">Freigeben Sie in dieser Methode nicht die **Variante** , auf die *pextrainfo* zeigt.</span><span class="sxs-lookup"><span data-stu-id="692d2-127">Within this method, do not free the **VARIANT** pointed to by *pExtraInfo*.</span></span> <span data-ttu-id="692d2-128">Außerdem wird die **Variante** nach der Rückgabe der Methode ungültig. versuchen Sie später nicht, darauf zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="692d2-128">Also, the **VARIANT** becomes invalid after the method returns, so do not try to reference it later.</span></span>

<span data-ttu-id="692d2-129">Implementieren Sie diese Methode, um so schnell wie möglich zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="692d2-129">Implement this method to return as quickly as possible.</span></span> <span data-ttu-id="692d2-130">Erstellen Sie innerhalb dieser Methode keine Funktionsaufrufe, die möglicherweise die Programmausführung blockieren.</span><span class="sxs-lookup"><span data-stu-id="692d2-130">Do not make function calls from inside this method that might block program execution.</span></span> <span data-ttu-id="692d2-131">Sie können z. b. keine Funktionen aufzurufen, die Fenster Meldungen senden, Ereignisse blockieren oder anderweitig die Ausführung blockieren.</span><span class="sxs-lookup"><span data-stu-id="692d2-131">For example, do not call functions that send window messages, block on events, or otherwise might block execution.</span></span> <span data-ttu-id="692d2-132">Dies könnte dazu führen, dass der Computer nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="692d2-132">Doing so could cause the computer to stop responding.</span></span>

<span data-ttu-id="692d2-133">Eine Liste der Fehler, die von des definiert werden, sowie die Bedeutung und den Datentyp der **Variant** , auf die *pextrainfo* zeigt, finden Sie unter [Rendern von Fehlern](rendering-errors.md).</span><span class="sxs-lookup"><span data-stu-id="692d2-133">For a list of errors defined by DES, along with the meaning and data type of the **VARIANT** pointed to by *pExtraInfo*, see [Rendering Errors](rendering-errors.md).</span></span>

> [!Note]  
> <span data-ttu-id="692d2-134">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="692d2-134">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="692d2-135">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="692d2-135">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="692d2-136">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="692d2-136">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="692d2-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="692d2-137">Requirements</span></span>



| <span data-ttu-id="692d2-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="692d2-138">Requirement</span></span> | <span data-ttu-id="692d2-139">Wert</span><span class="sxs-lookup"><span data-stu-id="692d2-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="692d2-140">Header</span><span class="sxs-lookup"><span data-stu-id="692d2-140">Header</span></span><br/>  | <dl> <span data-ttu-id="692d2-141"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="692d2-141"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="692d2-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="692d2-142">Library</span></span><br/> | <dl> <span data-ttu-id="692d2-143"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="692d2-143"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="692d2-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="692d2-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="692d2-145">**Iamerrorlog-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="692d2-145">**IAMErrorLog Interface**</span></span>](iamerrorlog.md)
</dt> <dt>

[<span data-ttu-id="692d2-146">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="692d2-146">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




