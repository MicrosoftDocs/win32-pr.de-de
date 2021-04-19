---
description: Die IsValid-Methode bestimmt, ob diesem-Objekt ein Haupttyp zugewiesen wurde.
ms.assetid: 22d28019-f360-4b93-972c-d1dfe83938f0
title: Cmediatype. IsValid-Methode (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.IsValid
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d8e1731060021b61eb5037e1baeeda95021e8f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367713"
---
# <a name="cmediatypeisvalid-method"></a><span data-ttu-id="7cffe-103">Cmediatype. IsValid-Methode</span><span class="sxs-lookup"><span data-stu-id="7cffe-103">CMediaType.IsValid method</span></span>

<span data-ttu-id="7cffe-104">Die- `IsValid` Methode bestimmt, ob diesem-Objekt ein Haupttyp zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="7cffe-104">The `IsValid` method determines whether a major type has been assigned to this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cffe-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7cffe-105">Syntax</span></span>


```C++
BOOL IsValid() const;
```



## <a name="parameters"></a><span data-ttu-id="7cffe-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7cffe-106">Parameters</span></span>

<span data-ttu-id="7cffe-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="7cffe-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7cffe-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7cffe-108">Return value</span></span>

<span data-ttu-id="7cffe-109">Gibt **true** zurück, wenn diesem Objekt ein Haupttyp zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="7cffe-109">Returns **TRUE** if a major type has been assigned to this object.</span></span> <span data-ttu-id="7cffe-110">Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7cffe-110">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cffe-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7cffe-111">Remarks</span></span>

<span data-ttu-id="7cffe-112">[**Cmediatype**](cmediatype.md) -Objekte werden standardmäßig mit einem Haupttyp von GUID NULL initialisiert \_ .</span><span class="sxs-lookup"><span data-stu-id="7cffe-112">By default, [**CMediaType**](cmediatype.md) objects are initialized with a major type of GUID\_NULL.</span></span> <span data-ttu-id="7cffe-113">Ruft diese Methode auf, um zu bestimmen, ob das Objekt ordnungsgemäß initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="7cffe-113">Call this method to determine whether the object has been correctly initialized.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cffe-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7cffe-114">Requirements</span></span>



| <span data-ttu-id="7cffe-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7cffe-115">Requirement</span></span> | <span data-ttu-id="7cffe-116">Wert</span><span class="sxs-lookup"><span data-stu-id="7cffe-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cffe-117">Header</span><span class="sxs-lookup"><span data-stu-id="7cffe-117">Header</span></span><br/>  | <dl> <span data-ttu-id="7cffe-118"><dt>Mtype. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7cffe-118"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="7cffe-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7cffe-119">Library</span></span><br/> | <dl> <span data-ttu-id="7cffe-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="7cffe-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cffe-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7cffe-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cffe-122">**Cmediatype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="7cffe-122">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




