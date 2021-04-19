---
description: Die Methode zum Verschieben gibt eine neue Präsentationszeit für einen zuvor in die Warteschlange eingereihten Befehl an.
ms.assetid: 6201eb18-8180-445c-8d29-980511748fe4
title: Cdeferredcommand. Verschiebungen-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Postpone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9ce19c5391541336f52dd872b44bb9f3a447c27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106374031"
---
# <a name="cdeferredcommandpostpone-method"></a><span data-ttu-id="bdde6-103">Cdeferredcommand. Verschiebungen-Methode</span><span class="sxs-lookup"><span data-stu-id="bdde6-103">CDeferredCommand.Postpone method</span></span>

<span data-ttu-id="bdde6-104">Die- `Postpone` Methode gibt eine neue Präsentationszeit für einen zuvor in die Warteschlange eingereihten Befehl an.</span><span class="sxs-lookup"><span data-stu-id="bdde6-104">The `Postpone` method specifies a new presentation time for a previously queued command.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdde6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bdde6-105">Syntax</span></span>


```C++
HRESULT Postpone(
   REFTIME newtime
);
```



## <a name="parameters"></a><span data-ttu-id="bdde6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bdde6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdde6-107">*Neuzeit*</span><span class="sxs-lookup"><span data-stu-id="bdde6-107">*newtime*</span></span> 
</dt> <dd>

<span data-ttu-id="bdde6-108">Neue Präsentationszeit.</span><span class="sxs-lookup"><span data-stu-id="bdde6-108">New presentation time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdde6-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bdde6-109">Return value</span></span>

<span data-ttu-id="bdde6-110">Gibt eine VFW E-Zeit zurück, die \_ \_ \_ bereits \_ vergangen ist, wenn *newTime* bereits vergangen ist</span><span class="sxs-lookup"><span data-stu-id="bdde6-110">Returns VFW\_E\_TIME\_ALREADY\_PASSED if *newtime* is already passed.</span></span> <span data-ttu-id="bdde6-111">Andernfalls wird ein **HRESULT** zurückgegeben, das sich aus einem Aufruf von [**ccmdqueue:: Remove**](ccmdqueue-remove.md) (beim Extrahieren aus der Liste) oder [**ccmdqueue:: Insert**](ccmdqueue-insert.md) ergibt (beim erneuten Verwenden der geänderten Zeit).</span><span class="sxs-lookup"><span data-stu-id="bdde6-111">Otherwise, returns an **HRESULT** resulting from a call to [**CCmdQueue::Remove**](ccmdqueue-remove.md) (when extracting from the list) or [**CCmdQueue::Insert**](ccmdqueue-insert.md) (when reinserting with the changed time).</span></span>

## <a name="remarks"></a><span data-ttu-id="bdde6-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bdde6-112">Remarks</span></span>

<span data-ttu-id="bdde6-113">Diese Member-Funktion implementiert die [**ideferredcommand::P ostpone**](/windows/desktop/api/Control/nf-control-ideferredcommand-postpone) -Methode.</span><span class="sxs-lookup"><span data-stu-id="bdde6-113">This member function implements the [**IDeferredCommand::Postpone**](/windows/desktop/api/Control/nf-control-ideferredcommand-postpone) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdde6-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bdde6-114">Requirements</span></span>



| <span data-ttu-id="bdde6-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bdde6-115">Requirement</span></span> | <span data-ttu-id="bdde6-116">Wert</span><span class="sxs-lookup"><span data-stu-id="bdde6-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdde6-117">Header</span><span class="sxs-lookup"><span data-stu-id="bdde6-117">Header</span></span><br/>  | <dl> <span data-ttu-id="bdde6-118"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bdde6-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bdde6-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bdde6-119">Library</span></span><br/> | <dl> <span data-ttu-id="bdde6-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="bdde6-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdde6-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bdde6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdde6-122">**Cdeferredcommand-Klasse**</span><span class="sxs-lookup"><span data-stu-id="bdde6-122">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




