---
description: 'CCritSec.~CCritSec-Destruktor : Destruktormethode.'
ms.assetid: cade850c-391c-41dc-adfe-56de8b2bbfff
title: CCritSec.~CCritSec-Destruktor (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.~CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6f282bfe6ea6bca8cb8553572c18cfbc85db6c77
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095808"
---
# <a name="ccritsecccritsec-destructor"></a><span data-ttu-id="eb1a6-103">CCritSec.~CCritSec-Destruktor</span><span class="sxs-lookup"><span data-stu-id="eb1a6-103">CCritSec.~CCritSec destructor</span></span>

<span data-ttu-id="eb1a6-104">Destruktormethode.</span><span class="sxs-lookup"><span data-stu-id="eb1a6-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb1a6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb1a6-105">Syntax</span></span>


```C++
~CCritSec();
```



## <a name="remarks"></a><span data-ttu-id="eb1a6-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb1a6-106">Remarks</span></span>

<span data-ttu-id="eb1a6-107">Diese Methode ruft die [**DeleteCriticalSection-Funktion**](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection) auf, um den kritischen Abschnitt zu löschen.</span><span class="sxs-lookup"><span data-stu-id="eb1a6-107">This method calls the [**DeleteCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection) function to delete the critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb1a6-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb1a6-108">Requirements</span></span>



| <span data-ttu-id="eb1a6-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb1a6-109">Requirement</span></span> | <span data-ttu-id="eb1a6-110">Wert</span><span class="sxs-lookup"><span data-stu-id="eb1a6-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb1a6-111">Header</span><span class="sxs-lookup"><span data-stu-id="eb1a6-111">Header</span></span><br/>  | <dl> <span data-ttu-id="eb1a6-112"><dt>Wxutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="eb1a6-112"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="eb1a6-113">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="eb1a6-113">Library</span></span><br/> | <dl> <span data-ttu-id="eb1a6-114"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="eb1a6-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb1a6-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="eb1a6-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb1a6-116">**CCritSec-Klasse**</span><span class="sxs-lookup"><span data-stu-id="eb1a6-116">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

