---
description: Die \_ Methode get LoopbackMode ruft den Multicast-Loopbackmodus ab.
ms.assetid: 2499c108-f70b-4afe-aa2b-2376c95b84bd
title: IMulticastControl::get_LoopbackMode-Methode (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87a3f9a600ea64bacf7cafdc5071df264d79079adfefd4a771eea9569fcbb092
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013020"
---
# <a name="imulticastcontrolget_loopbackmode-method"></a>IMulticastControl::get \_ LoopbackMode-Methode

\[**get \_ LoopbackMode** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **\_ Methode get LoopbackMode** ruft den Multicast-Loopbackmodus ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_LoopbackMode(
  [out] MULTICAST_LOOPBACK_MODE *pMode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMode* \[ out\]
</dt> <dd>

Zeiger auf den [**MULTICAST \_ LOOPBACK \_ MODE-Deskriptor**](multicast-loopback-mode.md) des aktuellen Loopbackmodus.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                        | Bedeutung                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Methode war erfolgreich.<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Der *pMode-Parameter* ist ungültig.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMulticastControl**](imulticastcontrol.md)
</dt> </dl>

 

 




