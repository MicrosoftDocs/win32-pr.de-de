---
description: Die Insert-Methode fügt der Warteschlange ein cdeferredcommand-Objekt hinzu.
ms.assetid: 41f9c30c-6267-435a-9089-eb34ae606896
title: Ccmdqueue. Insert-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Insert
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6bad004641258e29ed42d7142a5b0ab2c0ceb78d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369541"
---
# <a name="ccmdqueueinsert-method"></a><span data-ttu-id="c6484-103">Ccmdqueue. Insert-Methode</span><span class="sxs-lookup"><span data-stu-id="c6484-103">CCmdQueue.Insert method</span></span>

<span data-ttu-id="c6484-104">Die- `Insert` Methode fügt der Warteschlange ein [**cdeferredcommand**](cdeferredcommand.md) -Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="c6484-104">The `Insert` method adds a [**CDeferredCommand**](cdeferredcommand.md) object to the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6484-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6484-105">Syntax</span></span>


```C++
virtual HRESULT Insert(
   CDeferredCommand *pCmd
);
```



## <a name="parameters"></a><span data-ttu-id="c6484-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6484-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6484-107">*pCmd*</span><span class="sxs-lookup"><span data-stu-id="c6484-107">*pCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="c6484-108">Zeiger auf das **cdeferredcommand** -Objekt, das der Warteschlange hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c6484-108">Pointer to the **CDeferredCommand** object to add to the queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6484-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c6484-109">Return value</span></span>

<span data-ttu-id="c6484-110">Gibt S \_ OK in der Standard Implementierung zurück.</span><span class="sxs-lookup"><span data-stu-id="c6484-110">Returns S\_OK in the default implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6484-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6484-111">Requirements</span></span>



| <span data-ttu-id="c6484-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6484-112">Requirement</span></span> | <span data-ttu-id="c6484-113">Wert</span><span class="sxs-lookup"><span data-stu-id="c6484-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6484-114">Header</span><span class="sxs-lookup"><span data-stu-id="c6484-114">Header</span></span><br/>  | <dl> <span data-ttu-id="c6484-115"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c6484-115"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c6484-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c6484-116">Library</span></span><br/> | <dl> <span data-ttu-id="c6484-117">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c6484-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6484-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6484-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6484-119">**Ccmdqueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c6484-119">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




