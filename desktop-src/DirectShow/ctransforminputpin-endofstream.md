---
description: 'CTransformInputPin.EndOfStream-Methode: Die EndOfStream-Methode benachrichtigt den Pin, dass keine zusätzlichen Daten erwartet werden. Diese Methode implementiert die IPin::EndOfStream-Methode.'
ms.assetid: db9896eb-3db2-4d58-a787-4d80ce8f0d0e
title: CTransformInputPin.EndOfStream-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2035d0261447826098162f480ddc959544b101b7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084978"
---
# <a name="ctransforminputpinendofstream-method"></a>CTransformInputPin.EndOfStream-Methode

Die `EndOfStream` -Methode benachrichtigt den Pin, dass keine zusätzlichen Daten erwartet werden. Diese Methode implementiert die [**IPin::EndOfStream-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)

## <a name="syntax"></a>Syntax


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                           | Beschreibung                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>                         |
| <dl> <dt>**S \_ FALSE**</dt> </dl>               | Die Stecknadel wird gerade geleert.<br/>       |
| <dl> <dt>**VFW \_ E \_ NICHT \_ VERBUNDEN**</dt> </dl> | Der Ausgabepin ist nicht verbunden.<br/> |
| <dl> <dt>**VFW \_ E \_ \_ RUNTIME-FEHLER**</dt> </dl> | Es ist ein Laufzeitfehler aufgetreten.<br/>       |
| <dl> <dt>**VFW \_ E \_ WRONG \_ STATE**</dt> </dl>   | Die Stecknadel wird beendet.<br/>              |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft die [**CTransformFilter::EndOfStream-Methode**](ctransformfilter-endofstream.md) des Filters auf, um die End-of-Stream-Benachrichtigung downstreamzu übermitteln.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




