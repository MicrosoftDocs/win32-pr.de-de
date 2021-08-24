---
description: 'ITMediaCollection::get__NewEnum-Methode: Die get NewEnum-Methode gibt einen \_ \_ Enumerator für die Auflistung zurück.'
ms.assetid: 22b1eb48-e1ef-4694-a1dc-b2de326989c8
title: ITMediaCollection::get__NewEnum-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759ac5a36324e80e4f2ef3ab49f7e8617aa5d3f5faecb61ca7f8c2de82827354
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682680"
---
# <a name="itmediacollectionget__newenum-method"></a>ITMediaCollection::get \_ \_ NewEnum-Methode

\[Rendezvous IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

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

Rufen Sie [die QueryInterface-Methode](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für die **zurückgegebene IUnknown-Schnittstelle** auf, um einen Zeiger auf eine [IEnumVARIANT-Enumerationsschnittstelle](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) für die Auflistung zu erhalten. **IEnumVARIANT** bietet eine Reihe von Methoden, die Sie verwenden können, um die Auflistung zu iterieren.

Weitere Informationen finden Sie im folgenden Abschnitt "Hinweise".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>     | Der *pVal-Parameter* ist kein gültiger Zeiger.<br/>         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher vorhanden, um den Vorgang durchzuführen.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

## <a name="remarks"></a>Hinweise

Diese Methode ist mit get [**\_ EnumerationIf austauschbar,**](itmediacollection-get-enumerationif.md) gibt **jedoch IUnknown** anstelle von [**IEnumMedia zurück.**](ienummedia.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> </dl>

 

