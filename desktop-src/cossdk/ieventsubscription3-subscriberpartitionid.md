---
description: Die Partitions-GUID des Abonnenten.
ms.assetid: 0b2411d3-cdc1-492c-a54f-ca3d3bd8b953
title: 'IEventSubscription3:: abonniert-Eigenschaft'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.SubscriberPartitionID
- IEventSubscription3.get_SubscriberPartitionID
- IEventSubscription3.put_SubscriberPartitionID
api_type:
- COM
api_location: ''
ms.openlocfilehash: b09c41ac1b3a90c3275daf7afa0cd90fe2bb905c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214284"
---
# <a name="ieventsubscription3subscriberpartitionid-property"></a><span data-ttu-id="8bd45-103">IEventSubscription3:: abonniert-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8bd45-103">IEventSubscription3::SubscriberPartitionID property</span></span>

<span data-ttu-id="8bd45-104">Die Partitions-GUID des Abonnenten.</span><span class="sxs-lookup"><span data-stu-id="8bd45-104">The partition GUID of the subscriber.</span></span>

<span data-ttu-id="8bd45-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="8bd45-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bd45-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8bd45-106">Syntax</span></span>


```C++
HRESULT put_SubscriberPartitionID(
  [in]          BSTR bstrSubscriberPartitionID
);

HRESULT get_SubscriberPartitionID(
  [out, retval] BSTR *pbstrSubscriberPartitionID
);
```



## <a name="property-value"></a><span data-ttu-id="8bd45-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="8bd45-107">Property value</span></span>

<span data-ttu-id="8bd45-108">Eine Zeichenfolge, die die GUID der Abonnenten Partition enthält.</span><span class="sxs-lookup"><span data-stu-id="8bd45-108">A string containing the GUID of the subscriber partition.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8bd45-109">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="8bd45-109">Error codes</span></span>

<span data-ttu-id="8bd45-110">Diese Methode kann die Standard Rückgabewerte e \_ invalidArg, e \_ outo fmemory, e \_ unerwartet, e \_ Fail und S OK \_ zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="8bd45-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bd45-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8bd45-111">Requirements</span></span>



| <span data-ttu-id="8bd45-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8bd45-112">Requirement</span></span> | <span data-ttu-id="8bd45-113">Wert</span><span class="sxs-lookup"><span data-stu-id="8bd45-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="8bd45-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8bd45-114">Minimum supported client</span></span><br/> | <span data-ttu-id="8bd45-115">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8bd45-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8bd45-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8bd45-116">Minimum supported server</span></span><br/> | <span data-ttu-id="8bd45-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8bd45-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="8bd45-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8bd45-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bd45-119">**IEventSubscription3**</span><span class="sxs-lookup"><span data-stu-id="8bd45-119">**IEventSubscription3**</span></span>](ieventsubscription3.md)
</dt> </dl>

 

 




