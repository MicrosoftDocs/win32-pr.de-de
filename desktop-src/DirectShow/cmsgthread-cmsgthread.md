---
description: Konstruktormethode.
ms.assetid: 3f758c45-21ec-4728-ba7d-41da7b2fa02f
title: Cmsgthread. cmsgthread-Konstruktor (msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.CMsgThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e77d3a84e349ab370b6319cd973f6ba86d632366
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370738"
---
# <a name="cmsgthreadcmsgthread-constructor"></a><span data-ttu-id="3d066-103">Cmsgthread. cmsgthread-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="3d066-103">CMsgThread.CMsgThread constructor</span></span>

<span data-ttu-id="3d066-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="3d066-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d066-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d066-105">Syntax</span></span>


```C++
CMsgThread();
```



## <a name="parameters"></a><span data-ttu-id="3d066-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d066-106">Parameters</span></span>

<span data-ttu-id="3d066-107">Dieser Konstruktor weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="3d066-107">This constructor has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d066-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d066-108">Remarks</span></span>

<span data-ttu-id="3d066-109">Beim Konstruieren eines Nachrichten Thread Objekts wird der Thread nicht automatisch erstellt.</span><span class="sxs-lookup"><span data-stu-id="3d066-109">Constructing a message thread object does not automatically create the thread.</span></span> <span data-ttu-id="3d066-110">Sie müssen die Member-Funktion [**cmsgthread:: foratethread**](cmsgthread-createthread.md) aufrufen, um den Thread zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3d066-110">You must call the [**CMsgThread::CreateThread**](cmsgthread-createthread.md) member function to create the thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d066-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d066-111">Requirements</span></span>



| <span data-ttu-id="3d066-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d066-112">Requirement</span></span> | <span data-ttu-id="3d066-113">Wert</span><span class="sxs-lookup"><span data-stu-id="3d066-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d066-114">Header</span><span class="sxs-lookup"><span data-stu-id="3d066-114">Header</span></span><br/>  | <dl> <span data-ttu-id="3d066-115"><dt>Msgthrd. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3d066-115"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3d066-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3d066-116">Library</span></span><br/> | <dl> <span data-ttu-id="3d066-117">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="3d066-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d066-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d066-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d066-119">**Cmsgthread-Klasse**</span><span class="sxs-lookup"><span data-stu-id="3d066-119">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




