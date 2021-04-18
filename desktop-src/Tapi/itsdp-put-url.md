---
description: Die Put \_ URL-Methode legt die URL fest.
ms.assetid: 538bb1dd-c7ad-446d-9df7-23363b466263
title: Itsdp::p ut_Url-Methode (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b791d18b97851e6b0b27a4ba26d1dfdbce7dbb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368481"
---
# <a name="itsdpput_url-method"></a>Itsdp::p UT- \_ URL-Methode

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **Put \_ URL** -Methode legt die URL fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Url(
  [in] BSTR pUrl
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Purl* \[ in\]
</dt> <dd>

Zeiger auf eine **BSTR** -Darstellung der URL.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Der *Purl* -Parameter ist kein gültiger Zeiger.<br/>         |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/> |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ notimpl**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

## <a name="remarks"></a>Bemerkungen

Die Anwendung muss " [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) " verwenden, um Speicher für den *Purl* -Parameter zuzuweisen, und " [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) " verwenden, um den Arbeitsspeicher freizugeben, wenn die Variable nicht mehr benötigt wird.

Eine URL wird normalerweise verwendet, um auf eine Webseite mit zusätzlichen Ressourcen oder Hintergrundinformationen zu einer Konferenz zu verweisen.

Diese Funktion kann Daten in unverschlüsselter Form über das Netzwerk senden. aus diesem Grund kann ein Benutzer, der sich im Netzwerk befindet, möglicherweise die Daten lesen. Das Sicherheitsrisiko, dass Daten im Klartext gesendet werden, sollte vor der Verwendung dieser Methode berücksichtigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itsdp**](itsdp.md)
</dt> <dt>

[**Itsdp:: get- \_ URL**](itsdp-get-url.md)
</dt> </dl>

 

