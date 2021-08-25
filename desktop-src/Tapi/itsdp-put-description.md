---
description: Die Put \_ Description-Methode legt die Sitzungsbeschreibung fest.
ms.assetid: 535957e7-effe-4b1b-8cba-38a7a3fe9a9a
title: ITSdp::p ut_Description-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe47e55b41de2c656f04872846c8be9352c53a0f6265a27e0eefbb1ceb1d5d7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873690"
---
# <a name="itsdpput_description-method"></a>ITSdp::p ut \_ Description-Methode

\[Rendezvous-IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **Put \_ Description-Methode** legt die Sitzungsbeschreibung fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Description(
  [in] BSTR pDescription
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDescription* \[ In\]
</dt> <dd>

Zeiger auf einen **BSTR,** der die Sitzungsbeschreibung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | Der *pDescription-Parameter* ist kein gültiger Zeiger.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher zum Ausführen des Vorgangs vorhanden.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

## <a name="remarks"></a>Hinweise

Die Anwendung muss [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) verwenden, um Speicher für den *pDescription-Parameter* zuzuordnen, und [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den Arbeitsspeicher freizugeben, wenn die Variable nicht mehr benötigt wird.

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

[**ITSdp::get \_ Description**](itsdp-get-description.md)
</dt> </dl>

 

