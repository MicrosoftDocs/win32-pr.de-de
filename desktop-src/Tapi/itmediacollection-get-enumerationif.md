---
description: Die get \_ EnumerationIf-Methode ruft einen Zeiger auf eine Medienenumerationsschnittstelle ab.
ms.assetid: d5f1e10f-e5ad-45e6-a5ec-024905603012
title: ITMediaCollection::get_EnumerationIf-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfe14475e216b5143b599aab50d12d1d0c548b5f64dd8e44edd2e6aab249905c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060858"
---
# <a name="itmediacollectionget_enumerationif-method"></a>ITMediaCollection::get \_ EnumerationIf-Methode

\[Rendezvous-IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **get \_ EnumerationIf-Methode** ruft einen Zeiger auf eine Medienenumerationsschnittstelle ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_EnumerationIf(
  [out] IEnumMedia **pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVal* \[ out\]
</dt> <dd>

Zeiger auf die [**IEnumMedia-Schnittstelle**](ienummedia.md) für das gewünschte Element.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                         | Bedeutung                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | Der *pVal-Parameter* ist kein gültiger Zeiger.<br/>         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher zum Ausführen des Vorgangs vorhanden.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

## <a name="remarks"></a>Hinweise

Diese Methode ist mit [**get \_ \_ NewEnum**](itmediacollection-get--newenum.md) austauschbar, außer dass sie [**IEnumMedia**](ienummedia.md) anstelle von **IUnknown** zurückgibt.

TAPI ruft die **AddRef-Methode** für die [**IEnumMedia-Schnittstelle**](ienummedia.md) auf, die von **ITMediaCollection::get \_ Enumerationlf** zurückgegeben wird. Die Anwendung muss **Release** auf der **IEnumMedia-Schnittstelle** aufrufen, um zugeordnete Ressourcen freizugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IEnumMedia**](ienummedia.md)
</dt> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> </dl>

 

 




