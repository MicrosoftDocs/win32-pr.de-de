---
description: Mit der Put \_ MEDIANAME-Methode wird der Medien Name festgelegt. Definierte Medien sind Audiodaten, Videos, Whiteboards, Text und Daten.
ms.assetid: 0dd18add-6c7e-40a8-8b39-10c65bdfb2e0
title: ITmedia::p ut_MediaName-Methode (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66dcbd4e29f59694d610fb4e6af9fd49aa53323d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373702"
---
# <a name="itmediaput_medianame-method"></a><span data-ttu-id="3d17b-104">ITmedia::p UT \_ MEDIANAME-Methode</span><span class="sxs-lookup"><span data-stu-id="3d17b-104">ITMedia::put\_MediaName method</span></span>

<span data-ttu-id="3d17b-105">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3d17b-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3d17b-106">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="3d17b-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="3d17b-107">Mit der **Put \_ MEDIANAME** -Methode wird der Medien Name festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3d17b-107">The **put\_MediaName** method sets the media name.</span></span> <span data-ttu-id="3d17b-108">Definierte Medien sind Audiodaten, Videos, Whiteboards, Text und Daten.</span><span class="sxs-lookup"><span data-stu-id="3d17b-108">Defined media are audio, video, whiteboard, text, and data.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d17b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d17b-109">Syntax</span></span>


```C++
HRESULT put_MediaName(
  [in] BSTR pMediaName
);
```



## <a name="parameters"></a><span data-ttu-id="3d17b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d17b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d17b-111">*pmedianame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d17b-111">*pMediaName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d17b-112">Zeiger auf einen **BSTR** -Wert, der den festzulegenden Mediennamen enthält.</span><span class="sxs-lookup"><span data-stu-id="3d17b-112">Pointer to a **BSTR** containing the media name to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d17b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3d17b-113">Return value</span></span>

<span data-ttu-id="3d17b-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="3d17b-114">This method can return one of these values.</span></span>



| <span data-ttu-id="3d17b-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="3d17b-115">Return code</span></span>                                                                                   | <span data-ttu-id="3d17b-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d17b-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="3d17b-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3d17b-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3d17b-118">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="3d17b-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="3d17b-119"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="3d17b-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="3d17b-120">Der *pmedianame* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="3d17b-120">The *pMediaName* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="3d17b-121"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="3d17b-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3d17b-122">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="3d17b-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="3d17b-123"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="3d17b-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="3d17b-124">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="3d17b-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="3d17b-125"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="3d17b-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="3d17b-126">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="3d17b-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="3d17b-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d17b-127">Remarks</span></span>

<span data-ttu-id="3d17b-128">Die Anwendung muss " [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) " verwenden, um Speicher für den *pmedianame* -Parameter zuzuweisen, und " [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) " verwenden, um den Arbeitsspeicher freizugeben, wenn die Variable nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="3d17b-128">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pMediaName* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="3d17b-129">Diese Funktion kann Daten in unverschlüsselter Form über das Netzwerk senden. aus diesem Grund kann ein Benutzer, der sich im Netzwerk befindet, möglicherweise die Daten lesen.</span><span class="sxs-lookup"><span data-stu-id="3d17b-129">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="3d17b-130">Das Sicherheitsrisiko, dass Daten im Klartext gesendet werden, sollte vor der Verwendung dieser Methode berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="3d17b-130">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d17b-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d17b-131">Requirements</span></span>



| <span data-ttu-id="3d17b-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d17b-132">Requirement</span></span> | <span data-ttu-id="3d17b-133">Wert</span><span class="sxs-lookup"><span data-stu-id="3d17b-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3d17b-134">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="3d17b-134">TAPI version</span></span><br/> | <span data-ttu-id="3d17b-135">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="3d17b-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="3d17b-136">Header</span><span class="sxs-lookup"><span data-stu-id="3d17b-136">Header</span></span><br/>       | <dl> <span data-ttu-id="3d17b-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d17b-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="3d17b-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3d17b-138">Library</span></span><br/>      | <dl> <span data-ttu-id="3d17b-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3d17b-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="3d17b-140">DLL</span><span class="sxs-lookup"><span data-stu-id="3d17b-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="3d17b-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d17b-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d17b-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d17b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d17b-143">**ITmedia**</span><span class="sxs-lookup"><span data-stu-id="3d17b-143">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="3d17b-144">**ITmedia:: get \_ MEDIANAME**</span><span class="sxs-lookup"><span data-stu-id="3d17b-144">**ITMedia::get\_MediaName**</span></span>](itmedia-get-medianame.md)
</dt> </dl>

 

