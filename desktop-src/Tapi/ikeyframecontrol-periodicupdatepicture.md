---
description: Die periodicupdatepicture-Methode wird von einer Anwendung aufgerufen, um einen Timer im Stream zu konfigurieren, der regelmäßig Bildaktualisierungen anfordert. Bildaktualisierungen führen zu einer hohen Bandbreitenauslastung, sodass diese Methode normalerweise anstelle von Update Picture verwendet wird.
ms.assetid: 6ae3b5e9-bc11-4f3f-972b-21c9ac299987
title: Ikeyframecontrol::P eriodicupdatepicture-Methode (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50bbfb18b0be96d611f0fe385cc825602dc316ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352840"
---
# <a name="ikeyframecontrolperiodicupdatepicture-method"></a>Ikeyframecontrol::P eriodicupdatepicture-Methode

\[**Periodicupdatepicture** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **periodicupdatepicture** -Methode wird von einer Anwendung aufgerufen, um einen Timer im Stream zu konfigurieren, der regelmäßig Bildaktualisierungen anfordert. Bildaktualisierungen führen zu einer hohen Bandbreitenauslastung, sodass diese Methode normalerweise anstelle von [**Update Picture**](ikeyframecontrol-updatepicture.md)verwendet wird.

Wenn die-Methode aufgerufen wird, wenn der Stream aktiv ist, wird der Timer sofort gestartet. Wenn der Stream nicht aktiv ist, wird der Timer gestartet, wenn der Stream in den aktiven Zustand wechselt.

## <a name="syntax"></a>Syntax


```C++
HRESULT PeriodicUpdatePicture(
  [in] BOOL  fEnable,
  [in] DWORD dwInterval
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*fenckbar* \[ in\]
</dt> <dd>

**True** aktiviert den Timer. **False** deaktiviert es.

</dd> <dt>

*dwinterval* \[ in\]
</dt> <dd>

Das Intervall für den Timer in Sekunden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                            | Beschreibung                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Methode war erfolgreich.<br/>              |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl> | Unerwartete Gründe sind aufgetreten.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>H323priv. h</dt> </dl> |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[H323-msp](h323-msp.md)
</dt> </dl>

 

 




