---
description: Die get \_ TransportProtocol-Methode ruft das Transportprotokoll ab.
ms.assetid: d270d6f4-bdcf-4cf4-970b-65f0be706171
title: ITMedia::get_TransportProtocol-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7927469ff00caab36ab45af12939c6f2f6518a415d4a764c3d04f9c715db75e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682770"
---
# <a name="itmediaget_transportprotocol-method"></a>\_ITMedia::get-TransportProtocol-Methode

\[Rendezvous IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **get \_ TransportProtocol-Methode** ruft das Transportprotokoll ab. Dies wird zusätzlich zum Medienformat angegeben, sodass das gleiche Standardmedienformat auch dann über verschiedene Transportprotokolle übertragen werden kann, wenn das Netzwerkprotokoll identisch ist, z. B. bei Der PCM-Audiodatei und rtp-PCM-Audio.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_TransportProtocol(
  [out] BSTR *ppProtocol
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppProtocol* \[ out\]
</dt> <dd>

Zeiger auf die **BSTR-Darstellung** des Transportprotokolls.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>     | Der *ppProtocol-Parameter* ist kein gültiger Zeiger.<br/>   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher vorhanden, um den Vorgang durchzuführen.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

## <a name="remarks"></a>Hinweise

Die Anwendung muss [**SysFreeString verwenden,**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) um den für den *ppProtocol-Parameter* zugeordneten Arbeitsspeicher freizu geben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITMedia**](itmedia.md)
</dt> <dt>

[**ITMedia::put \_ TransportProtocol**](itmedia-put-transportprotocol.md)
</dt> </dl>

 

