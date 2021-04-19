---
description: Die beginflush-Methode startet einen Löschvorgang.
ms.assetid: d37b611e-742f-4bdf-bd72-a91cd1c473b3
title: Coutputqueue. beginflush-Methode (outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 462c3027e38bd94f061eb927c0d52576e29c997b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361584"
---
# <a name="coutputqueuebeginflush-method"></a>Coutputqueue. beginflush-Methode

Die- `BeginFlush` Methode startet einen Löschvorgang.

## <a name="syntax"></a>Syntax


```C++
void BeginFlush();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode legt die Element Variable [**coutputqueue:: m \_ bleerung**](coutputqueue-m-bflushing.md) auf **true** fest. Wenn das Objekt einen Thread verwendet, ruft der Thread die [**coutputqueue:: freesamples**](coutputqueue-freesamples.md) -Methode auf, um alle ausstehenden Beispiele freizugeben. Andernfalls ruft das-Objekt während der [**coutputqueue:: endflush**](coutputqueue-endflush.md) -Methode **freesamples** auf. Diese Methode legt auch die [**coutputqueue:: m- \_ HR**](coutputqueue-m-hr.md) -Member-Variable auf "false" fest \_ , was bewirkt, dass das-Objekt alle neuen-Beispiele verwerfen kann.

Das Objekt übergibt die Leerungs Benachrichtigung durch Aufrufen der [**IPin:: beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) -Methode für die Eingabe-PIN.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Outputq. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Coutputqueue-Klasse**](coutputqueue.md)
</dt> </dl>

 

 




