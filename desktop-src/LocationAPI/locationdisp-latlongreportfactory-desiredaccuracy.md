---
description: 'LocationDisp.LatLongReportFactory.DesiredAccuracy-Eigenschaft: Der aktuelle Wert für die gewünschte Genauigkeit.'
ms.assetid: dfad833b-bb0c-4c66-9942-da10abee5381
title: LocationDisp.LatLongReportFactory.DesiredAccuracy (Eigenschaft)
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
ms.openlocfilehash: afc5ec235df6c9e07a665410cb09e00f24305304
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088968"
---
# <a name="locationdisplatlongreportfactorydesiredaccuracy-property"></a>LocationDisp.LatLongReportFactory.DesiredAccuracy (Eigenschaft)

\[Das Location-API-Objektmodell steht für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen zur Verfügung. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen die [W3C-Geolocation-API,](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))um von einer Website aus auf den Standort zuzugreifen. Verwenden Sie die [**Windows.Devices.Geolocation-API,**](/uwp/api/Windows.Devices.Geolocation) um über eine Desktopanwendung auf den Standort zuzugreifen.\]

Der aktuelle gewünschte Genauigkeitswert.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```JScript
DesiredAccuracy = LocationDisp.LatLongReportFactory.DesiredAccuracy
LocationDisp.LatLongReportFactory.DesiredAccuracy = DesiredAccuracy
```



## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft ist ein ULONG-Objekt mit **Lese-/Schreibzugriff.**



| Wert                                                                        | Bedeutung                                                                                                                                                                                            |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Standard. Der Sensor sollte die Genauigkeit verwenden, für die er den Stromverbrauch und andere Kostenaspekte optimieren kann.<br/>                                                                          |
| <dl> <dt>1</dt> </dl> | Der Sensor sollte den bestmöglichen Bericht liefern. Dies beinhaltet die Verwendung von kostenpflichtigen Diensten oder Diensten mit höherem Akkuverbrauch oder höherer Verbindungsbandbreite.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Dieser Wert ist eine Anforderung an den Standortanbieter. Der Standortanbieter muss in dem von Ihnen angeforderten Intervall keine Berichte bereitstellen. Lesen Sie den Wert dieser Eigenschaft, um die Einstellung true report interval zu finden.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|--------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ 7-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                  |



 

