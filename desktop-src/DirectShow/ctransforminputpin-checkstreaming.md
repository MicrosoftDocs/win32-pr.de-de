---
description: Die checkstreaming-Methode bestimmt, ob die PIN Beispiele annehmen kann.
ms.assetid: fa063966-4c72-466e-933c-def6a6818621
title: Ctransforminputpin. checkstreaming-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e5c49a00054547193e3f492f0731f77af8331a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364742"
---
# <a name="ctransforminputpincheckstreaming-method"></a>Ctransforminputpin. checkstreaming-Methode

Die- `CheckStreaming` Methode bestimmt, ob die PIN Beispiele annehmen kann.

## <a name="syntax"></a>Syntax


```C++
HRESULT CheckStreaming();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                                           | Beschreibung                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>                         |
| <dl> <dt>**S \_ false**</dt> </dl>               | Die PIN wird zurzeit geleert.<br/>       |
| <dl> <dt>**VFW \_ E \_ nicht \_ verbunden**</dt> </dl> | Die Ausgabe-PIN ist nicht verbunden.<br/> |
| <dl> <dt>**VFW \_ E \_ Lauf \_ Zeitfehler**</dt> </dl> | Laufzeitfehler.<br/>       |
| <dl> <dt>**VFW \_ E \_ falscher \_ Zustand**</dt> </dl>   | Die PIN wurde beendet.<br/>              |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**cbaseinputpin:: checkstreaming**](cbaseinputpin-checkstreaming.md) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




