---
title: Ibasicdevice ManufacturerName-Methode
description: Ruft den Herstellernamen des Geräts ab.
ms.assetid: F04400C9-02FC-4CB5-B355-A7E84BECD098
keywords:
- ManufacturerName-Methode Medien Streaming-API
- ManufacturerName-Methode Medien Streaming-API, ibasicdevice-Schnittstelle
- Ibasicdevice-Schnittstelle Medien Streaming-API, ManufacturerName-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.ManufacturerName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 698b4b6c202ed157737b20296976a282c7f97ba3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106340248"
---
# <a name="ibasicdevicemanufacturername-method"></a><span data-ttu-id="5a802-106">Ibasicdevice:: ManufacturerName-Methode</span><span class="sxs-lookup"><span data-stu-id="5a802-106">IBasicDevice::ManufacturerName method</span></span>

<span data-ttu-id="5a802-107">Ruft den Herstellernamen des Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="5a802-107">Retrieves the device s manufacturer name.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a802-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a802-108">Syntax</span></span>


```C++
HRESULT ManufacturerName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="5a802-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a802-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a802-110">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5a802-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a802-111">Empfängt einen Zeiger auf den Herstellernamen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="5a802-111">Receives a pointer to the device s manufacturer name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a802-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5a802-112">Return value</span></span>

<span data-ttu-id="5a802-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="5a802-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5a802-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="5a802-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5a802-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="5a802-115">Return code</span></span>                                                                          | <span data-ttu-id="5a802-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5a802-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="5a802-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5a802-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="5a802-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5a802-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="5a802-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a802-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a802-120">**Ibasicdevice**</span><span class="sxs-lookup"><span data-stu-id="5a802-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





