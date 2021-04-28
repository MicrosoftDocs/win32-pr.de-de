---
description: 'CMsgThread.CMsgThread-Konstruktor : Konstruktormethode.'
ms.assetid: 3f758c45-21ec-4728-ba7d-41da7b2fa02f
title: CMsgThread.CMsgThread-Konstruktor (Msgthrd.h)
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
ms.openlocfilehash: 08d76ebecd09d95b7ba0fca22b300c1e402f5302
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095368"
---
# <a name="cmsgthreadcmsgthread-constructor"></a><span data-ttu-id="fb189-103">CMsgThread.CMsgThread-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="fb189-103">CMsgThread.CMsgThread constructor</span></span>

<span data-ttu-id="fb189-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="fb189-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb189-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb189-105">Syntax</span></span>


```C++
CMsgThread();
```



## <a name="parameters"></a><span data-ttu-id="fb189-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb189-106">Parameters</span></span>

<span data-ttu-id="fb189-107">Dieser Konstruktor verfügt über keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="fb189-107">This constructor has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb189-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb189-108">Remarks</span></span>

<span data-ttu-id="fb189-109">Beim Erstellen eines Nachrichtenthreadobjekts wird der Thread nicht automatisch erstellt.</span><span class="sxs-lookup"><span data-stu-id="fb189-109">Constructing a message thread object does not automatically create the thread.</span></span> <span data-ttu-id="fb189-110">Sie müssen die [**CMsgThread::CreateThread-Memberfunktion**](cmsgthread-createthread.md) aufrufen, um den Thread zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fb189-110">You must call the [**CMsgThread::CreateThread**](cmsgthread-createthread.md) member function to create the thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb189-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb189-111">Requirements</span></span>



| <span data-ttu-id="fb189-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb189-112">Requirement</span></span> | <span data-ttu-id="fb189-113">Wert</span><span class="sxs-lookup"><span data-stu-id="fb189-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb189-114">Header</span><span class="sxs-lookup"><span data-stu-id="fb189-114">Header</span></span><br/>  | <dl> <span data-ttu-id="fb189-115"><dt>Msgthrd.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="fb189-115"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fb189-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fb189-116">Library</span></span><br/> | <dl> <span data-ttu-id="fb189-117"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="fb189-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb189-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fb189-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb189-119">**CMsgThread-Klasse**</span><span class="sxs-lookup"><span data-stu-id="fb189-119">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




