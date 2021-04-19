---
description: Die \_ Methode Get conferenceblob erhält einen Zeiger auf das Textkonferenz-BLOB, das zurzeit im Konferenz-BLOB-Objekt gespeichert ist.
ms.assetid: eb378f84-11bc-4f6e-9133-bc303e07eb53
title: 'Itconferendceblob:: get_ConferenceBlob-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e5642f60f7abc1cb10734de1897d35bd5222dd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353001"
---
# <a name="itconferenceblobget_conferenceblob-method"></a>Itconferendceblob:: get- \_ Methode

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die Methode **get \_ conferenceblob** erhält einen Zeiger auf das Textkonferenz-BLOB, das zurzeit im Konferenz-BLOB-Objekt gespeichert ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_ConferenceBlob(
  [out] BSTR *ppBlob
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppBlob* \[ vorgenommen\]
</dt> <dd>

Zeiger auf ein **BSTR** , das das Konferenz-BLOB enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Der *ppBlob* -Parameter ist kein gültiger Zeiger.<br/>       |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/> |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ notimpl**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

## <a name="remarks"></a>Bemerkungen

Die Anwendung muss [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den für den *ppBlob* -Parameter zugeordneten Arbeitsspeicher freizugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itconfererceblob**](itconferenceblob.md)
</dt> <dt>

[**BLOB- \_ Zeichen \_ Satz**](blob-character-set.md)
</dt> </dl>

 

