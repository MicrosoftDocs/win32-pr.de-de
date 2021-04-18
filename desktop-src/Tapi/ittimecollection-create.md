---
description: Die Create-Methode erstellt eine neue ittime-Komponente.
ms.assetid: dee50454-8358-4898-b098-2de51505b658
title: 'Ittimecollection:: Create-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df62bbc8f1ad2a24a9b80a7f5d0a25bc01f713d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357627"
---
# <a name="ittimecollectioncreate-method"></a><span data-ttu-id="b7da8-103">Ittimecollection:: Create-Methode</span><span class="sxs-lookup"><span data-stu-id="b7da8-103">ITTimeCollection::Create method</span></span>

<span data-ttu-id="b7da8-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b7da8-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b7da8-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="b7da8-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b7da8-106">Die **Create** -Methode erstellt eine neue [**ittime**](ittime.md) -Komponente.</span><span class="sxs-lookup"><span data-stu-id="b7da8-106">The **Create** method creates a new [**ITTime**](ittime.md) component.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7da8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7da8-107">Syntax</span></span>


```C++
HRESULT Create(
  [in]  LONG   Index,
  [out] ITTime **ppTime
);
```



## <a name="parameters"></a><span data-ttu-id="b7da8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7da8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7da8-109">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b7da8-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7da8-110">Der Index des zu erstellenden Elements.</span><span class="sxs-lookup"><span data-stu-id="b7da8-110">Index of the item to create.</span></span> <span data-ttu-id="b7da8-111">(Das Index Array ist 1-basiert.)</span><span class="sxs-lookup"><span data-stu-id="b7da8-111">(The index array is one-based.)</span></span>

</dd> <dt>

<span data-ttu-id="b7da8-112">*pptime* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b7da8-112">*ppTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7da8-113">Zeiger auf die erstellte b-Komponente.</span><span class="sxs-lookup"><span data-stu-id="b7da8-113">Pointer to the b component created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7da8-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b7da8-114">Return value</span></span>

<span data-ttu-id="b7da8-115">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="b7da8-115">This method can return one of these values.</span></span>



| <span data-ttu-id="b7da8-116">Wert</span><span class="sxs-lookup"><span data-stu-id="b7da8-116">Value</span></span>                                                                                         | <span data-ttu-id="b7da8-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b7da8-117">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="b7da8-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b7da8-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b7da8-119">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="b7da8-119">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b7da8-120"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="b7da8-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b7da8-121">Der *pptime* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="b7da8-121">The *ppTime* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="b7da8-122"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="b7da8-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="b7da8-123">Der *Index* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="b7da8-123">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="b7da8-124"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="b7da8-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b7da8-125">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b7da8-125">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="b7da8-126"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="b7da8-126"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="b7da8-127">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="b7da8-127">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="b7da8-128"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="b7da8-128"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="b7da8-129">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="b7da8-129">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="b7da8-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b7da8-130">Remarks</span></span>

<span data-ttu-id="b7da8-131">TAPI Ruft die **adressf** -Methode für die [**ittime**](ittime.md) -Schnittstelle auf, die von **ittimecollection:: Create** zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="b7da8-131">TAPI calls the **AddRef** method on the [**ITTime**](ittime.md) interface returned by **ITTimeCollection::Create**.</span></span> <span data-ttu-id="b7da8-132">Die Anwendung muss Release auf der v-Schnittstelle aufzurufen, um Ressourcen frei **zugeben** , die ihr zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b7da8-132">The application must call **Release** on the v interface to free resources associated with it.</span></span>

<span data-ttu-id="b7da8-133">Diese Funktion kann Daten in unverschlüsselter Form über das Netzwerk senden. aus diesem Grund kann ein Benutzer, der sich im Netzwerk befindet, möglicherweise die Daten lesen.</span><span class="sxs-lookup"><span data-stu-id="b7da8-133">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="b7da8-134">Das Sicherheitsrisiko, dass Daten im Klartext gesendet werden, sollte vor der Verwendung dieser Methode berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="b7da8-134">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7da8-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7da8-135">Requirements</span></span>



| <span data-ttu-id="b7da8-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b7da8-136">Requirement</span></span> | <span data-ttu-id="b7da8-137">Wert</span><span class="sxs-lookup"><span data-stu-id="b7da8-137">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b7da8-138">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="b7da8-138">TAPI version</span></span><br/> | <span data-ttu-id="b7da8-139">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="b7da8-139">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="b7da8-140">Header</span><span class="sxs-lookup"><span data-stu-id="b7da8-140">Header</span></span><br/>       | <dl> <span data-ttu-id="b7da8-141"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7da8-141"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="b7da8-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b7da8-142">Library</span></span><br/>      | <dl> <span data-ttu-id="b7da8-143"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7da8-143"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="b7da8-144">DLL</span><span class="sxs-lookup"><span data-stu-id="b7da8-144">DLL</span></span><br/>          | <dl> <span data-ttu-id="b7da8-145"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7da8-145"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7da8-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7da8-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7da8-147">**Ittimecollection**</span><span class="sxs-lookup"><span data-stu-id="b7da8-147">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="b7da8-148">**Ittime**</span><span class="sxs-lookup"><span data-stu-id="b7da8-148">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

 




