---
description: Die Funktion dbgdumpobjectregiester zeigt Informationen zu aktiven Objekten an. Wird in Einzelhandels Builds ignoriert.
ms.assetid: 362d9912-662c-4a72-95b4-01f3d808e299
title: Dbgdumpobjectregiester-Funktion (wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgDumpObjectRegister
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 727d9c00ebbe3d48bb46797a1e27b9dd27c7b2c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356453"
---
# <a name="dbgdumpobjectregister-function"></a><span data-ttu-id="1bd98-104">Dbgdumpobjectregiester-Funktion</span><span class="sxs-lookup"><span data-stu-id="1bd98-104">DbgDumpObjectRegister function</span></span>

<span data-ttu-id="1bd98-105">Die- `DbgDumpObjectRegister` Funktion zeigt Informationen zu aktiven Objekten an.</span><span class="sxs-lookup"><span data-stu-id="1bd98-105">The `DbgDumpObjectRegister` function displays information about active objects.</span></span> <span data-ttu-id="1bd98-106">Wird in Einzelhandels Builds ignoriert.</span><span class="sxs-lookup"><span data-stu-id="1bd98-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bd98-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bd98-107">Syntax</span></span>


```C++
void DbgDumpObjectRegister(void);
```



## <a name="parameters"></a><span data-ttu-id="1bd98-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1bd98-108">Parameters</span></span>

<span data-ttu-id="1bd98-109">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="1bd98-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1bd98-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1bd98-110">Return value</span></span>

<span data-ttu-id="1bd98-111">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1bd98-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1bd98-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1bd98-112">Remarks</span></span>

<span data-ttu-id="1bd98-113">In Debugbuilds verwaltet die Debug-Bibliothek eine Liste aktiver Objekte.</span><span class="sxs-lookup"><span data-stu-id="1bd98-113">In debug builds, the debug library maintains a list of active objects.</span></span> <span data-ttu-id="1bd98-114">Die Liste enthält alle Objekte, die von [**cbaseobject**](cbaseobject.md)abgeleitet sind, vom aktuellen Modul erstellt wurden und nicht zerstört wurden.</span><span class="sxs-lookup"><span data-stu-id="1bd98-114">The list includes any objects that derive from [**CBaseObject**](cbaseobject.md), were created by the current module, and have not been destroyed.</span></span> <span data-ttu-id="1bd98-115">Der **cbaseobject** -Konstruktor und die dekonstruktormethoden aktualisieren die Liste.</span><span class="sxs-lookup"><span data-stu-id="1bd98-115">The **CBaseObject** constructor and destructor methods update the list.</span></span>

<span data-ttu-id="1bd98-116">Diese Funktion generiert mehrere Protokoll \_ Speicher Meldungen.</span><span class="sxs-lookup"><span data-stu-id="1bd98-116">This function generates several LOG\_MEMORY messages.</span></span> <span data-ttu-id="1bd98-117">Bei der Protokollierungs Stufe 1 zeigt die Funktion nur die Gesamtzahl der Objekte an.</span><span class="sxs-lookup"><span data-stu-id="1bd98-117">At logging level 1, the function displays only the total number of objects.</span></span> <span data-ttu-id="1bd98-118">In der Protokollierungs Stufe 2 oder höher wird eine Liste der Objekte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1bd98-118">At logging level 2 or higher, it displays a list of the objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bd98-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1bd98-119">Requirements</span></span>



| <span data-ttu-id="1bd98-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1bd98-120">Requirement</span></span> | <span data-ttu-id="1bd98-121">Wert</span><span class="sxs-lookup"><span data-stu-id="1bd98-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bd98-122">Header</span><span class="sxs-lookup"><span data-stu-id="1bd98-122">Header</span></span><br/>  | <dl> <span data-ttu-id="1bd98-123"><dt>Wxdebug. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1bd98-123"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1bd98-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1bd98-124">Library</span></span><br/> | <dl> <span data-ttu-id="1bd98-125">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="1bd98-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bd98-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1bd98-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bd98-127">Debug-Ausgabefunktionen</span><span class="sxs-lookup"><span data-stu-id="1bd98-127">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




