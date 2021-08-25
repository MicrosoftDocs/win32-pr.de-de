---
description: Die Init-Methode initialisiert das Konferenzblob basierend auf einer Textzeichenfolge. Wenn pBlob NULL ist, werden Standardwerte verwendet.
ms.assetid: ba492503-90ff-45dd-a39f-6d4451e57339
title: ITConferenceBlob::Init-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a4f7816d1de346e12b3fab799728f32fb146664846d9dcb6d7cd7df757d62e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991930"
---
# <a name="itconferenceblobinit-method"></a>ITConferenceBlob::Init-Methode

\[Rendezvous IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **Init-Methode** initialisiert das Konferenzblob basierend auf einer Textzeichenfolge. Wenn *pBlob* NULL **ist,** werden Standardwerte verwendet.

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

*pName* \[ In\]
</dt> <dd>

Zeiger auf eine **BSTR-Darstellung** des Konferenznamens.

</dd> <dt>

*CharacterSet* \[ In\]
</dt> <dd>

[**BLOB \_ CHARACTER \_ SET-Deskriptor**](blob-character-set.md) des Zeichensets.

</dd> <dt>

*pBlob* \[ In\]
</dt> <dd>

Zeiger auf einen **BSTR, der** das Konferenzblob enthält. Bei **NULL** wird das Konferenzblob mit Standardwerten initialisiert. Derzeit sind Standardkonferenzwerte nur verfügbar, wenn der *CharacterSet-Parameter* auf BCS ASCII festgelegt \_ ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                         | Bedeutung                                                                    |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                               |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Der *pName-,* *CharacterSet-* oder *pBlob-Parameter* ist ungültig.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher vorhanden, um den Vorgang durchzuführen.<br/>            |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Unbekannter Fehler.<br/>                                              |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                             |



 

## <a name="remarks"></a>Hinweise

**ITConferenceBlob::Init gibt** einen Fehler zurück, wenn das Blob bereits initialisiert wurde.

Die Anwendung muss [**SysAllocString verwenden,**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) um Arbeitsspeicher für die *Parameter pName* und *pBlob zu* reservieren. Die Anwendung muss [**SysFreeString verwenden,**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) um den Arbeitsspeicher frei zu geben, wenn die Variablen nicht mehr benötigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITConferenceBlob**](itconferenceblob.md)
</dt> <dt>

[**\_ \_ BLOB-ZEICHENSATZ**](blob-character-set.md)
</dt> </dl>

 

