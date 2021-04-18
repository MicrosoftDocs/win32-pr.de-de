---
description: Die ispartiallydefined-Methode bestimmt, ob der Medientyp teilweise definiert ist. Ein Medientyp ist partiell, wenn der Haupttyp, der Untertyp oder der Formattyp GUID \_ NULL ist.
ms.assetid: 26dd7a2b-b2f8-485f-a9af-31c3a9eb1def
title: Cmediatype. ispartiallyangegebene-Methode (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.IsPartiallySpecified
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32c39942ab3f97d45ecf71ba841d56b7afd4be62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360942"
---
# <a name="cmediatypeispartiallyspecified-method"></a><span data-ttu-id="96db2-104">Cmediatype. ispartiallyangegebene-Methode</span><span class="sxs-lookup"><span data-stu-id="96db2-104">CMediaType.IsPartiallySpecified method</span></span>

<span data-ttu-id="96db2-105">Die- `IsPartiallySpecified` Methode bestimmt, ob der Medientyp teilweise definiert ist.</span><span class="sxs-lookup"><span data-stu-id="96db2-105">The `IsPartiallySpecified` method determines if the media type is partially defined.</span></span> <span data-ttu-id="96db2-106">Ein Medientyp ist *partiell* , wenn der Haupttyp, der Untertyp oder der Formattyp GUID \_ NULL ist.</span><span class="sxs-lookup"><span data-stu-id="96db2-106">A media type is *partial* if the major type, subtype, or format type is GUID\_NULL.</span></span>

## <a name="syntax"></a><span data-ttu-id="96db2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="96db2-107">Syntax</span></span>


```C++
BOOL IsPartiallySpecified() const;
```



## <a name="parameters"></a><span data-ttu-id="96db2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="96db2-108">Parameters</span></span>

<span data-ttu-id="96db2-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="96db2-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="96db2-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="96db2-110">Return value</span></span>

<span data-ttu-id="96db2-111">Gibt **true** zurück, wenn der Medientyp teilweise angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="96db2-111">Returns **TRUE** if the media type is partially specified.</span></span> <span data-ttu-id="96db2-112">Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="96db2-112">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="96db2-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="96db2-113">Remarks</span></span>

<span data-ttu-id="96db2-114">Die [**IPin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) -Methode kann partielle Medientypen akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="96db2-114">The [**IPin::Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) method can accept partial media types.</span></span>

<span data-ttu-id="96db2-115">Die-Implementierung testet den Untertyp nicht tatsächlich.</span><span class="sxs-lookup"><span data-stu-id="96db2-115">The implementation does not actually test the subtype.</span></span> <span data-ttu-id="96db2-116">Wenn ein bestimmter Formattyp vorhanden ist, wird der Medientyp nicht als partiell betrachtet, auch wenn der Untertyp GUID \_ NULL ist.</span><span class="sxs-lookup"><span data-stu-id="96db2-116">If there is a specified format type, the media type is not considered partial, even if the subtype is GUID\_NULL.</span></span>

## <a name="requirements"></a><span data-ttu-id="96db2-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96db2-117">Requirements</span></span>



| <span data-ttu-id="96db2-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="96db2-118">Requirement</span></span> | <span data-ttu-id="96db2-119">Wert</span><span class="sxs-lookup"><span data-stu-id="96db2-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96db2-120">Header</span><span class="sxs-lookup"><span data-stu-id="96db2-120">Header</span></span><br/>  | <dl> <span data-ttu-id="96db2-121"><dt>Mtype. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="96db2-121"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="96db2-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="96db2-122">Library</span></span><br/> | <dl> <span data-ttu-id="96db2-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="96db2-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96db2-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="96db2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96db2-125">**Cmediatype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="96db2-125">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




