---
description: Die Partitions-GUID des Ereignis Klassen Objekts.
ms.assetid: 154849ac-350c-4b2f-bb51-ac6973f0a8fa
title: 'IEventSubscription3:: eventclasspartitionid (Eigenschaft)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.EventClassPartitionID
- IEventSubscription3.get_EventClassPartitionID
- IEventSubscription3.put_EventClassPartitionID
api_type:
- COM
api_location: ''
ms.openlocfilehash: d41d3e2a170deffb73f1f533226421d88f150c01
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524203"
---
# <a name="ieventsubscription3eventclasspartitionid-property"></a><span data-ttu-id="0f2c8-103">IEventSubscription3:: eventclasspartitionid (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0f2c8-103">IEventSubscription3::EventClassPartitionID property</span></span>

<span data-ttu-id="0f2c8-104">Die Partitions-GUID des Ereignis Klassen Objekts.</span><span class="sxs-lookup"><span data-stu-id="0f2c8-104">The partition GUID of the event class object.</span></span>

<span data-ttu-id="0f2c8-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="0f2c8-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f2c8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f2c8-106">Syntax</span></span>


```C++
HRESULT put_EventClassPartitionID(
  [in]          BSTR bstrEventClassPartitionID
);

HRESULT get_EventClassPartitionID(
  [out, retval] BSTR *pbstrEventClassPartitionID
);
```



## <a name="property-value"></a><span data-ttu-id="0f2c8-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="0f2c8-107">Property value</span></span>

<span data-ttu-id="0f2c8-108">Eine Zeichenfolge, die die GUID der Ereignis Klassen Partition enthält.</span><span class="sxs-lookup"><span data-stu-id="0f2c8-108">A string containing the GUID of the event class partition.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0f2c8-109">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="0f2c8-109">Error codes</span></span>

<span data-ttu-id="0f2c8-110">Diese Methode kann die Standard Rückgabewerte e \_ invalidArg, e \_ outo fmemory, e \_ unerwartet, e \_ Fail und S OK \_ zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="0f2c8-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f2c8-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f2c8-111">Requirements</span></span>



| <span data-ttu-id="0f2c8-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f2c8-112">Requirement</span></span> | <span data-ttu-id="0f2c8-113">Wert</span><span class="sxs-lookup"><span data-stu-id="0f2c8-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="0f2c8-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0f2c8-114">Minimum supported client</span></span><br/> | <span data-ttu-id="0f2c8-115">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0f2c8-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0f2c8-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0f2c8-116">Minimum supported server</span></span><br/> | <span data-ttu-id="0f2c8-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0f2c8-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="0f2c8-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f2c8-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f2c8-119">**IEventSubscription3**</span><span class="sxs-lookup"><span data-stu-id="0f2c8-119">**IEventSubscription3**</span></span>](ieventsubscription3.md)
</dt> </dl>

 

 




