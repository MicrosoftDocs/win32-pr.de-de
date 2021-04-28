---
description: 'CBaseRenderer.EndFlush-Methode: Die EndFlush-Methode beendet einen Leerungsvorgang.'
ms.assetid: 4c30abbf-7351-4eee-af9a-9330f6d1aa08
title: CBaseRenderer.EndFlush-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 87e29f405430ca87943773d19793ffc1941ec42c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095908"
---
# <a name="cbaserendererendflush-method"></a><span data-ttu-id="005e6-103">CBaseRenderer.EndFlush-Methode</span><span class="sxs-lookup"><span data-stu-id="005e6-103">CBaseRenderer.EndFlush method</span></span>

<span data-ttu-id="005e6-104">Die `EndFlush` -Methode beendet einen Leerungsvorgang.</span><span class="sxs-lookup"><span data-stu-id="005e6-104">The `EndFlush` method ends a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="005e6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="005e6-105">Syntax</span></span>


```C++
virtual HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="005e6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="005e6-106">Parameters</span></span>

<span data-ttu-id="005e6-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="005e6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="005e6-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="005e6-108">Return value</span></span>

<span data-ttu-id="005e6-109">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="005e6-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="005e6-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="005e6-110">Remarks</span></span>

<span data-ttu-id="005e6-111">Der Eingabepin des Filters ruft diese Methode auf, wenn er einen Aufruf der [**IPin::EndFlush-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) empfängt.</span><span class="sxs-lookup"><span data-stu-id="005e6-111">The filter's input pin calls this method when it receives a call to the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="005e6-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="005e6-112">Requirements</span></span>



| <span data-ttu-id="005e6-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="005e6-113">Requirement</span></span> | <span data-ttu-id="005e6-114">Wert</span><span class="sxs-lookup"><span data-stu-id="005e6-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="005e6-115">Header</span><span class="sxs-lookup"><span data-stu-id="005e6-115">Header</span></span><br/>  | <dl> <span data-ttu-id="005e6-116"><dt>Renbase.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="005e6-116"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="005e6-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="005e6-117">Library</span></span><br/> | <dl> <span data-ttu-id="005e6-118"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="005e6-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="005e6-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="005e6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="005e6-120">**CBaseRenderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="005e6-120">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




