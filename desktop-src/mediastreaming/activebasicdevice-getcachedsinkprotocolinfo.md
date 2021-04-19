---
title: Activebasicdevice getcachedsinkprotocolinfo-Methode (playtodevice. h)
description: Ruft die zwischengespeicherten senkenprotokollinformationen für das Gerät ab. | Activebasicdevice getcachedsinkprotocolinfo-Methode (playtodevice. h)
ms.assetid: C6A3C4B5-1883-4E71-83D2-11E378A4FBCA
keywords:
- Getcachedsinkprotocolinfo-Methode Medien Streaming-API
- Getcachedsinkprotocolinfo-Methode Medien Streaming-API, activebasicdevice-Schnittstelle
- Activebasicdevice-Schnittstelle Medien Streaming-API, getcachedsinkprotocolinfo-Methode
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedSinkProtocolInfo
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056cc351a1ecd1c8eef07d4e994da8e895aa85f8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106373458"
---
# <a name="activebasicdevicegetcachedsinkprotocolinfo-method"></a><span data-ttu-id="5469d-107">Activebasicdevice:: getcachedsink protocolinfo-Methode</span><span class="sxs-lookup"><span data-stu-id="5469d-107">ActiveBasicDevice::GetCachedSinkProtocolInfo method</span></span>

<span data-ttu-id="5469d-108">Ruft die zwischengespeicherten senkenprotokollinformationen für das Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="5469d-108">Gets the cached sink protocol info for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="5469d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="5469d-109">Syntax</span></span>


```C++
HRESULT GetCachedSinkProtocolInfo(
  [out, retval] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="5469d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5469d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5469d-111">*Wert* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="5469d-111">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="5469d-112">Die zwischengespeicherten senkenprotokollinformationen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="5469d-112">The cached sink protocol info for the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5469d-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5469d-113">Return value</span></span>

<span data-ttu-id="5469d-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="5469d-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5469d-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5469d-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5469d-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5469d-116">Requirements</span></span>



| <span data-ttu-id="5469d-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5469d-117">Requirement</span></span> | <span data-ttu-id="5469d-118">Wert</span><span class="sxs-lookup"><span data-stu-id="5469d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5469d-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5469d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5469d-120">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="5469d-120">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5469d-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5469d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5469d-122">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5469d-122">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5469d-123">Header</span><span class="sxs-lookup"><span data-stu-id="5469d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5469d-124"><dt>Playondevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="5469d-124"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="5469d-125">IDL</span><span class="sxs-lookup"><span data-stu-id="5469d-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5469d-126"><dt>Playto Device. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5469d-126"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="5469d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="5469d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5469d-128"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5469d-128"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5469d-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5469d-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="5469d-130">[**Activebasicdevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5469d-130">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

