---
description: Die get \_ URL-Methode ruft die URL ab.
ms.assetid: 9ea2ddf6-b8c7-4bfa-aab3-ff2d2056837f
title: 'Itsdp:: get_Url-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a207c158d405ac0931e42aa19995d1d4b3078fd0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370872"
---
# <a name="itsdpget_url-method"></a><span data-ttu-id="cf3f8-103">Itsdp:: get- \_ URL-Methode</span><span class="sxs-lookup"><span data-stu-id="cf3f8-103">ITSdp::get\_Url method</span></span>

<span data-ttu-id="cf3f8-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cf3f8-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cf3f8-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="cf3f8-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="cf3f8-106">Die **get \_ URL** -Methode ruft die URL ab.</span><span class="sxs-lookup"><span data-stu-id="cf3f8-106">The **get\_Url** method gets the URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf3f8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf3f8-107">Syntax</span></span>


```C++
HRESULT get_Url(
  [out] BSTR *ppUrl
);
```



## <a name="parameters"></a><span data-ttu-id="cf3f8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf3f8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf3f8-109">*ppurl* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cf3f8-109">*ppUrl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf3f8-110">Zeiger auf eine **BSTR** -Darstellung der URL.</span><span class="sxs-lookup"><span data-stu-id="cf3f8-110">Pointer to a **BSTR** representation of the URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf3f8-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf3f8-111">Return value</span></span>

<span data-ttu-id="cf3f8-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="cf3f8-112">This method can return one of these values.</span></span>



| <span data-ttu-id="cf3f8-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="cf3f8-113">Return code</span></span>                                                                                   | <span data-ttu-id="cf3f8-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cf3f8-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="cf3f8-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cf3f8-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="cf3f8-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="cf3f8-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="cf3f8-117"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="cf3f8-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="cf3f8-118">Der *ppurl* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="cf3f8-118">The *ppUrl* parameter is not a valid pointer.</span></span><br/>        |
| <dl> <span data-ttu-id="cf3f8-119"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="cf3f8-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="cf3f8-120">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="cf3f8-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="cf3f8-121"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="cf3f8-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="cf3f8-122">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="cf3f8-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="cf3f8-123"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="cf3f8-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="cf3f8-124">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="cf3f8-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="cf3f8-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf3f8-125">Remarks</span></span>

<span data-ttu-id="cf3f8-126">Die Anwendung muss [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den für den *ppurl* -Parameter zugewiesenen Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="cf3f8-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppUrl* parameter.</span></span>

<span data-ttu-id="cf3f8-127">Eine URL wird normalerweise verwendet, um auf eine Webseite mit zusätzlichen Ressourcen oder Hintergrundinformationen zu einer Konferenz zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="cf3f8-127">An URL is typically used to reference a Web page containing additional resources or background information about a conference.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf3f8-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf3f8-128">Requirements</span></span>



| <span data-ttu-id="cf3f8-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf3f8-129">Requirement</span></span> | <span data-ttu-id="cf3f8-130">Wert</span><span class="sxs-lookup"><span data-stu-id="cf3f8-130">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cf3f8-131">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="cf3f8-131">TAPI version</span></span><br/> | <span data-ttu-id="cf3f8-132">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="cf3f8-132">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="cf3f8-133">Header</span><span class="sxs-lookup"><span data-stu-id="cf3f8-133">Header</span></span><br/>       | <dl> <span data-ttu-id="cf3f8-134"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf3f8-134"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="cf3f8-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cf3f8-135">Library</span></span><br/>      | <dl> <span data-ttu-id="cf3f8-136"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf3f8-136"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="cf3f8-137">DLL</span><span class="sxs-lookup"><span data-stu-id="cf3f8-137">DLL</span></span><br/>          | <dl> <span data-ttu-id="cf3f8-138"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf3f8-138"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf3f8-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf3f8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf3f8-140">**Itsdp**</span><span class="sxs-lookup"><span data-stu-id="cf3f8-140">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="cf3f8-141">**Itsdp::p UT- \_ URL**</span><span class="sxs-lookup"><span data-stu-id="cf3f8-141">**ITSdp::put\_Url**</span></span>](itsdp-put-url.md)
</dt> </dl>

 

