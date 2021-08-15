---
description: 'IEnumMedia::Skip-Methode: Die Skip-Methode überspringt die nächste angegebene Anzahl von Elementen in der Enumerationssequenz.'
ms.assetid: 825972c9-5303-4c5a-9475-dc67c185af91
title: IEnumMedia::Skip-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e17dadb1db502dfa76645d0142b98da3a030efb9e391a029985460c89526d37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118865774"
---
# <a name="ienummediaskip-method"></a>IEnumMedia::Skip-Methode

\[Rendezvous-IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

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
| <dl> <dt>**S \_ OK**</dt> </dl>    | Die Anzahl der übersprungenen Elemente war *"celt".*<br/>     |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Die Anzahl der übersprungenen Elemente war nicht *"celt".*<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IEnumMedia**](ienummedia.md)
</dt> </dl>

 

 




