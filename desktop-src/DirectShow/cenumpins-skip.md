---
description: Die Skip-Methode überspringt eine angegebene Anzahl von Pins in der Enumerationssequenz. Diese Methode implementiert die IEnumPins::Skip-Methode.
ms.assetid: d42f958c-f488-4730-ab84-fc4e4150b186
title: CEnumPins.Skip-Methode (Amfilter.h)
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
ms.openlocfilehash: 02a499c38564fba4671e5c6dbf53bc59dcf9a1acd925f9cef4d558456b675efd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119389640"
---
# <a name="cenumpinsskip-method"></a>CEnumPins.Skip-Methode

Die `Skip` -Methode überspringt eine angegebene Anzahl von Pins in der Enumerationssequenz. Diese Methode implementiert die [**IEnumPins::Skip-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-skip)

## <a name="syntax"></a>Syntax


```C++
HRESULT Skip(
   ULONG cPins
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cPins* 
</dt> <dd>

Anzahl der zu überspringenden Pins.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.



| Rückgabecode                                                                                                | Beschreibung                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>                    | Übersprungen über das Ende der Sequenz.<br/>                                       |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Erfolg.<br/>                                                                    |
| <dl> <dt>**VFW \_ E \_ ENUM \_ OUT \_ OF \_ SYNC**</dt> </dl> | Der Status des Filters hat sich geändert und ist nun mit dem Enumerator inkonsistent.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CEnumPins-Klasse**](cenumpins.md)
</dt> </dl>

 

 




