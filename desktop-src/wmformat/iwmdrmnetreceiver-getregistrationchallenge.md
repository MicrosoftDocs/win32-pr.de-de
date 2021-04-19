---
title: Iwmdrmnetreceiver getregistrationchallenge-Methode (wmdrmsdk. h)
description: Mit der getregistrationchallenge-Methode wird eine Anforderungs Nachricht für die Registrierung von Windows Media DRM für Netzwerkgeräte generiert.
ms.assetid: 7b3641a1-ccc5-4e29-b0e9-808b111f8841
keywords:
- Getregistrationchallenge-Methode Windows Media-Format
- Getregistrationchallenge-Methode Windows Media-Format, iwmdrmnetreceiver-Schnittstelle
- Iwmdrmnetreceiver-Schnittstelle Windows Media-Format, getregistrationchallenge-Methode
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.GetRegistrationChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a292749e95ca6ba2dabc8f3829eae827dbdd8325
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356034"
---
# <a name="iwmdrmnetreceivergetregistrationchallenge-method"></a><span data-ttu-id="c2d17-106">Iwmdrmnetreceiver:: getregistrationchallenge-Methode</span><span class="sxs-lookup"><span data-stu-id="c2d17-106">IWMDRMNetReceiver::GetRegistrationChallenge method</span></span>

<span data-ttu-id="c2d17-107">Mit der **getregistrationchallenge** -Methode wird eine Anforderungs Nachricht für die Registrierung von Windows Media DRM für Netzwerkgeräte generiert.</span><span class="sxs-lookup"><span data-stu-id="c2d17-107">The **GetRegistrationChallenge** method generates a Windows Media DRM for Network Devices registration challenge message.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2d17-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2d17-108">Syntax</span></span>


```C++
HRESULT GetRegistrationChallenge(
  [out] BYTE  **ppbRegistrationChallenge,
  [out] DWORD *pcbRegistrationChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="c2d17-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2d17-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2d17-110">*ppbregistrationchallenge* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c2d17-110">*ppbRegistrationChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2d17-111">Adresse eines Zeigers, der die Adresse der generierten Herausforderung empfängt.</span><span class="sxs-lookup"><span data-stu-id="c2d17-111">Address of a pointer that receives the address of the generated challenge.</span></span> <span data-ttu-id="c2d17-112">Wenn Sie mit diesen Daten fertig sind, müssen Sie den Arbeitsspeicher freigeben, indem Sie " **CoTaskMemFree**" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c2d17-112">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span>

</dd> <dt>

<span data-ttu-id="c2d17-113">*pcbregistrationchallenge* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c2d17-113">*pcbRegistrationChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2d17-114">Adresse einer Variablen, die die Größe der Registrierungs Herausforderung in Bytes empfängt.</span><span class="sxs-lookup"><span data-stu-id="c2d17-114">Address of a variable that receives the size of the registration challenge in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2d17-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c2d17-115">Return value</span></span>

<span data-ttu-id="c2d17-116">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="c2d17-116">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c2d17-117">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c2d17-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c2d17-118">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c2d17-118">Return code</span></span>                                                                          | <span data-ttu-id="c2d17-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2d17-119">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="c2d17-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c2d17-120"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c2d17-121">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2d17-121">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c2d17-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2d17-122">Remarks</span></span>

<span data-ttu-id="c2d17-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="c2d17-123">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2d17-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2d17-124">Requirements</span></span>



| <span data-ttu-id="c2d17-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2d17-125">Requirement</span></span> | <span data-ttu-id="c2d17-126">Wert</span><span class="sxs-lookup"><span data-stu-id="c2d17-126">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c2d17-127">Header</span><span class="sxs-lookup"><span data-stu-id="c2d17-127">Header</span></span><br/> | <dl> <span data-ttu-id="c2d17-128"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2d17-128"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2d17-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2d17-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2d17-130">**Iwmdrmnetreceiver-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c2d17-130">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> <dt>

[<span data-ttu-id="c2d17-131">**Iwmdrmnetreceiver::P rocess RegistrationResponse**</span><span class="sxs-lookup"><span data-stu-id="c2d17-131">**IWMDRMNetReceiver::ProcessRegistrationResponse**</span></span>](iwmdrmnetreceiver-processregistrationresponse.md)
</dt> </dl>

 

 





