---
description: Die get \_ EnumerationIf-Methode gibt die IEnumTime-Enumerationsschnittstelle zurück, die ITTime aufzählt.
ms.assetid: 31f6fa94-d047-4c53-96ae-8dd7e66a4e33
title: ITTimeCollection::get_EnumerationIf-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb6afa99d1170180d0174bfd9b4d3f92f3733b1bee716ddd1e80b957e0c9bf33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905906"
---
# <a name="ittimecollectionget_enumerationif-method"></a>ITTimeCollection::get \_ EnumerationIf-Methode

\[Rendezvous-IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **get \_ EnumerationIf-Methode** gibt die [**IEnumTime-Enumerationsschnittstelle**](ienumtime.md) zurück, die [**ITTime**](ittime.md)aufzählt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_EnumerationIf(
  [out] IEnumTime **pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVal* \[ out\]
</dt> <dd>

Zeiger auf die [**IEnumTime-Schnittstelle.**](ienumtime.md)

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

Diese Methode kann mit [**get \_ \_ NewEnum**](ittimecollection-get--newenum.md) austauschbar sein, mit der Ausnahme, dass sie [**IEnumTime**](ienumtime.md) anstelle von **IUnknown** zurückgibt.

TAPI ruft die **AddRef-Methode** für die [**IEnumTime-Schnittstelle**](ienumtime.md) auf, die von **ITTimeCollection::get \_ EnumerationIf** zurückgegeben wird. Die Anwendung muss **Release** auf der [**IEnumTime-Schnittstelle**](ienumtime.md) aufrufen, um zugeordnete Ressourcen freizugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IEnumTime**](ienumtime.md)
</dt> <dt>

[**ITTimeCollection**](ittimecollection.md)
</dt> <dt>

[**ITTime**](ittime.md)
</dt> </dl>

 

 




