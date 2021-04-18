---
description: Die Remove-Methode entfernt das cdeferredcommand-Objekt aus der Warteschlange.
ms.assetid: b3cff57d-9625-40db-b815-9529ac706f45
title: Ccmdqueue. Remove-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Remove
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef9f45c8176645c5937b5ad74045130ff8cd8c06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364458"
---
# <a name="ccmdqueueremove-method"></a><span data-ttu-id="a4af7-103">Ccmdqueue. Remove-Methode</span><span class="sxs-lookup"><span data-stu-id="a4af7-103">CCmdQueue.Remove method</span></span>

<span data-ttu-id="a4af7-104">Die- `Remove` Methode entfernt das [**cdeferredcommand**](cdeferredcommand.md) -Objekt aus der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="a4af7-104">The `Remove` method removes the [**CDeferredCommand**](cdeferredcommand.md) object from the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4af7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4af7-105">Syntax</span></span>


```C++
virtual HRESULT Remove(
   CDeferredCommand *pCmd
);
```



## <a name="parameters"></a><span data-ttu-id="a4af7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4af7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4af7-107">*pCmd*</span><span class="sxs-lookup"><span data-stu-id="a4af7-107">*pCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="a4af7-108">Zeiger auf das **cdeferredcommand** -Objekt, das aus der Warteschlange entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a4af7-108">Pointer to the **CDeferredCommand** object to remove from the queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4af7-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a4af7-109">Return value</span></span>

<span data-ttu-id="a4af7-110">Gibt VFW \_ E \_ nicht \_ gefunden zurück, wenn das Objekt in der Warteschlange nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="a4af7-110">Returns VFW\_E\_NOT\_FOUND if the object is not found in the queue.</span></span> <span data-ttu-id="a4af7-111">Andernfalls gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="a4af7-111">Otherwise, returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4af7-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a4af7-112">Requirements</span></span>



| <span data-ttu-id="a4af7-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a4af7-113">Requirement</span></span> | <span data-ttu-id="a4af7-114">Wert</span><span class="sxs-lookup"><span data-stu-id="a4af7-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4af7-115">Header</span><span class="sxs-lookup"><span data-stu-id="a4af7-115">Header</span></span><br/>  | <dl> <span data-ttu-id="a4af7-116"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a4af7-116"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a4af7-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a4af7-117">Library</span></span><br/> | <dl> <span data-ttu-id="a4af7-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a4af7-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4af7-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4af7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4af7-120">**Ccmdqueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a4af7-120">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




