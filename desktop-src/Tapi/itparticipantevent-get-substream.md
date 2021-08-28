---
description: Der get SubStream ruft einen Zeiger auf ein Array von ITSubStream-Schnittstellen ab, die die am \_ Ereignis beteiligten Unterstreams darstellen.
ms.assetid: 0af9097a-2481-4543-bb3d-35ccd352e992
title: ITParticipantEvent::get_SubStream-Methode (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f258f68815a5bc7cd201d94ab55199d59ebe6759eb2e279a1c80add91ea6c3d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774660"
---
# <a name="itparticipanteventget_substream-method"></a>ITParticipantEvent::get \_ SubStream-Methode

\[**get \_ SubStream** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Der **get \_ SubStream** ruft einen Zeiger auf ein Array von [**ITSubStream-Schnittstellen**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) ab, die die am Ereignis beteiligten Unterstreams darstellen.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_SubStream(
  [out] ITSubStream **ppSubStream
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppSubStream* \[ out\]
</dt> <dd>

Zeiger auf ein Array von [**ITSubStream-Zeigern.**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                           | Bedeutung                                                         |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>            | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**TAPI \_ E \_ NOITEMS**</dt> </dl> | Dem Ereignis sind keine Unterstreams zugeordnet.<br/>   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>   | Es ist nicht genügend Arbeitsspeicher vorhanden, um den Vorgang durchzuführen.<br/> |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>       | Der *ppSubStream-Parameter* ist kein gültiger Zeiger.<br/>  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITParticipantEvent**](itparticipantevent.md)
</dt> <dt>

[**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

