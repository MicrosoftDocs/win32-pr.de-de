---
description: 'Die getallocator-Methode ruft die von dieser Pin vorgeschlagene Speicherzuweisung ab. Diese Methode implementiert die IMemInputPin:: getallocator-Methode.'
ms.assetid: 07bc77f8-a877-4403-b424-20bda715a818
title: Cbasinput PIN. getallocator-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.GetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 098738fc63ba1834b1eefb4b2518e3309db35c43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368336"
---
# <a name="cbaseinputpingetallocator-method"></a>Cbasinput PIN. getallocator-Methode

Die- `GetAllocator` Methode ruft die von dieser Pin vorgeschlagene Speicherzuweisung ab. Diese Methode implementiert die [**IMemInputPin:: getallocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAllocator(
   IMemAllocator **ppAllocator
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppzuzuweisung* 
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf die [**imemfercator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle des Zuordners empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt " \_ OK" zurück, wenn erfolgreich, oder einen Fehlercode aus der **cokreateinzustance** -Funktion.

## <a name="remarks"></a>Bemerkungen

Diese Methode erstellt ein [**cmemzuordcator**](cmemallocator.md) -Objekt. Überschreiben Sie diese Methode, wenn der Filter eine Zuweisung aus einer downstreampin oder eine benutzerdefinierte Zuweisung verwendet.

Wenn die Methode erfolgreich ausgeführt wird, hat die **imemzuordcator** -Schnittstelle einen ausstehenden Verweis Zähler. Stellen Sie sicher, dass Sie Sie freigeben, wenn Sie dies erledigt haben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaseingeputpin-Klasse**](cbaseinputpin.md)
</dt> </dl>

 

 




