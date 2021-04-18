---
title: Ibasicdevice remotestreamingurls-Methode
description: Gibt einen Vektor von Remotestreaming-URLs zurück.
ms.assetid: 19B4475F-A7E4-4DC4-9C88-68D91D023AF4
keywords:
- Remotestreamingurls-Methode Medien Streaming-API
- Remotestreamingurls-Methode Medien Streaming-API, ibasicdevice-Schnittstelle
- Ibasicdevice-Schnittstelle Medien Streaming-API, remotestreamingurls-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.RemoteStreamingUrls
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fdc4bd363096e7b808a51cfbddb764daabe03a55
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389120"
---
# <a name="ibasicdeviceremotestreamingurls-method"></a><span data-ttu-id="24c6d-106">Ibasicdevice:: remotestreamingurls-Methode</span><span class="sxs-lookup"><span data-stu-id="24c6d-106">IBasicDevice::RemoteStreamingUrls method</span></span>

<span data-ttu-id="24c6d-107">Gibt einen Vektor von Remotestreaming-URLs zurück.</span><span class="sxs-lookup"><span data-stu-id="24c6d-107">Returns a vector of remote streaming URLs.</span></span>

## <a name="syntax"></a><span data-ttu-id="24c6d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="24c6d-108">Syntax</span></span>


```C++
HRESULT RemoteStreamingUrls(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a><span data-ttu-id="24c6d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="24c6d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24c6d-110">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="24c6d-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24c6d-111">Empfängt eine Aufzähl Bare Auflistung von Zeigern auf Remotestreaming-URLs.</span><span class="sxs-lookup"><span data-stu-id="24c6d-111">Receives an enumerable collection of pointers to remote streaming URLs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24c6d-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="24c6d-112">Return value</span></span>

<span data-ttu-id="24c6d-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="24c6d-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="24c6d-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="24c6d-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="24c6d-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="24c6d-115">Return code</span></span>                                                                          | <span data-ttu-id="24c6d-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="24c6d-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="24c6d-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="24c6d-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="24c6d-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="24c6d-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="24c6d-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24c6d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24c6d-120">**Ibasicdevice**</span><span class="sxs-lookup"><span data-stu-id="24c6d-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





