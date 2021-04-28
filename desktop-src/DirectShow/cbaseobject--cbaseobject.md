---
description: 'CBaseObject.~CBaseObject-Destruktor : Destruktormethode.'
ms.assetid: 3714d030-f0bd-4826-a3c5-fc206bb88561
title: CBaseObject.~CBaseObject-Destruktor (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseObject.~CBaseObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 552dbcc764f335e639cb50e2e01411dee200068f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096238"
---
# <a name="cbaseobjectcbaseobject-destructor"></a><span data-ttu-id="22d10-103">CBaseObject.~CBaseObject-Destruktor</span><span class="sxs-lookup"><span data-stu-id="22d10-103">CBaseObject.~CBaseObject destructor</span></span>

<span data-ttu-id="22d10-104">Destruktormethode.</span><span class="sxs-lookup"><span data-stu-id="22d10-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="22d10-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="22d10-105">Syntax</span></span>


```C++
~CBaseObject();
```



## <a name="remarks"></a><span data-ttu-id="22d10-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22d10-106">Remarks</span></span>

<span data-ttu-id="22d10-107">Diese Methode dekrementt die Anzahl der Aktiv-Objekte.</span><span class="sxs-lookup"><span data-stu-id="22d10-107">This method decrements the active-object count.</span></span> <span data-ttu-id="22d10-108">(Siehe [**CBaseObject::ObjectsActive**](cbaseobject-objectsactive.md).)</span><span class="sxs-lookup"><span data-stu-id="22d10-108">(See [**CBaseObject::ObjectsActive**](cbaseobject-objectsactive.md).)</span></span>

## <a name="requirements"></a><span data-ttu-id="22d10-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22d10-109">Requirements</span></span>



| <span data-ttu-id="22d10-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22d10-110">Requirement</span></span> | <span data-ttu-id="22d10-111">Wert</span><span class="sxs-lookup"><span data-stu-id="22d10-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22d10-112">Header</span><span class="sxs-lookup"><span data-stu-id="22d10-112">Header</span></span><br/>  | <dl> <span data-ttu-id="22d10-113"><dt>Combase.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="22d10-113"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="22d10-114">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="22d10-114">Library</span></span><br/> | <dl> <span data-ttu-id="22d10-115"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="22d10-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22d10-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="22d10-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22d10-117">**CBaseObject-Klasse**</span><span class="sxs-lookup"><span data-stu-id="22d10-117">**CBaseObject Class**</span></span>](cbaseobject.md)
</dt> </dl>

 

 




