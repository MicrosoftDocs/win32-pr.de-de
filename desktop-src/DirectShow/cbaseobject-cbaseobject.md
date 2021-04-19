---
description: Konstruktormethode.
ms.assetid: 20c3c4af-b22f-4b74-a6b6-5ee309de4eef
title: Cbaseobject. cbaseobject-Konstruktor (ComBase. h)
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
ms.openlocfilehash: 4b13fe906af1900dbf067e8aa9273d811b3c1ef3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369552"
---
# <a name="cbaseobjectcbaseobject-constructor"></a><span data-ttu-id="88abd-103">Cbaseobject. cbaseobject-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="88abd-103">CBaseObject.CBaseObject constructor</span></span>

<span data-ttu-id="88abd-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="88abd-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="88abd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="88abd-105">Syntax</span></span>


```C++
CBaseObject(
   const TCHAR *pName
);
```



## <a name="parameters"></a><span data-ttu-id="88abd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="88abd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88abd-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="88abd-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="88abd-108">Eine Zeichenfolge, die den Namen des Objekts zu Debuggingzwecken enthält.</span><span class="sxs-lookup"><span data-stu-id="88abd-108">String that contains the name of the object, for debugging purposes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="88abd-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="88abd-109">Remarks</span></span>

<span data-ttu-id="88abd-110">Diese Methode erhöht die Anzahl von aktiven Objekten.</span><span class="sxs-lookup"><span data-stu-id="88abd-110">This method increments the active-object count.</span></span> <span data-ttu-id="88abd-111">(Siehe [**cbaseobject:: objeczactive**](cbaseobject-objectsactive.md).)</span><span class="sxs-lookup"><span data-stu-id="88abd-111">(See [**CBaseObject::ObjectsActive**](cbaseobject-objectsactive.md).)</span></span>

<span data-ttu-id="88abd-112">Weisen Sie den *PName* -Parameter im statischen Arbeitsspeicher zu:</span><span class="sxs-lookup"><span data-stu-id="88abd-112">Allocate the *pName* parameter in static memory:</span></span>


```C++
// Correct.
CBaseObject *pObject = new CBaseObject(NAME("My Object"));

// Incorrect.
TCHAR ObjectName[] = TEXT("My Object");
CBaseObject *pObject = new CObject(ObjectName);
```



<span data-ttu-id="88abd-113">Das [**Name**](name.md) -Makro wird in Einzelhandels Builds in **null** kompiliert, sodass statische Zeichen folgen nur in Debugbuilds angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="88abd-113">The [**NAME**](name.md) macro compiles to **NULL** in retail builds, so that static strings appear only in debug builds.</span></span> <span data-ttu-id="88abd-114">Weitere Informationen finden Sie unter [**dbgdumpobjectregiester**](dbgdumpobjectregister.md).</span><span class="sxs-lookup"><span data-stu-id="88abd-114">For more information, see [**DbgDumpObjectRegister**](dbgdumpobjectregister.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="88abd-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88abd-115">Requirements</span></span>



| <span data-ttu-id="88abd-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88abd-116">Requirement</span></span> | <span data-ttu-id="88abd-117">Wert</span><span class="sxs-lookup"><span data-stu-id="88abd-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88abd-118">Header</span><span class="sxs-lookup"><span data-stu-id="88abd-118">Header</span></span><br/>  | <dl> <span data-ttu-id="88abd-119"><dt>ComBase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="88abd-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="88abd-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="88abd-120">Library</span></span><br/> | <dl> <span data-ttu-id="88abd-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="88abd-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88abd-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88abd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88abd-123">**Cbaseobject-Klasse**</span><span class="sxs-lookup"><span data-stu-id="88abd-123">**CBaseObject Class**</span></span>](cbaseobject.md)
</dt> </dl>

 

 




