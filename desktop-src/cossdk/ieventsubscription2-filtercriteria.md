---
description: Die Filterkriterien für das Abonnement.
ms.assetid: cfc3ba9e-0566-45fd-917f-34842b8ff377
title: 'IEventSubscription2:: filterCriteria (Eigenschaft)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription2.FilterCriteria
- IEventSubscription2.get_FilterCriteria
- IEventSubscription2.put_FilterCriteria
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1443a89433cff91a298e8c390fce8f1f64b99f1b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127408"
---
# <a name="ieventsubscription2filtercriteria-property"></a><span data-ttu-id="a57ce-103">IEventSubscription2:: filterCriteria (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a57ce-103">IEventSubscription2::FilterCriteria property</span></span>

<span data-ttu-id="a57ce-104">Die Filterkriterien für das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a57ce-104">The filter criteria governing the subscription.</span></span>

<span data-ttu-id="a57ce-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a57ce-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a57ce-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a57ce-106">Syntax</span></span>


```C++
HRESULT put_FilterCriteria(
  [in]          BSTR bstrFilterCriteria
);

HRESULT get_FilterCriteria(
  [out, retval] BSTR *pbstrFilterCriteria
);
```



## <a name="property-value"></a><span data-ttu-id="a57ce-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="a57ce-107">Property value</span></span>

<span data-ttu-id="a57ce-108">Die Filterkriterien oder die CLSID für eine Klasse, die [**ipublisherfilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter)implementiert.</span><span class="sxs-lookup"><span data-stu-id="a57ce-108">The filter criteria or the CLSID for a class implementing [**IPublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter).</span></span>

## <a name="error-codes"></a><span data-ttu-id="a57ce-109">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="a57ce-109">Error codes</span></span>

<span data-ttu-id="a57ce-110">Diese Methode kann die Standard Rückgabewerte e \_ invalidArg, e \_ outo fmemory, e \_ unerwartet, e \_ Fail und S OK \_ zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="a57ce-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="a57ce-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a57ce-111">Requirements</span></span>



| <span data-ttu-id="a57ce-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a57ce-112">Requirement</span></span> | <span data-ttu-id="a57ce-113">Wert</span><span class="sxs-lookup"><span data-stu-id="a57ce-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="a57ce-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a57ce-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a57ce-115">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a57ce-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a57ce-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a57ce-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a57ce-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a57ce-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="a57ce-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a57ce-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a57ce-119">**IEventSubscription2**</span><span class="sxs-lookup"><span data-stu-id="a57ce-119">**IEventSubscription2**</span></span>](ieventsubscription2.md)
</dt> </dl>

 

 




