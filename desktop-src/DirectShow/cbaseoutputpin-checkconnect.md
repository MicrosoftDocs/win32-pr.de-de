---
description: 'CBaseOutputPin.CheckConnect-Methode: Die CheckConnect-Methode bestimmt, ob eine Pinverbindung geeignet ist.'
ms.assetid: 50ab59ad-8ff7-4d7b-add3-b59203d93307
title: CBaseOutputPin.CheckConnect-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ca35cb98f279674285610fbd06b0399e93a68d59749fe4129475ab8bd970824a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658863"
---
# <a name="cbaseoutputpincheckconnect-method"></a>CBaseOutputPin.CheckConnect-Methode

Die `CheckConnect` -Methode bestimmt, ob eine Stecknadelverbindung geeignet ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pPin* 
</dt> <dd>

Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des Eingabepins.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT-Werte** zurück.



| Rückgabecode                                                                                               | Beschreibung                                                                 |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                      | Erfolg.<br/>                                                         |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl>             | Der Eingabepin unterstützt [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)nicht.<br/> |
| <dl> <dt>**VFW \_ E \_ INVALID \_ DIRECTION**</dt> </dl> | Stecknadelrichtungen sind nicht kompatibel.<br/>                               |



 

## <a name="remarks"></a>Hinweise

Diese Methode ruft die [**CBasePin::CheckConnect-Methode**](cbasepin-checkconnect.md) der Basisklasse auf und fragt dann den Eingabepin nach der [**IMemInputPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) ab.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseOutputPin-Klasse**](cbaseoutputpin.md)
</dt> </dl>

 

 




