---
description: Die CoInitializeHelper-Methode ruft die CoInitializeEx-Funktion am Anfang des Threads auf.
ms.assetid: 1a981e1e-c059-4e51-81d8-33bcb39ee580
title: WEBCAMThread.CoInitializeHelper-Methode (Wxutil.h)
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
ms.openlocfilehash: 41a763a4b9151f22615aa0af3dae57af8281751209a016dc3135f3572e9d8ef3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768290"
---
# <a name="camthreadcoinitializehelper-method"></a>CAMThread.CoInitializeHelper-Methode

Die `CoInitializeHelper` -Methode ruft die CoInitializeEx-Funktion am Anfang des Threads auf.

## <a name="syntax"></a>Syntax


```C++
static HRESULT CoInitializeHelper();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Im Folgenden finden Sie mögliche Werte.



| Rückgabecode                                                                             | Beschreibung                                              |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Die CoInitializeEx-Funktion ist nicht verfügbar.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Erfolg.<br/>                                      |
| <dl> <dt>**E \_ FAIL**</dt> </dl>  | Fehler.<br/>                                      |



 

## <a name="remarks"></a>Hinweise

Die [**METHODECAMThread::InitialThreadProc**](camthread-initialthreadproc.md) ruft diese Hilfsmethode auf, die die CoInitializeEx-Funktion aufruft. Es verwendet das FLAG COINIT \_ DISABLE \_ OLE1DDE, um dynamische Daten Exchange (DDE) zu deaktivieren. Weitere Informationen finden Sie im Plattform-SDK.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CAMThread-Klasse**](camthread.md)
</dt> </dl>

 

 




