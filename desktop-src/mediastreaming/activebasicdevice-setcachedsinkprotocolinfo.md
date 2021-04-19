---
title: Activebasicdevice setcachedsinkprotocolinfo-Methode (playtodevice. h)
description: Ruft die zwischengespeicherten senkenprotokollinformationen für das Gerät ab. | Activebasicdevice setcachedsinkprotocolinfo-Methode (playtodevice. h)
ms.assetid: C4856B97-89F9-43EC-B778-9E0CDAAF2C47
keywords:
- Setcachedsinkprotocolinfo-Methode Medien Streaming-API
- Setcachedsinkprotocolinfo-Methode Medien Streaming-API, activebasicdevice-Schnittstelle
- Activebasicdevice-Schnittstelle Medien Streaming-API, setcachedsink protocolinfo-Methode
topic_type:
- apiref
api_name:
- ActiveBasicDevice.SetCachedSinkProtocolInfo
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9100cb8faeb685a0cc7a8b7b73deb11afca29a3e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106366431"
---
# <a name="activebasicdevicesetcachedsinkprotocolinfo-method"></a><span data-ttu-id="be2d4-107">Activebasicdevice:: setcachedsink protocolinfo-Methode</span><span class="sxs-lookup"><span data-stu-id="be2d4-107">ActiveBasicDevice::SetCachedSinkProtocolInfo method</span></span>

<span data-ttu-id="be2d4-108">Ruft die zwischengespeicherten senkenprotokollinformationen für das Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="be2d4-108">Gets the cached sink protocol info for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="be2d4-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="be2d4-109">Syntax</span></span>


```C++
HRESULT SetCachedSinkProtocolInfo(
  [in] GUID   physicalNetworkInterface,
  [in] UINT64 bitrate
);
```



## <a name="parameters"></a><span data-ttu-id="be2d4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="be2d4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be2d4-111">*physicalnetworkinterface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="be2d4-111">*physicalNetworkInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be2d4-112">Gibt die physische Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="be2d4-112">Specifies the physical network interface.</span></span>

</dd> <dt>

<span data-ttu-id="be2d4-113">*Bitrate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="be2d4-113">*bitrate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be2d4-114">Der Bitrate-Wert.</span><span class="sxs-lookup"><span data-stu-id="be2d4-114">The bitrate value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be2d4-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="be2d4-115">Return value</span></span>

<span data-ttu-id="be2d4-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="be2d4-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="be2d4-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="be2d4-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="be2d4-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be2d4-118">Requirements</span></span>



| <span data-ttu-id="be2d4-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be2d4-119">Requirement</span></span> | <span data-ttu-id="be2d4-120">Wert</span><span class="sxs-lookup"><span data-stu-id="be2d4-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="be2d4-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="be2d4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="be2d4-122">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="be2d4-122">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="be2d4-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="be2d4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="be2d4-124">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="be2d4-124">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="be2d4-125">Header</span><span class="sxs-lookup"><span data-stu-id="be2d4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="be2d4-126"><dt>Playondevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="be2d4-126"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="be2d4-127">IDL</span><span class="sxs-lookup"><span data-stu-id="be2d4-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="be2d4-128"><dt>Playto Device. idl</dt></span><span class="sxs-lookup"><span data-stu-id="be2d4-128"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="be2d4-129">DLL</span><span class="sxs-lookup"><span data-stu-id="be2d4-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be2d4-130"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be2d4-130"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be2d4-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be2d4-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="be2d4-132">[**Activebasicdevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="be2d4-132">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

