---
title: IReferenceClock-advientime-Methode
description: Die AdviseTime-Methode fordert eine asynchrone Benachrichtigung an, dass eine Zeit verstrichen ist.
ms.assetid: 8f3f8713-b53c-4110-ac7a-724bbc49368e
keywords:
- Advi-Time-Methode Windows Media-Format
- Advi-Time-Methode Windows Media-Format, IReferenceClock-Schnittstelle
- IReferenceClock-Schnittstelle Windows Media-Format, advientime-Methode
topic_type:
- apiref
api_name:
- IReferenceClock.AdviseTime
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3fa91338b4bff8f925f00e7159a36089e0de0aa8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106339246"
---
# <a name="ireferenceclockadvisetime-method"></a>IReferenceClock:: advientime-Methode

Die **AdviseTime** -Methode fordert eine asynchrone Benachrichtigung an, dass eine Zeit verstrichen ist.

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

*rtbasetime* \[ in\]
</dt> <dd>

Basis Verweis Zeit in 100-Nanosecond-Einheiten.

</dd> <dt>

*rtstreamtime* \[ in\]
</dt> <dd>

Streamoffset Zeit in 100-Nanosecond-Einheiten.

</dd> <dt>

*hevent* \[ in\]
</dt> <dd>

Handle für ein Ereignis, das vom Aufrufer erstellt wurde. Dieses Ereignis wird signalisiert, wenn die angegebene Zeit abgelaufen ist.

</dd> <dt>

*pdwadviabcookie* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die einen Bezeichner für die Anforderung empfängt. Diese wird verwendet, um den Aufruf von **adviin** der Zukunft zu identifizieren, um beispielsweise die Anforderung abzubrechen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                               | Beschreibung                                             |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Die Methode wurde erfolgreich ausgeführt.<br/>                        |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl> | Der *pdwadvietcookie* -Parameter ist **null**.<br/> |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>    | Nicht spezifizierter Fehler.<br/>                         |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IReferenceClock-Schnittstelle**](ireferenceclock.md)
</dt> </dl>

 

 





