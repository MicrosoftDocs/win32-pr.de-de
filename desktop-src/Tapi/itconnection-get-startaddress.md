---
description: Die get \_ STARTADDRESS-Methode ruft die erste Adresse ab, die für die Sitzung verwendet werden soll.
ms.assetid: 3c4fec19-1b7d-4052-afd8-7aaf095907d0
title: 'Itconnection:: get_StartAddress-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84266d1874e7d04acb594bcfb9d99b440b0390b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352913"
---
# <a name="itconnectionget_startaddress-method"></a>Itconnection:: get \_ STARTADDRESS-Methode

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **get \_ STARTADDRESS** -Methode ruft die erste Adresse ab, die für die Sitzung verwendet werden soll.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_StartAddress(
  [out] BSTR *ppStartAddress
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppstartaddress* \[ vorgenommen\]
</dt> <dd>

Zeiger auf einen **BSTR** -Wert, der die Anfangsadresse für die Sitzung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                       |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                      |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Der *ppstartaddress* -Parameter ist kein gültiger Zeiger.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/>   |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>        | Unbekannter Fehler.<br/>                                     |
| <dl> <dt>**E \_ notimpl**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                    |



 

## <a name="remarks"></a>Bemerkungen

Die Anwendung muss [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den für den *ppstartaddress* -Parameter zugewiesenen Arbeitsspeicher freizugeben.

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

 

