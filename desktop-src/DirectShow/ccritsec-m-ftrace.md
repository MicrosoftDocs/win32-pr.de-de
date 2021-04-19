---
description: Boolescher Wert, der angibt, ob diese Sperre verfolgt werden soll.
ms.assetid: 23417410-cfdc-426e-a662-7d6580b43a28
title: 'Ccritsec:: m_fTrace Member (wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_fTrace
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 691e078bb3b502704aed585ba020d49b2bd99af1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370322"
---
# <a name="ccritsecm_ftrace-member"></a><span data-ttu-id="5fe77-103">Ccritsec:: m \_ ftrace-Member</span><span class="sxs-lookup"><span data-stu-id="5fe77-103">CCritSec::m\_fTrace member</span></span>

<span data-ttu-id="5fe77-104">Boolescher Wert, der angibt, ob diese Sperre verfolgt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5fe77-104">Boolean value that specifies whether to trace this lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fe77-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5fe77-105">Syntax</span></span>


```C++
BOOL m_fTrace;
```



## <a name="remarks"></a><span data-ttu-id="5fe77-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5fe77-106">Remarks</span></span>

<span data-ttu-id="5fe77-107">Diese Member-Variable wird nur in der Debugversion der Basisklasse definiert.</span><span class="sxs-lookup"><span data-stu-id="5fe77-107">This member variable is defined only in the debug version of the base class.</span></span> <span data-ttu-id="5fe77-108">Wenn der Wert **true** ist, wird eine Ablauf Verfolgung des Sperr Zustands in das Debugprotokoll geschrieben.</span><span class="sxs-lookup"><span data-stu-id="5fe77-108">If the value is **TRUE**, a trace of the lock state is written to the debug log.</span></span> <span data-ttu-id="5fe77-109">(Die Debugprotokollierung für kritische Abschnitte muss aktiv sein.) Weitere Informationen finden Sie unter [**dbglocktrace**](dbglocktrace.md).</span><span class="sxs-lookup"><span data-stu-id="5fe77-109">(Debug logging for critical sections must be active.) For more information, see [**DbgLockTrace**](dbglocktrace.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5fe77-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5fe77-110">Requirements</span></span>



| <span data-ttu-id="5fe77-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5fe77-111">Requirement</span></span> | <span data-ttu-id="5fe77-112">Wert</span><span class="sxs-lookup"><span data-stu-id="5fe77-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fe77-113">Header</span><span class="sxs-lookup"><span data-stu-id="5fe77-113">Header</span></span><br/>  | <dl> <span data-ttu-id="5fe77-114"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5fe77-114"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="5fe77-115">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5fe77-115">Library</span></span><br/> | <dl> <span data-ttu-id="5fe77-116">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="5fe77-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fe77-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5fe77-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fe77-118">**Ccritsec-Klasse**</span><span class="sxs-lookup"><span data-stu-id="5fe77-118">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

 




