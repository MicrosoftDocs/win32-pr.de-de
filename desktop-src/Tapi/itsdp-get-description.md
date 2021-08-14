---
description: Die \_ Methode get Description ruft die Sitzungsbeschreibung (BSTR) ab.
ms.assetid: 09a372fe-0dcd-4daf-8f13-c4c89b1ecd16
title: ITSdp::get_Description-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5466200a3efe51e102af5bb2abb92e86dff5c49a10f3f6498c77a992ba43073d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117945046"
---
# <a name="itsdpget_description-method"></a>ITSdp::get \_ Description-Methode

\[Rendezvous-IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **Get \_ Description-Methode** ruft die Sitzungsbeschreibung ab (**BSTR**). Dies muss eine ascii-konvertierbare Zeichenfolge sein, wenn der Zeichensatz ASCII ist. (Andernfalls kann dies eine beliebige **BSTR-Zeichenfolge** sein.)

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Description(
  [out] BSTR *ppDescription
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppDescription* \[ out\]
</dt> <dd>

Zeiger auf einen **BSTR,** der die Sitzungsbeschreibung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                     |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | Der *ppDescription-Parameter* ist kein gültiger Zeiger.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher zum Ausführen des Vorgangs vorhanden.<br/>  |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Unbekannter Fehler.<br/>                                    |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                   |



 

## <a name="remarks"></a>Hinweise

Die Anwendung muss [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den *ppDescription-Parameter* frei zu machen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> <dt>

[**ITSdp::put \_ Description**](itsdp-put-description.md)
</dt> </dl>

 

