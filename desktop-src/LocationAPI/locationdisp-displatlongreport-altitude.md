---
description: Aktuelle Höhe in Meter. Die Höhe ist relativ zum Verweis Ellipsoid.
ms.assetid: fbe9984c-aa9d-4ce0-9f8b-d79ca06764d4
title: LocationDisp. displatlongreport. Altitude (Eigenschaft)
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
ms.openlocfilehash: 2004c8df6c61fb890bf8f71fb3c2b5446d71d79a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865479"
---
# <a name="locationdispdisplatlongreportaltitude-property"></a>LocationDisp. displatlongreport. Altitude (Eigenschaft)

\[Das Location-API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen die [W3C-geolozierungs-API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)), um auf den Standort von einer Website zuzugreifen. Verwenden Sie die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API, um auf den Speicherort einer Desktop Anwendung zuzugreifen.\]

Aktuelle Höhe in Meter. Die Höhe ist relativ zum Verweis Ellipsoid.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
Altitude = LocationDisp.DispLatLongReport.Altitude
```



## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (Gleit Komma Wert mit doppelter Genauigkeit).

## <a name="remarks"></a>Bemerkungen

Location-Sensoren sind nicht erforderlich, um diese Eigenschaft bereitzustellen. Sie sollten Ausnahmen behandeln, wenn Sie versuchen, auf diese Eigenschaft zuzugreifen.

Die **Höhen** Methode ruft die Höhe in Bezug auf den Verweis Ellipsoid ab, der durch die neueste Revision des World Geodetic System (WGS 84) definiert wird, anstatt die Höhe relativ zur Meeres Ebene.

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieser Eigenschaft finden Sie unter [Beispiel für einen einfachen latlong-Bericht](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                  |



 

