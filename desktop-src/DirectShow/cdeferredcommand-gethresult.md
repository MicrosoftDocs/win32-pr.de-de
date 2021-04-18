---
description: Die GetHRESULT-Methode ruft den HRESULT-Wert aus dem aufgerufenen Befehl ab.
ms.assetid: 7e88a2bd-6b1b-4e59-b185-5dfd501fc37a
title: Cdeferredcommand. GetHRESULT-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetHResult
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5b09049bc443991dabe07a7626ffc42097feceee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371559"
---
# <a name="cdeferredcommandgethresult-method"></a><span data-ttu-id="1e8a2-103">Cdeferredcommand. GetHRESULT-Methode</span><span class="sxs-lookup"><span data-stu-id="1e8a2-103">CDeferredCommand.GetHResult method</span></span>

<span data-ttu-id="1e8a2-104">Die- `GetHResult` Methode ruft den **HRESULT** -Wert aus dem aufgerufenen Befehl ab.</span><span class="sxs-lookup"><span data-stu-id="1e8a2-104">The `GetHResult` method retrieves the **HRESULT** value from the invoked command.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e8a2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e8a2-105">Syntax</span></span>


```C++
HRESULT GetHResult(
   HRESULT *phrResult
);
```



## <a name="parameters"></a><span data-ttu-id="1e8a2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e8a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e8a2-107">*phrresult*</span><span class="sxs-lookup"><span data-stu-id="1e8a2-107">*phrResult*</span></span> 
</dt> <dd>

<span data-ttu-id="1e8a2-108">Zeiger auf den **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="1e8a2-108">Pointer to the **HRESULT** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e8a2-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1e8a2-109">Return value</span></span>

<span data-ttu-id="1e8a2-110">Gibt E \_ Abort zurück, wenn **m \_ pqueue** den Wert **null** hat.</span><span class="sxs-lookup"><span data-stu-id="1e8a2-110">Returns E\_ABORT if **m\_pQueue** is **NULL**.</span></span> <span data-ttu-id="1e8a2-111">Andernfalls gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="1e8a2-111">Otherwise, returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e8a2-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e8a2-112">Remarks</span></span>

<span data-ttu-id="1e8a2-113">Diese Member-Funktion implementiert die [**ideferredcommand:: GetHRESULT**](/windows/desktop/api/Control/nf-control-ideferredcommand-gethresult) -Methode.</span><span class="sxs-lookup"><span data-stu-id="1e8a2-113">This member function implements the [**IDeferredCommand::GetHResult**](/windows/desktop/api/Control/nf-control-ideferredcommand-gethresult) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e8a2-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e8a2-114">Requirements</span></span>



| <span data-ttu-id="1e8a2-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e8a2-115">Requirement</span></span> | <span data-ttu-id="1e8a2-116">Wert</span><span class="sxs-lookup"><span data-stu-id="1e8a2-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e8a2-117">Header</span><span class="sxs-lookup"><span data-stu-id="1e8a2-117">Header</span></span><br/>  | <dl> <span data-ttu-id="1e8a2-118"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1e8a2-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1e8a2-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1e8a2-119">Library</span></span><br/> | <dl> <span data-ttu-id="1e8a2-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="1e8a2-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e8a2-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e8a2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e8a2-122">**Cdeferredcommand-Klasse**</span><span class="sxs-lookup"><span data-stu-id="1e8a2-122">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




