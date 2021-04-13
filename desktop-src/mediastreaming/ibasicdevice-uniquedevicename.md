---
title: Ibasicdevice uniquedevicename-Methode
description: Ruft den eindeutigen Gerätenamen (User Name, udn) des Geräts ab.
ms.assetid: 393EFF96-69E1-4081-905D-D8CC47B5FC4A
keywords:
- Uniquedevicename-Methode Medien Streaming-API
- Uniquedevicename-Methode Medien Streaming-API, ibasicdevice-Schnittstelle
- Ibasicdevice-Schnittstelle Medien Streaming-API, uniquedevicename-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.UniqueDeviceName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4b3103640fd49880dc5ae5ca881618ac1091de62
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389107"
---
# <a name="ibasicdeviceuniquedevicename-method"></a><span data-ttu-id="6052c-106">Ibasicdevice:: uniquedevicename-Methode</span><span class="sxs-lookup"><span data-stu-id="6052c-106">IBasicDevice::UniqueDeviceName method</span></span>

<span data-ttu-id="6052c-107">Ruft den eindeutigen Gerätenamen (User Name, udn) des Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="6052c-107">Retrieves the device s unique device name (UDN).</span></span>

## <a name="syntax"></a><span data-ttu-id="6052c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6052c-108">Syntax</span></span>


```C++
HRESULT UniqueDeviceName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="6052c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6052c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6052c-110">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6052c-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6052c-111">Empfängt einen Zeiger auf das Modell-udn des Geräts.</span><span class="sxs-lookup"><span data-stu-id="6052c-111">Receives a pointer to the device s model UDN.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6052c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6052c-112">Return value</span></span>

<span data-ttu-id="6052c-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="6052c-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="6052c-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6052c-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="6052c-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6052c-115">Return code</span></span>                                                                          | <span data-ttu-id="6052c-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6052c-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="6052c-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6052c-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="6052c-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6052c-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="6052c-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6052c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6052c-120">**Ibasicdevice**</span><span class="sxs-lookup"><span data-stu-id="6052c-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





