---
description: Konstruktormethode.
ms.assetid: 7f7a0a9f-e531-4e22-8601-b84ab088e9e7
title: Cmediaevent. cmediaevent-Konstruktor (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.CMediaEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 77b87fa589728592874b0dea96f7b6efca501471
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354168"
---
# <a name="cmediaeventcmediaevent-constructor"></a>Cmediaevent. cmediaevent-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CMediaEvent(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* 
</dt> <dd>

Zeiger auf den Namen des Objekts zu Debuggingzwecken.

</dd> <dt>

*Kro* 
</dt> <dd>

Zeiger auf den Besitzer dieses Objekts.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Weisen Sie den *PName* -Parameter im statischen Arbeitsspeicher zu. Dieser Name wird beim Erstellen und Löschen des Objekts im Terminal Debuggen angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediaevent-Klasse**](cmediaevent.md)
</dt> </dl>

 

 




