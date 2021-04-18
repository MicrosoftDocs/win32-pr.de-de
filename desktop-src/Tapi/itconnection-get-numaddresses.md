---
description: Die get \_ numadkleidungs-Methode ruft die Anzahl der Adressen ab, die für die Sitzung verwendet werden sollen.
ms.assetid: c3aef5df-02e9-4c7e-99aa-8e4043798bf4
title: 'Itconnection:: get_NumAddresses-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24b121275c6af8f026e7321e4fd85327e970eb78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364887"
---
# <a name="itconnectionget_numaddresses-method"></a>Itconnection:: get \_ numadkleider-Methode

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **get \_ numadkleidungs** -Methode ruft die Anzahl der Adressen ab, die für die Sitzung verwendet werden sollen.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_NumAddresses(
  [out] LONG *pNumAddresses
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pnumadkleider* \[ vorgenommen\]
</dt> <dd>

Anzahl der Adressen für die Sitzung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                     |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Der *pnumaddresse* s-Parameter ist kein gültiger Zeiger.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/>  |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>        | Unbekannter Fehler.<br/>                                    |
| <dl> <dt>**E \_ notimpl**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itconnection**](itconnection.md)
</dt> </dl>

 

 




