---
description: Die CheckStreaming-Methode bestimmt, ob der Pin Stichproben akzeptieren kann.
ms.assetid: fa063966-4c72-466e-933c-def6a6818621
title: CTransformInputPin.CheckStreaming-Methode (Transfrm.h)
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
ms.openlocfilehash: c32dce44e48b033e0a76f5bb5af6aff3eb71948d54c73d670c6226571a1c938b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767606"
---
# <a name="ctransforminputpincheckstreaming-method"></a>CTransformInputPin.CheckStreaming-Methode

Die `CheckStreaming` -Methode bestimmt, ob der Pin Stichproben akzeptieren kann.

## <a name="syntax"></a>Syntax


```C++
HRESULT CheckStreaming();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle aufgeführten **HRESULT-Werte** zurück.



| Rückgabecode                                                                                           | Beschreibung                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>                         |
| <dl> <dt>**S \_ FALSE**</dt> </dl>               | Pin wird gerade geleert.<br/>       |
| <dl> <dt>**VFW \_ E \_ NICHT \_ VERBUNDEN**</dt> </dl> | Der Ausgabepin ist nicht verbunden.<br/> |
| <dl> <dt>**VFW \_ \_ E-LAUFZEITFEHLER \_**</dt> </dl> | Es ist ein Laufzeitfehler aufgetreten.<br/>       |
| <dl> <dt>**VFW \_ E \_ WRONG \_ STATE**</dt> </dl>   | Die Stecknadel wird beendet.<br/>              |



 

## <a name="remarks"></a>Hinweise

Diese Methode überschreibt die [**CBaseInputPin::CheckStreaming-Methode.**](cbaseinputpin-checkstreaming.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




