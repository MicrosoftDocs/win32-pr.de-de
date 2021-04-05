---
title: Ibasicdevice FriendlyName-Methode
description: Ruft den anzeigen amen des Geräts ab.
ms.assetid: 693806E1-CA66-457D-A25B-D79064776965
keywords:
- FriendlyName-Methode Medien Streaming-API
- FriendlyName-Methode Medien Streaming-API, ibasicdevice-Schnittstelle
- Ibasicdevice-Schnittstelle Medien Streaming-API, FriendlyName-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.FriendlyName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec2b2edfa3a98dfdbbdd1d236acb6e1f1433f141
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718564"
---
# <a name="ibasicdevicefriendlyname-method"></a><span data-ttu-id="7eab8-106">Ibasicdevice:: FriendlyName-Methode</span><span class="sxs-lookup"><span data-stu-id="7eab8-106">IBasicDevice::FriendlyName method</span></span>

<span data-ttu-id="7eab8-107">Ruft den anzeigen amen des Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="7eab8-107">Retrieves the device s friendly name.</span></span>

## <a name="syntax"></a><span data-ttu-id="7eab8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7eab8-108">Syntax</span></span>


```C++
HRESULT FriendlyName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="7eab8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7eab8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7eab8-110">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7eab8-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7eab8-111">Empfängt einen Zeiger auf den anzeigen amen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="7eab8-111">Receives a pointer to the device s friendly name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7eab8-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7eab8-112">Return value</span></span>

<span data-ttu-id="7eab8-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="7eab8-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="7eab8-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7eab8-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="7eab8-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7eab8-115">Return code</span></span>                                                                          | <span data-ttu-id="7eab8-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7eab8-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="7eab8-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7eab8-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="7eab8-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7eab8-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="7eab8-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7eab8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7eab8-120">**Ibasicdevice**</span><span class="sxs-lookup"><span data-stu-id="7eab8-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





