---
description: 'IEnumTime::Skip-Methode: Die Skip-Methode überspringt die nächste angegebene Anzahl von Elementen in der Enumerationssequenz.'
ms.assetid: e4d9c95d-1b68-4af6-beb2-2014074e5089
title: IEnumTime::Skip-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 190a98c14cb8f551276a173e2d73872d876f2ceb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090718"
---
# <a name="ienumtimeskip-method"></a>IEnumTime::Skip-Methode

\[ Rendezvous IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **Skip-Methode** überspringt die nächste angegebene Anzahl von Elementen in der Enumerationssequenz.

## <a name="syntax"></a>Syntax


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*celt* \[ In\]
</dt> <dd>

Anzahl der zu überspringenden Elemente.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                             | Beschreibung                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | Number of elements skipped was *celt*.<br/>     |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Number of elements skipped was *not celt*.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IEnumTime**](ienumtime.md)
</dt> </dl>

 

 




