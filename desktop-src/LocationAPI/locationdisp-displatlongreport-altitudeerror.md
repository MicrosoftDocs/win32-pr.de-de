---
description: Höhenfehler in Metern.
ms.assetid: 36ebb079-26e6-4b3f-ad73-547a47bd23d7
title: LocationDisp.DispLatLongReport.AltitudeError-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.AltitudeError
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8d84c09a143808302a623ab7b098a105ef74ee4ad7aecfe3a4a172b765fcbdfa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117809526"
---
# <a name="locationdispdisplatlongreportaltitudeerror-property"></a>LocationDisp.DispLatLongReport.AltitudeError-Eigenschaft

\[Das Location API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen die [W3C-Geolocation-API,](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))um von einer Website aus auf den Standort zuzugreifen. Um von einer Desktopanwendung aus auf den Speicherort zuzugreifen, verwenden Sie die [**Windows. Devices.Geolocation-API.**](/uwp/api/Windows.Devices.Geolocation)\]

Höhenfehler in Metern.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
AltitudeError = LocationDisp.DispLatLongReport.AltitudeError
```



## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (Gleitkommazahl mit doppelter Genauigkeit).

## <a name="remarks"></a>Hinweise

Standortsensoren sind nicht erforderlich, um diese Eigenschaft bereitzustellen. Sie sollten Ausnahmen behandeln, wenn Sie versuchen, auf diese Eigenschaft zuzugreifen.

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieser Eigenschaft finden Sie unter [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                  |



 

