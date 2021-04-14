---
title: Activebasicdevice getcachedextrasink protocolinfo-Methode (playtodevice. h)
description: Ruft zusätzliche Informationen zum zwischengespeicherten senkenprotokoll für das Gerät ab.
ms.assetid: 97112921-1C1D-4FC9-8FE6-1381F3773351
keywords:
- Getcachedextrasink protocolinfo-Methode Medien Streaming-API
- Getcachedextrasink protocolinfo-Methode Medien Streaming-API, activebasicdevice-Schnittstelle
- Activebasicdevice-Schnittstelle Medien Streaming-API, getcachedextrasink protocolinfo-Methode
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedExtraSinkProtocolInfo
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be5bb013d1356d5ff02e709a92f01eceff6c2e0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392008"
---
# <a name="activebasicdevicegetcachedextrasinkprotocolinfo-method"></a><span data-ttu-id="2e3ac-106">Activebasicdevice:: getcachedextrasink protocolinfo-Methode</span><span class="sxs-lookup"><span data-stu-id="2e3ac-106">ActiveBasicDevice::GetCachedExtraSinkProtocolInfo method</span></span>

<span data-ttu-id="2e3ac-107">Ruft zusätzliche Informationen zum zwischengespeicherten senkenprotokoll für das Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="2e3ac-107">Gets additional cached sink protocol info for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e3ac-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e3ac-108">Syntax</span></span>


```C++
HRESULT GetCachedExtraSinkProtocolInfo(
  [out, retval] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="2e3ac-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e3ac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e3ac-110">*Wert* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="2e3ac-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="2e3ac-111">Die zusätzlichen zwischengespeicherten senkenprotokollinformationen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="2e3ac-111">The extra cached sink protocol info for the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e3ac-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2e3ac-112">Return value</span></span>

<span data-ttu-id="2e3ac-113">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="2e3ac-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2e3ac-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2e3ac-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e3ac-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e3ac-115">Requirements</span></span>



| <span data-ttu-id="2e3ac-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e3ac-116">Requirement</span></span> | <span data-ttu-id="2e3ac-117">Wert</span><span class="sxs-lookup"><span data-stu-id="2e3ac-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e3ac-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2e3ac-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2e3ac-119">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="2e3ac-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2e3ac-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2e3ac-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2e3ac-121">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2e3ac-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2e3ac-122">Header</span><span class="sxs-lookup"><span data-stu-id="2e3ac-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e3ac-123"><dt>Playondevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e3ac-123"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="2e3ac-124">IDL</span><span class="sxs-lookup"><span data-stu-id="2e3ac-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2e3ac-125"><dt>Playto Device. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2e3ac-125"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="2e3ac-126">DLL</span><span class="sxs-lookup"><span data-stu-id="2e3ac-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e3ac-127"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e3ac-127"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e3ac-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e3ac-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="2e3ac-129">[**Activebasicdevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2e3ac-129">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

