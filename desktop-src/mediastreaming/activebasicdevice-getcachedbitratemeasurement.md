---
title: Activebasicdevice getcachedbitratemeasurement-Methode (playondevice. h)
description: Ruft die zwischengespeicherte Bitrate ab.
ms.assetid: 78C3C5D7-C46B-413D-BC18-C3861E5FDAA5
keywords:
- Getcachedbitratemeasurement-Methode Medien Streaming-API
- Getcachedbitratemeasurement-Methode Medien Streaming-API, activebasicdevice-Schnittstelle
- Activebasicdevice-Schnittstelle Medien Streaming-API, getcachedbitratemeasurement-Methode
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedBitrateMeasurement
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d15b38ba2730d2023b09c2fa0352ade1f1532724
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518701"
---
# <a name="activebasicdevicegetcachedbitratemeasurement-method"></a><span data-ttu-id="9aac7-106">Activebasicdevice:: getcachedbitratemeasurement-Methode</span><span class="sxs-lookup"><span data-stu-id="9aac7-106">ActiveBasicDevice::GetCachedBitrateMeasurement method</span></span>

<span data-ttu-id="9aac7-107">Ruft die zwischengespeicherte Bitrate ab.</span><span class="sxs-lookup"><span data-stu-id="9aac7-107">Gets the cached bitrate.</span></span>

## <a name="syntax"></a><span data-ttu-id="9aac7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9aac7-108">Syntax</span></span>


```C++
HRESULT GetCachedBitrateMeasurement(
  [in]          GUID   physicalNetworkInterface,
  [out, retval] UINT64 *bitrate
);
```



## <a name="parameters"></a><span data-ttu-id="9aac7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9aac7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9aac7-110">*physicalnetworkinterface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9aac7-110">*physicalNetworkInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aac7-111">Gibt die physische Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="9aac7-111">Specifies the physical network interface.</span></span>

</dd> <dt>

<span data-ttu-id="9aac7-112">*Bitrate* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="9aac7-112">*bitrate* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="9aac7-113">Empfängt den Bitrate-Wert.</span><span class="sxs-lookup"><span data-stu-id="9aac7-113">Receives the bitrate value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9aac7-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9aac7-114">Return value</span></span>

<span data-ttu-id="9aac7-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="9aac7-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9aac7-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9aac7-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9aac7-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9aac7-117">Requirements</span></span>



| <span data-ttu-id="9aac7-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9aac7-118">Requirement</span></span> | <span data-ttu-id="9aac7-119">Wert</span><span class="sxs-lookup"><span data-stu-id="9aac7-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9aac7-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9aac7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9aac7-121">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="9aac7-121">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9aac7-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9aac7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9aac7-123">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9aac7-123">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9aac7-124">Header</span><span class="sxs-lookup"><span data-stu-id="9aac7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9aac7-125"><dt>Playondevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="9aac7-125"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="9aac7-126">IDL</span><span class="sxs-lookup"><span data-stu-id="9aac7-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9aac7-127"><dt>Playto Device. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9aac7-127"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="9aac7-128">DLL</span><span class="sxs-lookup"><span data-stu-id="9aac7-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9aac7-129"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9aac7-129"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9aac7-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9aac7-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="9aac7-131">[**Activebasicdevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9aac7-131">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

