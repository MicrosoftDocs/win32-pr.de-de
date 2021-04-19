---
description: Hilfsobjekt, um Seek-Befehle zu übergeben.
ms.assetid: 2ca9bae7-a133-4e09-8aa7-1c4601ec5db0
title: 'Ctransformoutputpin:: m_pPosition Member (Transfrm. h)'
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
ms.openlocfilehash: dc98e439d7f6a2d6c6392ffb665b04e502047eb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361386"
---
# <a name="ctransformoutputpinm_pposition-member"></a><span data-ttu-id="43612-103">Ctransformoutputpin:: m \_ pposition-Member</span><span class="sxs-lookup"><span data-stu-id="43612-103">CTransformOutputPin::m\_pPosition member</span></span>

<span data-ttu-id="43612-104">Hilfsobjekt, um Seek-Befehle zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="43612-104">Helper object to pass seek commands upstream.</span></span>

## <a name="syntax"></a><span data-ttu-id="43612-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="43612-105">Syntax</span></span>


```C++
IUnknown *m_pPosition;
```



## <a name="remarks"></a><span data-ttu-id="43612-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43612-106">Remarks</span></span>

<span data-ttu-id="43612-107">Wenn die PIN zum ersten Mal für die [**imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition) -oder [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) -Schnittstelle abgefragt wird, wird ein [**cpospassthru**](cpospassthru.md) -Hilfsobjekt erstellt und aggregiert.</span><span class="sxs-lookup"><span data-stu-id="43612-107">When the pin is first queried for the [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) or [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface, it creates and aggregates a [**CPosPassThru**](cpospassthru.md) helper object.</span></span>

## <a name="requirements"></a><span data-ttu-id="43612-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43612-108">Requirements</span></span>



| <span data-ttu-id="43612-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43612-109">Requirement</span></span> | <span data-ttu-id="43612-110">Wert</span><span class="sxs-lookup"><span data-stu-id="43612-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43612-111">Header</span><span class="sxs-lookup"><span data-stu-id="43612-111">Header</span></span><br/>  | <dl> <span data-ttu-id="43612-112"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="43612-112"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="43612-113">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="43612-113">Library</span></span><br/> | <dl> <span data-ttu-id="43612-114">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="43612-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




