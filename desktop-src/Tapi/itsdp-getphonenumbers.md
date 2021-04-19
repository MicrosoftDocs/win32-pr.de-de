---
description: Die getphonenumbers-Methode ruft ein Array von Telefonnummern ab, die einem Konferenz-BLOB zugeordnet sind.
ms.assetid: c4ad6c5a-e15c-45ae-94de-763a843554bb
title: 'Itsdp:: getphonenumbers-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 465bc6b2d2167ca17d25b8f50466f111724ea3b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372478"
---
# <a name="itsdpgetphonenumbers-method"></a>Itsdp:: getphonenumbers-Methode

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **getphonenumbers** -Methode ruft ein Array von Telefonnummern ab, die einem Konferenz-BLOB zugeordnet sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPhoneNumbers(
  [out] VARIANT *pNumbers,
  [out] VARIANT *pNames
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pnumbers* \[ vorgenommen\]
</dt> <dd>

**Variant** -Zeiger auf ein SafeArray von **BSTR** s, das Telefonnummern auflistet.

</dd> <dt>

*pnames* \[ vorgenommen\]
</dt> <dd>

**Variant** -Zeiger auf ein SafeArray von **BSTR** s-Auflistungs Namen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                             |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                            |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Der *pnumbers* -oder *pnames* -Parameter ist kein gültiger Zeiger.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/>         |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>        | Unbekannter Fehler.<br/>                                           |
| <dl> <dt>**E \_ notimpl**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                          |



 

## <a name="remarks"></a>Bemerkungen

Die Listen, auf die *pnumbers* und *pnames* zeigen, haben dieselbe Länge.

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
</dt> </dl>

 

 




