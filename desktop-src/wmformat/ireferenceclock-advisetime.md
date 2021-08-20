---
title: IReferenceClock AdviseTime-Methode
description: Die AdviseTime-Methode fordert eine asynchrone Benachrichtigung an, dass eine Zeit verstrichen ist.
ms.assetid: 8f3f8713-b53c-4110-ac7a-724bbc49368e
keywords:
- AdviseTime-Methode – Windows-Medienformat
- AdviseTime-Methode windows Media Format , IReferenceClock-Schnittstelle
- IReferenceClock-Schnittstelle windows Media Format , AdviseTime-Methode
topic_type:
- apiref
api_name:
- IReferenceClock.AdviseTime
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b648c1c1305503f049b3c02669d1fa3c49be428d31c0cd292801b3541a25cc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117655367"
---
# <a name="ireferenceclockadvisetime-method"></a>IReferenceClock::AdviseTime-Methode

Die **AdviseTime-Methode** fordert eine asynchrone Benachrichtigung an, dass eine Zeit verstrichen ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT AdviseTime(
  [in]  REFERENCE_TIME rtBaseTime,
  [in]  REFERENCE_TIME rtStreamTime,
  [in]  HEVENT         hEvent,
  [out] DWORD          *pdwAdviseCookie
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*rtBaseTime* \[ In\]
</dt> <dd>

Basisverweiszeit in Einheiten von 100 Nanosekunden.

</dd> <dt>

*rtStreamTime* \[ In\]
</dt> <dd>

Streamoffsetzeit in Einheiten von 100 Nanosekunden.

</dd> <dt>

*hEvent* \[ In\]
</dt> <dd>

Handle für ein Ereignis, das vom Aufrufer erstellt wurde. Dieses Ereignis wird signalisiert, wenn die angegebene Zeit verstrichen ist.

</dd> <dt>

*pdwAdviseCookie* \[ out\]
</dt> <dd>

Zeiger auf eine Variable, die einen Bezeichner für die Anforderung empfängt. Dieser wird verwendet, um diesen Aufruf von **AdviseTime** in Zukunft zu identifizieren, z. B. zum Abbrechen der Anforderung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                               | Beschreibung                                             |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Die Methode wurde erfolgreich ausgeführt.<br/>                        |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl> | Der *pdwAdviseCookie-Parameter* ist **NULL.**<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>    | Nicht angegebener Fehler.<br/>                         |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IReferenceClock-Schnittstelle**](ireferenceclock.md)
</dt> </dl>

 

 





