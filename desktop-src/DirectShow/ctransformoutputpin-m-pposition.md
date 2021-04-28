---
description: 'CTransformOutputPin::m_pPosition Member : Hilfsobjekt zum Übergeben von Seek-Befehlen im Upstream.'
ms.assetid: 2ca9bae7-a133-4e09-8aa7-1c4601ec5db0
title: CTransformOutputPin::m_pPosition-Member (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pPosition
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b9c5a1b5d5ced7a9f3985ceebdd2bdcb8e491d2e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084858"
---
# <a name="ctransformoutputpinm_pposition-member"></a><span data-ttu-id="d027a-103">CTransformOutputPin::m \_ pPosition-Member</span><span class="sxs-lookup"><span data-stu-id="d027a-103">CTransformOutputPin::m\_pPosition member</span></span>

<span data-ttu-id="d027a-104">Hilfsobjekt zum Übergeben von Suchbefehlen im Upstream.</span><span class="sxs-lookup"><span data-stu-id="d027a-104">Helper object to pass seek commands upstream.</span></span>

## <a name="syntax"></a><span data-ttu-id="d027a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d027a-105">Syntax</span></span>


```C++
IUnknown *m_pPosition;
```



## <a name="remarks"></a><span data-ttu-id="d027a-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d027a-106">Remarks</span></span>

<span data-ttu-id="d027a-107">Wenn der Pin zum ersten Mal nach der [**IMediaPosition-**](/windows/desktop/api/Control/nn-control-imediaposition) oder [**IMediaSeeking-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) abgefragt wird, wird ein [**CPosPassThru-Hilfsobjekt**](cpospassthru.md) erstellt und aggregiert.</span><span class="sxs-lookup"><span data-stu-id="d027a-107">When the pin is first queried for the [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) or [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface, it creates and aggregates a [**CPosPassThru**](cpospassthru.md) helper object.</span></span>

## <a name="requirements"></a><span data-ttu-id="d027a-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d027a-108">Requirements</span></span>



| <span data-ttu-id="d027a-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d027a-109">Requirement</span></span> | <span data-ttu-id="d027a-110">Wert</span><span class="sxs-lookup"><span data-stu-id="d027a-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d027a-111">Header</span><span class="sxs-lookup"><span data-stu-id="d027a-111">Header</span></span><br/>  | <dl> <span data-ttu-id="d027a-112"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="d027a-112"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d027a-113">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d027a-113">Library</span></span><br/> | <dl> <span data-ttu-id="d027a-114"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d027a-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




