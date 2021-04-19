---
description: Die setconferenceblob-Methode führt einen Commit für Änderungen an das Konferenz-BLOB aus. Verwenden Sie stattdessen die Init-Methode, um das Konferenz-BLOB zum ersten Mal zu initialisieren.
ms.assetid: 4a65edb9-77de-42d9-85a1-1e3c41706417
title: 'Itconfererceblob:: setconfererceblob-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47779807e5bde6a070b4600aec903309c7679dc8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370093"
---
# <a name="itconferenceblobsetconferenceblob-method"></a>Itconfererceblob:: setconfererceblob-Methode

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **setconferenceblob** -Methode führt einen Commit für Änderungen an das Konferenz-BLOB aus. Verwenden Sie stattdessen die [**Init**](itconferenceblob-init.md) -Methode, um das Konferenz-BLOB zum ersten Mal zu initialisieren.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetConferenceBlob(
  [in] BLOB_CHARACTER_SET CharacterSet,
  [in] BSTR               pBlob
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Merkmal Satz* \[ in\]
</dt> <dd>

[**BLOB \_ \_Zeichensatz**](blob-character-set.md) Deskriptor für den Zeichensatz des Konferenz-BLOBs.

</dd> <dt>

*pBlob* \[ in\]
</dt> <dd>

Zeiger auf ein **BSTR** , das das Konferenz-BLOB enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                     |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Der *charakterisetyp* oder der *pBlob* -Parameter ist ungültig.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/>  |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>        | Unbekannter Fehler.<br/>                                    |
| <dl> <dt>**E \_ notimpl**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                   |



 

## <a name="remarks"></a>Bemerkungen

Die Anwendung muss " [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) " verwenden, um Speicher für den *pBlob* -Parameter zuzuweisen, und " [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) " verwenden, um den Arbeitsspeicher freizugeben, wenn die Variable nicht mehr benötigt wird.

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

 

