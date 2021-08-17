---
description: Der put \_ LoopbackMode legt den Multicast-Loopbackmodus fest.
ms.assetid: 38b28529-224f-4624-bb5e-22fee500e8e6
title: IMulticastControl::p ut_LoopbackMode-Methode (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d564fbfd3e5ea0db2c168b6207823945eceb148af17d78bed25cbc59bb4e5ee6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140413"
---
# <a name="imulticastcontrolput_loopbackmode-method"></a>IMulticastControl::p ut \_ LoopbackMode-Methode

\[**put \_ LoopbackMode** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Der **put \_ LoopbackMode legt** den Multicast-Loopbackmodus fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_LoopbackMode(
  [in] MULTICAST_LOOPBACK_MODE mode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*-Modus* \[ In\]
</dt> <dd>

[**MULTICAST \_ LOOPBACK \_ MODE-Deskriptor**](multicast-loopback-mode.md) des neuen Loopbackmodus.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                  | Beschreibung                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Methode war erfolgreich.<br/>                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Der *mode-Parameter* ist ungültig.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMulticastControl**](imulticastcontrol.md)
</dt> </dl>

 

 




