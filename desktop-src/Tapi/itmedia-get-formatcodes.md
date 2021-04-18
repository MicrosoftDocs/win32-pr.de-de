---
description: Die get \_ Formatcodes-Methode ruft die Liste der Formatcodes der Medien Nutzlast ab. Die Variante gibt ein SafeArray von bstrinray zurück. Jedes BSTR in diesem Array ist eine Format Code Zeichenfolge.
ms.assetid: 8663d7e8-d46f-44d1-93db-9b5142bb28dd
title: 'ITmedia:: get_FormatCodes-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce9e28a0323ac001c948a3b19b8dae2cfe9daf5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352026"
---
# <a name="itmediaget_formatcodes-method"></a><span data-ttu-id="b4dcf-105">ITmedia:: get \_ Formatcodes-Methode</span><span class="sxs-lookup"><span data-stu-id="b4dcf-105">ITMedia::get\_FormatCodes method</span></span>

<span data-ttu-id="b4dcf-106">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-106">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b4dcf-107">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="b4dcf-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b4dcf-108">Die **get \_ Formatcodes** -Methode ruft die Liste der Formatcodes der Medien Nutzlast ab.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-108">The **get\_FormatCodes** method gets the list of media payload format codes.</span></span> <span data-ttu-id="b4dcf-109">Die Variante gibt ein SafeArray von **BSTR** s zurück.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-109">The variant returns a SAFEARRAY of **BSTR** s.</span></span> <span data-ttu-id="b4dcf-110">Jedes **BSTR** in diesem Array ist eine Format Code Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-110">Each **BSTR** within that array is a format code string.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4dcf-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4dcf-111">Syntax</span></span>


```C++
HRESULT get_FormatCodes(
  [out] VARIANT *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="b4dcf-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4dcf-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4dcf-113">*PVal* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b4dcf-113">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4dcf-114">Array von Medien Nutzlast-Formatcodes.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-114">Array of media payload format codes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4dcf-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b4dcf-115">Return value</span></span>

<span data-ttu-id="b4dcf-116">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-116">This method can return one of these values.</span></span>



| <span data-ttu-id="b4dcf-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b4dcf-117">Return code</span></span>                                                                                   | <span data-ttu-id="b4dcf-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b4dcf-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="b4dcf-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b4dcf-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b4dcf-120">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b4dcf-121"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="b4dcf-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b4dcf-122">Der *PVal* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-122">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="b4dcf-123"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="b4dcf-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b4dcf-124">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="b4dcf-125"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="b4dcf-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="b4dcf-126">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="b4dcf-127"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="b4dcf-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="b4dcf-128">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="b4dcf-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4dcf-129">Remarks</span></span>

<span data-ttu-id="b4dcf-130">Wenn eine Liste mit Nutz Last Formaten angegeben wird, bedeutet dies, dass alle diese Formate in der Sitzung verwendet werden können, aber das erste dieser Formate ist das Standardformat für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-130">When a list of payload formats is given, this implies that all of these formats may be used in the session, but the first of these formats is the default format for the session.</span></span> <span data-ttu-id="b4dcf-131">Wenn das Transportprotokoll RTP ist, sind die Formatcodes RTP-Nutz Last Typen.</span><span class="sxs-lookup"><span data-stu-id="b4dcf-131">When the transport protocol is RTP, the format codes are RTP payload types.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4dcf-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4dcf-132">Requirements</span></span>



| <span data-ttu-id="b4dcf-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b4dcf-133">Requirement</span></span> | <span data-ttu-id="b4dcf-134">Wert</span><span class="sxs-lookup"><span data-stu-id="b4dcf-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b4dcf-135">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="b4dcf-135">TAPI version</span></span><br/> | <span data-ttu-id="b4dcf-136">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="b4dcf-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="b4dcf-137">Header</span><span class="sxs-lookup"><span data-stu-id="b4dcf-137">Header</span></span><br/>       | <dl> <span data-ttu-id="b4dcf-138"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4dcf-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="b4dcf-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b4dcf-139">Library</span></span><br/>      | <dl> <span data-ttu-id="b4dcf-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4dcf-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="b4dcf-141">DLL</span><span class="sxs-lookup"><span data-stu-id="b4dcf-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="b4dcf-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4dcf-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4dcf-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4dcf-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4dcf-144">**ITmedia**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-144">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="b4dcf-145">**ITmedia::p UT- \_ Formatcodes**</span><span class="sxs-lookup"><span data-stu-id="b4dcf-145">**ITMedia::put\_FormatCodes**</span></span>](itmedia-put-formatcodes.md)
</dt> </dl>

 

 




