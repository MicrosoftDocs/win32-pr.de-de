---
description: Der aktuelle Wert für die gewünschte Genauigkeit.
ms.assetid: dfad833b-bb0c-4c66-9942-da10abee5381
title: LocationDisp. latlongreportfactory. desiredaccuracy (Eigenschaft)
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
ms.openlocfilehash: e17e415d9503660d873ae4df67d2469c646dd80e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363782"
---
# <a name="locationdisplatlongreportfactorydesiredaccuracy-property"></a>LocationDisp. latlongreportfactory. desiredaccuracy (Eigenschaft)

\[Das Location-API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen die [W3C-geolozierungs-API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)), um auf den Standort von einer Website zuzugreifen. Verwenden Sie die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API, um auf den Speicherort einer Desktop Anwendung zuzugreifen.\]

Der aktuelle Wert für die gewünschte Genauigkeit.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```JScript
DesiredAccuracy = LocationDisp.LatLongReportFactory.DesiredAccuracy
LocationDisp.LatLongReportFactory.DesiredAccuracy = DesiredAccuracy
```



## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft ist ein Lese- **/Schreib-ULONG**.



| Wert                                                                        | Bedeutung                                                                                                                                                                                            |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Standard. Der Sensor sollte die Genauigkeit verwenden, bei der der Energieverbrauch und andere Kostenüberlegungen optimiert werden können.<br/>                                                                          |
| <dl> <dt>1</dt> </dl> | Der Sensor sollte den genauesten Bericht übermitteln. Dies beinhaltet die Verwendung von kostenpflichtigen Diensten oder Diensten mit höherem Akkuverbrauch oder höherer Verbindungsbandbreite.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Dieser Wert ist eine Anforderung an den Speicherort Anbieter. Es ist nicht erforderlich, dass der standortanbieter Berichte in dem von Ihnen angeforderten Intervall bereitstellt. Lesen Sie den Wert dieser Eigenschaft, um die Einstellung für das tatsächliche Berichts Intervall zu ermitteln.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                  |



 

