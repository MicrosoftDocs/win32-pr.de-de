---
description: 'CDynamicOutputPin.CompleteConnect-Methode: Die CompleteConnect-Methode schließt eine Verbindung mit einem Eingabepin ab.'
ms.assetid: c23195e7-8d66-4217-bd59-8889459ce4f1
title: CDynamicOutputPin.CompleteConnect-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5fa15c84b9d9e0b686e17110c656b74161687705
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095738"
---
# <a name="cdynamicoutputpincompleteconnect-method"></a>CDynamicOutputPin.CompleteConnect-Methode

Die `CompleteConnect` -Methode schließt eine Verbindung mit einem Eingabepin ab.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des Eingabepins.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg S \_ OK oder einen **HRESULT-Wert** zurück, der die Ursache des Fehlers angibt.

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**CBaseOutputPin::CompleteConnect-Methode.**](cbaseoutputpin-completeconnect.md) Um dynamische Wiederherstellungsverknüpfungen zu unterstützen, committet diese Methode die Zuweisung, wenn der Filter aktiv ist. In der Basisklasse können Verbindungen nur auftreten, wenn der Filter beendet wird, sodass für die Zuweisung immer ein Commit in der [**CBaseOutputPin::Active-Methode**](cbaseoutputpin-active.md) ausgeführt wird.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h einschließen)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CDynamicOutputPin-Klasse**](cdynamicoutputpin.md)
</dt> </dl>

 

 




