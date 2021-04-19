---
description: Die get- \_ Zeichensatz Methode ruft einen BLOB- \_ \_ Zeichensatz Deskriptor des Zeichensatzes ab, der im aktuellen Konferenz-BLOB verwendet wird.
ms.assetid: 9783d18c-79f6-4faa-b12d-9504c13d54e3
title: 'Itconferendceblob:: get_CharacterSet-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 681085672f49c75a8434c4b0311e75d2b9cea270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367033"
---
# <a name="itconferenceblobget_characterset-method"></a>Itconferenceblob:: get- \_ Merkmal Satz Methode

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **get \_** -Zeichensatz Methode ruft einen [**BLOB- \_ \_ Zeichensatz**](blob-character-set.md) Deskriptor des Zeichensatzes ab, der im aktuellen Konferenz-BLOB verwendet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_CharacterSet(
  [out] BLOB_CHARACTER_SET *pCharacterSet
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcharakteriseset* \[ vorgenommen\]
</dt> <dd>

Zeiger auf einen [**BLOB \_ - \_ Zeichensatz**](blob-character-set.md) Deskriptor des Zeichensatzes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                                   | Beschreibung                                                      |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                          | Methode war erfolgreich.<br/>                                     |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>                     | Der *pcharakteriset* -Parameter ist kein gültiger Zeiger.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl>                 | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/>  |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>                        | Unbekannter Fehler.<br/>                                    |
| <dl> <dt>**E \_ notimpl**</dt> </dl>                     | Diese Methode ist noch nicht implementiert.<br/>                   |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>                  | *pcharakteriset* ist **null**.<br/>                          |
| <dl> <dt>**HRESULT \_ungültige \_ Daten**</dt> </dl> | Der aktuelle Zeichensatz ist ungültig oder nicht verfügbar.<br/>  |



 

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

 

 




