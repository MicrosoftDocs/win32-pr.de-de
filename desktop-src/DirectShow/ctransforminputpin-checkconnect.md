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
ms.openlocfilehash: 3e981254677c2e0a361a0a21f125f734ff1403db
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095088"
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



 

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**CBasePin::CheckConnect-Methode.**](cbasepin-checkconnect.md) Sie ruft die [**CTransformFilter::CheckConnect-Methode**](ctransformfilter-checkconnect.md) des Filters auf, die S \_ OK in der Basisklasse zurückgibt. Die abgeleitete Klasse kann die **CTransformFilter::CheckConnect-Methode** überschreiben, um zusätzliche Überprüfungen durchzuführen.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (streams.h enthalten)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




