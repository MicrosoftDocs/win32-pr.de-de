---
description: 'Die Skip-Methode überspringt eine angegebene Anzahl von Pins in der enumerationssequenz. Diese Methode implementiert die iumumpins:: Skip-Methode.'
ms.assetid: d42f958c-f488-4730-ab84-fc4e4150b186
title: Cenumpins. Skip-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Skip
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1865453a89130303f28f338d8b7567e856c64173
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372590"
---
# <a name="cenumpinsskip-method"></a>Cenumpins. Skip-Methode

Die- `Skip` Methode überspringt eine angegebene Anzahl von Pins in der enumerationssequenz. Diese Methode implementiert die [**iumumpins:: Skip**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-skip) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT Skip(
   ULONG cPins
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cpins* 
</dt> <dd>

Anzahl der Pins, die übersprungen werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                                                | Beschreibung                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>                    | Wird über das Ende der Sequenz übersprungen.<br/>                                       |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Erfolg.<br/>                                                                    |
| <dl> <dt>**VFW \_ E \_ Enum \_ nicht \_ \_ synchron**</dt> </dl> | Der Zustand des Filters wurde geändert und ist nun inkonsistent mit dem Enumerator.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cenumpins-Klasse**](cenumpins.md)
</dt> </dl>

 

 




