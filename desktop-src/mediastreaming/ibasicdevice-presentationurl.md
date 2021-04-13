---
title: Ibasicdevice presentationurl-Methode
description: Ruft die Präsentations-URL des Geräts ab.
ms.assetid: F1EF1BBE-F35D-4828-B4F6-D6DEFF5A6391
keywords:
- Presentationurl-Methode Media Streaming-API
- Presentationurl-Methode Medien Streaming-API, ibasicdevice-Schnittstelle
- Ibasicdevice-Schnittstelle Medien Streaming-API, presentationurl-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.PresentationUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89d10187329692c4f279a94cde004455a182733e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389119"
---
# <a name="ibasicdevicepresentationurl-method"></a><span data-ttu-id="5daa3-106">Ibasicdevice::P-Methode "Ressentiments ationurl"</span><span class="sxs-lookup"><span data-stu-id="5daa3-106">IBasicDevice::PresentationUrl method</span></span>

<span data-ttu-id="5daa3-107">Ruft die Präsentations-URL des Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="5daa3-107">Retrieves the device s presentation URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="5daa3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5daa3-108">Syntax</span></span>


```C++
HRESULT PresentationUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="5daa3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5daa3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5daa3-110">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5daa3-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5daa3-111">Empfängt einen Zeiger auf die Präsentations-URL des Geräts.</span><span class="sxs-lookup"><span data-stu-id="5daa3-111">Receives a pointer to the device s presentation URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5daa3-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5daa3-112">Return value</span></span>

<span data-ttu-id="5daa3-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="5daa3-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5daa3-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="5daa3-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5daa3-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="5daa3-115">Return code</span></span>                                                                          | <span data-ttu-id="5daa3-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5daa3-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="5daa3-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5daa3-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="5daa3-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5daa3-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="5daa3-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5daa3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5daa3-120">**Ibasicdevice**</span><span class="sxs-lookup"><span data-stu-id="5daa3-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





