---
description: Die Init-Methode initialisiert das Konferenz-BLOB auf Grundlage einer Text Zeichenfolge. Wenn pBlob den Wert NULL hat, werden Standardwerte verwendet.
ms.assetid: ba492503-90ff-45dd-a39f-6d4451e57339
title: 'Itconferendceblob:: Init-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81bdd512ffeb4b380da04e59deb17315d00b7285
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369709"
---
# <a name="itconferenceblobinit-method"></a>Itconferendceblob:: Init-Methode

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **Init** -Methode initialisiert das Konferenz-BLOB auf Grundlage einer Text Zeichenfolge. Wenn *pBlob* den Wert **null** hat, werden Standardwerte verwendet.

## <a name="syntax"></a>Syntax


```C++
HRESULT Init(
  [in] BSTR               pName,
  [in] BLOB_CHARACTER_SET CharacterSet,
  [in] BSTR               pBlob
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PName* \[ in\]
</dt> <dd>

Zeiger auf eine **BSTR** -Darstellung des Konferenz namens.

</dd> <dt>

*Merkmal Satz* \[ in\]
</dt> <dd>

[**BLOB \_ \_Zeichensatz**](blob-character-set.md) Deskriptor des Zeichensatzes.

</dd> <dt>

*pBlob* \[ in\]
</dt> <dd>

Zeiger auf ein **BSTR** , das das Konferenz-BLOB enthält. Wenn der Wert **null** ist, wird das Konferenz-BLOB mit den Standardwerten initialisiert. Derzeit sind Standard-Konferenz Werte nur verfügbar, wenn der Parameter " *Merkmal Satz* " auf BCS ASCII festgelegt ist \_ .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                         | Bedeutung                                                                    |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                               |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Der Parameter " *PName*", " *Merkmal Satz*" oder " *pBlob* " ist ungültig.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/>            |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>        | Unbekannter Fehler.<br/>                                              |
| <dl> <dt>**E \_ notimpl**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                             |



 

## <a name="remarks"></a>Bemerkungen

**Itconfererceblob:: init** gibt einen Fehler zurück, wenn das BLOB bereits initialisiert wurde.

Die Anwendung muss " [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) " verwenden, um Arbeitsspeicher für die Parameter " *PName* " und " *pBlob* " zuzuweisen. Die Anwendung muss [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den Arbeitsspeicher freizugeben, wenn die Variablen nicht mehr benötigt werden.

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

 

