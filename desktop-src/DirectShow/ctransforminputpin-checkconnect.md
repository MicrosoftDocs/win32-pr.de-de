---
description: Die checkConnect-Methode bestimmt, ob eine PIN-Verbindung geeignet ist.
ms.assetid: b8ace40d-31f5-49b0-a4cd-6ece0f883d96
title: Ctransforminputpin. checkConnect-Methode (Transfrm. h)
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
ms.openlocfilehash: e10c174a4e295576cfa9ce902faeac889f5a6a9b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368454"
---
# <a name="ctransforminputpincheckconnect-method"></a>Ctransforminputpin. checkConnect-Methode

Die- `CheckConnect` Methode bestimmt, ob eine PIN-Verbindung geeignet ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppin* 
</dt> <dd>

Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der Ausgabe-PIN.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind in der folgenden Tabelle aufgeführt.



| Rückgabecode                                                                                               | Beschreibung                    |
|-----------------------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                      | Erfolg<br/>             |
| <dl> <dt>**VFW \_ E \_ ungültige \_ Richtung**</dt> </dl> | Falsche PIN-Richtung<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**cbasepin:: checkConnect**](cbasepin-checkconnect.md) -Methode. Er ruft die [**ctransformfilter:: checkConnect**](ctransformfilter-checkconnect.md) -Methode des Filters auf, die \_ in der Basisklasse den Wert s OK zurückgibt. Die abgeleitete Klasse kann die **ctransformfilter:: checkConnect** -Methode überschreiben, um zusätzliche Überprüfungen auszuführen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




