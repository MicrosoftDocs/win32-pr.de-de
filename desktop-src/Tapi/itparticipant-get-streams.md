---
description: Die get \_ Streams-Methode erstellt eine Auflistung von Streams, die dem aktuellen Teilnehmer zugeordnet sind.
ms.assetid: 9ab05b14-8ef8-4e7f-b598-05795011e35d
title: ITParticipant::get_Streams-Methode (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b66447cd320110db45e1624d677c9b76e518f926da341805bd7de992d0e0eec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003288"
---
# <a name="itparticipantget_streams-method"></a>ITParticipant::get \_ Streams-Methode

\[**get \_ Streams** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **get \_ Streams-Methode** erstellt eine Auflistung von Streams, die dem aktuellen Teilnehmer zugeordnet sind. Diese Methode wird für Automation-Clientanwendungen bereitgestellt, z. B. in Visual Basic geschriebene Anwendungen. C- und C++-Anwendungen müssen die [**EnumerateStreams-Methode**](itparticipant-enumeratestreams.md) verwenden.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Streams(
  [out] VARIANT *pVariant
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVariant* \[ out\]
</dt> <dd>

Zeiger auf **VARIANT,** der eine [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) von [**ITStream-Schnittstellenzeigern**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                         | Bedeutung                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher zum Ausführen des Vorgangs vorhanden.<br/> |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | Der *pVariant-Parameter* ist kein gültiger Zeiger.<br/>     |



 

## <a name="remarks"></a>Hinweise

TAPI ruft die **AddRef-Methode** auf der [**ITStream-Schnittstelle**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) auf, die von **ITParticipant::get \_ Streams** zurückgegeben wird. Die Anwendung muss **Release** auf der **ITStream-Schnittstelle** aufrufen, um zugeordnete Ressourcen freizugeben.

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

[**EnumerateStreams**](itparticipant-enumeratestreams.md)
</dt> <dt>

[**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> <dt>

[**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)
</dt> <dt>

[**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> </dl>

 

