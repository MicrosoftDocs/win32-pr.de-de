---
description: Die Anwendungs-GUID des Ereignis Klassen Objekts.
ms.assetid: 0d19183a-429c-4564-b6a5-f06481d27e00
title: 'IEventSubscription3:: eventclassapplicationid (Eigenschaft)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.EventClassApplicationID
- IEventSubscription3.get_EventClassApplicationID
- IEventSubscription3.put_EventClassApplicationID
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3e80a8d8f557c80a1b2605328728260eb8ae7bd7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127029"
---
# <a name="ieventsubscription3eventclassapplicationid-property"></a><span data-ttu-id="73d3f-103">IEventSubscription3:: eventclassapplicationid (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="73d3f-103">IEventSubscription3::EventClassApplicationID property</span></span>

<span data-ttu-id="73d3f-104">Die Anwendungs-GUID des Ereignis Klassen Objekts.</span><span class="sxs-lookup"><span data-stu-id="73d3f-104">The application GUID of the event class object.</span></span>

<span data-ttu-id="73d3f-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="73d3f-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="73d3f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="73d3f-106">Syntax</span></span>


```C++
HRESULT put_EventClassApplicationID(
  [in]          BSTR bstrEventClassApplicationID
);

HRESULT get_EventClassApplicationID(
  [out, retval] BSTR *pbstrEventClassApplicationID
);
```



## <a name="property-value"></a><span data-ttu-id="73d3f-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="73d3f-107">Property value</span></span>

<span data-ttu-id="73d3f-108">Eine Zeichenfolge, die die GUID der Ereignis Klassen Anwendung enthält.</span><span class="sxs-lookup"><span data-stu-id="73d3f-108">A string containing the GUID of the event class application.</span></span>

## <a name="error-codes"></a><span data-ttu-id="73d3f-109">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="73d3f-109">Error codes</span></span>

<span data-ttu-id="73d3f-110">Diese Methode kann die Standard Rückgabewerte e \_ invalidArg, e \_ outo fmemory, e \_ unerwartet, e \_ Fail und S OK \_ zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="73d3f-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="73d3f-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73d3f-111">Requirements</span></span>



| <span data-ttu-id="73d3f-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="73d3f-112">Requirement</span></span> | <span data-ttu-id="73d3f-113">Wert</span><span class="sxs-lookup"><span data-stu-id="73d3f-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="73d3f-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="73d3f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="73d3f-115">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73d3f-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="73d3f-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="73d3f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="73d3f-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73d3f-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="73d3f-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73d3f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73d3f-119">**IEventSubscription3**</span><span class="sxs-lookup"><span data-stu-id="73d3f-119">**IEventSubscription3**</span></span>](ieventsubscription3.md)
</dt> </dl>

 

 




