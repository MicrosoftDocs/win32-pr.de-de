---
description: Die Put \_ transportprotocol-Methode legt das Transportprotokoll fest.
ms.assetid: d2f74d4a-a65d-4829-ad17-7548ef06cfeb
title: ITmedia::p ut_TransportProtocol-Methode (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c6b4228a5d2a6ea49ae3f87b9306ea80e94fc36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366713"
---
# <a name="itmediaput_transportprotocol-method"></a><span data-ttu-id="d4fe4-103">ITmedia::p UT \_ transportprotocol-Methode</span><span class="sxs-lookup"><span data-stu-id="d4fe4-103">ITMedia::put\_TransportProtocol method</span></span>

<span data-ttu-id="d4fe4-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d4fe4-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d4fe4-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="d4fe4-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="d4fe4-106">Die **Put \_ transportprotocol** -Methode legt das Transportprotokoll fest.</span><span class="sxs-lookup"><span data-stu-id="d4fe4-106">The **put\_TransportProtocol** method sets the transport protocol.</span></span> <span data-ttu-id="d4fe4-107">Diese Angabe wird zusätzlich zum Medienformat angegeben, sodass dasselbe Standard Medienformat auch dann über verschiedene Transportprotokolle übertragen werden kann, wenn das Netzwerkprotokoll identisch ist, z. b. mit der Mehrwertsteuer-und RTP-PCM-Audiodatei.</span><span class="sxs-lookup"><span data-stu-id="d4fe4-107">This is specified in addition to the media format so that the same standard media format may be carried over different transport protocols even when the network protocol is the same, such as with Vat PCM audio and RTP PCM audio.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4fe4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4fe4-108">Syntax</span></span>


```C++
HRESULT put_TransportProtocol(
  [in] BSTR pProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="d4fe4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4fe4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4fe4-110">*pprotocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d4fe4-110">*pProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4fe4-111">Zeiger auf ein **BSTR** , das das Transportprotokoll enthält.</span><span class="sxs-lookup"><span data-stu-id="d4fe4-111">Pointer to a **BSTR** containing the transport protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4fe4-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d4fe4-112">Return value</span></span>

<span data-ttu-id="d4fe4-113">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="d4fe4-113">This method can return one of these values.</span></span>



| <span data-ttu-id="d4fe4-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d4fe4-114">Return code</span></span>                                                                                   | <span data-ttu-id="d4fe4-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d4fe4-115">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="d4fe4-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d4fe4-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d4fe4-117">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="d4fe4-117">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="d4fe4-118"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="d4fe4-118"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d4fe4-119">Der *pprotocol* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="d4fe4-119">The *pProtocol* parameter is not a valid pointer.</span></span><br/>    |
| <dl> <span data-ttu-id="d4fe4-120"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="d4fe4-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d4fe4-121">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d4fe4-121">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="d4fe4-122"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="d4fe4-122"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="d4fe4-123">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="d4fe4-123">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="d4fe4-124"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="d4fe4-124"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="d4fe4-125">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="d4fe4-125">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="d4fe4-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4fe4-126">Remarks</span></span>

<span data-ttu-id="d4fe4-127">Die Anwendung muss " [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) " verwenden, um Speicher für den *pprotocol* -Parameter zuzuweisen, und " [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) " verwenden, um den Arbeitsspeicher freizugeben, wenn die Variable nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="d4fe4-127">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pProtocol* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="d4fe4-128">Diese Funktion kann Daten in unverschlüsselter Form über das Netzwerk senden. aus diesem Grund kann ein Benutzer, der sich im Netzwerk befindet, möglicherweise die Daten lesen.</span><span class="sxs-lookup"><span data-stu-id="d4fe4-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="d4fe4-129">Das Sicherheitsrisiko, dass Daten im Klartext gesendet werden, sollte vor der Verwendung dieser Methode berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="d4fe4-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4fe4-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4fe4-130">Requirements</span></span>



| <span data-ttu-id="d4fe4-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4fe4-131">Requirement</span></span> | <span data-ttu-id="d4fe4-132">Wert</span><span class="sxs-lookup"><span data-stu-id="d4fe4-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d4fe4-133">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="d4fe4-133">TAPI version</span></span><br/> | <span data-ttu-id="d4fe4-134">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="d4fe4-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="d4fe4-135">Header</span><span class="sxs-lookup"><span data-stu-id="d4fe4-135">Header</span></span><br/>       | <dl> <span data-ttu-id="d4fe4-136"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4fe4-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="d4fe4-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d4fe4-137">Library</span></span><br/>      | <dl> <span data-ttu-id="d4fe4-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4fe4-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="d4fe4-139">DLL</span><span class="sxs-lookup"><span data-stu-id="d4fe4-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="d4fe4-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4fe4-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4fe4-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4fe4-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4fe4-142">**ITmedia**</span><span class="sxs-lookup"><span data-stu-id="d4fe4-142">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="d4fe4-143">**ITmedia:: get \_ transportprotocol**</span><span class="sxs-lookup"><span data-stu-id="d4fe4-143">**ITMedia::get\_TransportProtocol**</span></span>](itmedia-get-transportprotocol.md)
</dt> </dl>

 

