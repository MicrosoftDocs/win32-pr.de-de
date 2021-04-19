---
title: Iwmdrmsecurity getmachinecertificate-Methode (wmdrmsdk. h)
description: Die getmachinecertificate-Methode ruft das Computer Zertifikat des DRM-Subsystems auf dem Client Computer ab.
ms.assetid: 38b8e812-e997-4a63-b906-ebd26a5556be
keywords:
- Getmachinecertificate-Methode Windows Media-Format
- Getmachinecertificate-Methode, Windows Media-Format, iwmdrmsecurity-Schnittstelle
- Iwmdrmsecurity-Schnittstelle Windows Media-Format, getmachinecertificate-Methode
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetMachineCertificate
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d6c66c54ab9528a458910def5978ec83b191654
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371088"
---
# <a name="iwmdrmsecuritygetmachinecertificate-method"></a><span data-ttu-id="3e9c8-106">Iwmdrmsecurity:: getmachinecertificate-Methode</span><span class="sxs-lookup"><span data-stu-id="3e9c8-106">IWMDRMSecurity::GetMachineCertificate method</span></span>

<span data-ttu-id="3e9c8-107">Die **getmachinecertificate** -Methode ruft das Computer Zertifikat des DRM-Subsystems auf dem Client Computer ab.</span><span class="sxs-lookup"><span data-stu-id="3e9c8-107">The **GetMachineCertificate** method retrieves the machine certificate of the DRM subsystem on the client computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e9c8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e9c8-108">Syntax</span></span>


```C++
HRESULT GetMachineCertificate(
  [in]      DWORD dwCertificateType,
  [out]     BYTE  rgbVersion[4],
  [out]     BYTE  **ppbCertificate,
  [in, out] DWORD *pcbCertificate
);
```



## <a name="parameters"></a><span data-ttu-id="3e9c8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e9c8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e9c8-110">*dwcertifialisietype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e9c8-110">*dwCertificateType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e9c8-111">Der Typ des abzurufenden Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="3e9c8-111">Type of certificate to retrieve.</span></span> <span data-ttu-id="3e9c8-112">Legen Sie auf einen der Werte in der folgenden Tabelle fest.</span><span class="sxs-lookup"><span data-stu-id="3e9c8-112">Set to one of the values in the following table.</span></span>



| <span data-ttu-id="3e9c8-113">Wert</span><span class="sxs-lookup"><span data-stu-id="3e9c8-113">Value</span></span>                        | <span data-ttu-id="3e9c8-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e9c8-114">Description</span></span>                                                                           |
|------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3e9c8-115">WMDRM \_ - \_ Zertifikattyp \_ v1</span><span class="sxs-lookup"><span data-stu-id="3e9c8-115">WMDRM\_CERTIFICATE\_TYPE\_V1</span></span> | <span data-ttu-id="3e9c8-116">Das Zertifikat wird im von Legacy Komponenten verwendeten Format abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3e9c8-116">The certificate will be retrieved in the format used by legacy components.</span></span>            |
| <span data-ttu-id="3e9c8-117">WMDRM \_ - \_ Zertifikattyp \_ v2</span><span class="sxs-lookup"><span data-stu-id="3e9c8-117">WMDRM\_CERTIFICATE\_TYPE\_V2</span></span> | <span data-ttu-id="3e9c8-118">Das Zertifikat wird in dem Format abgerufen, das von den Windows Vista-Komponenten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3e9c8-118">The certificate will be retrieved in the format used by the Windows Vista components.</span></span> |



 

</dd> <dt>

<span data-ttu-id="3e9c8-119">*rgbversion \[ 4 \]* ausgehend \[\]</span><span class="sxs-lookup"><span data-stu-id="3e9c8-119">*rgbVersion\[4\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e9c8-120">Array von vier Bytes, die die Version des DRM-Subsystems auf dem Client Computer angeben.</span><span class="sxs-lookup"><span data-stu-id="3e9c8-120">Array of four bytes specifying the version of the DRM subsystem on the client computer.</span></span>

</dd> <dt>

<span data-ttu-id="3e9c8-121">*ppbcertificate* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3e9c8-121">*ppbCertificate* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e9c8-122">Adresse einer Variablen, die einen Zeiger auf die Zertifikat Daten empfängt.</span><span class="sxs-lookup"><span data-stu-id="3e9c8-122">Address of a variable that receives a pointer to the certificate data.</span></span> <span data-ttu-id="3e9c8-123">Legen Sie diese Einstellung auf **null** fest, damit die Methode die Puffergröße bereitstellt, die zum Speichern des Zertifikats in *pcbcertificate* erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="3e9c8-123">Set to **NULL** to have the method provide the buffer size required to hold the certificate in *pcbCertificate*.</span></span>

</dd> <dt>

<span data-ttu-id="3e9c8-124">*pcbcertificate* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3e9c8-124">*pcbCertificate* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e9c8-125">Größe des Zertifikats in Bytes.</span><span class="sxs-lookup"><span data-stu-id="3e9c8-125">Size of the certificate in bytes.</span></span> <span data-ttu-id="3e9c8-126">Wenn *ppbcertificate* den Wert **null** hat, wird dieser Wert auf die Größe des Zertifikats festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3e9c8-126">If *ppbCertificate* is **NULL**, this value will be set to the size of the certificate.</span></span> <span data-ttu-id="3e9c8-127">Wenn *ppbcertificate* nicht **null** ist, muss dieser Wert auf die Größe des Puffers festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3e9c8-127">If *ppbCertificate* is not **NULL**, this value must be set to the size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e9c8-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3e9c8-128">Return value</span></span>

<span data-ttu-id="3e9c8-129">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="3e9c8-129">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3e9c8-130">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="3e9c8-130">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3e9c8-131">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="3e9c8-131">Return code</span></span>                                                                          | <span data-ttu-id="3e9c8-132">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3e9c8-132">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="3e9c8-133"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3e9c8-133"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3e9c8-134">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3e9c8-134">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3e9c8-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e9c8-135">Requirements</span></span>



| <span data-ttu-id="3e9c8-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3e9c8-136">Requirement</span></span> | <span data-ttu-id="3e9c8-137">Wert</span><span class="sxs-lookup"><span data-stu-id="3e9c8-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e9c8-138">Header</span><span class="sxs-lookup"><span data-stu-id="3e9c8-138">Header</span></span><br/>  | <dl> <span data-ttu-id="3e9c8-139"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e9c8-139"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="3e9c8-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3e9c8-140">Library</span></span><br/> | <dl> <span data-ttu-id="3e9c8-141"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3e9c8-141"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e9c8-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e9c8-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e9c8-143">**Iwmdrmsecurity-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="3e9c8-143">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





