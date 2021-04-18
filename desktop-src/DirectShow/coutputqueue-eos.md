---
description: Die EOS-Methode übermittelt einen streamingdatenstrom für den eingabepin.
ms.assetid: 65e8db14-6ca8-4c4f-8bd8-2442f743499e
title: Coutputqueue. EOS-Methode (outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.EOS
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ab05d4ab3f2620c11bd62d566be851e16b28cecd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365529"
---
# <a name="coutputqueueeos-method"></a>Coutputqueue. EOS-Methode

Die- `EOS` Methode stellt einen End-of-Stream-Rückruf für die Eingabe-PIN bereit.

## <a name="syntax"></a>Syntax


```C++
void EOS();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn das Objekt einen Thread verwendet, wird eine EOS-Paket Steuerungs Meldung in die Warteschlange eingereiht \_ . Der Thread liefert alle ausstehenden Beispiele und ruft die [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) -Methode für die Eingabe-PIN auf.

Wenn das Objekt keinen Thread verwendet, ruft es die [**coutputqueue:: sendanyway**](coutputqueue-sendanyway.md) -Methode auf, um alle ausstehenden Beispiele bereitzustellen. Anschließend wird **IPin:: EndOf Stream** für die Eingabe-PIN aufgerufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Outputq. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Coutputqueue-Klasse**](coutputqueue.md)
</dt> </dl>

 

 




