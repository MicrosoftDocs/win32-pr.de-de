---
description: Das aktuelle Ereignisintervall für den Breiten-/Längengradbericht in Millisekunden.
ms.assetid: bb33c4c1-805d-4519-8363-b0221d420b36
title: LocationDisp.LatLongReportFactory.ReportInterval (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.ReportInterval
api_type:
- COM
api_location: ''
ms.openlocfilehash: d12ceab473ae9375a9a1a96ff28d5389cccf324f4a447f17df7c628a514dcf4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118386687"
---
# <a name="locationdisplatlongreportfactoryreportinterval-property"></a>LocationDisp.LatLongReportFactory.ReportInterval (Eigenschaft)

\[Das Location-API-Objektmodell steht für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen zur Verfügung. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen die [W3C-Geolocation-API,](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))um von einer Website aus auf den Standort zuzugreifen. Um von einer Desktopanwendung aus auf den Speicherort zu zugreifen, verwenden Sie [**die Windows. Devices.Geolocation-API.**](/uwp/api/Windows.Devices.Geolocation)\]

Das aktuelle Ereignisintervall für den Breiten-/Längengradbericht in Millisekunden.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```JScript
ReportInterval = LocationDisp.LatLongReportFactory.ReportInterval
LocationDisp.LatLongReportFactory.ReportInterval = ReportInterval
```



## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft ist ein ULONG-Objekt mit **Lese-/Schreibzugriff.**

## <a name="remarks"></a>Hinweise

Dieser Wert ist eine Anforderung an den Standortanbieter. Der Standortanbieter muss in dem von Ihnen geforderten Intervall keine Berichte bereitstellen. Lesen Sie den Wert dieser Eigenschaft, um die Einstellung true report interval zu finden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                  |



 

