---
description: Überprüft, ob alle vorübergehenden Abonnenten im Datenspeicher vorhanden sind. Wenn Sie diese Methode aufrufen, können Sie sicherstellen, dass alle im Datenspeicher aufgelisteten vorübergehenden Abonnenten aktiv sind.
ms.assetid: fffdde33-e960-42ef-a089-8ea8a6f33d52
title: 'IEventSystem2:: verifytransientabonnenten-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2.VerifyTransientSubscribers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4415f405b95f341b645ca1dccbf254df2ffc7167
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958320"
---
# <a name="ieventsystem2verifytransientsubscribers-method"></a><span data-ttu-id="baf0c-104">IEventSystem2:: verifytransientabonnenten-Methode</span><span class="sxs-lookup"><span data-stu-id="baf0c-104">IEventSystem2::VerifyTransientSubscribers method</span></span>

<span data-ttu-id="baf0c-105">Überprüft, ob alle vorübergehenden Abonnenten im Datenspeicher vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="baf0c-105">Verifies the existence of all transient subscribers in the data store.</span></span> <span data-ttu-id="baf0c-106">Wenn Sie diese Methode aufrufen, können Sie sicherstellen, dass alle im Datenspeicher aufgelisteten vorübergehenden Abonnenten aktiv sind.</span><span class="sxs-lookup"><span data-stu-id="baf0c-106">By calling this method, you can ensure that all transient subscribers listed in the data store are active.</span></span>

## <a name="syntax"></a><span data-ttu-id="baf0c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="baf0c-107">Syntax</span></span>


```C++
HRESULT VerifyTransientSubscribers();
```



## <a name="parameters"></a><span data-ttu-id="baf0c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="baf0c-108">Parameters</span></span>

<span data-ttu-id="baf0c-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="baf0c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="baf0c-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="baf0c-110">Return value</span></span>

<span data-ttu-id="baf0c-111">Diese Methode kann die Standard Rückgabewerte e \_ invalidArg, e \_ outo fmemory, e \_ unerwartet, e \_ Fail und S OK \_ zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="baf0c-111">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="baf0c-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="baf0c-112">Requirements</span></span>



| <span data-ttu-id="baf0c-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="baf0c-113">Requirement</span></span> | <span data-ttu-id="baf0c-114">Wert</span><span class="sxs-lookup"><span data-stu-id="baf0c-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="baf0c-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="baf0c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="baf0c-116">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="baf0c-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="baf0c-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="baf0c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="baf0c-118">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="baf0c-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="baf0c-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="baf0c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baf0c-120">**IEventSystem2**</span><span class="sxs-lookup"><span data-stu-id="baf0c-120">**IEventSystem2**</span></span>](ieventsystem2.md)
</dt> </dl>

 

 




