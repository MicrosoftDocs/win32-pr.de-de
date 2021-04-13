---
title: Ibasicdevice-Typmethode
description: Ruft einen Enumerationswert ab, der den Gerätetyp des DLNA-Geräts angibt.
ms.assetid: D9FB3A02-7796-4ACB-B7D3-D171D1D9B77F
keywords:
- Type-Methode Medien Streaming-API
- Type-Methode Medien Streaming-API, ibasicdevice-Schnittstelle
- Ibasicdevice-Schnittstelle Medien Streaming-API, Type-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.Type
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a69f0671c82363ff61179c0120b3db8f6e755de9
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2020
ms.locfileid: "104391199"
---
# <a name="ibasicdevicetype-method"></a><span data-ttu-id="6aed1-106">Ibasicdevice:: Type-Methode</span><span class="sxs-lookup"><span data-stu-id="6aed1-106">IBasicDevice::Type method</span></span>

<span data-ttu-id="6aed1-107">Ruft einen Enumerationswert ab, der den Gerätetyp des DLNA-Geräts angibt.</span><span class="sxs-lookup"><span data-stu-id="6aed1-107">Retrieves an enumeration value indicating the device type of the DLNA device.</span></span>

## <a name="syntax"></a><span data-ttu-id="6aed1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6aed1-108">Syntax</span></span>


```C++
HRESULT Type(
  [out] DeviceTypes *value
);
```



## <a name="parameters"></a><span data-ttu-id="6aed1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6aed1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6aed1-110">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6aed1-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6aed1-111">Empfängt einen Zeiger auf einen Wert vom Typ " [**de vicetypes**](devicetypes.md) ".</span><span class="sxs-lookup"><span data-stu-id="6aed1-111">Receives a pointer to a [**DeviceTypes**](devicetypes.md) value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6aed1-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6aed1-112">Return value</span></span>

<span data-ttu-id="6aed1-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="6aed1-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="6aed1-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6aed1-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="6aed1-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6aed1-115">Return code</span></span>                                                                          | <span data-ttu-id="6aed1-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6aed1-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="6aed1-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6aed1-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="6aed1-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6aed1-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="6aed1-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6aed1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6aed1-120">**Ibasicdevice**</span><span class="sxs-lookup"><span data-stu-id="6aed1-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





