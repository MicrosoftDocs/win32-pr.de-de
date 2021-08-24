---
title: IReferenceClock GetTime-Methode
description: Die GetTime-Methode ruft die aktuelle Verweiszeit ab.
ms.assetid: 9bf5050a-ae09-4a72-a3f2-3df8339d99b9
keywords:
- GetTime-Methode windows Media Format
- GetTime-Methode windows Media Format , IReferenceClock-Schnittstelle
- IReferenceClock-Schnittstelle windows Media Format , GetTime-Methode
topic_type:
- apiref
api_name:
- IReferenceClock.GetTime
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f7756240e8987199e1f1b5d79e3f0b676d4808520781fbac18dfa18dd75e88d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055440"
---
# <a name="ireferenceclockgettime-method"></a>IReferenceClock::GetTime-Methode

Die **GetTime-Methode** ruft die aktuelle Verweiszeit ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTime(
  [out] REFERENCE_TIME *pTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pTime* \[ out\]
</dt> <dd>

Zeiger auf eine Variable, die die aktuelle Zeit in Einheiten von 100 Nanosekunden empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                               | Beschreibung                                   |
|-------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Die Methode wurde erfolgreich ausgeführt.<br/>              |
| <dl> <dt>**E \_ POINTER**</dt> </dl> | Der *pTime-Parameter* ist **NULL.**<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IReferenceClock-Schnittstelle**](ireferenceclock.md)
</dt> </dl>

 

 





