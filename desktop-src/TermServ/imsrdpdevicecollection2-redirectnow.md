---
title: IMsRdpDeviceCollection2 redirectnow-Methode
description: Erzwingt das umgeleitet oder Entfernen von Geräten, die in der Sammlung ausgewählt oder nicht ausgewählt wurden.
ms.assetid: 9cd5849d-a589-43f3-b904-6b2e15ca033d
ms.tgt_platform: multiple
keywords:
- Redirectnow-Methode Remotedesktopdienste
- Redirectnow-Methode Remotedesktopdienste, IMsRdpDeviceCollection2-Schnittstelle
- IMsRdpDeviceCollection2-Schnittstelle Remotedesktopdienste, redirectnow-Methode
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection2.RedirectNow
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 893d1e26f504d5aeb45f795ea7425eeefc3a6232
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949431"
---
# <a name="imsrdpdevicecollection2redirectnow-method"></a><span data-ttu-id="cd4ea-106">IMsRdpDeviceCollection2:: redirectnow-Methode</span><span class="sxs-lookup"><span data-stu-id="cd4ea-106">IMsRdpDeviceCollection2::RedirectNow method</span></span>

<span data-ttu-id="cd4ea-107">Erzwingt das umgeleitet oder Entfernen von Geräten, die in der Sammlung ausgewählt oder nicht ausgewählt wurden.</span><span class="sxs-lookup"><span data-stu-id="cd4ea-107">Forces devices that were selected or unselected from the collection to be redirected or removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd4ea-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd4ea-108">Syntax</span></span>


```C++
HRESULT RedirectNow(
  [in] RedirectDeviceType Type
);
```



## <a name="parameters"></a><span data-ttu-id="cd4ea-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd4ea-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd4ea-110">*Typ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd4ea-110">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd4ea-111">Type: **[ **redirectdevicetype**](redirectdevicetype.md)**</span><span class="sxs-lookup"><span data-stu-id="cd4ea-111">Type: **[**RedirectDeviceType**](redirectdevicetype.md)**</span></span>

<span data-ttu-id="cd4ea-112">Ein Wert der [**redirectdevicetype**](redirectdevicetype.md) -Enumeration, der den Gerätetyp angibt, der umgeleitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cd4ea-112">A value of the [**RedirectDeviceType**](redirectdevicetype.md) enumeration that specifies the type of device to be redirected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd4ea-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cd4ea-113">Return value</span></span>

<span data-ttu-id="cd4ea-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="cd4ea-114">Type: **HRESULT**</span></span>

<span data-ttu-id="cd4ea-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="cd4ea-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cd4ea-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cd4ea-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd4ea-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd4ea-117">Requirements</span></span>



| <span data-ttu-id="cd4ea-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cd4ea-118">Requirement</span></span> | <span data-ttu-id="cd4ea-119">Wert</span><span class="sxs-lookup"><span data-stu-id="cd4ea-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd4ea-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cd4ea-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cd4ea-121">Windows 8</span><span class="sxs-lookup"><span data-stu-id="cd4ea-121">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="cd4ea-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cd4ea-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cd4ea-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cd4ea-123">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="cd4ea-124">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="cd4ea-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="cd4ea-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd4ea-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="cd4ea-126">DLL</span><span class="sxs-lookup"><span data-stu-id="cd4ea-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd4ea-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd4ea-127"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd4ea-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd4ea-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd4ea-129">**Redirectde vicetype**</span><span class="sxs-lookup"><span data-stu-id="cd4ea-129">**RedirectDeviceType**</span></span>](redirectdevicetype.md)
</dt> <dt>

[<span data-ttu-id="cd4ea-130">**IMsRdpDeviceCollection2**</span><span class="sxs-lookup"><span data-stu-id="cd4ea-130">**IMsRdpDeviceCollection2**</span></span>](imsrdpdevicecollection2.md)
</dt> </dl>

 

 





