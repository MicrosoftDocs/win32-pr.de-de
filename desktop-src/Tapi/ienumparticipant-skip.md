---
description: Die Skip-Methode überspringt die nächste angegebene Anzahl von Elementen in der enumerationssequenz. Diese Methode ist in Visual Basic-und Skriptsprachen ausgeblendet.
ms.assetid: 7f641354-c3f5-4eb3-ad1c-98abf7694106
title: 'Ienumparticipants:: Skip-Methode (confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dc406a69c126c25b1c554679595868a595b839b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369174"
---
# <a name="ienumparticipantskip-method"></a>Ienumteilnehmer:: Skip-Methode

\[**Skip** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **Skip** -Methode überspringt die nächste angegebene Anzahl von Elementen in der enumerationssequenz. Diese Methode ist in Visual Basic-und Skriptsprachen ausgeblendet.

## <a name="syntax"></a>Syntax


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*celt* \[ in\]
</dt> <dd>

Anzahl der zu überspringenden Elemente.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Die Anzahl übersprungener Elemente war " *celt*".<br/>               |
| <dl> <dt>**S \_ false**</dt> </dl>       | Die Anzahl übersprungener Elemente war nicht " *celt*".<br/>           |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>"Confpriv. h"</dt> </dl> |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ienumteilnehmer**](ienumparticipant.md)
</dt> <dt>

[**Itteilnehmer**](itparticipant.md)
</dt> </dl>

 

 




