---
description: 'Die notifyzucator-Methode gibt eine Zuweisung für die Verbindung an. Mit dieser Methode wird die IMemInputPin:: notifyzucator-Methode implementiert.'
ms.assetid: 16167bd5-2d33-4329-87ec-6a6c578e0060
title: Cbaseingeputpin. notifyzucator-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ce5bc3cfe165b1adb6b5b970ca43d31c8ace98f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355996"
---
# <a name="cbaseinputpinnotifyallocator-method"></a>Cbaseingeputpin. notifyzucator-Methode

Die- `NotifyAllocator` Methode gibt eine Zuweisung für die Verbindung an. Mit dieser Methode wird die [**IMemInputPin:: notifyzucator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) -Methode implementiert.

## <a name="syntax"></a>Syntax


```C++
HRESULT NotifyAllocator(
   IMemAllocator *pAllocator,
   BOOL          bReadOnly
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pallocator* 
</dt> <dd>

Ein Zeiger auf die [**imemfercator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle des Zuordners.

</dd> <dt>

*nur Bread* 
</dt> <dd>

Flag, das angibt, ob Beispiele aus dieser Zuweisung schreibgeschützt sind. **True** gibt an, dass die Beispiele schreibgeschützt sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Während der Pin-Verbindung wählt die Ausgabe-PIN eine Zuweisung aus und ruft diese Methode auf, um die Eingabe-PIN zu benachrichtigen. Die Ausgabepin kann die Zuweisung verwenden, die die Eingabe-PIN in der [**IMemInputPin:: getallocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) -Methode vorgeschlagen hat, oder Sie kann Ihre eigene Zuweisung bereitstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaseingeputpin-Klasse**](cbaseinputpin.md)
</dt> </dl>

 

 




