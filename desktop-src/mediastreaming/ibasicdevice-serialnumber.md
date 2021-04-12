---
title: Ibasicdevice-SerialNumber-Methode
description: Ruft die Seriennummer des Geräts ab.
ms.assetid: 238A5999-0E8B-4462-AFCF-790DB58CFCB4
keywords:
- SerialNumber-Methode Medien Streaming-API
- SerialNumber-Methode Medien Streaming-API, ibasicdevice-Schnittstelle
- Ibasicdevice-Schnittstelle Medien Streaming-API, SerialNumber-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.SerialNumber
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f24fad2e74c3ec2a5b489d8f5dd57265ea6d21bf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312486"
---
# <a name="ibasicdeviceserialnumber-method"></a><span data-ttu-id="d1c0d-106">Ibasicdevice:: SerialNumber-Methode</span><span class="sxs-lookup"><span data-stu-id="d1c0d-106">IBasicDevice::SerialNumber method</span></span>

<span data-ttu-id="d1c0d-107">Ruft die Seriennummer des Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="d1c0d-107">Retrieves the device s serial number.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1c0d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1c0d-108">Syntax</span></span>


```C++
HRESULT SerialNumber(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="d1c0d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1c0d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1c0d-110">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d1c0d-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1c0d-111">Empfängt einen Zeiger auf die Seriennummer des Geräts.</span><span class="sxs-lookup"><span data-stu-id="d1c0d-111">Receives a pointer to the device s serial number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1c0d-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d1c0d-112">Return value</span></span>

<span data-ttu-id="d1c0d-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="d1c0d-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d1c0d-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d1c0d-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d1c0d-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d1c0d-115">Return code</span></span>                                                                          | <span data-ttu-id="d1c0d-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d1c0d-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d1c0d-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d1c0d-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d1c0d-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d1c0d-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="d1c0d-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1c0d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1c0d-120">**Ibasicdevice**</span><span class="sxs-lookup"><span data-stu-id="d1c0d-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





