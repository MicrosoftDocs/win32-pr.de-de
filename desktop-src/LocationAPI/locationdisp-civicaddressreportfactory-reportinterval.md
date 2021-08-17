---
description: Das aktuelle Ereignisintervall des Stadtadressberichts in Millisekunden.
ms.assetid: 495dd8a1-4244-468f-b295-337b393aea8a
title: LocationDisp.CivicAddressReportFactory.ReportInterval-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.ReportInterval
api_type:
- COM
api_location: ''
ms.openlocfilehash: d18db71ac97bbfca60d4892bb151388eee97dbb481508b86b595d5dda74954fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118387161"
---
# <a name="locationdispcivicaddressreportfactoryreportinterval-property"></a>LocationDisp.CivicAddressReportFactory.ReportInterval-Eigenschaft

\[Das Location API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen die [W3C-Geolocation-API,](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))um von einer Website aus auf den Standort zuzugreifen. Um von einer Desktopanwendung aus auf den Speicherort zuzugreifen, verwenden Sie die [**Windows. Devices.Geolocation-API.**](/uwp/api/Windows.Devices.Geolocation)\]

Das aktuelle Ereignisintervall des Stadtadressberichts in Millisekunden.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```JScript
ReportInterval = LocationDisp.CivicAddressReportFactory.ReportInterval
LocationDisp.CivicAddressReportFactory.ReportInterval = ReportInterval
```



## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft ist ein **ULONG-Objekt** mit Lese-/Schreibzugriff.

## <a name="remarks"></a>Hinweise

Dieser Wert ist eine Anforderung für den Standortanbieter. Der Standortanbieter muss keine Berichte in dem von Ihnen angeforderten Intervall bereitstellen. Lesen Sie den Wert dieser Eigenschaft, um die Einstellung true report interval zu ermitteln.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                  |



 

