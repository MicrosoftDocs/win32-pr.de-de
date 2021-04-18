---
description: Die get \_ bandwidthmodifier-Methode ruft den Bandbreiten-Modifizierer ab, bei dem es sich um ein einzelnes alphanumerisches Wort handelt, das die Bedeutung der Bandbreiten Abbildung bereitstellt. Die beiden definierten Modifizierer sind CT (Conference Total) und AS (anwendungsspezifisches Maximum).
ms.assetid: 29bf137d-e88b-437f-8bf1-824e335d47a1
title: 'Itconnection:: get_BandwidthModifier-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e278edfbdc9ae56d89547c0bcf64f90fde77baf4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371043"
---
# <a name="itconnectionget_bandwidthmodifier-method"></a>Itconnection:: get \_ bandwidthmodifier-Methode

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **get \_ bandwidthmodifier** -Methode ruft den Bandbreiten-Modifizierer ab, bei dem es sich um ein einzelnes alphanumerisches Wort handelt, das die Bedeutung der Bandbreiten Abbildung bereitstellt. Die beiden definierten Modifizierer sind CT (Conference Total) und AS (anwendungsspezifisches Maximum).

## <a name="syntax"></a>Syntax


```C++
HRESULT get_BandwidthModifier(
  [out] BSTR *ppModifier
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppmodifier* \[ vorgenommen\]
</dt> <dd>

Zeiger auf ein **BSTR** , das den Bandbreiten-Modifizierer enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Der *ppmodifier* -Parameter ist kein gültiger Zeiger.<br/>   |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/> |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ notimpl**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

## <a name="remarks"></a>Bemerkungen

Die Anwendung muss [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den für den *ppmodifier* -Parameter zugeordneten Arbeitsspeicher freizugeben.

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

 

