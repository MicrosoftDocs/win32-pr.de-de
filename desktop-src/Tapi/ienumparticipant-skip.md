---
description: Die Skip-Methode überspringt die nächste angegebene Anzahl von Elementen in der Enumerationssequenz. Diese Methode ist vor Visual Basic und Skriptsprachen verborgen.
ms.assetid: 7f641354-c3f5-4eb3-ad1c-98abf7694106
title: IEnumParticipant::Skip-Methode (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25a55eb3298578738bb427efd6ab2b830b9a7850668aa3c9fa4712cc1bf48d22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660700"
---
# <a name="ienumparticipantskip-method"></a>IEnumParticipant::Skip-Methode

\[**Skip** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **Skip-Methode** überspringt die nächste angegebene Anzahl von Elementen in der Enumerationssequenz. Diese Methode ist vor Visual Basic und Skriptsprachen verborgen.

## <a name="syntax"></a>Syntax


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Celt* \[ In\]
</dt> <dd>

Anzahl der zu überspringenden Elemente.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Die Anzahl der übersprungenen Elemente war *"celt".*<br/>               |
| <dl> <dt>**S \_ FALSE**</dt> </dl>       | Die Anzahl der übersprungenen Elemente war nicht *"celt".*<br/>           |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher zum Ausführen des Vorgangs vorhanden.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IEnumParticipant**](ienumparticipant.md)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

 




