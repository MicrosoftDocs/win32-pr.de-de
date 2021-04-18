---
title: Iwmdrmnetreceiver processregistrationresponse-Methode (wmdrmsdk. h)
description: Die Methode processregistrationresponse verarbeitet eine vom Sender gesendete Registrierungs Antwort als Antwort auf eine Registrierungs Aufforderung.
ms.assetid: d0260e93-0a5e-494b-a723-bb62206ed55b
keywords:
- Processregistrationresponse-Methode Windows Media-Format
- Processregistrationresponse-Methode Windows Media-Format, iwmdrmnetreceiver-Schnittstelle
- Iwmdrmnetreceiver-Schnittstelle Windows Media-Format, processregistrationresponse-Methode
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.ProcessRegistrationResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a77b01f443d57825d82b7cf9556d7585745bb99e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358271"
---
# <a name="iwmdrmnetreceiverprocessregistrationresponse-method"></a><span data-ttu-id="908ce-106">Iwmdrmnetreceiver::P rocess RegistrationResponse-Methode</span><span class="sxs-lookup"><span data-stu-id="908ce-106">IWMDRMNetReceiver::ProcessRegistrationResponse method</span></span>

<span data-ttu-id="908ce-107">Die Methode **processregistrationresponse** verarbeitet eine vom Sender gesendete Registrierungs Antwort als Antwort auf eine Registrierungs Aufforderung.</span><span class="sxs-lookup"><span data-stu-id="908ce-107">The **ProcessRegistrationResponse** method processes a registration response sent by the transmitter in reply to a registration challenge.</span></span>

## <a name="syntax"></a><span data-ttu-id="908ce-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="908ce-108">Syntax</span></span>


```C++
HRESULT ProcessRegistrationResponse(
  [in]  BYTE     *pbRegistrationResponse,
  [in]  DWORD    cbRegistrationResponse,
  [out] IUnknown **ppunkCancellationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="908ce-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="908ce-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="908ce-110">*pbregistrationresponse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="908ce-110">*pbRegistrationResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="908ce-111">Vom Sender empfangene Registrierungs Antwort.</span><span class="sxs-lookup"><span data-stu-id="908ce-111">Registration response received from the transmitter.</span></span>

</dd> <dt>

<span data-ttu-id="908ce-112">*cbregistrationresponse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="908ce-112">*cbRegistrationResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="908ce-113">Größe der Registrierungs Antwort in Bytes.</span><span class="sxs-lookup"><span data-stu-id="908ce-113">Size of the registration response in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="908ce-114">*ppunkcancellationcookie* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="908ce-114">*ppunkCancellationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="908ce-115">Ein Zeiger, der einen Zeiger auf die **IUnknown** -Schnittstelle eines Objekts empfängt, das diesen asynchronen-Befehl identifiziert.</span><span class="sxs-lookup"><span data-stu-id="908ce-115">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="908ce-116">Dieser Schnittstellen Zeiger kann zum Abbrechen des asynchronen Aufrufs verwendet werden, indem die [**iwmdrmeventgenerator:: cancelasyncoperation**](iwmdrmeventgenerator-cancelasyncoperation.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="908ce-116">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="908ce-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="908ce-117">Return value</span></span>

<span data-ttu-id="908ce-118">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="908ce-118">The method returns an **HRESULT**.</span></span> <span data-ttu-id="908ce-119">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="908ce-119">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="908ce-120">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="908ce-120">Return code</span></span>                                                                          | <span data-ttu-id="908ce-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="908ce-121">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="908ce-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="908ce-122"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="908ce-123">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="908ce-123">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="908ce-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="908ce-124">Remarks</span></span>

<span data-ttu-id="908ce-125">Diese Methode wird asynchron ausgeführt. Wenn die Verarbeitung abgeschlossen ist, wird das meproximitycomplete-Ereignis an die **imfmediaeventgenerator** -Schnittstelle gesendet.</span><span class="sxs-lookup"><span data-stu-id="908ce-125">This method executes asynchronously; when processing is complete, the MEProximityCompleted event is sent to the **IMFMediaEventGenerator** interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="908ce-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="908ce-126">Requirements</span></span>



| <span data-ttu-id="908ce-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="908ce-127">Requirement</span></span> | <span data-ttu-id="908ce-128">Wert</span><span class="sxs-lookup"><span data-stu-id="908ce-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="908ce-129">Header</span><span class="sxs-lookup"><span data-stu-id="908ce-129">Header</span></span><br/> | <dl> <span data-ttu-id="908ce-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="908ce-130"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="908ce-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="908ce-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="908ce-132">**Iwmdrmnetreceiver-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="908ce-132">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> <dt>

[<span data-ttu-id="908ce-133">**Iwmdrmnetreceiver:: getregistrationchallenge**</span><span class="sxs-lookup"><span data-stu-id="908ce-133">**IWMDRMNetReceiver::GetRegistrationChallenge**</span></span>](iwmdrmnetreceiver-getregistrationchallenge.md)
</dt> </dl>

 

 





