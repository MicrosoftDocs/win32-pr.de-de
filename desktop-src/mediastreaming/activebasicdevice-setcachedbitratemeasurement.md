---
title: Activebasicdevice setcachedbitratemeasurement-Methode (playondevice. h)
description: Legt die zwischengespeicherte Bitrate fest.
ms.assetid: 53530217-CFF7-4376-B155-E11044621E2D
keywords:
- Setcachedbitratemeasurement-Methode Medien Streaming-API
- Setcachedbitratemeasurement-Methode Medien Streaming-API, activebasicdevice-Schnittstelle
- Activebasicdevice-Schnittstelle Medien Streaming-API, setcachedbitratemeasurement-Methode
topic_type:
- apiref
api_name:
- ActiveBasicDevice.SetCachedBitrateMeasurement
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c681776b00eb9d911a4fa75a9d360b39a3d2b8c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478975"
---
# <a name="activebasicdevicesetcachedbitratemeasurement-method"></a><span data-ttu-id="715bc-106">Activebasicdevice:: setcachedbitratemeasurement-Methode</span><span class="sxs-lookup"><span data-stu-id="715bc-106">ActiveBasicDevice::SetCachedBitrateMeasurement method</span></span>

<span data-ttu-id="715bc-107">Legt die zwischengespeicherte Bitrate fest.</span><span class="sxs-lookup"><span data-stu-id="715bc-107">Sets the cached bitrate.</span></span>

## <a name="syntax"></a><span data-ttu-id="715bc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="715bc-108">Syntax</span></span>


```C++
HRESULT SetCachedBitrateMeasurement(
  [in] GUID   physicalNetworkInterface,
  [in] UINT64 bitrate
);
```



## <a name="parameters"></a><span data-ttu-id="715bc-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="715bc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="715bc-110">*physicalnetworkinterface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="715bc-110">*physicalNetworkInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="715bc-111">Gibt die physische Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="715bc-111">Specifies the physical network interface.</span></span>

</dd> <dt>

<span data-ttu-id="715bc-112">*Bitrate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="715bc-112">*bitrate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="715bc-113">Der Wert, auf den die Bitrate festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="715bc-113">The value to set the bitrate to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="715bc-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="715bc-114">Return value</span></span>

<span data-ttu-id="715bc-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="715bc-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="715bc-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="715bc-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="715bc-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="715bc-117">Requirements</span></span>



| <span data-ttu-id="715bc-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="715bc-118">Requirement</span></span> | <span data-ttu-id="715bc-119">Wert</span><span class="sxs-lookup"><span data-stu-id="715bc-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="715bc-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="715bc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="715bc-121">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="715bc-121">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="715bc-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="715bc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="715bc-123">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="715bc-123">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="715bc-124">Header</span><span class="sxs-lookup"><span data-stu-id="715bc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="715bc-125"><dt>Playondevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="715bc-125"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="715bc-126">IDL</span><span class="sxs-lookup"><span data-stu-id="715bc-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="715bc-127"><dt>Playto Device. idl</dt></span><span class="sxs-lookup"><span data-stu-id="715bc-127"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="715bc-128">DLL</span><span class="sxs-lookup"><span data-stu-id="715bc-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="715bc-129"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="715bc-129"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="715bc-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="715bc-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="715bc-131">[**Activebasicdevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="715bc-131">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

