---
description: 'CBaseObject.CBaseObject-Konstruktor : Konstruktormethode.'
ms.assetid: 20c3c4af-b22f-4b74-a6b6-5ee309de4eef
title: CBaseObject.CBaseObject-Konstruktor (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseObject.CBaseObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 14fa2d3d38d42fa0feb387b477205cc51e0b6b87
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099618"
---
# <a name="cbaseobjectcbaseobject-constructor"></a><span data-ttu-id="322fe-103">CBaseObject.CBaseObject-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="322fe-103">CBaseObject.CBaseObject constructor</span></span>

<span data-ttu-id="322fe-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="322fe-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="322fe-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="322fe-105">Syntax</span></span>


```C++
CBaseObject(
   const TCHAR *pName
);
```



## <a name="parameters"></a><span data-ttu-id="322fe-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="322fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="322fe-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="322fe-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="322fe-108">Zeichenfolge, die den Namen des Objekts zu Debugzwecken enthält.</span><span class="sxs-lookup"><span data-stu-id="322fe-108">String that contains the name of the object, for debugging purposes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="322fe-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="322fe-109">Remarks</span></span>

<span data-ttu-id="322fe-110">Diese Methode erhöht die Anzahl der aktiven Objekte.</span><span class="sxs-lookup"><span data-stu-id="322fe-110">This method increments the active-object count.</span></span> <span data-ttu-id="322fe-111">(Siehe [**CBaseObject::ObjectsActive**](cbaseobject-objectsactive.md).)</span><span class="sxs-lookup"><span data-stu-id="322fe-111">(See [**CBaseObject::ObjectsActive**](cbaseobject-objectsactive.md).)</span></span>

<span data-ttu-id="322fe-112">Ordnen Sie den *pName-Parameter* im statischen Speicher zu:</span><span class="sxs-lookup"><span data-stu-id="322fe-112">Allocate the *pName* parameter in static memory:</span></span>


```C++
// Correct.
CBaseObject *pObject = new CBaseObject(NAME("My Object"));

// Incorrect.
TCHAR ObjectName[] = TEXT("My Object");
CBaseObject *pObject = new CObject(ObjectName);
```



<span data-ttu-id="322fe-113">Das [**NAME-Makro**](name.md) wird in Verkaufsbuilds zu **NULL** kompiliert, sodass statische Zeichenfolgen nur in Debugbuilds angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="322fe-113">The [**NAME**](name.md) macro compiles to **NULL** in retail builds, so that static strings appear only in debug builds.</span></span> <span data-ttu-id="322fe-114">Weitere Informationen finden Sie unter [**DbgDumpObjectRegister**](dbgdumpobjectregister.md).</span><span class="sxs-lookup"><span data-stu-id="322fe-114">For more information, see [**DbgDumpObjectRegister**](dbgdumpobjectregister.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="322fe-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="322fe-115">Requirements</span></span>



| <span data-ttu-id="322fe-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="322fe-116">Requirement</span></span> | <span data-ttu-id="322fe-117">Wert</span><span class="sxs-lookup"><span data-stu-id="322fe-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="322fe-118">Header</span><span class="sxs-lookup"><span data-stu-id="322fe-118">Header</span></span><br/>  | <dl> <span data-ttu-id="322fe-119"><dt>Combase.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="322fe-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="322fe-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="322fe-120">Library</span></span><br/> | <dl> <span data-ttu-id="322fe-121"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="322fe-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="322fe-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="322fe-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="322fe-123">**CBaseObject-Klasse**</span><span class="sxs-lookup"><span data-stu-id="322fe-123">**CBaseObject Class**</span></span>](cbaseobject.md)
</dt> </dl>

 

 




