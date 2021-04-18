---
description: Die get \_ numports-Methode ruft die Anzahl der für die Sitzung benötigten Ports ab. Die Sitzung verwendet die angegebene Anzahl von Ports beginnend mit dem Wert, der von Get startport zurückgegeben wird \_ .
ms.assetid: 9ebdcf51-e095-4173-97d6-7754560abfb5
title: 'ITmedia:: get_NumPorts-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc223ddd5d210d2c1d440c52ca4201ccd6334b08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371362"
---
# <a name="itmediaget_numports-method"></a>ITmedia:: get- \_ numports-Methode

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **get \_ numports** -Methode ruft die Anzahl der für die Sitzung benötigten Ports ab. Die Sitzung verwendet die angegebene Anzahl von Ports beginnend mit dem Wert, der von [**get \_ startport**](itmedia-get-startport.md)zurückgegeben wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_NumPorts(
  [out] LONG *pNumPorts
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pnumports* \[ vorgenommen\]
</dt> <dd>

Zeiger auf die Anzahl von Ports.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Der *pnumports* -Parameter ist kein gültiger Zeiger.<br/>    |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/> |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ notimpl**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITmedia**](itmedia.md)
</dt> </dl>

 

 




