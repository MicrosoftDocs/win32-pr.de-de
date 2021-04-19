---
description: Die EndRun-Methode wechselt zum beendeten oder angehaltenen Modus.
ms.assetid: 2c41262c-a809-4f3b-898c-02c0891dc6f8
title: Ccmdqueue. EndRun-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.EndRun
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 367ef026402ff191ceb04657c21d6f3bd11ebe73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356312"
---
# <a name="ccmdqueueendrun-method"></a>Ccmdqueue. EndRun-Methode

Die `EndRun` Methode wechselt zum beendeten oder angehaltenen Modus.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT EndRun();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück, der von der-Implementierung abhängig ist.

## <a name="remarks"></a>Bemerkungen

Die Zeit Zuordnung zwischen der streamzeit und der Präsentationszeit ist nicht bekannt, nachdem diese Element Funktion aufgerufen wurde. Verwenden Sie die Funktion [**ccmdqueue:: Run**](ccmdqueue-run.md) Member, um diese Zuordnung auszuführen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ccmdqueue-Klasse**](ccmdqueue.md)
</dt> </dl>

 

 




