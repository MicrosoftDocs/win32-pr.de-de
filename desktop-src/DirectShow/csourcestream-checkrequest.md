---
description: Die CheckRequest-Methode überprüft, ob eine Thread Anforderung vorhanden ist, ohne zu blockieren.
ms.assetid: b4691dde-abec-4671-bea6-0f22cc4e7c61
title: Csourcestream. CheckRequest-Methode (Quelle. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CheckRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3100d449d2f29b2080541c5968cad6abc5643b26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359406"
---
# <a name="csourcestreamcheckrequest-method"></a><span data-ttu-id="2bf39-103">Csourcestream. CheckRequest-Methode</span><span class="sxs-lookup"><span data-stu-id="2bf39-103">CSourceStream.CheckRequest method</span></span>

<span data-ttu-id="2bf39-104">Die- `CheckRequest` Methode überprüft, ob eine Thread Anforderung vorhanden ist, ohne zu blockieren.</span><span class="sxs-lookup"><span data-stu-id="2bf39-104">The `CheckRequest` method checks if there is a thread request, without blocking.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bf39-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2bf39-105">Syntax</span></span>


```C++
BOOL CheckRequest(
   Command *pCom
);
```



## <a name="parameters"></a><span data-ttu-id="2bf39-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2bf39-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bf39-107">*pCom*</span><span class="sxs-lookup"><span data-stu-id="2bf39-107">*pCom*</span></span> 
</dt> <dd>

<span data-ttu-id="2bf39-108">Ein Zeiger auf eine Variable, die den Wert empfängt, der beim letzten Aufruf der Methode " [**camthread:: callworker**](camthread-callworker.md) " übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="2bf39-108">Pointer to a variable that receives the value passed in the last call to the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bf39-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2bf39-109">Return value</span></span>

<span data-ttu-id="2bf39-110">Gibt **true** zurück, wenn eine ausstehende Anforderung vorhanden ist, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="2bf39-110">Returns **TRUE** if there is a pending request, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bf39-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2bf39-111">Remarks</span></span>

<span data-ttu-id="2bf39-112">Diese Methode überschreibt die Methode " [**camthread:: CheckRequest**](camthread-checkrequest.md) ", um eine Typüberprüfung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="2bf39-112">This method overrides the [**CAMThread::CheckRequest**](camthread-checkrequest.md) method to perform type-checking.</span></span> <span data-ttu-id="2bf39-113">Die **csourcestream** -Klasse definiert den folgenden enumerierten Typ für den *pCom* -Parameter:</span><span class="sxs-lookup"><span data-stu-id="2bf39-113">The **CSourceStream** class defines the following enumerated type for the *pCom* parameter:</span></span>


```C++
enum Command {CMD_INIT, CMD_PAUSE, CMD_RUN, CMD_STOP, CMD_EXIT};
```



## <a name="requirements"></a><span data-ttu-id="2bf39-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2bf39-114">Requirements</span></span>



| <span data-ttu-id="2bf39-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2bf39-115">Requirement</span></span> | <span data-ttu-id="2bf39-116">Wert</span><span class="sxs-lookup"><span data-stu-id="2bf39-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bf39-117">Header</span><span class="sxs-lookup"><span data-stu-id="2bf39-117">Header</span></span><br/>  | <dl> <span data-ttu-id="2bf39-118"><dt>Source. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2bf39-118"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="2bf39-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2bf39-119">Library</span></span><br/> | <dl> <span data-ttu-id="2bf39-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="2bf39-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bf39-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2bf39-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bf39-122">**Csourcestream-Klasse**</span><span class="sxs-lookup"><span data-stu-id="2bf39-122">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




