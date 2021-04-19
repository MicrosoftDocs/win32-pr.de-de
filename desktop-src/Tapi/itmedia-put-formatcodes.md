---
description: Mit der Put \_ Formatcodes-Methode wird die Liste der Formatcodes der Medien Nutzlast festgelegt. Die Variante enthält ein SafeArray von bstrinray. Jedes BSTR in diesem Array ist eine Format Code Zeichenfolge.
ms.assetid: b76a7fee-0fae-41fb-a8cd-6803458d9182
title: ITmedia::p ut_FormatCodes-Methode (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9131f946635c2bb066e704f1d6245c1c30d1372
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352007"
---
# <a name="itmediaput_formatcodes-method"></a><span data-ttu-id="9123a-105">ITmedia::p UT- \_ Formatcodes-Methode</span><span class="sxs-lookup"><span data-stu-id="9123a-105">ITMedia::put\_FormatCodes method</span></span>

<span data-ttu-id="9123a-106">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9123a-106">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9123a-107">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="9123a-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="9123a-108">Mit der **Put \_ Formatcodes** -Methode wird die Liste der Formatcodes der Medien Nutzlast festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9123a-108">The **put\_FormatCodes** method sets the list of media payload format codes.</span></span> <span data-ttu-id="9123a-109">Die Variante enthält ein SafeArray von **BSTR** s.</span><span class="sxs-lookup"><span data-stu-id="9123a-109">The variant contains a SAFEARRAY of **BSTR** s.</span></span> <span data-ttu-id="9123a-110">Jedes **BSTR** in diesem Array ist eine Format Code Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="9123a-110">Each **BSTR** within that array is a format code string.</span></span>

## <a name="syntax"></a><span data-ttu-id="9123a-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="9123a-111">Syntax</span></span>


```C++
HRESULT put_FormatCodes(
  [in] VARIANT NewVal
);
```



## <a name="parameters"></a><span data-ttu-id="9123a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9123a-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9123a-113">*NewVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9123a-113">*NewVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9123a-114">Die Liste der Formatcodes für Medien Nutzlast.</span><span class="sxs-lookup"><span data-stu-id="9123a-114">List of media payload format codes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9123a-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9123a-115">Return value</span></span>

<span data-ttu-id="9123a-116">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="9123a-116">This method can return one of these values.</span></span>



| <span data-ttu-id="9123a-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9123a-117">Return code</span></span>                                                                                   | <span data-ttu-id="9123a-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9123a-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="9123a-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9123a-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9123a-120">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="9123a-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="9123a-121"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="9123a-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="9123a-122">Der *NewVal* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="9123a-122">The *NewVal* parameter is not valid.</span></span><br/>                 |
| <dl> <span data-ttu-id="9123a-123"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="9123a-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="9123a-124">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="9123a-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="9123a-125"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="9123a-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="9123a-126">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="9123a-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="9123a-127"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="9123a-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="9123a-128">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="9123a-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="9123a-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9123a-129">Remarks</span></span>

<span data-ttu-id="9123a-130">Wenn eine Liste mit Nutz Last Formaten angegeben wird, bedeutet dies, dass alle diese Formate in der Sitzung verwendet werden können, aber das erste dieser Formate ist das Standardformat für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="9123a-130">When a list of payload formats is given, this implies that all of these formats may be used in the session, but the first of these formats is the default format for the session.</span></span> <span data-ttu-id="9123a-131">Wenn das Transportprotokoll RTP ist, sind die Formatcodes RTP-Nutz Last Typen.</span><span class="sxs-lookup"><span data-stu-id="9123a-131">When the transport protocol is RTP, the format codes are RTP payload types.</span></span>

## <a name="requirements"></a><span data-ttu-id="9123a-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9123a-132">Requirements</span></span>



| <span data-ttu-id="9123a-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9123a-133">Requirement</span></span> | <span data-ttu-id="9123a-134">Wert</span><span class="sxs-lookup"><span data-stu-id="9123a-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9123a-135">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="9123a-135">TAPI version</span></span><br/> | <span data-ttu-id="9123a-136">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="9123a-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="9123a-137">Header</span><span class="sxs-lookup"><span data-stu-id="9123a-137">Header</span></span><br/>       | <dl> <span data-ttu-id="9123a-138"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="9123a-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="9123a-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9123a-139">Library</span></span><br/>      | <dl> <span data-ttu-id="9123a-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9123a-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="9123a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="9123a-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="9123a-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9123a-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9123a-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9123a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9123a-144">**ITmedia**</span><span class="sxs-lookup"><span data-stu-id="9123a-144">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="9123a-145">**ITmedia:: get- \_ Formatcodes**</span><span class="sxs-lookup"><span data-stu-id="9123a-145">**ITMedia::get\_FormatCodes**</span></span>](itmedia-get-formatcodes.md)
</dt> </dl>

 

 




