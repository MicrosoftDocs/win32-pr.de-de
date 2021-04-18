---
description: Die Exit-Methode signalisiert dem streamingthread, den Vorgang zu beenden.
ms.assetid: 1bb59848-e405-40f9-87ec-33de8754e2dd
title: Csourcestream. Exit-Methode (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Exit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1ede6cf2318fa9226b8e220ff526f411def9b0f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351372"
---
# <a name="csourcestreamexit-method"></a><span data-ttu-id="ba615-103">Csourcestream. Exit-Methode</span><span class="sxs-lookup"><span data-stu-id="ba615-103">CSourceStream.Exit method</span></span>

<span data-ttu-id="ba615-104">Die- `Exit` Methode signalisiert dem streamingthread, zu beenden.</span><span class="sxs-lookup"><span data-stu-id="ba615-104">The `Exit` method signals the streaming thread to exit.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba615-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba615-105">Syntax</span></span>


```C++
HRESULT Exit();
```



## <a name="parameters"></a><span data-ttu-id="ba615-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba615-106">Parameters</span></span>

<span data-ttu-id="ba615-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ba615-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ba615-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ba615-108">Return value</span></span>

<span data-ttu-id="ba615-109">Gibt \_ OK oder E \_ unerwartet zurück.</span><span class="sxs-lookup"><span data-stu-id="ba615-109">Returns S\_OK or E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba615-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba615-110">Remarks</span></span>

<span data-ttu-id="ba615-111">Die [**csourcestream:: inaktive**](csourcestream-inactive.md) -Methode ruft diese Methode auf.</span><span class="sxs-lookup"><span data-stu-id="ba615-111">The [**CSourceStream::Inactive**](csourcestream-inactive.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba615-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ba615-112">Requirements</span></span>



| <span data-ttu-id="ba615-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ba615-113">Requirement</span></span> | <span data-ttu-id="ba615-114">Wert</span><span class="sxs-lookup"><span data-stu-id="ba615-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba615-115">Header</span><span class="sxs-lookup"><span data-stu-id="ba615-115">Header</span></span><br/>  | <dl> <span data-ttu-id="ba615-116"><dt>Source. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ba615-116"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ba615-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ba615-117">Library</span></span><br/> | <dl> <span data-ttu-id="ba615-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ba615-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba615-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba615-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba615-120">**Csourcestream-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ba615-120">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




