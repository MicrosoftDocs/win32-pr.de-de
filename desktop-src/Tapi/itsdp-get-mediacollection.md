---
description: Die Methode get \_ MediaCollection ruft einen Zeiger auf die ITMediaCollection-Schnittstelle für die Konferenz ab.
ms.assetid: 8109582a-74f0-47e8-91d1-0d89c3d3c331
title: ITSdp::get_MediaCollection-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cf358089a394775c753adc0642897021e91df5bfcd5f23418e638df82db03a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774510"
---
# <a name="itsdpget_mediacollection-method"></a>ITSdp::get \_ MediaCollection-Methode

\[Rendezvous-IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **Methode get \_ MediaCollection** ruft einen Zeiger auf die [**ITMediaCollection-Schnittstelle**](itmediacollection.md) für die Konferenz ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_MediaCollection(
  [out] ITMediaCollection **ppMediaCollection
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppMediaCollection* \[ out\]
</dt> <dd>

Zeiger auf [**ITMediaCollection**](itmediacollection.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                                                           | Bedeutung                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                            | Methode war erfolgreich.<br/>                                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                                    | Der *ppMediaCollection-Parameter* ist kein gültiger Zeiger.<br/>                        |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>                                   | Es ist nicht genügend Arbeitsspeicher zum Ausführen des Vorgangs vorhanden.<br/>                             |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                                          | Unbekannter Fehler.<br/>                                                               |
| <dl> <dt>**HRESULT \_ FROM \_ ERROR \_ CODE(ERROR \_ INVALID \_ DATA)**</dt> </dl> | Ein interner Fehler ist in der Regel aufgrund des Fehlers einer vorherigen Methode aufgetreten.<br/> |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>                                       | Diese Methode ist noch nicht implementiert.<br/>                                              |



 

## <a name="remarks"></a>Hinweise

Ein [**ITMediaCollection-Zeiger**](itmediacollection.md) kann auch mit **QueryInterface** abgerufen werden.

TAPI ruft die **AddRef-Methode** auf der [**ITMediaCollection-Schnittstelle**](itmediacollection.md) auf, die von **ITSdp::get \_ MediaCollection** zurückgegeben wird. Die Anwendung muss **Release** auf der **ITMediaCollection-Schnittstelle** aufrufen, um zugeordnete Ressourcen freizugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> </dl>

 

 




