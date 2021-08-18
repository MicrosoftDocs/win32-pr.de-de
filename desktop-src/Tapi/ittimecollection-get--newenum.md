---
description: 'ITTimeCollection::get__NewEnum-Methode: Die get \_ \_ NewEnum-Methode gibt einen Enumerator für die Auflistung zurück.'
ms.assetid: 0c2d739d-736d-4773-9747-1107546a973c
title: ITTimeCollection::get__NewEnum-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ba76f1d10e2cb9ee937ec688af3e87e0bb9310df9fc39afaef64e60ea55b1dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991900"
---
# <a name="ittimecollectionget__newenum-method"></a>ITTimeCollection::get \_ \_ NewEnum-Methode

\[Rendezvous-IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **get \_ \_ NewEnum-Methode** gibt einen Enumerator für die Auflistung zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT get__NewEnum(
  [out] IUnknown **pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVal* \[ out\]
</dt> <dd>

Zeiger auf eine [IUnknown-Schnittstelle](/windows/win32/api/unknwn/nn-unknwn-iunknown) für ein Enumeratorobjekt für die Auflistung.

Rufen Sie die [QueryInterface-Methode](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für die zurückgegebene **IUnknown-Schnittstelle** auf, um einen Zeiger auf eine [IEnumVARIANT-Enumerationsschnittstelle](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) für die Auflistung abzurufen. **IEnumVARIANT** stellt eine Reihe von Methoden bereit, mit denen Sie die Auflistung durchlaufen können.

Weitere Informationen finden Sie im folgenden Abschnitt "Hinweise".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | Der *pVal-Parameter* ist kein gültiger Zeiger.<br/>         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher zum Ausführen des Vorgangs vorhanden.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

## <a name="remarks"></a>Hinweise

Diese Methode ist mit [**get \_ EnumerationIf**](ittimecollection-get-enumerationif.md) austauschbar, gibt jedoch **IUnknown** anstelle von [**IEnumTime**](ienumtime.md)zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITTimeCollection**](ittimecollection.md)
</dt> <dt>

[**ITTime**](ittime.md)
</dt> </dl>

 

