---
title: Devicepair-Server Eigenschaft (asptlb. h)
description: Ruft den Server für das aktive Basic-Geräte Paar ab.
ms.assetid: 25FD523F-36C7-4165-BBB2-6A3410D896EF
keywords:
- Server Eigenschaft Medien Streaming-API
- Server Eigenschaft Medien Streaming-API, devicepair-Schnittstelle
- Devicepair Interface Medien Streaming-API, Server Eigenschaft
topic_type:
- apiref
api_name:
- DevicePair.Server
- DevicePair.get_Server
api_location:
- asptlb.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eec2c28e8118f6cf11e89c7ab4a5ba04abd8b8f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371960"
---
# <a name="devicepairserver-property"></a><span data-ttu-id="f653d-106">Devicepair:: Server-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f653d-106">DevicePair::Server property</span></span>

<span data-ttu-id="f653d-107">Ruft den Server für das aktive Basic-Geräte Paar ab.</span><span class="sxs-lookup"><span data-stu-id="f653d-107">Gets the server for the active basic device pair.</span></span>

<span data-ttu-id="f653d-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f653d-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f653d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f653d-109">Syntax</span></span>


```C++
HRESULT get_Server(
  [out] ActiveBasicDevice **value
);
```



## <a name="property-value"></a><span data-ttu-id="f653d-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f653d-110">Property value</span></span>

<span data-ttu-id="f653d-111">Empfängt ein [**activebasicdevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) -Objekt, das das Server Gerät darstellt.</span><span class="sxs-lookup"><span data-stu-id="f653d-111">Receives a [**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) object that represents the server device.</span></span>

## <a name="requirements"></a><span data-ttu-id="f653d-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f653d-112">Requirements</span></span>



| <span data-ttu-id="f653d-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f653d-113">Requirement</span></span> | <span data-ttu-id="f653d-114">Wert</span><span class="sxs-lookup"><span data-stu-id="f653d-114">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f653d-115">Header</span><span class="sxs-lookup"><span data-stu-id="f653d-115">Header</span></span><br/> | <dl> <span data-ttu-id="f653d-116"><dt>Asptlb. h</dt></span><span class="sxs-lookup"><span data-stu-id="f653d-116"><dt>Asptlb.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f653d-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f653d-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="f653d-118">[**Devicepair**](/previous-versions/windows/desktop/legacy/dn385771(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f653d-118">[**DevicePair**](/previous-versions/windows/desktop/legacy/dn385771(v=vs.85))</span></span>
</dt> </dl>

 

