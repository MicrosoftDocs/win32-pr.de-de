---
description: Die get \_ Originator-Methode ruft den Absender der Konferenz ab.
ms.assetid: a324098d-ae22-42e9-901e-b277433af199
title: 'Itsdp:: get_Originator-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f751dd5a9dffe2d3bbc7883b8a0f8f18f8e6381
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360365"
---
# <a name="itsdpget_originator-method"></a>Itsdp:: get \_ Originator-Methode

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **get \_ Originator** -Methode ruft den Absender der Konferenz ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Originator(
  [out] BSTR *ppOriginator
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pporiginator* \[ vorgenommen\]
</dt> <dd>

Zeiger auf eine **BSTR** -Darstellung des Konferenz Ursprungs.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Der *pporiginator* -Parameter ist kein gültiger Zeiger.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/> |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ notimpl**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

## <a name="remarks"></a>Bemerkungen

Die Anwendung muss [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den für den *pporiginator* -Parameter reservierten Arbeitsspeicher freizugeben.

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

[**Itsdp: \_ :p UT-Absender**](itsdp-put-originator.md)
</dt> </dl>

 

