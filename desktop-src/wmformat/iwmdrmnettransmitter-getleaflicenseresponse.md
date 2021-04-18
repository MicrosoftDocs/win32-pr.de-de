---
title: Iwmdrmnettransmitter getleaflicenseresponse-Methode (wmdrmsdk. h)
description: Die getleaflicenseresponse-Methode generiert eine Blatt Lizenz-Antwortnachricht.
ms.assetid: b2893d22-b6f3-44d2-b6db-e2b07fbe098d
keywords:
- Getleaflicenseresponse-Methode, Windows Media-Format
- Getleaflicenseresponse-Methode, Windows Media-Format, iwmdrmnettransmitter-Schnittstelle
- Iwmdrmnettransmitter-Schnittstelle Windows Media-Format, getleaflicenseresponse-Methode
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.GetLeafLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf2374966abfae4353a72755313c1cbbdfb7287
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351211"
---
# <a name="iwmdrmnettransmittergetleaflicenseresponse-method"></a><span data-ttu-id="e632b-106">Iwmdrmnettransmitter:: getleaflicenseresponse-Methode</span><span class="sxs-lookup"><span data-stu-id="e632b-106">IWMDRMNetTransmitter::GetLeafLicenseResponse method</span></span>

<span data-ttu-id="e632b-107">Die **getleaflicenseresponse** -Methode generiert eine Blatt Lizenz-Antwortnachricht.</span><span class="sxs-lookup"><span data-stu-id="e632b-107">The **GetLeafLicenseResponse** method generates a leaf license response message.</span></span>

## <a name="syntax"></a><span data-ttu-id="e632b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e632b-108">Syntax</span></span>


```C++
HRESULT GetLeafLicenseResponse(
  [in]  BSTR            bstrKID,
  [in]  WMDRMNET_POLICY *pPolicy,
  [out] IWMDRMEncrypt   **ppIWMDRMEncrypt,
  [out] BYTE            **ppbLicenseResponse,
  [out] DWORD           *pcbLicenseResponse
);
```



## <a name="parameters"></a><span data-ttu-id="e632b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e632b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e632b-110">*bstrinkid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e632b-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e632b-111">Base64-codierter Schlüssel Bezeichner, der für die neue Blatt Lizenz verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e632b-111">Base64-encoded key identifier to be used for the new leaf license.</span></span> <span data-ttu-id="e632b-112">Der Schlüssel Bezeichner muss ein zufällig generierter GUID-Wert sein.</span><span class="sxs-lookup"><span data-stu-id="e632b-112">The key identifier should be a randomly generated GUID value.</span></span>

</dd> <dt>

<span data-ttu-id="e632b-113">*pPolicy* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e632b-113">*pPolicy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e632b-114">Ein Zeiger auf die [**wmdrmnet- \_ Richtlinien**](wmdrmnet-policy.md) Struktur, die die Richtlinie definiert, die für die Blatt Lizenz verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e632b-114">Pointer to the [**WMDRMNET\_POLICY**](wmdrmnet-policy.md) structure that defines the policy to use for the leaf license.</span></span>

</dd> <dt>

<span data-ttu-id="e632b-115">*ppiwmdrmencrypt* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e632b-115">*ppIWMDRMEncrypt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e632b-116">Adresse einer Variablen, die einen Zeiger auf die [**iwmdrmencrypt**](iwmdrmencrypt.md) -Schnittstelle empfängt, die zum Verschlüsseln von Daten für die neue Blatt Lizenz verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e632b-116">Address of a variable that receives a pointer to the [**IWMDRMEncrypt**](iwmdrmencrypt.md) interface that can be used to encrypt data for the new leaf license.</span></span>

</dd> <dt>

<span data-ttu-id="e632b-117">*ppblicenseresponse* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e632b-117">*ppbLicenseResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e632b-118">Adresse einer Variablen, die die Adresse der generierten Lizenz Antwort empfängt.</span><span class="sxs-lookup"><span data-stu-id="e632b-118">Address of a variable that receives the address of the generated license response.</span></span> <span data-ttu-id="e632b-119">Wenn Sie mit diesen Daten fertig sind, müssen Sie den Arbeitsspeicher freigeben, indem Sie " **CoTaskMemFree**" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e632b-119">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span>

</dd> <dt>

<span data-ttu-id="e632b-120">*pcblicenseresponse* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e632b-120">*pcbLicenseResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e632b-121">Adresse einer Variablen, die die Größe der Lizenz Antwort erhält (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="e632b-121">Address of a variable that receives the size of the license response, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e632b-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e632b-122">Return value</span></span>

<span data-ttu-id="e632b-123">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="e632b-123">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e632b-124">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e632b-124">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e632b-125">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e632b-125">Return code</span></span>                                                                                                | <span data-ttu-id="e632b-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e632b-126">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="e632b-127"><dt>**NS \_ E \_ DRM- \_ RIV \_ zu \_ klein**</dt></span><span class="sxs-lookup"><span data-stu-id="e632b-127"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="e632b-128">Es wird eine aktualisierte Inhalts Sperr Liste benötigt.</span><span class="sxs-lookup"><span data-stu-id="e632b-128">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="e632b-129"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e632b-129"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="e632b-130">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e632b-130">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="e632b-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e632b-131">Remarks</span></span>

<span data-ttu-id="e632b-132">Keine.</span><span class="sxs-lookup"><span data-stu-id="e632b-132">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="e632b-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e632b-133">Requirements</span></span>



| <span data-ttu-id="e632b-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e632b-134">Requirement</span></span> | <span data-ttu-id="e632b-135">Wert</span><span class="sxs-lookup"><span data-stu-id="e632b-135">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e632b-136">Header</span><span class="sxs-lookup"><span data-stu-id="e632b-136">Header</span></span><br/> | <dl> <span data-ttu-id="e632b-137"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="e632b-137"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e632b-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e632b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e632b-139">**Iwmdrmnettransmitter-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="e632b-139">**IWMDRMNetTransmitter Interface**</span></span>](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





