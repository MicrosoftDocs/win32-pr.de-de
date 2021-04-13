---
title: Ibasicdevice-IPADRESSEN-Methode
description: Gibt einen Vektor von IP-Adressen zurück.
ms.assetid: F48B91DC-3AE2-462F-835B-292BF86904B3
keywords:
- IPADRESSEN-Methode Medien Streaming-API
- IPADRESSEN-Methode Medien Streaming-API, ibasicdevice-Schnittstelle
- Ibasicdevice-Schnittstelle Medien Streaming-API, IPADRESSEN-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.IpAddresses
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0623b6e2e5d96cb0a400ab1e820424b7eecf46c9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389131"
---
# <a name="ibasicdeviceipaddresses-method"></a><span data-ttu-id="158f1-106">Ibasicdevice:: IPADRESSEN-Methode</span><span class="sxs-lookup"><span data-stu-id="158f1-106">IBasicDevice::IpAddresses method</span></span>

<span data-ttu-id="158f1-107">Gibt einen Vektor von IP-Adressen zurück.</span><span class="sxs-lookup"><span data-stu-id="158f1-107">Returns a vector of IP addresses.</span></span>

## <a name="syntax"></a><span data-ttu-id="158f1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="158f1-108">Syntax</span></span>


```C++
HRESULT IpAddresses(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a><span data-ttu-id="158f1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="158f1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="158f1-110">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="158f1-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="158f1-111">Empfängt eine Aufzähl Bare Auflistung von Zeigern auf IP-Adressen.</span><span class="sxs-lookup"><span data-stu-id="158f1-111">Receives an enumerable collection of pointers to IP addresses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="158f1-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="158f1-112">Return value</span></span>

<span data-ttu-id="158f1-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="158f1-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="158f1-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="158f1-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="158f1-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="158f1-115">Return code</span></span>                                                                          | <span data-ttu-id="158f1-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="158f1-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="158f1-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="158f1-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="158f1-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="158f1-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="158f1-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="158f1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="158f1-120">**Ibasicdevice**</span><span class="sxs-lookup"><span data-stu-id="158f1-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





