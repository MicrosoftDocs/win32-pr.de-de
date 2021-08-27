---
description: 'LocationDisp.LatLongReportFactory.DesiredAccuracy-Eigenschaft: Der aktuelle Wert für gewünschte Genauigkeit.'
ms.assetid: dfad833b-bb0c-4c66-9942-da10abee5381
title: LocationDisp.LatLongReportFactory.DesiredAccuracy-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.DesiredAccuracy
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3deccb2dcc71a62b64a508e55759e5cc9c00b5cb0a7a59fb3390046371d2fac4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129850"
---
# <a name="locationdisplatlongreportfactorydesiredaccuracy-property"></a>LocationDisp.LatLongReportFactory.DesiredAccuracy-Eigenschaft

\[Das Location API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen die [W3C-Geolocation-API,](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))um von einer Website aus auf den Standort zuzugreifen. Verwenden Sie den Windows, um von einer Desktopanwendung aus auf den Speicherort [**zuzugreifen. Devices.Geolocation-API.**](/uwp/api/Windows.Devices.Geolocation)\]

Der aktuelle Wert für die gewünschte Genauigkeit.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```JScript
DesiredAccuracy = LocationDisp.LatLongReportFactory.DesiredAccuracy
LocationDisp.LatLongReportFactory.DesiredAccuracy = DesiredAccuracy
```



## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft ist ein **ULONG-Objekt** mit Lese-/Schreibzugriff.



| Wert                                                                        | Bedeutung                                                                                                                                                                                            |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Standard. Der Sensor sollte die Genauigkeit verwenden, für die er die Energienutzung und andere Kostenaspekte optimieren kann.<br/>                                                                          |
| <dl> <dt>1</dt> </dl> | Der Sensor sollte den genauesten Bericht liefern. Dies beinhaltet die Verwendung von kostenpflichtigen Diensten oder Diensten mit höherem Akkuverbrauch oder höherer Verbindungsbandbreite.<br/> |



 

## <a name="remarks"></a>Hinweise

Dieser Wert ist eine Anforderung an den Standortanbieter. Der Standortanbieter muss keine Berichte in dem von Ihnen angeforderten Intervall bereitstellen. Lesen Sie den Wert dieser Eigenschaft, um die Einstellung true report interval zu ermitteln.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                  |



 

