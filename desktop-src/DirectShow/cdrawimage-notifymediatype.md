---
description: Die notifymediatype-Methode benachrichtigt das cdrawimage-Objekt des aktuellen Medientyps.
ms.assetid: 419d516f-4b96-47aa-80cc-ac785e65af8b
title: Cdrawimage. notifymediatype-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.NotifyMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e3af4d926bd0ca8db5ef11839dd0ca84523c374
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365761"
---
# <a name="cdrawimagenotifymediatype-method"></a><span data-ttu-id="05b8f-103">Cdrawimage. notifymediatype-Methode</span><span class="sxs-lookup"><span data-stu-id="05b8f-103">CDrawImage.NotifyMediaType method</span></span>

<span data-ttu-id="05b8f-104">Die- `NotifyMediaType` Methode benachrichtigt das **cdrawimage** -Objekt des aktuellen Medientyps.</span><span class="sxs-lookup"><span data-stu-id="05b8f-104">The `NotifyMediaType` method notifies the **CDrawImage** object of the current media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="05b8f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="05b8f-105">Syntax</span></span>


```C++
void NotifyMediaType(
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="05b8f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="05b8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05b8f-107">*pmediatype*</span><span class="sxs-lookup"><span data-stu-id="05b8f-107">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="05b8f-108">Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt oder **null** , um den Medientyp zu löschen.</span><span class="sxs-lookup"><span data-stu-id="05b8f-108">Pointer to a [**CMediaType**](cmediatype.md) object, or **NULL** to clear the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05b8f-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="05b8f-109">Return value</span></span>

<span data-ttu-id="05b8f-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="05b8f-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="05b8f-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="05b8f-111">Remarks</span></span>

<span data-ttu-id="05b8f-112">Der besitzende Filter sollte diese Methode immer dann aufzurufen, wenn sich der Medientyp ändert.</span><span class="sxs-lookup"><span data-stu-id="05b8f-112">The owning filter should call this method whenever the media type changes.</span></span> <span data-ttu-id="05b8f-113">Dies tritt normalerweise auf, wenn die PIN zum ersten Mal eine Verbindung herstellt und nach einer Änderung des dynamischen Formats.</span><span class="sxs-lookup"><span data-stu-id="05b8f-113">Typically this occurs when the pin first connects, and after a dynamic format change.</span></span>

<span data-ttu-id="05b8f-114">Das **cdrawimage** -Objekt speichert den *pmediatype* -Zeiger in der Member-Variablen " **m \_ pmediatype** ".</span><span class="sxs-lookup"><span data-stu-id="05b8f-114">The **CDrawImage** object stores the *pMediaType* pointer in the **m\_pMediaType** member variable.</span></span> <span data-ttu-id="05b8f-115">Wenn der Aufrufer also das **cmediatype** -Objekt freigeben muss, sollte es das **cdrawimage** -Objekt durch erneutes Aufrufen dieser Methode aktualisieren, entweder mit einem neuen Zeiger oder mit einem **null** -Wert.</span><span class="sxs-lookup"><span data-stu-id="05b8f-115">Therefore, if the caller needs to release the **CMediaType** object, it should update the **CDrawImage** object by calling this method again, either with a new pointer or with a **NULL** value.</span></span> <span data-ttu-id="05b8f-116">Andernfalls kann ein Fehler auftreten, wenn das **cdrawimage** -Objekt versucht, auf den alten Zeiger zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="05b8f-116">Otherwise, an error can occur when the **CDrawImage** object attempts to reference the old pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="05b8f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05b8f-117">Requirements</span></span>



| <span data-ttu-id="05b8f-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="05b8f-118">Requirement</span></span> | <span data-ttu-id="05b8f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="05b8f-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05b8f-120">Header</span><span class="sxs-lookup"><span data-stu-id="05b8f-120">Header</span></span><br/>  | <dl> <span data-ttu-id="05b8f-121"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="05b8f-121"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="05b8f-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="05b8f-122">Library</span></span><br/> | <dl> <span data-ttu-id="05b8f-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="05b8f-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05b8f-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05b8f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05b8f-125">**Cdrawimage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="05b8f-125">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




