---
description: Eine Entfernung vom gemeldeten Speicherort in Meter. In Kombination mit dem gemeldeten Speicherort als Ursprung beschreibt dieser RADIUS den Kreis, in dem sich der tatsächliche Speicherort wahrscheinlich befindet.
ms.assetid: a9565bd5-d1e0-45f8-abeb-3191b16480fa
title: LocationDisp. displatlongreport. errorradius-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.ErrorRadius
api_type:
- COM
api_location: ''
ms.openlocfilehash: f99ff9b03451738158a98541bfae0e67a8827717
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362286"
---
# <a name="locationdispdisplatlongreporterrorradius-property"></a>LocationDisp. displatlongreport. errorradius-Eigenschaft

\[Das Location-API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen die [W3C-geolozierungs-API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)), um auf den Standort von einer Website zuzugreifen. Verwenden Sie die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API, um auf den Speicherort einer Desktop Anwendung zuzugreifen.\]

Eine Entfernung vom gemeldeten Speicherort in Meter. In Kombination mit dem gemeldeten Speicherort als Ursprung beschreibt dieser RADIUS den Kreis, in dem sich der tatsächliche Speicherort wahrscheinlich befindet.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
ErrorRadius = LocationDisp.DispLatLongReport.ErrorRadius
```



## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (Gleit Komma Wert mit doppelter Genauigkeit).

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieser Eigenschaft finden Sie unter [Beispiel für einen einfachen latlong-Bericht](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                  |



 

