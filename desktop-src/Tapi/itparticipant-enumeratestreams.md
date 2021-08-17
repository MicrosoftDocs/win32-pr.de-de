---
description: Die EnumerateStreams-Methode aufzählt streams derzeit mit den Teilnehmern. Diese Methode wird für C- und C++-Anwendungen bereitgestellt. Automatisierungsclientanwendungen, z. B. in Visual Basic, müssen die get Streams \_ verwenden.
ms.assetid: 69db198d-fb4c-482b-bf49-5c636ac2f86b
title: ITParticipant::EnumerateStreams-Methode (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1ec901c81bb0df666877ee06462b88da965b41bedd961e71cebbf25cd78ee30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140303"
---
# <a name="itparticipantenumeratestreams-method"></a>ITParticipant::EnumerateStreams-Methode

\[**EnumerateStreams** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **EnumerateStreams-Methode** aufzählt streams derzeit mit den Teilnehmern. Diese Methode wird für C- und C++-Anwendungen bereitgestellt. Automatisierungsclientanwendungen, z. B. in Visual Basic, müssen die [**get Streams \_**](itparticipant-get-streams.md) verwenden.

## <a name="syntax"></a>Syntax


```C++
HRESULT EnumerateStreams(
  [out] IEnumStream **ppEnumStream
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppEnumStream* \[ out\]
</dt> <dd>

Zeiger auf den [**IEnumStream-Schnittstellenzeiger.**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                     | Bedeutung                                                         |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl> | Der *ppEnumStream-Parameter* ist kein gültiger Zeiger.<br/> |



 

## <a name="remarks"></a>Hinweise

TAPI ruft die **AddRef-Methode** für die [**IEnumStream-Schnittstelle auf,**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) die von **ITParticipant::EnumerateStreams zurückgegeben wird.** Die Anwendung muss **Release auf der** **IEnumStream-Schnittstelle** aufrufen, um zugeordnete Ressourcen frei zu geben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                |
| Header<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**get \_ Streams**](itparticipant-get-streams.md)
</dt> <dt>

[**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> </dl>

 

 




