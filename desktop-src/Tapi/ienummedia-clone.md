---
description: 'IEnumMedia::Clone-Methode: Die Clone-Methode erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle enthält.'
ms.assetid: b48399f5-daaa-40e4-bd80-a918539d25c6
title: IEnumMedia::Clone-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 894457684e94d07426511979dcb40cfcbbe75ed9fec91e024f09175389261620
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992440"
---
# <a name="ienummediaclone-method"></a>IEnumMedia::Clone-Methode

\[Rendezvous-IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **Clone-Methode** erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle enthält.

## <a name="syntax"></a>Syntax


```C++
HRESULT Clone(
  [out] IEnumMedia **ppEnum
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppEnum* \[ out\]
</dt> <dd>

Zeiger auf das neue [**IEnumMedia-Objekt.**](ienummedia.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                         | Bedeutung                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | Der *ppEnum-Parameter* ist kein gültiger Zeiger.<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher zum Ausführen des Vorgangs vorhanden.<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>  | Fehler aus unbekannten Gründen.<br/>                          |



 

## <a name="remarks"></a>Hinweise

TAPI ruft die **AddRef-Methode** für die [**IEnumMedia-Schnittstelle**](ienummedia.md) auf, die von **IEnumMedia::Clone** zurückgegeben wird. Die Anwendung muss **Release** auf der **IEnumMedia-Schnittstelle** aufrufen, um zugeordnete Ressourcen freizugeben.

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
</dt> </dl>

 

 




