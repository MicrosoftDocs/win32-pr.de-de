---
description: Eine-Aufzählung, mit der der Typ eines Ereignisses angegeben wird.
MS-HAID: vspixengine.EVENTTYPE
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: EventType-Enumeration
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F7A6F396-5BC0-4963-ABFD-ACB7AAE475F5
api_name:
- EVENTTYPE
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 60af0090e440cd101211394cff98c9d9a501f4ba
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392554"
---
# <a name="span-idvspixengineeventtypespaneventtype-enumeration"></a><span data-ttu-id="377b9-103"><span id="vspixengine.eventtype"></span>EventType-Enumeration</span><span class="sxs-lookup"><span data-stu-id="377b9-103"><span id="vspixengine.eventtype"></span>EVENTTYPE enumeration</span></span>

<span data-ttu-id="377b9-104">Eine-Aufzählung, mit der der Typ eines Ereignisses angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="377b9-104">An enum used to indicate the type of an event.</span></span>

## <a name="syntax"></a><span data-ttu-id="377b9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="377b9-105">Syntax</span></span>

```cpp
C++ 
enum EVENTTYPE {
  ET_NONE = 0, 
  ET_SESSIONSTART, 
  ET_SESSIONEND, 
  ET_PROCESSSTART, 
  ET_PROCESSEND, 
  ET_FRAMEBEGIN, 
  ET_FRAMEEND, 
  ET_USEREVENTBEGIN, 
  ET_USEREVENTEND, 
  ET_USERMARKER, 
  ET_CALL, 
  ET_OBJECTCREATION, 
  ET_OBJECTPOPULATION, 
  ET_CALLSYNC, 
  ET_DRAW, 
  ET_DISPATCH 
};
```

## <a name="constants"></a><span data-ttu-id="377b9-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="377b9-106">Constants</span></span>

<span data-ttu-id="377b9-107"><span id="ET_NONE"></span><span id="et_none"></span>**\_kein et**</span><span class="sxs-lookup"><span data-stu-id="377b9-107"><span id="ET_NONE"></span><span id="et_none"></span>**ET\_NONE**</span></span>  
<span data-ttu-id="377b9-108">Ein-Wert, der keinem Ereignis entspricht.</span><span class="sxs-lookup"><span data-stu-id="377b9-108">A value that corresponds to no event.</span></span>

<span data-ttu-id="377b9-109"><span id="ET_SESSIONSTART"></span><span id="et_sessionstart"></span>**\_etsessionstart**</span><span class="sxs-lookup"><span data-stu-id="377b9-109"><span id="ET_SESSIONSTART"></span><span id="et_sessionstart"></span>**ET\_SESSIONSTART**</span></span>  
<span data-ttu-id="377b9-110">Ein-Wert, der einem Sitzungsstart Ereignis entspricht.</span><span class="sxs-lookup"><span data-stu-id="377b9-110">A value that corresponds to a session start event.</span></span>

<span data-ttu-id="377b9-111"><span id="ET_SESSIONEND"></span><span id="et_sessionend"></span>**\_etsessionend**</span><span class="sxs-lookup"><span data-stu-id="377b9-111"><span id="ET_SESSIONEND"></span><span id="et_sessionend"></span>**ET\_SESSIONEND**</span></span>  
<span data-ttu-id="377b9-112">Ein-Wert, der einem Session End-Ereignis entspricht.</span><span class="sxs-lookup"><span data-stu-id="377b9-112">A value that corresponds to a session end event.</span></span>

<span data-ttu-id="377b9-113"><span id="ET_PROCESSSTART"></span><span id="et_processstart"></span>**ET- \_ processstart**</span><span class="sxs-lookup"><span data-stu-id="377b9-113"><span id="ET_PROCESSSTART"></span><span id="et_processstart"></span>**ET\_PROCESSSTART**</span></span>  
<span data-ttu-id="377b9-114">Ein-Wert, der einem Prozessstart Ereignis entspricht.</span><span class="sxs-lookup"><span data-stu-id="377b9-114">A value that corresponds to a process start event.</span></span>

<span data-ttu-id="377b9-115"><span id="ET_PROCESSEND"></span><span id="et_processend"></span>**ET- \_ processend**</span><span class="sxs-lookup"><span data-stu-id="377b9-115"><span id="ET_PROCESSEND"></span><span id="et_processend"></span>**ET\_PROCESSEND**</span></span>  
<span data-ttu-id="377b9-116">Ein-Wert, der einem Prozess Ende-Ereignis entspricht.</span><span class="sxs-lookup"><span data-stu-id="377b9-116">A value that corresponds to a process end event.</span></span>

<span data-ttu-id="377b9-117"><span id="ET_FRAMEBEGIN"></span><span id="et_framebegin"></span>**\_etframebegin**</span><span class="sxs-lookup"><span data-stu-id="377b9-117"><span id="ET_FRAMEBEGIN"></span><span id="et_framebegin"></span>**ET\_FRAMEBEGIN**</span></span>  
<span data-ttu-id="377b9-118">Ein-Wert, der einem Frame BEGIN-Ereignis entspricht.</span><span class="sxs-lookup"><span data-stu-id="377b9-118">A value that corresponds to a frame begin event.</span></span>

<span data-ttu-id="377b9-119"><span id="ET_FRAMEEND"></span><span id="et_frameend"></span>**\_etframeend**</span><span class="sxs-lookup"><span data-stu-id="377b9-119"><span id="ET_FRAMEEND"></span><span id="et_frameend"></span>**ET\_FRAMEEND**</span></span>  
<span data-ttu-id="377b9-120">Ein-Wert, der einem Frame-End-Ereignis entspricht.</span><span class="sxs-lookup"><span data-stu-id="377b9-120">A value that corresponds to a frame end event.</span></span> <span data-ttu-id="377b9-121">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="377b9-121">Not used.</span></span>

<span data-ttu-id="377b9-122"><span id="ET_USEREVENTBEGIN"></span><span id="et_usereventbegin"></span>**ET \_ usereventbegin**</span><span class="sxs-lookup"><span data-stu-id="377b9-122"><span id="ET_USEREVENTBEGIN"></span><span id="et_usereventbegin"></span>**ET\_USEREVENTBEGIN**</span></span>  
<span data-ttu-id="377b9-123">Ein-Wert, der einem Ereignis für den Benutzer Ereignis Anfang entspricht.</span><span class="sxs-lookup"><span data-stu-id="377b9-123">A value that corresponds to a user-event begin event.</span></span>

<span data-ttu-id="377b9-124"><span id="ET_USEREVENTEND"></span><span id="et_usereventend"></span>**ET \_ usereventend**</span><span class="sxs-lookup"><span data-stu-id="377b9-124"><span id="ET_USEREVENTEND"></span><span id="et_usereventend"></span>**ET\_USEREVENTEND**</span></span>  
<span data-ttu-id="377b9-125">Ein-Wert, der einem Benutzer Ereignis-Endereignis entspricht.</span><span class="sxs-lookup"><span data-stu-id="377b9-125">A value that corresponds to a user-event end event.</span></span> <span data-ttu-id="377b9-126">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="377b9-126">Not used.</span></span>

<span data-ttu-id="377b9-127"><span id="ET_USERMARKER"></span><span id="et_usermarker"></span>**\_usermarker für et**</span><span class="sxs-lookup"><span data-stu-id="377b9-127"><span id="ET_USERMARKER"></span><span id="et_usermarker"></span>**ET\_USERMARKER**</span></span>  
<span data-ttu-id="377b9-128">Ein-Wert, der einem Benutzer Markierungs Ereignis entspricht.</span><span class="sxs-lookup"><span data-stu-id="377b9-128">A value that corresponds to a user-marker event.</span></span>

<span data-ttu-id="377b9-129"><span id="ET_CALL"></span><span id="et_call"></span>**ET \_ -Befehl**</span><span class="sxs-lookup"><span data-stu-id="377b9-129"><span id="ET_CALL"></span><span id="et_call"></span>**ET\_CALL**</span></span>  
<span data-ttu-id="377b9-130">Ein-Wert, der einem-Ereignis entspricht.</span><span class="sxs-lookup"><span data-stu-id="377b9-130">A value that corresponds to a call event.</span></span>

<span data-ttu-id="377b9-131"><span id="ET_OBJECTCREATION"></span><span id="et_objectcreation"></span>**ET \_ objectcreation**</span><span class="sxs-lookup"><span data-stu-id="377b9-131"><span id="ET_OBJECTCREATION"></span><span id="et_objectcreation"></span>**ET\_OBJECTCREATION**</span></span>  
<span data-ttu-id="377b9-132">Ein-Wert, der einem Objekt Erstellungs Ereignis entspricht.</span><span class="sxs-lookup"><span data-stu-id="377b9-132">A value that corresponds to an object creation event.</span></span>

<span data-ttu-id="377b9-133"><span id="ET_OBJECTPOPULATION"></span><span id="et_objectpopulation"></span>**\_objectpopulation in et**</span><span class="sxs-lookup"><span data-stu-id="377b9-133"><span id="ET_OBJECTPOPULATION"></span><span id="et_objectpopulation"></span>**ET\_OBJECTPOPULATION**</span></span>  
<span data-ttu-id="377b9-134">Ein-Wert, der einem Objekt auffüllungs Ereignis entspricht.</span><span class="sxs-lookup"><span data-stu-id="377b9-134">A value that corresponds to an object population event.</span></span>

<span data-ttu-id="377b9-135"><span id="ET_CALLSYNC"></span><span id="et_callsync"></span>**ET \_ callsync**</span><span class="sxs-lookup"><span data-stu-id="377b9-135"><span id="ET_CALLSYNC"></span><span id="et_callsync"></span>**ET\_CALLSYNC**</span></span>  

<span data-ttu-id="377b9-136"><span id="ET_DRAW"></span><span id="et_draw"></span>**\_etdraw**</span><span class="sxs-lookup"><span data-stu-id="377b9-136"><span id="ET_DRAW"></span><span id="et_draw"></span>**ET\_DRAW**</span></span>  
<span data-ttu-id="377b9-137">Ein-Wert, der einem zeichnen-Ereignis Ereignis entspricht.</span><span class="sxs-lookup"><span data-stu-id="377b9-137">A value that corresponds to a draw call event.</span></span>

<span data-ttu-id="377b9-138"><span id="ET_DISPATCH"></span><span id="et_dispatch"></span>**\_etdispatch**</span><span class="sxs-lookup"><span data-stu-id="377b9-138"><span id="ET_DISPATCH"></span><span id="et_dispatch"></span>**ET\_DISPATCH**</span></span>  
<span data-ttu-id="377b9-139">Ein-Wert, der einem Dispatch-Ereignis entspricht.</span><span class="sxs-lookup"><span data-stu-id="377b9-139">A value that corresponds to a dispatch event.</span></span>

## <a name="requirements"></a><span data-ttu-id="377b9-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="377b9-140">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="377b9-141">Header</span><span class="sxs-lookup"><span data-stu-id="377b9-141">Header</span></span></p></td><td><span data-ttu-id="377b9-142">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="377b9-142">Vspixengine.h</span></span></td></tr></tbody></table>
