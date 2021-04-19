---
description: Die coinitializehelper-Methode ruft die CoInitializeEx-Funktion am Anfang des Threads auf.
ms.assetid: 1a981e1e-c059-4e51-81d8-33bcb39ee580
title: Camthread. coinitializehelper-Methode (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CoInitializeHelper
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6c3eb7fbcb9e4abada43098339a29d208ded0d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356422"
---
# <a name="camthreadcoinitializehelper-method"></a>Camthread. coinitializehelper-Methode

Die- `CoInitializeHelper` Methode ruft die CoInitializeEx-Funktion am Anfang des Threads auf.

## <a name="syntax"></a>Syntax


```C++
static HRESULT CoInitializeHelper();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                             | Beschreibung                                              |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Die CoInitializeEx-Funktion ist nicht verfügbar.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Erfolg.<br/>                                      |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>  | Fehler.<br/>                                      |



 

## <a name="remarks"></a>Bemerkungen

Die Methode " [**camthread:: initialthread proc**](camthread-initialthreadproc.md) " ruft diese Hilfsmethode auf, die die Funktion "CoInitializeEx" aufruft. Er verwendet das coinit- \_ Flag "deaktivierte \_ OLE1DDE", um dynamischer Datenaustausch (DDE) zu deaktivieren. Weitere Informationen finden Sie unter Platform SDK.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Camthread-Klasse**](camthread.md)
</dt> </dl>

 

 




