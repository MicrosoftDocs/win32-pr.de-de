---
title: Iwmdrmnettransmitter getrootlicenseresponse-Methode (wmdrmsdk. h)
description: Die getrootlicenseresponse-Methode generiert eine Stamm Lizenz-Antwortnachricht.
ms.assetid: c735ee52-f0e0-4404-881b-18ee9a7fa9f9
keywords:
- Getrootlicenseresponse-Methode Windows Media-Format
- Getrootlicenseresponse-Methode, Windows Media-Format, iwmdrmnettransmitter-Schnittstelle
- Iwmdrmnettransmitter-Schnittstelle Windows Media-Format, getrootlicenseresponse-Methode
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.GetRootLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3497a3eaedb872b7d2c9eb5d7782d01f8b35462
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359345"
---
# <a name="iwmdrmnettransmittergetrootlicenseresponse-method"></a><span data-ttu-id="a6871-106">Iwmdrmnettransmitter:: getrootlicenseresponse-Methode</span><span class="sxs-lookup"><span data-stu-id="a6871-106">IWMDRMNetTransmitter::GetRootLicenseResponse method</span></span>

<span data-ttu-id="a6871-107">Die **getrootlicenseresponse** -Methode generiert eine Stamm Lizenz-Antwortnachricht.</span><span class="sxs-lookup"><span data-stu-id="a6871-107">The **GetRootLicenseResponse** method generates a root license response message.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6871-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6871-108">Syntax</span></span>


```C++
HRESULT GetRootLicenseResponse(
  [in]  BSTR  bstrKID,
  [out] BYTE  **ppbLicenseResponse,
  [out] DWORD *pcbLicenseResponse
);
```



## <a name="parameters"></a><span data-ttu-id="a6871-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6871-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6871-110">*bstrinkid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6871-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6871-111">Base64-codierter Schlüssel Bezeichner, der für die neue Stamm Lizenz verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a6871-111">Base64-encoded key identifier to be used for the new root license.</span></span> <span data-ttu-id="a6871-112">Der Schlüssel Bezeichner muss ein zufällig generierter GUID-Wert sein.</span><span class="sxs-lookup"><span data-stu-id="a6871-112">The key identifier should be a randomly generated GUID value.</span></span>

</dd> <dt>

<span data-ttu-id="a6871-113">*ppblicenseresponse* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a6871-113">*ppbLicenseResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6871-114">Adresse einer Variablen, die die Adresse der generierten Lizenz Antwort empfängt.</span><span class="sxs-lookup"><span data-stu-id="a6871-114">Address of a variable that receives the address of the generated license response.</span></span> <span data-ttu-id="a6871-115">Wenn Sie mit diesen Daten fertig sind, müssen Sie den Arbeitsspeicher freigeben, indem Sie " **CoTaskMemFree**" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a6871-115">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span>

</dd> <dt>

<span data-ttu-id="a6871-116">*pcblicenseresponse* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a6871-116">*pcbLicenseResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6871-117">Adresse einer Variablen, die die Größe der Lizenz Antwort erhält (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="a6871-117">Address of a variable that receives the size of the license response, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6871-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a6871-118">Return value</span></span>

<span data-ttu-id="a6871-119">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="a6871-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a6871-120">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a6871-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a6871-121">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a6871-121">Return code</span></span>                                                                                                | <span data-ttu-id="a6871-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a6871-122">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="a6871-123"><dt>**NS \_ E \_ DRM- \_ RIV \_ zu \_ klein**</dt></span><span class="sxs-lookup"><span data-stu-id="a6871-123"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="a6871-124">Es wird eine aktualisierte Inhalts Sperr Liste benötigt.</span><span class="sxs-lookup"><span data-stu-id="a6871-124">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="a6871-125"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a6871-125"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="a6871-126">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a6871-126">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="a6871-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6871-127">Remarks</span></span>

<span data-ttu-id="a6871-128">Die generierte Stamm Lizenz wird mithilfe der Informationen aus den Lizenz Abfrage Daten erstellt, die für die Schnittstelle verarbeitet werden, indem [**setlicensechallenge**](iwmdrmnettransmitter-setlicensechallenge.md)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a6871-128">The generated root license is created using the information from the license challenge data, which is processed for the interface by calling [**SetLicenseChallenge**](iwmdrmnettransmitter-setlicensechallenge.md).</span></span>

<span data-ttu-id="a6871-129">Die Stamm Lizenz wird bei der Generierung von Blatt Lizenzen verwendet. Dies wird durch Aufrufen der [**getleaflicenseresponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) -Methode erreicht.</span><span class="sxs-lookup"><span data-stu-id="a6871-129">The root license is used in the generation of leaf licenses, which is accomplished by calling the [**GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) method.</span></span> <span data-ttu-id="a6871-130">Die **iwmdrmnettransmitter** -Schnittstelle verwaltet eine Kopie der Stamm Lizenz für diese Verwendung.</span><span class="sxs-lookup"><span data-stu-id="a6871-130">The **IWMDRMNetTransmitter** interface maintains a copy of the root license for that use.</span></span>

<span data-ttu-id="a6871-131">Die Stamm Lizenz, die durch den Aufruf dieser Methode erstellt wurde, verfügt über keine Richtlinien und ist so konfiguriert, dass Sie auf dem empfangenden Gerät nicht persistent gespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a6871-131">The root license created by calling this method does not have any policies and is configured so that it cannot be persisted on the receiving device.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6871-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6871-132">Requirements</span></span>



| <span data-ttu-id="a6871-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a6871-133">Requirement</span></span> | <span data-ttu-id="a6871-134">Wert</span><span class="sxs-lookup"><span data-stu-id="a6871-134">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a6871-135">Header</span><span class="sxs-lookup"><span data-stu-id="a6871-135">Header</span></span><br/> | <dl> <span data-ttu-id="a6871-136"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6871-136"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6871-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6871-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6871-138">**Iwmdrmnettransmitter-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a6871-138">**IWMDRMNetTransmitter Interface**</span></span>](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





