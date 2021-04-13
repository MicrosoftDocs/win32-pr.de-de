---
title: Ibasicdevice modelurl-Methode
description: Ruft die Modell-URL des Geräts ab.
ms.assetid: 093D306B-5DFC-4A68-803D-3DDE195A8B85
keywords:
- Modelurl-Methode Medien Streaming-API
- Modelurl-Methode Medien Streaming-API, ibasicdevice-Schnittstelle
- Ibasicdevice-Schnittstelle Medien Streaming-API, modelurl-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.ModelUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4f616d1a122f5fe6025c80742df61eb86d41514a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312450"
---
# <a name="ibasicdevicemodelurl-method"></a><span data-ttu-id="0b87f-106">Ibasicdevice:: modelurl-Methode</span><span class="sxs-lookup"><span data-stu-id="0b87f-106">IBasicDevice::ModelUrl method</span></span>

<span data-ttu-id="0b87f-107">Ruft die Modell-URL des Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="0b87f-107">Retrieves the device s model URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b87f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b87f-108">Syntax</span></span>


```C++
HRESULT ModelUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="0b87f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b87f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b87f-110">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0b87f-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b87f-111">Empfängt einen Zeiger auf die Modell-URL des Geräts.</span><span class="sxs-lookup"><span data-stu-id="0b87f-111">Receives a pointer to the device s model URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b87f-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0b87f-112">Return value</span></span>

<span data-ttu-id="0b87f-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="0b87f-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0b87f-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="0b87f-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0b87f-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0b87f-115">Return code</span></span>                                                                          | <span data-ttu-id="0b87f-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b87f-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="0b87f-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0b87f-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="0b87f-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0b87f-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="0b87f-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b87f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b87f-120">**Ibasicdevice**</span><span class="sxs-lookup"><span data-stu-id="0b87f-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





