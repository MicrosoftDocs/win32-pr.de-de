---
description: 'CBaseInputPin.GetAllocator-Methode: Die GetAllocator-Methode ruft die von dieser Stecknadel vorgeschlagene Speicherbelegung ab. Diese Methode implementiert die IMemInputPin::GetAllocator-Methode.'
ms.assetid: 07bc77f8-a877-4403-b424-20bda715a818
title: CBaseInputPin.GetAllocator-Methode (Amfilter.h)
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
ms.openlocfilehash: 119f3ffaa5863584b55210306b38b011c758f9bab0febac47547bdfe469b5ac0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056340"
---
# <a name="cbaseinputpingetallocator-method"></a>CBaseInputPin.GetAllocator-Methode

Die `GetAllocator` -Methode ruft die von dieser Stecknadel vorgeschlagene Speicherbelegung ab. Diese Methode implementiert die [**IMemInputPin::GetAllocator-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator)

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAllocator(
   IMemAllocator **ppAllocator
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppAllocator* 
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf die [**IMemAllocator-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) der Zuweisung empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg S \_ OK oder einen Fehlercode aus der **CoCreateInstance-Funktion** zurück.

## <a name="remarks"></a>Hinweise

Diese Methode erstellt ein [**CMemAllocator-Objekt.**](cmemallocator.md) Überschreiben Sie diese Methode, wenn Ihr Filter eine Zuweisung aus einem Downstreampin oder eine benutzerdefinierte Zuweisung verwendet.

Wenn die Methode erfolgreich ist, verfügt die **IMemAllocator-Schnittstelle** über einen ausstehenden Verweiszähler. Stellen Sie sicher, dass Sie es freigeben, wenn Sie fertig sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseInputPin-Klasse**](cbaseinputpin.md)
</dt> </dl>

 

 




