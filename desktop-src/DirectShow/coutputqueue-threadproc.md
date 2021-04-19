---
description: Die ThreadProc-Methode ruft Beispiele aus der Warteschlange ab und übergibt sie an die eingabepin.
ms.assetid: e5da0a12-c722-4d08-bf84-5e3aa60b64a9
title: Coutputqueue. ThreadProc-Methode (outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 75e2e6bd7fa05480603f30e68eeaf0487918ae7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367447"
---
# <a name="coutputqueuethreadproc-method"></a>Coutputqueue. ThreadProc-Methode

Die `ThreadProc` -Methode ruft Beispiele aus der Warteschlange ab und übergibt sie an die eingabepin.

## <a name="syntax"></a>Syntax


```C++
DWORD ThreadProc();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück.

## <a name="remarks"></a>Bemerkungen

Die [**coutputqueue:: initialthread proc**](coutputqueue-initialthreadproc.md) -Methode ruft diese Methode auf, die die Haupt Thread Schleife implementiert. Innerhalb der-Schleife führt die-Methode die folgenden Schritte aus:

1.  Ruft ein Beispiel für die Warteschlange ab.
2.  Wenn das Beispiel eine Kontroll Meldung ist, führt der Thread die Steuerungs Aktion aus. Andernfalls wird das Beispiel im [**coutputqueue:: m \_ ppsamples**](coutputqueue-m-ppsamples.md) -Array platziert.
3.  Wenn das Array voll ist (oder wenn [**coutputqueue:: m \_ bbatchexact**](coutputqueue-m-bbatchexact.md) den Wert **false** hat), ruft der Thread die [**IMemInputPin:: receivemultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) -Methode auf, um die Beispiele zu übermitteln.
4.  Wenn keine Beispiele in die Warteschlange eingereiht werden, wartet der Thread auf [**coutputqueue:: m \_ hsem**](coutputqueue-m-hsem.md) Semaphore.

Der Thread wird beendet, wenn die " [**coutputqueue \_ :: m**](coutputqueue-m-bterminate.md) "-Member-Variable " **true**" lautet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Outputq. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Coutputqueue-Klasse**](coutputqueue.md)
</dt> </dl>

 

 




