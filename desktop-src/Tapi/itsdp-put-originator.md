---
description: Die put \_ Originator-Methode legt den Konferenzursprungsgeber fest.
ms.assetid: b70fc584-3536-4296-bc38-e20ff6630abc
title: ITSdp::p ut_Originator-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49937ed5f7da71a2ab6c23e19ba4b2f31435ae0f2d0b37a2fa3a869213a221a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682639"
---
# <a name="itsdpput_originator-method"></a>ITSdp::p ut \_ Originator-Methode

\[Rendezvous-IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **put \_ Originator-Methode** legt den Konferenzursprungsgeber fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Originator(
  [in] BSTR pOriginator
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOriginator* \[ In\]
</dt> <dd>

Zeiger auf eine **BSTR-Darstellung** des Konferenzursprungsgebers.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | Der *pOriginator-Parameter* ist kein gültiger Zeiger.<br/>  |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher zum Ausführen des Vorgangs vorhanden.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

## <a name="remarks"></a>Hinweise

Die Anwendung muss [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) verwenden, um Speicher für den *pOriginator-Parameter* zu belegen, und [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den Arbeitsspeicher freizugeben, wenn die Variable nicht mehr benötigt wird.

Diese Funktion kann Daten über das Kabel in unverschlüsselter Form senden. Daher kann eine Person, die im Netzwerk lauscht, die Daten lesen. Das Sicherheitsrisiko beim Senden der Daten in Klartext sollte vor der Verwendung dieser Methode berücksichtigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> <dt>

[**ITSdp::get \_ Originator**](itsdp-get-originator.md)
</dt> </dl>

 

