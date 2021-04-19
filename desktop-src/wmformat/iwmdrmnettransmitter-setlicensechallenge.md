---
title: Iwmdrmnettransmitter setlicensechallenge-Methode (wmdrmsdk. h)
description: Die setlicensechallenge-Methode verarbeitet eine Lizenz Herausforderung, die von einem Windows Media DRM für den Empfänger von Netzwerkgeräten gesendet wird.
ms.assetid: 3d4cd029-a8f5-49fc-ba8c-d8615ff94366
keywords:
- Setlicensechallenge-Methode, Windows Media-Format
- Setlicensechallenge-Methode Windows Media-Format, iwmdrmnettransmitter-Schnittstelle
- Iwmdrmnettransmitter-Schnittstelle Windows Media-Format, setlicensechallenge-Methode
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.SetLicenseChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94b83ca615896039a592d147fe8c14d15493cec0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367582"
---
# <a name="iwmdrmnettransmittersetlicensechallenge-method"></a><span data-ttu-id="10b1a-106">Iwmdrmnettransmitter:: setlicensechallenge-Methode</span><span class="sxs-lookup"><span data-stu-id="10b1a-106">IWMDRMNetTransmitter::SetLicenseChallenge method</span></span>

<span data-ttu-id="10b1a-107">Die **setlicensechallenge** -Methode verarbeitet eine Lizenz Herausforderung, die von einem Windows Media DRM für den Empfänger von Netzwerkgeräten gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="10b1a-107">The **SetLicenseChallenge** method processes a license challenge sent by a Windows Media DRM for Network Devices receiver.</span></span>

## <a name="syntax"></a><span data-ttu-id="10b1a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="10b1a-108">Syntax</span></span>


```C++
HRESULT SetLicenseChallenge(
  [in] BYTE  *pbLicenseChallenge,
  [in] DWORD cbLicenseChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="10b1a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="10b1a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10b1a-110">*pblicenabchallenge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10b1a-110">*pbLicenseChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10b1a-111">Zeiger auf die Lizenz Aufforderungs Daten, die von einem Empfänger gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="10b1a-111">Pointer to the license challenge data that was sent by a receiver.</span></span>

</dd> <dt>

<span data-ttu-id="10b1a-112">*cblicenanchallenge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10b1a-112">*cbLicenseChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10b1a-113">Die Größe der Lizenz Herausforderung in Bytes.</span><span class="sxs-lookup"><span data-stu-id="10b1a-113">Size of license challenge in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10b1a-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="10b1a-114">Return value</span></span>

<span data-ttu-id="10b1a-115">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="10b1a-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="10b1a-116">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="10b1a-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="10b1a-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="10b1a-117">Return code</span></span>                                                                          | <span data-ttu-id="10b1a-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10b1a-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="10b1a-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="10b1a-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="10b1a-120">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="10b1a-120">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="10b1a-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="10b1a-121">Remarks</span></span>

<span data-ttu-id="10b1a-122">Wenn diese Methode erfolgreich ausgeführt wird, werden bei nachfolgenden Aufrufen der anderen Methoden von **iwmdrmnettransmitter** die Informationen in der verarbeiteten Abfrage verwendet.</span><span class="sxs-lookup"><span data-stu-id="10b1a-122">If this method succeeds, subsequent calls to the other methods of **IWMDRMNetTransmitter** will use the information in the processed challenge.</span></span>

## <a name="requirements"></a><span data-ttu-id="10b1a-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="10b1a-123">Requirements</span></span>



| <span data-ttu-id="10b1a-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="10b1a-124">Requirement</span></span> | <span data-ttu-id="10b1a-125">Wert</span><span class="sxs-lookup"><span data-stu-id="10b1a-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="10b1a-126">Header</span><span class="sxs-lookup"><span data-stu-id="10b1a-126">Header</span></span><br/> | <dl> <span data-ttu-id="10b1a-127"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="10b1a-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10b1a-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10b1a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10b1a-129">**Iwmdrmnettransmitter-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="10b1a-129">**IWMDRMNetTransmitter Interface**</span></span>](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





