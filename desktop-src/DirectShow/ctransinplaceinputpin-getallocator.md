---
description: 'Die getallocator-Methode ruft die von dieser Pin vorgeschlagene Speicherzuweisung ab. Diese Methode implementiert die IMemInputPin:: getallocator-Methode.'
ms.assetid: e9db4aa0-4f53-4ca4-babb-5e0215c7c284
title: Ctransinplaceinputpin. getallocator-Methode (transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.GetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7798640297539a8fa8f6349c799e61e7e22a453d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358307"
---
# <a name="ctransinplaceinputpingetallocator-method"></a>Ctransinplaceinputpin. getallocator-Methode

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

Empfängt einen Zeiger auf die [**imemfercator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle des Zuordners.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind in der folgenden Tabelle aufgeführt.



| Rückgabecode                                                                                          | Beschreibung                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                 | Erfolg.<br/>                   |
| <dl> <dt>**VFW \_ E \_ No- \_ Zuweisung**</dt> </dl> | Es ist keine Zuweisung verfügbar.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Wenn die Ausgabe-PIN des Filters verbunden ist, fordert diese Methode eine Zuweisung aus der Eingabe-PIN des downstreamfilters an.

Wenn die Ausgabe-PIN des Filters nicht verbunden ist, erstellt diese Methode eine temporäre Zuweisung. Wenn die Ausgabepin später verbunden ist, stellt der Filter erneut eine Verbindung mit der eingabepin her und verhandelt die Zuweisung erneut.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransinplaceinputpin-Klasse**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




