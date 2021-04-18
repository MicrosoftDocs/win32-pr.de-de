---
description: Die get \_ Description-Methode ruft die Sitzungs Beschreibung (BSTR) ab.
ms.assetid: 09a372fe-0dcd-4daf-8f13-c4c89b1ecd16
title: 'Itsdp:: get_Description-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5f60f7aefcfac852a1665f54a59ff0541b1d82a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354836"
---
# <a name="itsdpget_description-method"></a>Itsdp:: get \_ Description-Methode

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **get \_ Description** -Methode ruft die Sitzungs Beschreibung (**BSTR**) ab. Dies muss eine ASCII-konvertierbare Zeichenfolge sein, wenn es sich um einen ASCII-Zeichensatz handelt. (Andernfalls kann es sich um eine beliebige **BSTR** -Zeichenfolge handeln.)

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Description(
  [out] BSTR *ppDescription
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppdescription* \[ vorgenommen\]
</dt> <dd>

Zeiger auf einen **BSTR** -Wert, der die Sitzungs Beschreibung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                     |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Der *ppdescription* -Parameter ist kein gültiger Zeiger.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/>  |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>        | Unbekannter Fehler.<br/>                                    |
| <dl> <dt>**E \_ notimpl**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                   |



 

## <a name="remarks"></a>Bemerkungen

Die Anwendung muss [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) zum Freigeben des *ppdescription* -Parameters verwenden.

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

[**Itsdp::p UT- \_ Beschreibung**](itsdp-put-description.md)
</dt> </dl>

 

