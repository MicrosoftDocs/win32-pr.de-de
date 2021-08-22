---
description: Aktuelle Höhe in Metern. Die Höhe ist relativ zum Verweisellipsoid.
ms.assetid: fbe9984c-aa9d-4ce0-9f8b-d79ca06764d4
title: LocationDisp.DispLatLongReport.Altitude-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.Altitude
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8ee6c2cd4257d7f7db97b89a5af4603f5c5129b7f07fe9bfbe6444bb9d347422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067940"
---
# <a name="locationdispdisplatlongreportaltitude-property"></a>LocationDisp.DispLatLongReport.Altitude-Eigenschaft

\[Das Location API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen die [W3C-Geolocation-API,](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))um von einer Website aus auf den Standort zuzugreifen. Um von einer Desktopanwendung aus auf den Speicherort zuzugreifen, verwenden Sie die [**Windows. Devices.Geolocation-API.**](/uwp/api/Windows.Devices.Geolocation)\]

Aktuelle Höhe in Metern. Die Höhe ist relativ zum Verweisellipsoid.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
Altitude = LocationDisp.DispLatLongReport.Altitude
```



## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (Gleitkommazahl mit doppelter Genauigkeit).

## <a name="remarks"></a>Hinweise

Standortsensoren sind nicht erforderlich, um diese Eigenschaft bereitzustellen. Sie sollten Ausnahmen behandeln, wenn Sie versuchen, auf diese Eigenschaft zuzugreifen.

Die **Methode Höhe** ruft die Höhe relativ zum Referenzellipsoid ab, das durch die neueste Revision des World Geodetic System (WGS 84) definiert wird, anstatt die Höhe relativ zum Seegrad.

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieser Eigenschaft finden Sie unter [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                  |



 

