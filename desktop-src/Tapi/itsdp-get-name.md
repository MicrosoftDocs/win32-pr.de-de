---
description: Die \_ Methode Get Name Ruft den Namen der Sitzung ab.
ms.assetid: 97b44a01-585b-434c-ad59-51c35e8a1ceb
title: 'Itsdp:: get_name-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b41d431a76f3d0bb2122847e8ee5c3a4dde3c1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360326"
---
# <a name="itsdpget_name-method"></a><span data-ttu-id="00792-103">Itsdp:: get \_ Name-Methode</span><span class="sxs-lookup"><span data-stu-id="00792-103">ITSdp::get\_Name method</span></span>

<span data-ttu-id="00792-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="00792-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="00792-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="00792-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="00792-106">Die Methode **get \_ Name** Ruft den Namen der Sitzung ab.</span><span class="sxs-lookup"><span data-stu-id="00792-106">The **get\_Name** method gets the session name.</span></span> <span data-ttu-id="00792-107">Dies muss eine ASCII-konvertierbare Zeichenfolge sein, wenn es sich um einen ASCII-Zeichensatz handelt.</span><span class="sxs-lookup"><span data-stu-id="00792-107">This has to be an ASCII convertible string if the character set is ASCII.</span></span> <span data-ttu-id="00792-108">(Andernfalls kann es sich um eine beliebige **BSTR** -Zeichenfolge handeln.)</span><span class="sxs-lookup"><span data-stu-id="00792-108">(Otherwise, it can be any **BSTR** string.)</span></span>

## <a name="syntax"></a><span data-ttu-id="00792-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="00792-109">Syntax</span></span>


```C++
HRESULT get_Name(
  [out] BSTR *ppName
);
```



## <a name="parameters"></a><span data-ttu-id="00792-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="00792-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00792-111">*ppName* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="00792-111">*ppName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00792-112">Zeiger auf einen **BSTR** -Wert, der den Sitzungs Namen enthält.</span><span class="sxs-lookup"><span data-stu-id="00792-112">Pointer to a **BSTR** containing the session name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00792-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="00792-113">Return value</span></span>

<span data-ttu-id="00792-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="00792-114">This method can return one of these values.</span></span>



| <span data-ttu-id="00792-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="00792-115">Return code</span></span>                                                                                   | <span data-ttu-id="00792-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="00792-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="00792-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="00792-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="00792-118">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="00792-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="00792-119"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="00792-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="00792-120">Der *ppName* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="00792-120">The *ppName* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="00792-121"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="00792-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="00792-122">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="00792-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="00792-123"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="00792-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="00792-124">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="00792-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="00792-125"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="00792-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="00792-126">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="00792-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="00792-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="00792-127">Remarks</span></span>

<span data-ttu-id="00792-128">Die Anwendung muss [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den für den Parameter *ppName* zugewiesenen Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="00792-128">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppName* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="00792-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00792-129">Requirements</span></span>



| <span data-ttu-id="00792-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="00792-130">Requirement</span></span> | <span data-ttu-id="00792-131">Wert</span><span class="sxs-lookup"><span data-stu-id="00792-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="00792-132">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="00792-132">TAPI version</span></span><br/> | <span data-ttu-id="00792-133">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="00792-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="00792-134">Header</span><span class="sxs-lookup"><span data-stu-id="00792-134">Header</span></span><br/>       | <dl> <span data-ttu-id="00792-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="00792-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="00792-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="00792-136">Library</span></span><br/>      | <dl> <span data-ttu-id="00792-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="00792-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="00792-138">DLL</span><span class="sxs-lookup"><span data-stu-id="00792-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="00792-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00792-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00792-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00792-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00792-141">**Itsdp**</span><span class="sxs-lookup"><span data-stu-id="00792-141">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="00792-142">**Itsdp::p UT- \_ Name**</span><span class="sxs-lookup"><span data-stu-id="00792-142">**ITSdp::put\_Name**</span></span>](itsdp-put-name.md)
</dt> </dl>

 

