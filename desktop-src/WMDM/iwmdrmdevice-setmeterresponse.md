---
title: Iwmdrmdevice-setmeterresponse-Methode
description: Die setmeterresponse-Methode legt die Messungs Antwort fest.
ms.assetid: 3f2e7d7c-6470-4d53-96b0-d3eebdb08329
keywords:
- Setmeterresponse-Methode (Windows Media Device Manager)
- Setmeterresponse-Methode Windows Media Device Manager, iwmdrmdevice-Schnittstelle
- Iwmdrmdevice-Schnittstelle Windows Media Device Manager, setmeterresponse-Methode
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetMeterResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ed70b158215eb831296ad083af8cd2c001cb38f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364677"
---
# <a name="iwmdrmdevicesetmeterresponse-method"></a><span data-ttu-id="dc5ba-106">Iwmdrmdevice:: setmeterresponse-Methode</span><span class="sxs-lookup"><span data-stu-id="dc5ba-106">IWMDRMDevice::SetMeterResponse method</span></span>

<span data-ttu-id="dc5ba-107">Die **setmeterresponse** -Methode legt die Messungs Antwort fest.</span><span class="sxs-lookup"><span data-stu-id="dc5ba-107">The **SetMeterResponse** method sets the metering response.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc5ba-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc5ba-108">Syntax</span></span>


```C++
HRESULT SetMeterResponse(
  [in]  BYTE  *pbMeterResponse,
  [in]  DWORD cbMeterResponse,
  [out] DWORD *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="dc5ba-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc5ba-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc5ba-110">*pbmeterantwort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc5ba-110">*pbMeterResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc5ba-111">Die festzulegende Messungs Antwort.</span><span class="sxs-lookup"><span data-stu-id="dc5ba-111">The metering response to be set.</span></span>

</dd> <dt>

<span data-ttu-id="dc5ba-112">*cbmeter Response* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc5ba-112">*cbMeterResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc5ba-113">Größe der Messungs Antwort in Bytes.</span><span class="sxs-lookup"><span data-stu-id="dc5ba-113">Size of the metering response, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="dc5ba-114">*pdwflags* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dc5ba-114">*pdwFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc5ba-115">Antwortflags.</span><span class="sxs-lookup"><span data-stu-id="dc5ba-115">Response flags.</span></span> <span data-ttu-id="dc5ba-116">Bei diesem Wert muss es sich um eines der folgenden Flags handeln.</span><span class="sxs-lookup"><span data-stu-id="dc5ba-116">This value must be one of the following flags.</span></span>



| <span data-ttu-id="dc5ba-117">Flag</span><span class="sxs-lookup"><span data-stu-id="dc5ba-117">Flag</span></span>                            | <span data-ttu-id="dc5ba-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dc5ba-118">Description</span></span>              |
|---------------------------------|--------------------------|
| <span data-ttu-id="dc5ba-119">WMDRM- \_ Zähler für \_ \_ alle Zähler</span><span class="sxs-lookup"><span data-stu-id="dc5ba-119">WMDRM\_METER\_RESPONSE\_ALL</span></span>     | <span data-ttu-id="dc5ba-120">Alle Meter Antworten.</span><span class="sxs-lookup"><span data-stu-id="dc5ba-120">All meter responses.</span></span>     |
| <span data-ttu-id="dc5ba-121">WMDRM- \_ Messgeräte \_ Antwort \_ partiell</span><span class="sxs-lookup"><span data-stu-id="dc5ba-121">WMDRM\_METER\_RESPONSE\_PARTIAL</span></span> | <span data-ttu-id="dc5ba-122">Teil Messungs Antworten.</span><span class="sxs-lookup"><span data-stu-id="dc5ba-122">Partial meter responses.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc5ba-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dc5ba-123">Return value</span></span>

<span data-ttu-id="dc5ba-124">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="dc5ba-124">The method returns an **HRESULT**.</span></span> <span data-ttu-id="dc5ba-125">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="dc5ba-125">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="dc5ba-126">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="dc5ba-126">Return code</span></span>                                                                          | <span data-ttu-id="dc5ba-127">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dc5ba-127">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="dc5ba-128"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dc5ba-128"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="dc5ba-129">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dc5ba-129">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="dc5ba-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc5ba-130">Requirements</span></span>



| <span data-ttu-id="dc5ba-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc5ba-131">Requirement</span></span> | <span data-ttu-id="dc5ba-132">Wert</span><span class="sxs-lookup"><span data-stu-id="dc5ba-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc5ba-133">Header</span><span class="sxs-lookup"><span data-stu-id="dc5ba-133">Header</span></span><br/>  | <dl> <span data-ttu-id="dc5ba-134"><dt>Wmddrmsp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dc5ba-134"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="dc5ba-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dc5ba-135">Library</span></span><br/> | <dl> <span data-ttu-id="dc5ba-136"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dc5ba-136"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc5ba-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc5ba-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc5ba-138">**Iwmdrmdevice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="dc5ba-138">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





