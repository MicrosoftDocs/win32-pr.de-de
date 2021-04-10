---
description: Die Anwendungs-GUID des Abonnenten.
ms.assetid: 46c91cae-ca31-4eac-baa8-d36910917f0f
title: 'IEventSubscription3:: abonniert ApplicationId (Eigenschaft)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.SubscriberApplicationID
- IEventSubscription3.get_SubscriberApplicationID
- IEventSubscription3.put_SubscriberApplicationID
api_type:
- COM
api_location: ''
ms.openlocfilehash: c2e726d97821a7a7143f4971a4918227235adb9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214119"
---
# <a name="ieventsubscription3subscriberapplicationid-property"></a><span data-ttu-id="10a02-103">IEventSubscription3:: abonniert ApplicationId (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="10a02-103">IEventSubscription3::SubscriberApplicationID property</span></span>

<span data-ttu-id="10a02-104">Die Anwendungs-GUID des Abonnenten.</span><span class="sxs-lookup"><span data-stu-id="10a02-104">The application GUID of the subscriber.</span></span>

<span data-ttu-id="10a02-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="10a02-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="10a02-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="10a02-106">Syntax</span></span>


```C++
HRESULT put_SubscriberApplicationID(
  [in]          BSTR bstrSubscriberApplicationID
);

HRESULT get_SubscriberApplicationID(
  [out, retval] BSTR *pbstrSubscriberApplicationID
);
```



## <a name="property-value"></a><span data-ttu-id="10a02-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="10a02-107">Property value</span></span>

<span data-ttu-id="10a02-108">Eine Zeichenfolge, die die GUID der Abonnenten Anwendung enthält.</span><span class="sxs-lookup"><span data-stu-id="10a02-108">A string containing the GUID of the subscriber application.</span></span>

## <a name="error-codes"></a><span data-ttu-id="10a02-109">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="10a02-109">Error codes</span></span>

<span data-ttu-id="10a02-110">Diese Methode kann die Standard Rückgabewerte e \_ invalidArg, e \_ outo fmemory, e \_ unerwartet, e \_ Fail und S OK \_ zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="10a02-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="10a02-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="10a02-111">Requirements</span></span>



| <span data-ttu-id="10a02-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="10a02-112">Requirement</span></span> | <span data-ttu-id="10a02-113">Wert</span><span class="sxs-lookup"><span data-stu-id="10a02-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="10a02-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="10a02-114">Minimum supported client</span></span><br/> | <span data-ttu-id="10a02-115">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="10a02-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="10a02-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="10a02-116">Minimum supported server</span></span><br/> | <span data-ttu-id="10a02-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="10a02-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="10a02-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10a02-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10a02-119">**IEventSubscription3**</span><span class="sxs-lookup"><span data-stu-id="10a02-119">**IEventSubscription3**</span></span>](ieventsubscription3.md)
</dt> </dl>

 

 




