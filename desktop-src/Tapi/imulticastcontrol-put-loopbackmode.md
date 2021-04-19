---
description: Das put \_ loopbackmode legt den Multicast-Loopback Modus fest.
ms.assetid: 38b28529-224f-4624-bb5e-22fee500e8e6
title: Imulticastcontrol::p ut_LoopbackMode-Methode (confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de5b5e51b3814b380cc06d9c960db1a4e4b9ecb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354732"
---
# <a name="imulticastcontrolput_loopbackmode-method"></a>Imulticastcontrol::p UT \_ loopbackmode-Methode

\[**Put \_ Loopbackmode** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Das **Put \_ loopbackmode** legt den Multicast-Loopback Modus fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_LoopbackMode(
  [in] MULTICAST_LOOPBACK_MODE mode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Modus* \[ in\]
</dt> <dd>

[**Multicast \_ Der Loopback \_ Modus**](multicast-loopback-mode.md) -Deskriptor des neuen Loopback Modus.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                  | Beschreibung                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Methode war erfolgreich.<br/>                  |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Der *Mode* -Parameter ist ungültig.<br/> |



 

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

 

 




