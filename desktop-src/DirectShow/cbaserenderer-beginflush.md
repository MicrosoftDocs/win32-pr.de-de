---
description: 'CBaseRenderer.BeginFlush-Methode: Die BeginFlush-Methode startet einen Leerungsvorgang.'
ms.assetid: dc652394-c24e-4cea-ac28-30a1e6de205f
title: CBaseRenderer.BeginFlush-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 76dfd77a5170a83813871143781868cae55c45ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095938"
---
# <a name="cbaserendererbeginflush-method"></a><span data-ttu-id="32b3a-103">CBaseRenderer.BeginFlush-Methode</span><span class="sxs-lookup"><span data-stu-id="32b3a-103">CBaseRenderer.BeginFlush method</span></span>

<span data-ttu-id="32b3a-104">Die `BeginFlush` -Methode startet einen Leerungsvorgang.</span><span class="sxs-lookup"><span data-stu-id="32b3a-104">The `BeginFlush` method begins a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="32b3a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="32b3a-105">Syntax</span></span>


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="32b3a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="32b3a-106">Parameters</span></span>

<span data-ttu-id="32b3a-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="32b3a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="32b3a-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="32b3a-108">Return value</span></span>

<span data-ttu-id="32b3a-109">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="32b3a-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="32b3a-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="32b3a-110">Remarks</span></span>

<span data-ttu-id="32b3a-111">Der Eingabepin des Filters ruft diese Methode auf, wenn er einen Aufruf der [**IPin::BeginFlush-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) empfängt.</span><span class="sxs-lookup"><span data-stu-id="32b3a-111">The filter's input pin calls this method when it receives a call to the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method.</span></span> <span data-ttu-id="32b3a-112">Der Filter gibt den Streamingthread und alle Beispiele frei, die er für das Rendering enthalten hat.</span><span class="sxs-lookup"><span data-stu-id="32b3a-112">The filter releases the streaming thread, and releases any sample that it was holding for rendering.</span></span>

## <a name="requirements"></a><span data-ttu-id="32b3a-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="32b3a-113">Requirements</span></span>



| <span data-ttu-id="32b3a-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="32b3a-114">Requirement</span></span> | <span data-ttu-id="32b3a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="32b3a-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32b3a-116">Header</span><span class="sxs-lookup"><span data-stu-id="32b3a-116">Header</span></span><br/>  | <dl> <span data-ttu-id="32b3a-117"><dt>Renbase.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="32b3a-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="32b3a-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="32b3a-118">Library</span></span><br/> | <dl> <span data-ttu-id="32b3a-119"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="32b3a-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32b3a-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="32b3a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32b3a-121">**CBaseRenderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="32b3a-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




