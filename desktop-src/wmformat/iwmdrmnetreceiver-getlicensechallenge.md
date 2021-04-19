---
title: Iwmdrmnetreceiver getlicensechallenge-Methode (wmdrmsdk. h)
description: Mit der getlicencchallenge-Methode wird eine Windows Media DRM for Network Devices-Lizenz Aufforderung generiert, die beim Anfordern geschützter Inhalte an einen Sender gesendet werden kann.
ms.assetid: c13b9e9e-b076-411b-a106-b602544faaba
keywords:
- Getlicencchallenge-Methode, Windows Media-Format
- Getlicensechallenge-Methode, Windows Media-Format, iwmdrmnetreceiver-Schnittstelle
- Iwmdrmnetreceiver-Schnittstelle Windows Media-Format, getlicensechallenge-Methode
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.GetLicenseChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61f58b85b8dc5edd6c23e809dda8c18bf30137f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370590"
---
# <a name="iwmdrmnetreceivergetlicensechallenge-method"></a><span data-ttu-id="7a06f-106">Iwmdrmnetreceiver:: getlicensechallenge-Methode</span><span class="sxs-lookup"><span data-stu-id="7a06f-106">IWMDRMNetReceiver::GetLicenseChallenge method</span></span>

<span data-ttu-id="7a06f-107">Mit der **getlicencchallenge** -Methode wird eine Windows Media DRM for Network Devices-Lizenz Aufforderung generiert, die beim Anfordern geschützter Inhalte an einen Sender gesendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7a06f-107">The **GetLicenseChallenge** method generates a Windows Media DRM for Network Devices license challenge that can be sent to a transmitter when requesting protected content.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a06f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a06f-108">Syntax</span></span>


```C++
HRESULT GetLicenseChallenge(
  [in]  BSTR  bstrAction,
  [out] BYTE  **ppbLicenseChallenge,
  [out] DWORD *pcbLicenseChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="7a06f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a06f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a06f-110">*bstrAction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7a06f-110">*bstrAction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a06f-111">Die Aktion, für die die Herausforderung generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7a06f-111">Action for which to generate the challenge.</span></span>

</dd> <dt>

<span data-ttu-id="7a06f-112">*ppblicenabchallenge* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7a06f-112">*ppbLicenseChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a06f-113">Adresse eines Zeigers, der auf die Adresse der generierten Challenge festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7a06f-113">Address of a pointer that is set to the address of the generated challenge.</span></span> <span data-ttu-id="7a06f-114">Wenn Sie mit diesen Daten fertig sind, müssen Sie den Arbeitsspeicher freigeben, indem Sie " **CoTaskMemFree**" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7a06f-114">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span>

</dd> <dt>

<span data-ttu-id="7a06f-115">*pcblicenanchallenge* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7a06f-115">*pcbLicenseChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a06f-116">Adresse einer Variablen, die die Größe der Lizenz Herausforderung in Bytes erhält.</span><span class="sxs-lookup"><span data-stu-id="7a06f-116">Address of a variable that receives the size of the license challenge in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a06f-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7a06f-117">Return value</span></span>

<span data-ttu-id="7a06f-118">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="7a06f-118">The method returns an **HRESULT**.</span></span> <span data-ttu-id="7a06f-119">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7a06f-119">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="7a06f-120">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7a06f-120">Return code</span></span>                                                                          | <span data-ttu-id="7a06f-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7a06f-121">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="7a06f-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7a06f-122"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="7a06f-123">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7a06f-123">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7a06f-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a06f-124">Remarks</span></span>

<span data-ttu-id="7a06f-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="7a06f-125">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a06f-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a06f-126">Requirements</span></span>



| <span data-ttu-id="7a06f-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a06f-127">Requirement</span></span> | <span data-ttu-id="7a06f-128">Wert</span><span class="sxs-lookup"><span data-stu-id="7a06f-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7a06f-129">Header</span><span class="sxs-lookup"><span data-stu-id="7a06f-129">Header</span></span><br/> | <dl> <span data-ttu-id="7a06f-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a06f-130"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a06f-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a06f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a06f-132">**Iwmdrmnetreceiver-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="7a06f-132">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> <dt>

[<span data-ttu-id="7a06f-133">**Iwmdrmnetreceiver::P rocess licenseresponse**</span><span class="sxs-lookup"><span data-stu-id="7a06f-133">**IWMDRMNetReceiver::ProcessLicenseResponse**</span></span>](iwmdrmnetreceiver-processlicenseresponse.md)
</dt> </dl>

 

 





