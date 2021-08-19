---
description: Die Active-Methode benachrichtigt den Pin, dass der Filter jetzt aktiv ist. Diese Methode überschreibt die CBasePin::Active-Methode. Wenn die Stecknadel verbunden ist, startet diese Methode den Streamingthread.
ms.assetid: ea32b602-2583-4de6-96ec-6ea875c49d14
title: CSourceStream.Active-Methode (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 427c0318bad4df810b29f3596e3a9516f8dbb73e97dd7e378c561bef28bf2f38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073343"
---
# <a name="csourcestreamactive-method"></a>CSourceStream.Active-Methode

Die `Active` -Methode benachrichtigt den Pin, dass der Filter jetzt aktiv ist. Diese Methode überschreibt die [**CBasePin::Active-Methode.**](cbasepin-active.md) Wenn die Stecknadel verbunden ist, startet diese Methode den Streamingthread.

## <a name="syntax"></a>Syntax


```C++
HRESULT Active();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                             | Beschreibung                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Die Stecknadel ist bereits aktiv.<br/>  |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Erfolg.<br/>                    |
| <dl> <dt>**E \_ FAIL**</dt> </dl>  | Der Thread konnte nicht gestartet werden.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSourceStream-Klasse**](csourcestream.md)
</dt> </dl>

 

 




