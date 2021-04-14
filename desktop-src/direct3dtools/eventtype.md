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
# <a name="span-idvspixengineeventtypespaneventtype-enumeration"></a><span id="vspixengine.eventtype"></span>EventType-Enumeration

Eine-Aufzählung, mit der der Typ eines Ereignisses angegeben wird.

## <a name="syntax"></a>Syntax

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

## <a name="constants"></a>Konstanten

<span id="ET_NONE"></span><span id="et_none"></span>**\_kein et**  
Ein-Wert, der keinem Ereignis entspricht.

<span id="ET_SESSIONSTART"></span><span id="et_sessionstart"></span>**\_etsessionstart**  
Ein-Wert, der einem Sitzungsstart Ereignis entspricht.

<span id="ET_SESSIONEND"></span><span id="et_sessionend"></span>**\_etsessionend**  
Ein-Wert, der einem Session End-Ereignis entspricht.

<span id="ET_PROCESSSTART"></span><span id="et_processstart"></span>**ET- \_ processstart**  
Ein-Wert, der einem Prozessstart Ereignis entspricht.

<span id="ET_PROCESSEND"></span><span id="et_processend"></span>**ET- \_ processend**  
Ein-Wert, der einem Prozess Ende-Ereignis entspricht.

<span id="ET_FRAMEBEGIN"></span><span id="et_framebegin"></span>**\_etframebegin**  
Ein-Wert, der einem Frame BEGIN-Ereignis entspricht.

<span id="ET_FRAMEEND"></span><span id="et_frameend"></span>**\_etframeend**  
Ein-Wert, der einem Frame-End-Ereignis entspricht. Nicht verwendet.

<span id="ET_USEREVENTBEGIN"></span><span id="et_usereventbegin"></span>**ET \_ usereventbegin**  
Ein-Wert, der einem Ereignis für den Benutzer Ereignis Anfang entspricht.

<span id="ET_USEREVENTEND"></span><span id="et_usereventend"></span>**ET \_ usereventend**  
Ein-Wert, der einem Benutzer Ereignis-Endereignis entspricht. Nicht verwendet.

<span id="ET_USERMARKER"></span><span id="et_usermarker"></span>**\_usermarker für et**  
Ein-Wert, der einem Benutzer Markierungs Ereignis entspricht.

<span id="ET_CALL"></span><span id="et_call"></span>**ET \_ -Befehl**  
Ein-Wert, der einem-Ereignis entspricht.

<span id="ET_OBJECTCREATION"></span><span id="et_objectcreation"></span>**ET \_ objectcreation**  
Ein-Wert, der einem Objekt Erstellungs Ereignis entspricht.

<span id="ET_OBJECTPOPULATION"></span><span id="et_objectpopulation"></span>**\_objectpopulation in et**  
Ein-Wert, der einem Objekt auffüllungs Ereignis entspricht.

<span id="ET_CALLSYNC"></span><span id="et_callsync"></span>**ET \_ callsync**  

<span id="ET_DRAW"></span><span id="et_draw"></span>**\_etdraw**  
Ein-Wert, der einem zeichnen-Ereignis Ereignis entspricht.

<span id="ET_DISPATCH"></span><span id="et_dispatch"></span>**\_etdispatch**  
Ein-Wert, der einem Dispatch-Ereignis entspricht.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>
