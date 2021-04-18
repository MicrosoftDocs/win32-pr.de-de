---
title: Iwmdrmnetreceiver processlicenseresponse-Methode (wmdrmsdk. h)
description: Die processlicenseresponse-Methode verarbeitet die vom Sender gesendete Lizenz Antwort als Antwort auf eine Lizenz Herausforderung.
ms.assetid: b6d04651-746b-474e-8a02-6b7cbee9db46
keywords:
- Processlicenseresponse-Methode Windows Media-Format
- Processlicenseresponse-Methode, Windows Media-Format, iwmdrmnetreceiver-Schnittstelle
- Iwmdrmnetreceiver-Schnittstelle Windows Media-Format, processlicenseresponse-Methode
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.ProcessLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45a09ebab81b71e21b9ef922423a7bbe67b20596
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357563"
---
# <a name="iwmdrmnetreceiverprocesslicenseresponse-method"></a><span data-ttu-id="41c57-106">Iwmdrmnetreceiver::P rocess licenseresponse-Methode</span><span class="sxs-lookup"><span data-stu-id="41c57-106">IWMDRMNetReceiver::ProcessLicenseResponse method</span></span>

<span data-ttu-id="41c57-107">Die **processlicenseresponse** -Methode verarbeitet die vom Sender gesendete Lizenz Antwort als Antwort auf eine Lizenz Herausforderung.</span><span class="sxs-lookup"><span data-stu-id="41c57-107">The **ProcessLicenseResponse** method processes the license response that is sent by the transmitter in reply to a license challenge.</span></span>

## <a name="syntax"></a><span data-ttu-id="41c57-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="41c57-108">Syntax</span></span>


```C++
HRESULT ProcessLicenseResponse(
  [in]  BYTE  *pbLicenseResponse,
  [in]  DWORD cbLicenseResponse,
  [out] BYTE  **ppbWMDRMNetLicenseRepresentation,
  [out] DWORD *pcbWMDRMNetLicenseRepresentation
);
```



## <a name="parameters"></a><span data-ttu-id="41c57-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="41c57-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41c57-110">*pblicenseresponse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41c57-110">*pbLicenseResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41c57-111">Vom Sender empfangene Lizenz Antwort.</span><span class="sxs-lookup"><span data-stu-id="41c57-111">License response received from the transmitter.</span></span>

</dd> <dt>

<span data-ttu-id="41c57-112">*cblicenseresponse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41c57-112">*cbLicenseResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41c57-113">Größe der Antwort in Bytes.</span><span class="sxs-lookup"><span data-stu-id="41c57-113">Size of the response in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="41c57-114">*ppbwmdrmnetlicenserepresentation* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="41c57-114">*ppbWMDRMNetLicenseRepresentation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41c57-115">Adresse einer Variablen, die die Adresse der internen Lizenz Darstellung für die in der Lizenz Antwortnachricht enthaltene Lizenz empfängt.</span><span class="sxs-lookup"><span data-stu-id="41c57-115">Address of a variable that receives the address of the internal license representation for the license contained in the license response message.</span></span> <span data-ttu-id="41c57-116">Wenn Sie mit diesen Daten fertig sind, müssen Sie den Arbeitsspeicher freigeben, indem Sie " **CoTaskMemFree**" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="41c57-116">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span> <span data-ttu-id="41c57-117">Dieser Parameter kann auf **null** festgelegt werden, wenn die Lizenz Darstellung nicht benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="41c57-117">This parameter may be set to **NULL** if the license representation is not needed.</span></span>

</dd> <dt>

<span data-ttu-id="41c57-118">*pcbwmdrmnetlicenserepresentation* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="41c57-118">*pcbWMDRMNetLicenseRepresentation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41c57-119">Adresse einer Variablen, die die Größe der Lizenz Darstellung erhält.</span><span class="sxs-lookup"><span data-stu-id="41c57-119">Address of a variable that receives the size of the license representation.</span></span> <span data-ttu-id="41c57-120">Muss auf **null** festgelegt werden, wenn *ppbwmdrmnetlicenserepresentation* **null** ist.</span><span class="sxs-lookup"><span data-stu-id="41c57-120">Must be set to **NULL** if *ppbWMDRMNetLicenseRepresentation* is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41c57-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="41c57-121">Return value</span></span>

<span data-ttu-id="41c57-122">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="41c57-122">The method returns an **HRESULT**.</span></span> <span data-ttu-id="41c57-123">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="41c57-123">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="41c57-124">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="41c57-124">Return code</span></span>                                                                                                | <span data-ttu-id="41c57-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="41c57-125">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="41c57-126"><dt>**NS \_ E \_ DRM- \_ RIV \_ zu \_ klein**</dt></span><span class="sxs-lookup"><span data-stu-id="41c57-126"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="41c57-127">Es wird eine aktualisierte Inhalts Sperr Liste benötigt.</span><span class="sxs-lookup"><span data-stu-id="41c57-127">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="41c57-128"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="41c57-128"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="41c57-129">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="41c57-129">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="41c57-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41c57-130">Remarks</span></span>

<span data-ttu-id="41c57-131">Die mit dieser Methode verarbeitete Lizenz Antwort muss der letzten Lizenz Herausforderung entsprechen, die auf dem Client Computer generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="41c57-131">The license response processed by using this method must correspond to the last license challenge generated on the client computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="41c57-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41c57-132">Requirements</span></span>



| <span data-ttu-id="41c57-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41c57-133">Requirement</span></span> | <span data-ttu-id="41c57-134">Wert</span><span class="sxs-lookup"><span data-stu-id="41c57-134">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="41c57-135">Header</span><span class="sxs-lookup"><span data-stu-id="41c57-135">Header</span></span><br/> | <dl> <span data-ttu-id="41c57-136"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="41c57-136"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41c57-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41c57-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41c57-138">**Iwmdrmnetreceiver-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="41c57-138">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> <dt>

[<span data-ttu-id="41c57-139">**Iwmdrmnetreceiver:: getlicensechallenge**</span><span class="sxs-lookup"><span data-stu-id="41c57-139">**IWMDRMNetReceiver::GetLicenseChallenge**</span></span>](iwmdrmnetreceiver-getlicensechallenge.md)
</dt> </dl>

 

 





