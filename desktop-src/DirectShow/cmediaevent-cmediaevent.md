---
description: 'CMediaEvent.CMediaEvent-Konstruktor : Konstruktormethode.'
ms.assetid: 7f7a0a9f-e531-4e22-8601-b84ab088e9e7
title: CMediaEvent.CMediaEvent-Konstruktor (Ctlutil.h)
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
ms.openlocfilehash: 36cd82b086241012542701001c4de1fe16ac2d8e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095558"
---
# <a name="cmediaeventcmediaevent-constructor"></a>CMediaEvent.CMediaEvent-Konstruktor

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

Zeiger auf den Namen des Objekts zu Debugzwecken.

</dd> <dt>

*Punk* 
</dt> <dd>

Zeiger auf den Besitzer dieses Objekts.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Ordnen Sie den *pName-Parameter* im statischen Speicher zu. Dieser Name wird beim Erstellen und Löschen des Objekts im Debugterminal angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (einschließlich Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CMediaEvent-Klasse**](cmediaevent.md)
</dt> </dl>

 

 




