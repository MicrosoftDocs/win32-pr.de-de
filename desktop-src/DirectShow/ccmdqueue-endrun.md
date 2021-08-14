---
description: Die EndRun-Methode wechselt in den beendeten oder angehaltenen Modus.
ms.assetid: 2c41262c-a809-4f3b-898c-02c0891dc6f8
title: CCmdQueue.EndRun-Methode (Winutil.h)
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
ms.openlocfilehash: 2c5a20917c82ba26c941b063941e8667a3a30adce15176aed52362140a15ce90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757360"
---
# <a name="ccmdqueueendrun-method"></a>CCmdQueue.EndRun-Methode

Die `EndRun` -Methode wechselt in den beendeten oder angehaltenen Modus.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT EndRun();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück, der von der Implementierung abhängt.

## <a name="remarks"></a>Hinweise

Die Zeitzuordnung zwischen Streamzeit und Präsentationszeit ist nicht bekannt, nachdem diese Memberfunktion aufgerufen wurde. Rufen Sie [**die CCmdQueue::Run-Memberfunktion**](ccmdqueue-run.md) auf, um diese Zuordnung zu erstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CCmdQueue-Klasse**](ccmdqueue.md)
</dt> </dl>

 

 




