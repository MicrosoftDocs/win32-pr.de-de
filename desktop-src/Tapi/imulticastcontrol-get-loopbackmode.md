---
description: Die get \_ loopbackmode-Methode ruft den Multicast-Loopback Modus ab.
ms.assetid: 2499c108-f70b-4afe-aa2b-2376c95b84bd
title: 'Imulticastcontrol:: get_LoopbackMode-Methode (confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 203d68f5b620ddf5e5ce7a36e4f8b85820deab2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364927"
---
# <a name="imulticastcontrolget_loopbackmode-method"></a>Imulticastcontrol:: get \_ loopbackmode-Methode

\[**get \_ Loopbackmode** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **get \_ loopbackmode** -Methode ruft den Multicast-Loopback Modus ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_LoopbackMode(
  [out] MULTICAST_LOOPBACK_MODE *pMode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmode* \[ vorgenommen\]
</dt> <dd>

Zeiger auf den [**Multicast- \_ Loopback \_ Modus**](multicast-loopback-mode.md) -Deskriptor des aktuellen Loopback Modus.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                        | Bedeutung                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Methode war erfolgreich.<br/>                   |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Der *pmode* -Parameter ist ungültig.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>"Confpriv. h"</dt> </dl> |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imulticastcontrol**](imulticastcontrol.md)
</dt> </dl>

 

 




