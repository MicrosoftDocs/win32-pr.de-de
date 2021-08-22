---
description: Die methode \_ get CharacterSet ruft einen BLOB CHARACTER SET-Deskriptor des Zeichensets ab, der \_ \_ im aktuellen Konferenzblob verwendet wird.
ms.assetid: 9783d18c-79f6-4faa-b12d-9504c13d54e3
title: ITConferenceBlob::get_CharacterSet-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20a9dd719d2ae9742a6ec4b3295e3e22ffe871b4a38c55d07e07a3421271553d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060998"
---
# <a name="itconferenceblobget_characterset-method"></a>ITConferenceBlob::get \_ CharacterSet-Methode

\[Rendezvous IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **methode \_ get CharacterSet** ruft einen [**BLOB CHARACTER \_ SET-Deskriptor \_**](blob-character-set.md) des Zeichensets ab, der im aktuellen Konferenzblob verwendet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_CharacterSet(
  [out] BLOB_CHARACTER_SET *pCharacterSet
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pCharacterSet* \[ out\]
</dt> <dd>

Zeiger auf einen [**BLOB \_ CHARACTER SET-Deskriptor \_**](blob-character-set.md) des Zeichensets.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                                   | Beschreibung                                                      |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                          | Methode war erfolgreich.<br/>                                     |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>                     | Der *pCharacterSet-Parameter* ist kein gültiger Zeiger.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>                 | Es ist nicht genügend Arbeitsspeicher vorhanden, um den Vorgang durchzuführen.<br/>  |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                        | Unbekannter Fehler.<br/>                                    |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>                     | Diese Methode ist noch nicht implementiert.<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                  | *pCharacterSet* ist **NULL.**<br/>                          |
| <dl> <dt>**(HRESULT) FEHLER \_ UNGÜLTIGE \_ DATEN**</dt> </dl> | Der aktuelle Zeichensatz ist ungültig oder nicht verfügbar.<br/>  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITConferenceBlob**](itconferenceblob.md)
</dt> <dt>

[**\_ \_ BLOB-ZEICHENSATZ**](blob-character-set.md)
</dt> </dl>

 

 




