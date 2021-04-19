---
description: Das \_ Transportprotokoll wird von der Get transportprotocol-Methode abgerufen.
ms.assetid: d270d6f4-bdcf-4cf4-970b-65f0be706171
title: 'ITmedia:: get_TransportProtocol-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf2bc66a98e181674bbf6f7956579bbaa0b5a72
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367552"
---
# <a name="itmediaget_transportprotocol-method"></a><span data-ttu-id="f234a-103">ITmedia:: get \_ transportprotocol-Methode</span><span class="sxs-lookup"><span data-stu-id="f234a-103">ITMedia::get\_TransportProtocol method</span></span>

<span data-ttu-id="f234a-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f234a-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f234a-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="f234a-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f234a-106">Das Transportprotokoll wird von der **get \_ transportprotocol** -Methode abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f234a-106">The **get\_TransportProtocol** method gets the transport protocol.</span></span> <span data-ttu-id="f234a-107">Diese Angabe wird zusätzlich zum Medienformat angegeben, sodass dasselbe Standard Medienformat auch dann über verschiedene Transportprotokolle übertragen werden kann, wenn das Netzwerkprotokoll identisch ist, z. b. mit der Mehrwertsteuer-und RTP-PCM-Audiodatei.</span><span class="sxs-lookup"><span data-stu-id="f234a-107">This is specified in addition to the media format so that the same standard media format may be carried over different transport protocols even when the network protocol is the same, such as with Vat PCM audio and RTP PCM audio.</span></span>

## <a name="syntax"></a><span data-ttu-id="f234a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f234a-108">Syntax</span></span>


```C++
HRESULT get_TransportProtocol(
  [out] BSTR *ppProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="f234a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f234a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f234a-110">*ppprotocol* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f234a-110">*ppProtocol* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f234a-111">Ein Zeiger auf die **BSTR** -Darstellung des Transport Protokolls.</span><span class="sxs-lookup"><span data-stu-id="f234a-111">Pointer to the **BSTR** representation of the transport protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f234a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f234a-112">Return value</span></span>

<span data-ttu-id="f234a-113">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f234a-113">This method can return one of these values.</span></span>



| <span data-ttu-id="f234a-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f234a-114">Return code</span></span>                                                                                   | <span data-ttu-id="f234a-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f234a-115">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="f234a-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f234a-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f234a-117">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f234a-117">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f234a-118"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="f234a-118"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f234a-119">Der *ppprotocol* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="f234a-119">The *ppProtocol* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="f234a-120"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="f234a-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f234a-121">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f234a-121">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="f234a-122"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="f234a-122"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="f234a-123">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="f234a-123">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="f234a-124"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="f234a-124"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="f234a-125">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f234a-125">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="f234a-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f234a-126">Remarks</span></span>

<span data-ttu-id="f234a-127">Die Anwendung muss [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den für den *ppprotocol* -Parameter belegten Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="f234a-127">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppProtocol* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="f234a-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f234a-128">Requirements</span></span>



| <span data-ttu-id="f234a-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f234a-129">Requirement</span></span> | <span data-ttu-id="f234a-130">Wert</span><span class="sxs-lookup"><span data-stu-id="f234a-130">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f234a-131">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="f234a-131">TAPI version</span></span><br/> | <span data-ttu-id="f234a-132">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="f234a-132">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="f234a-133">Header</span><span class="sxs-lookup"><span data-stu-id="f234a-133">Header</span></span><br/>       | <dl> <span data-ttu-id="f234a-134"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="f234a-134"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="f234a-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f234a-135">Library</span></span><br/>      | <dl> <span data-ttu-id="f234a-136"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f234a-136"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="f234a-137">DLL</span><span class="sxs-lookup"><span data-stu-id="f234a-137">DLL</span></span><br/>          | <dl> <span data-ttu-id="f234a-138"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f234a-138"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f234a-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f234a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f234a-140">**ITmedia**</span><span class="sxs-lookup"><span data-stu-id="f234a-140">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="f234a-141">**ITmedia::p UT \_ transportprotocol**</span><span class="sxs-lookup"><span data-stu-id="f234a-141">**ITMedia::put\_TransportProtocol**</span></span>](itmedia-put-transportprotocol.md)
</dt> </dl>

 

