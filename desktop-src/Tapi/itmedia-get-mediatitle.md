---
description: Die get \_ mediatitle-Methode ruft einen Text Titel für die Medien ab, der von der Anwendung zur Informations-oder Anzeige Zwecken verwendet werden kann. Dies muss eine ASCII-konvertierbare Zeichenfolge sein, wenn der Zeichensatz ASCII ist. Andernfalls kann es sich um eine beliebige BSTR-Zeichenfolge handeln.
ms.assetid: c5567672-54f0-45d6-81d2-5a501a33c25f
title: 'ITmedia:: get_MediaTitle-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59f2ec4bf16fc27c23277113ee13c8fe02f89c6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364707"
---
# <a name="itmediaget_mediatitle-method"></a><span data-ttu-id="a4b2f-105">ITmedia:: get \_ mediatitle-Methode</span><span class="sxs-lookup"><span data-stu-id="a4b2f-105">ITMedia::get\_MediaTitle method</span></span>

<span data-ttu-id="a4b2f-106">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a4b2f-106">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a4b2f-107">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="a4b2f-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a4b2f-108">Die **get \_ mediatitle** -Methode ruft einen Text Titel für die Medien ab, der von der Anwendung zur Informations-oder Anzeige Zwecken verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a4b2f-108">The **get\_MediaTitle** method retrieves a textual title for the media that the application can use for informational or display purposes.</span></span> <span data-ttu-id="a4b2f-109">Dies muss eine ASCII-konvertierbare Zeichenfolge sein, wenn der Zeichensatz ASCII ist.</span><span class="sxs-lookup"><span data-stu-id="a4b2f-109">This must be an ASCII convertible string if the character set is ASCII.</span></span> <span data-ttu-id="a4b2f-110">Andernfalls kann es sich um eine beliebige **BSTR** -Zeichenfolge handeln.</span><span class="sxs-lookup"><span data-stu-id="a4b2f-110">Otherwise, it can be any **BSTR** string.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4b2f-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4b2f-111">Syntax</span></span>


```C++
HRESULT get_MediaTitle(
  [out] BSTR *ppMediaTitle
);
```



## <a name="parameters"></a><span data-ttu-id="a4b2f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4b2f-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4b2f-113">*ppmediatitle* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a4b2f-113">*ppMediaTitle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4b2f-114">Zeiger auf einen **BSTR** -Wert, der den Titel des Mediums enthält.</span><span class="sxs-lookup"><span data-stu-id="a4b2f-114">Pointer to a **BSTR** containing the title of the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4b2f-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a4b2f-115">Return value</span></span>

<span data-ttu-id="a4b2f-116">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="a4b2f-116">This method can return one of these values.</span></span>



| <span data-ttu-id="a4b2f-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a4b2f-117">Return code</span></span>                                                                                   | <span data-ttu-id="a4b2f-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a4b2f-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="a4b2f-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a4b2f-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a4b2f-120">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="a4b2f-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a4b2f-121"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="a4b2f-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a4b2f-122">Der *ppmediatitle* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="a4b2f-122">The *ppMediaTitle* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="a4b2f-123"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="a4b2f-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a4b2f-124">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a4b2f-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="a4b2f-125"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="a4b2f-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="a4b2f-126">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="a4b2f-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="a4b2f-127"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="a4b2f-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="a4b2f-128">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="a4b2f-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="a4b2f-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a4b2f-129">Remarks</span></span>

<span data-ttu-id="a4b2f-130">Die Anwendung muss [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den Arbeitsspeicher freizugeben, der dem *ppmediatitle* -Parameter zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a4b2f-130">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppMediaTitle* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4b2f-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a4b2f-131">Requirements</span></span>



| <span data-ttu-id="a4b2f-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a4b2f-132">Requirement</span></span> | <span data-ttu-id="a4b2f-133">Wert</span><span class="sxs-lookup"><span data-stu-id="a4b2f-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a4b2f-134">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="a4b2f-134">TAPI version</span></span><br/> | <span data-ttu-id="a4b2f-135">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="a4b2f-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a4b2f-136">Header</span><span class="sxs-lookup"><span data-stu-id="a4b2f-136">Header</span></span><br/>       | <dl> <span data-ttu-id="a4b2f-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4b2f-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="a4b2f-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a4b2f-138">Library</span></span><br/>      | <dl> <span data-ttu-id="a4b2f-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a4b2f-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a4b2f-140">DLL</span><span class="sxs-lookup"><span data-stu-id="a4b2f-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="a4b2f-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4b2f-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4b2f-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4b2f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4b2f-143">**ITmedia**</span><span class="sxs-lookup"><span data-stu-id="a4b2f-143">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="a4b2f-144">**ITmedia::P UT \_ mediatitle**</span><span class="sxs-lookup"><span data-stu-id="a4b2f-144">**ITMedia::Put\_MediaTitle**</span></span>](itmedia-put-mediatitle.md)
</dt> </dl>

 

