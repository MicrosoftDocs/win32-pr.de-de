---
description: Die getnumoffunktionalitäten-Methode ruft die Anzahl der Funktionen ab, die dem aktuellen Format zugeordnet sind.
ms.assetid: 26e51c0d-c1cb-410f-ab19-eb884afa8431
title: 'Itformatcontrol:: getnumoffunktionalitäten-Methode (ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e29153f5ee9ce8c5e12b93a1d219905c40f80418
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367661"
---
# <a name="itformatcontrolgetnumberofcapabilities-method"></a>Itformatcontrol:: getnumoffunktionalitäten-Methode

\[ Diese Methode ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **getnumoffunktionalitäten** -Methode ruft die Anzahl der Funktionen ab, die dem aktuellen Format zugeordnet sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetNumberOfCapabilities(
  [out] DWORD *pdwCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdwCount* \[ vorgenommen\]
</dt> <dd>

Anzahl der Funktionen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,1<br/>                                                         |
| Header<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itformatcontrol**](itformatcontrol.md)
</dt> </dl>

 

 




