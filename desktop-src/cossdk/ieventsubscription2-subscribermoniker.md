---
description: Der Abonnenten Moniker.
ms.assetid: d33d8c80-3251-4ec7-9cf3-d0b60d91ed5a
title: IEventSubscription2SubscriberMoniker-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription2.SubscriberMoniker
- IEventSubscription2.get_SubscriberMoniker
- IEventSubscription2.put_SubscriberMoniker
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9496a3046b4bb0e99a88322892e557588a92aab8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748304"
---
# <a name="ieventsubscription2subscribermoniker-property"></a><span data-ttu-id="90d34-103">IEventSubscription2:: abonniert-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="90d34-103">IEventSubscription2::SubscriberMoniker property</span></span>

<span data-ttu-id="90d34-104">Der Moniker des Abonnenten.</span><span class="sxs-lookup"><span data-stu-id="90d34-104">The subscriber's moniker.</span></span>

<span data-ttu-id="90d34-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="90d34-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="90d34-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="90d34-106">Syntax</span></span>


```C++
HRESULT put_SubscriberMoniker(
  [in]          BSTR bstrMoniker
);

HRESULT get_SubscriberMoniker(
  [out, retval] BSTR *pbstrMoniker
);
```



## <a name="property-value"></a><span data-ttu-id="90d34-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="90d34-107">Property value</span></span>

<span data-ttu-id="90d34-108">Eine Monikerzeichenfolge, die den Abonnenten angibt.</span><span class="sxs-lookup"><span data-stu-id="90d34-108">A moniker string specifying the subscriber.</span></span>

## <a name="error-codes"></a><span data-ttu-id="90d34-109">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="90d34-109">Error codes</span></span>

<span data-ttu-id="90d34-110">Diese Methode kann die Standard Rückgabewerte e \_ invalidArg, e \_ outo fmemory, e \_ unerwartet, e \_ Fail und S OK \_ zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="90d34-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="90d34-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="90d34-111">Requirements</span></span>



| <span data-ttu-id="90d34-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="90d34-112">Requirement</span></span> | <span data-ttu-id="90d34-113">Wert</span><span class="sxs-lookup"><span data-stu-id="90d34-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="90d34-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="90d34-114">Minimum supported client</span></span><br/> | <span data-ttu-id="90d34-115">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90d34-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="90d34-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="90d34-116">Minimum supported server</span></span><br/> | <span data-ttu-id="90d34-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90d34-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="90d34-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90d34-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90d34-119">**IEventSubscription2**</span><span class="sxs-lookup"><span data-stu-id="90d34-119">**IEventSubscription2**</span></span>](ieventsubscription2.md)
</dt> </dl>

 

 




