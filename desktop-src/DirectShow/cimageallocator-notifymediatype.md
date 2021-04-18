---
description: Die notifymediatype-Methode informiert das-Objekt über den aktuellen Medientyp.
ms.assetid: 6fb708ff-e968-4867-baca-ebe2515c9fab
title: Cimagezuzuordcator. notifymediatype-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.NotifyMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb9261884b8940b571876502741fcc52e1c40a33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372661"
---
# <a name="cimageallocatornotifymediatype-method"></a><span data-ttu-id="d44b8-103">Cimagezuzuordcator. notifymediatype-Methode</span><span class="sxs-lookup"><span data-stu-id="d44b8-103">CImageAllocator.NotifyMediaType method</span></span>

<span data-ttu-id="d44b8-104">Die- `NotifyMediaType` Methode informiert das-Objekt über den aktuellen Medientyp.</span><span class="sxs-lookup"><span data-stu-id="d44b8-104">The `NotifyMediaType` method informs the object of the current media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="d44b8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d44b8-105">Syntax</span></span>


```C++
void NotifyMediaType(
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="d44b8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d44b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d44b8-107">*pmediatype*</span><span class="sxs-lookup"><span data-stu-id="d44b8-107">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="d44b8-108">Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt oder **null** , um den Medientyp zu löschen.</span><span class="sxs-lookup"><span data-stu-id="d44b8-108">Pointer to a [**CMediaType**](cmediatype.md) object, or **NULL** to clear the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d44b8-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d44b8-109">Return value</span></span>

<span data-ttu-id="d44b8-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d44b8-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d44b8-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d44b8-111">Remarks</span></span>

<span data-ttu-id="d44b8-112">Der besitzende Filter sollte diese Methode immer dann aufzurufen, wenn sich der Medientyp ändert.</span><span class="sxs-lookup"><span data-stu-id="d44b8-112">The owning filter should call this method whenever the media type changes.</span></span> <span data-ttu-id="d44b8-113">Dies tritt normalerweise auf, wenn die PIN zum ersten Mal eine Verbindung herstellt und nach einer Änderung des dynamischen Formats.</span><span class="sxs-lookup"><span data-stu-id="d44b8-113">Typically this occurs when the pin first connects, and after a dynamic format change.</span></span> <span data-ttu-id="d44b8-114">Der Zuweiser verwendet den Medientyp zum Überprüfen der vorgeschlagenen zuordnereigenschaften und auch beim Erstellen von Medien Beispielen.</span><span class="sxs-lookup"><span data-stu-id="d44b8-114">The allocator uses the media type to validate proposed allocator properties, and also when it creates media samples.</span></span>

<span data-ttu-id="d44b8-115">Das **cimagezuordcator** -Objekt speichert den *pmediatype* -Zeiger in der Member-Variablen " **m \_ pmediatype** ".</span><span class="sxs-lookup"><span data-stu-id="d44b8-115">The **CImageAllocator** object stores the *pMediaType* pointer in the **m\_pMediaType** member variable.</span></span> <span data-ttu-id="d44b8-116">Wenn der Aufrufer das **cmediatype** -Objekt freigeben muss, sollte es daher die Zuweisung aktualisieren, indem diese Methode erneut aufgerufen wird, entweder mit einem neuen Zeiger oder mit einem **null** -Wert.</span><span class="sxs-lookup"><span data-stu-id="d44b8-116">Therefore, if the caller needs to release the **CMediaType** object, it should update the allocator by calling this method again, either with a new pointer or with a **NULL** value.</span></span> <span data-ttu-id="d44b8-117">Andernfalls kann ein Fehler auftreten, wenn die Zuweisung versucht, auf den alten Zeiger zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="d44b8-117">Otherwise, an error can occur when the allocator attempts to reference the old pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="d44b8-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d44b8-118">Requirements</span></span>



| <span data-ttu-id="d44b8-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d44b8-119">Requirement</span></span> | <span data-ttu-id="d44b8-120">Wert</span><span class="sxs-lookup"><span data-stu-id="d44b8-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d44b8-121">Header</span><span class="sxs-lookup"><span data-stu-id="d44b8-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d44b8-122"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d44b8-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d44b8-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d44b8-123">Library</span></span><br/> | <dl> <span data-ttu-id="d44b8-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d44b8-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d44b8-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d44b8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d44b8-126">**Cimagezuordcator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d44b8-126">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 




