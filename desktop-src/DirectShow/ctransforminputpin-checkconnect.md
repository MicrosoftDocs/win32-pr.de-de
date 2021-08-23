---
description: 'CTransformInputPin.CheckConnect-Methode: Die CheckConnect-Methode bestimmt, ob eine Stecknadelverbindung geeignet ist.'
ms.assetid: b8ace40d-31f5-49b0-a4cd-6ece0f883d96
title: CTransformInputPin.CheckConnect-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a48bd2d3231979a30f8f7ff0d8144929115c51b9ca3f464f85d6d0163954ad7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823720"
---
# <a name="ctransforminputpincheckconnect-method"></a>CTransformInputPin.CheckConnect-Methode

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

Zeiger auf die IPin-Schnittstelle des [**Ausgabepins.**](/windows/desktop/api/Strmif/nn-strmif-ipin)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle gezeigten Werte.



| Rückgabecode                                                                                               | Beschreibung                    |
|-----------------------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                      | Erfolg<br/>             |
| <dl> <dt>**VFW \_ E \_ UNGÜLTIGE \_ RICHTUNG**</dt> </dl> | Falsche Stecknadelrichtung<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode überschreibt die [**CBasePin::CheckConnect-Methode.**](cbasepin-checkconnect.md) Sie ruft die [**CTransformFilter::CheckConnect-Methode**](ctransformfilter-checkconnect.md) des Filters auf, die S \_ OK in der Basisklasse zurückgibt. Die abgeleitete Klasse kann die **CTransformFilter::CheckConnect-Methode** überschreiben, um zusätzliche Überprüfungen durchzuführen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




