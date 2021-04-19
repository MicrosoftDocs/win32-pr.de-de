---
description: Die get \_ \_ netwenum-Methode gibt einen Enumerator für die Auflistung zurück.
ms.assetid: 0c2d739d-736d-4773-9747-1107546a973c
title: 'Ittimecollection:: get__NewEnum-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e3fbd171696b81bf5bd67c99b9a91294f4581d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370636"
---
# <a name="ittimecollectionget__newenum-method"></a>Ittimecollection:: get- \_ \_ Methode "netwenum"

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **get \_ \_ netwenum** -Methode gibt einen Enumerator für die Auflistung zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT get__NewEnum(
  [out] IUnknown **pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PVal* \[ vorgenommen\]
</dt> <dd>

Zeiger auf eine [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle für ein Enumeratorobjekt für die Auflistung.

Rufen Sie die [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode auf der zurückgegebenen **IUnknown** -Schnittstelle auf, um einen Zeiger auf eine [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Enumerationsschnittstelle für die Auflistung zu erhalten. **IEnumVARIANT** bietet eine Reihe von Methoden, die Sie verwenden können, um die Auflistung zu durchlaufen.

Weitere Informationen finden Sie im folgenden Abschnitt "Hinweise".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Der *PVal* -Parameter ist kein gültiger Zeiger.<br/>         |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/> |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ notimpl**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode ist mit [**get \_ enumerationif**](ittimecollection-get-enumerationif.md) austauschbar, mit dem Unterschied, dass Sie anstelle von [**ienumtime**](ienumtime.md) **IUnknown** zurückgibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ittimecollection**](ittimecollection.md)
</dt> <dt>

[**Ittime**](ittime.md)
</dt> </dl>

 

