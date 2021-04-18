---
description: Die get \_ MEDIANAME-Methode ruft den Mediennamen ab. Definierte Medien sind Audiodaten, Videos, Whiteboards, Text und Daten.
ms.assetid: 4afb24f9-582e-420d-8bda-772a3dc4d96c
title: 'ITmedia:: get_MediaName-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9152994eac98d5e846ac147072a51a3334930da9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358736"
---
# <a name="itmediaget_medianame-method"></a><span data-ttu-id="2cdeb-104">ITmedia:: get \_ MEDIANAME-Methode</span><span class="sxs-lookup"><span data-stu-id="2cdeb-104">ITMedia::get\_MediaName method</span></span>

<span data-ttu-id="2cdeb-105">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cdeb-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2cdeb-106">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="2cdeb-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="2cdeb-107">Die **get \_ MEDIANAME** -Methode ruft den Mediennamen ab.</span><span class="sxs-lookup"><span data-stu-id="2cdeb-107">The **get\_MediaName** method gets the media name.</span></span> <span data-ttu-id="2cdeb-108">Definierte Medien sind Audiodaten, Videos, Whiteboards, Text und Daten.</span><span class="sxs-lookup"><span data-stu-id="2cdeb-108">Defined media are audio, video, whiteboard, text, and data.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cdeb-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2cdeb-109">Syntax</span></span>


```C++
HRESULT get_MediaName(
  [out] BSTR *ppMediaName
);
```



## <a name="parameters"></a><span data-ttu-id="2cdeb-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2cdeb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cdeb-111">*ppmedianame* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2cdeb-111">*ppMediaName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2cdeb-112">Zeiger auf einen **BSTR** -Wert, der den Namen des Mediums enthält, z. b. Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="2cdeb-112">Pointer to a **BSTR** containing the name of the media, such as audio.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cdeb-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2cdeb-113">Return value</span></span>

<span data-ttu-id="2cdeb-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="2cdeb-114">This method can return one of these values.</span></span>



| <span data-ttu-id="2cdeb-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="2cdeb-115">Return code</span></span>                                                                                   | <span data-ttu-id="2cdeb-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2cdeb-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="2cdeb-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2cdeb-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2cdeb-118">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="2cdeb-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="2cdeb-119"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="2cdeb-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="2cdeb-120">Der *ppmedianame* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="2cdeb-120">The *ppMediaName* parameter is not a valid pointer.</span></span><br/>  |
| <dl> <span data-ttu-id="2cdeb-121"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="2cdeb-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2cdeb-122">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="2cdeb-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="2cdeb-123"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="2cdeb-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="2cdeb-124">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="2cdeb-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="2cdeb-125"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="2cdeb-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="2cdeb-126">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="2cdeb-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="2cdeb-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2cdeb-127">Remarks</span></span>

<span data-ttu-id="2cdeb-128">Die Anwendung muss [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den für den *ppmedianame* -Parameter zugeordneten Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="2cdeb-128">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppMediaName* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cdeb-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2cdeb-129">Requirements</span></span>



| <span data-ttu-id="2cdeb-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2cdeb-130">Requirement</span></span> | <span data-ttu-id="2cdeb-131">Wert</span><span class="sxs-lookup"><span data-stu-id="2cdeb-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2cdeb-132">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="2cdeb-132">TAPI version</span></span><br/> | <span data-ttu-id="2cdeb-133">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="2cdeb-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="2cdeb-134">Header</span><span class="sxs-lookup"><span data-stu-id="2cdeb-134">Header</span></span><br/>       | <dl> <span data-ttu-id="2cdeb-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cdeb-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="2cdeb-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2cdeb-136">Library</span></span><br/>      | <dl> <span data-ttu-id="2cdeb-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2cdeb-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="2cdeb-138">DLL</span><span class="sxs-lookup"><span data-stu-id="2cdeb-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="2cdeb-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cdeb-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cdeb-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2cdeb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cdeb-141">**ITmedia**</span><span class="sxs-lookup"><span data-stu-id="2cdeb-141">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="2cdeb-142">**ITmedia::p UT \_ MEDIANAME**</span><span class="sxs-lookup"><span data-stu-id="2cdeb-142">**ITMedia::put\_MediaName**</span></span>](itmedia-put-medianame.md)
</dt> </dl>

 

