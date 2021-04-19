---
title: "' Iwmdrmdevice ' getsecureclock-Methode"
description: Die getsecureclock-Methode ruft die sichere Uhr ab. Daher können zeitbasierte Lizenzen erzwungen werden.
ms.assetid: 6de9b7ce-9c2a-44e5-9de7-40cfbaf4d92c
keywords:
- Getsecureclock-Methode, Windows Media Device Manager
- Getsecureclock-Methode Windows Media Device Manager, iwmdrmdevice-Schnittstelle
- Iwmdrmdevice-Schnittstelle Windows Media Device Manager, getsecureclock-Methode
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSecureClock
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaa92c3bc2ee82facf2f2e1043e71467a0c55bd8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367420"
---
# <a name="iwmdrmdevicegetsecureclock-method"></a><span data-ttu-id="86af8-106">Iwmdrmdevice:: getsecureclock-Methode</span><span class="sxs-lookup"><span data-stu-id="86af8-106">IWMDRMDevice::GetSecureClock method</span></span>

<span data-ttu-id="86af8-107">Die **getsecureclock** -Methode ruft die sichere Uhr ab. Daher können zeitbasierte Lizenzen erzwungen werden.</span><span class="sxs-lookup"><span data-stu-id="86af8-107">The **GetSecureClock** method retrieves the secure clock, so time-based licenses can be enforced.</span></span>

## <a name="syntax"></a><span data-ttu-id="86af8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="86af8-108">Syntax</span></span>


```C++
HRESULT GetSecureClock(
  [out] BYTE  **ppbSecureClock,
  [out] DWORD *pcbSecureClock,
  [out] DWORD *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="86af8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="86af8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86af8-110">*ppbsecureclock* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="86af8-110">*ppbSecureClock* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86af8-111">Die sichere Uhr wurde abgerufen.</span><span class="sxs-lookup"><span data-stu-id="86af8-111">Retrieved secure clock.</span></span>

</dd> <dt>

<span data-ttu-id="86af8-112">*pcbsecureclock* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="86af8-112">*pcbSecureClock* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86af8-113">Größe der sicheren Uhr (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="86af8-113">Size of the secure clock, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="86af8-114">*pdwflags* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="86af8-114">*pdwFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86af8-115">Gerätestatusflags.</span><span class="sxs-lookup"><span data-stu-id="86af8-115">Device status flags.</span></span> <span data-ttu-id="86af8-116">Bei diesem Wert muss es sich um eines der folgenden Flags handeln.</span><span class="sxs-lookup"><span data-stu-id="86af8-116">This value must be one of the following flags.</span></span>



| <span data-ttu-id="86af8-117">Flag</span><span class="sxs-lookup"><span data-stu-id="86af8-117">Flag</span></span>                     | <span data-ttu-id="86af8-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="86af8-118">Description</span></span>                            |
|--------------------------|----------------------------------------|
| <span data-ttu-id="86af8-119">WMDRM- \_ Gerät \_ iswmdrm</span><span class="sxs-lookup"><span data-stu-id="86af8-119">WMDRM\_DEVICE\_ISWMDRM</span></span>   | <span data-ttu-id="86af8-120">Das Gerät unterstützt Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="86af8-120">The device supports Windows Media DRM.</span></span> |
| <span data-ttu-id="86af8-121">WMDRM- \_ Geräte- \_ needclock</span><span class="sxs-lookup"><span data-stu-id="86af8-121">WMDRM\_DEVICE\_NEEDCLOCK</span></span> | <span data-ttu-id="86af8-122">Das Gerät benötigt die Uhr.</span><span class="sxs-lookup"><span data-stu-id="86af8-122">The device needs clock.</span></span>                |
| <span data-ttu-id="86af8-123">WMDRM- \_ Gerät gesperrt \_</span><span class="sxs-lookup"><span data-stu-id="86af8-123">WMDRM\_DEVICE\_REVOKED</span></span>   | <span data-ttu-id="86af8-124">Das Gerät wurde widerrufen.</span><span class="sxs-lookup"><span data-stu-id="86af8-124">The device has been revoked.</span></span>           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86af8-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="86af8-125">Return value</span></span>

<span data-ttu-id="86af8-126">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="86af8-126">The method returns an **HRESULT**.</span></span> <span data-ttu-id="86af8-127">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="86af8-127">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="86af8-128">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="86af8-128">Return code</span></span>                                                                          | <span data-ttu-id="86af8-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="86af8-129">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="86af8-130"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="86af8-130"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="86af8-131">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="86af8-131">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="86af8-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="86af8-132">Requirements</span></span>



| <span data-ttu-id="86af8-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="86af8-133">Requirement</span></span> | <span data-ttu-id="86af8-134">Wert</span><span class="sxs-lookup"><span data-stu-id="86af8-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86af8-135">Header</span><span class="sxs-lookup"><span data-stu-id="86af8-135">Header</span></span><br/>  | <dl> <span data-ttu-id="86af8-136"><dt>Wmddrmsp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="86af8-136"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="86af8-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="86af8-137">Library</span></span><br/> | <dl> <span data-ttu-id="86af8-138"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86af8-138"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86af8-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86af8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86af8-140">**Getsecureclockchallenge**</span><span class="sxs-lookup"><span data-stu-id="86af8-140">**GetSecureClockChallenge**</span></span>](iwmdrmdevice-getsecureclockchallenge.md)
</dt> <dt>

[<span data-ttu-id="86af8-141">**Iwmdrmdevice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="86af8-141">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> <dt>

[<span data-ttu-id="86af8-142">**Setsecureclockresponse**</span><span class="sxs-lookup"><span data-stu-id="86af8-142">**SetSecureClockResponse**</span></span>](iwmdrmdevice-setsecureclockresponse.md)
</dt> </dl>

 

 





