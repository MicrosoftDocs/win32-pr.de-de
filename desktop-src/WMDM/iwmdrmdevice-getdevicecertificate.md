---
title: Iwmdrmdevice getdevicecertificate-Methode
description: Die getdevicecertificate-Methode ruft das Gerätezertifikat ab.
ms.assetid: 9e345bf9-a158-4c0e-a9f1-e4ce3ec16b58
keywords:
- Getdevicecertificate-Methode, Windows Media Device Manager
- Getdevicecertificate-Methode Windows Media Device Manager, iwmdrmdevice-Schnittstelle
- Iwmdrmdevice-Schnittstelle Windows Media Device Manager, getdevicecertificate-Methode
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetDeviceCertificate
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9ceecca32f2455d73ca1dce76a4f8a17613a1ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357311"
---
# <a name="iwmdrmdevicegetdevicecertificate-method"></a><span data-ttu-id="01267-106">Iwmdrmdevice:: getdevicecertificate-Methode</span><span class="sxs-lookup"><span data-stu-id="01267-106">IWMDRMDevice::GetDeviceCertificate method</span></span>

<span data-ttu-id="01267-107">Die **getdevicecertificate** -Methode ruft das Gerätezertifikat ab.</span><span class="sxs-lookup"><span data-stu-id="01267-107">The **GetDeviceCertificate** method retrieves the device certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="01267-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="01267-108">Syntax</span></span>


```C++
HRESULT GetDeviceCertificate(
  [out] BSTR *pbstrDevCert
);
```



## <a name="parameters"></a><span data-ttu-id="01267-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="01267-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01267-110">*pbstraudevcert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="01267-110">*pbstrDevCert* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="01267-111">Zeiger auf einen **BSTR** -Wert, der das abgerufene Gerätezertifikat enthält.</span><span class="sxs-lookup"><span data-stu-id="01267-111">Pointer to a **BSTR** containing the retrieved device certificate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01267-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="01267-112">Return value</span></span>

<span data-ttu-id="01267-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="01267-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="01267-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="01267-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="01267-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="01267-115">Return code</span></span>                                                                          | <span data-ttu-id="01267-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="01267-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="01267-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="01267-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="01267-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="01267-118">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="01267-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="01267-119">Requirements</span></span>



| <span data-ttu-id="01267-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="01267-120">Requirement</span></span> | <span data-ttu-id="01267-121">Wert</span><span class="sxs-lookup"><span data-stu-id="01267-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01267-122">Header</span><span class="sxs-lookup"><span data-stu-id="01267-122">Header</span></span><br/>  | <dl> <span data-ttu-id="01267-123"><dt>Wmddrmsp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="01267-123"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="01267-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="01267-124">Library</span></span><br/> | <dl> <span data-ttu-id="01267-125"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="01267-125"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01267-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01267-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01267-127">**Iwmdrmdevice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="01267-127">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





