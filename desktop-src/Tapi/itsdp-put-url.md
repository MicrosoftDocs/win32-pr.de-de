---
description: Die Put \_ URL-Methode legt die URL fest.
ms.assetid: 538bb1dd-c7ad-446d-9df7-23363b466263
title: Itsdp::p ut_Url-Methode (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b791d18b97851e6b0b27a4ba26d1dfdbce7dbb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368481"
---
# <a name="itsdpput_url-method"></a><span data-ttu-id="1a6ad-103">Itsdp::p UT- \_ URL-Methode</span><span class="sxs-lookup"><span data-stu-id="1a6ad-103">ITSdp::put\_Url method</span></span>

<span data-ttu-id="1a6ad-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1a6ad-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1a6ad-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="1a6ad-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1a6ad-106">Die **Put \_ URL** -Methode legt die URL fest.</span><span class="sxs-lookup"><span data-stu-id="1a6ad-106">The **put\_Url** method sets the URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a6ad-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a6ad-107">Syntax</span></span>


```C++
HRESULT put_Url(
  [in] BSTR pUrl
);
```



## <a name="parameters"></a><span data-ttu-id="1a6ad-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a6ad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a6ad-109">*Purl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a6ad-109">*pUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a6ad-110">Zeiger auf eine **BSTR** -Darstellung der URL.</span><span class="sxs-lookup"><span data-stu-id="1a6ad-110">Pointer to a **BSTR** representation of the URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a6ad-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1a6ad-111">Return value</span></span>

<span data-ttu-id="1a6ad-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="1a6ad-112">This method can return one of these values.</span></span>



| <span data-ttu-id="1a6ad-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1a6ad-113">Return code</span></span>                                                                                   | <span data-ttu-id="1a6ad-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1a6ad-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="1a6ad-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1a6ad-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1a6ad-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="1a6ad-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="1a6ad-117"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="1a6ad-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="1a6ad-118">Der *Purl* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="1a6ad-118">The *pUrl* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="1a6ad-119"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="1a6ad-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1a6ad-120">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1a6ad-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="1a6ad-121"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="1a6ad-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="1a6ad-122">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="1a6ad-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="1a6ad-123"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="1a6ad-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="1a6ad-124">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="1a6ad-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="1a6ad-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1a6ad-125">Remarks</span></span>

<span data-ttu-id="1a6ad-126">Die Anwendung muss " [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) " verwenden, um Speicher für den *Purl* -Parameter zuzuweisen, und " [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) " verwenden, um den Arbeitsspeicher freizugeben, wenn die Variable nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="1a6ad-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pUrl* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="1a6ad-127">Eine URL wird normalerweise verwendet, um auf eine Webseite mit zusätzlichen Ressourcen oder Hintergrundinformationen zu einer Konferenz zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="1a6ad-127">An URL is typically used to reference a Web page containing additional resources or background information about a conference.</span></span>

<span data-ttu-id="1a6ad-128">Diese Funktion kann Daten in unverschlüsselter Form über das Netzwerk senden. aus diesem Grund kann ein Benutzer, der sich im Netzwerk befindet, möglicherweise die Daten lesen.</span><span class="sxs-lookup"><span data-stu-id="1a6ad-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="1a6ad-129">Das Sicherheitsrisiko, dass Daten im Klartext gesendet werden, sollte vor der Verwendung dieser Methode berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="1a6ad-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a6ad-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1a6ad-130">Requirements</span></span>



| <span data-ttu-id="1a6ad-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1a6ad-131">Requirement</span></span> | <span data-ttu-id="1a6ad-132">Wert</span><span class="sxs-lookup"><span data-stu-id="1a6ad-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1a6ad-133">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="1a6ad-133">TAPI version</span></span><br/> | <span data-ttu-id="1a6ad-134">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="1a6ad-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="1a6ad-135">Header</span><span class="sxs-lookup"><span data-stu-id="1a6ad-135">Header</span></span><br/>       | <dl> <span data-ttu-id="1a6ad-136"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a6ad-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="1a6ad-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1a6ad-137">Library</span></span><br/>      | <dl> <span data-ttu-id="1a6ad-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a6ad-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="1a6ad-139">DLL</span><span class="sxs-lookup"><span data-stu-id="1a6ad-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="1a6ad-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a6ad-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a6ad-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a6ad-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a6ad-142">**Itsdp**</span><span class="sxs-lookup"><span data-stu-id="1a6ad-142">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="1a6ad-143">**Itsdp:: get- \_ URL**</span><span class="sxs-lookup"><span data-stu-id="1a6ad-143">**ITSdp::get\_Url**</span></span>](itsdp-get-url.md)
</dt> </dl>

 

