---
description: 'LocationDisp.LatLongReportFactory.Status-Eigenschaft: Der aktuelle Berichtsstatus.'
ms.assetid: bcdf76b5-88c4-481a-89ac-2b9558cecfc0
title: LocationDisp.LatLongReportFactory.Status-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.Status
api_type:
- COM
api_location: ''
ms.openlocfilehash: 37e66c3f289f5376b31ffe516f45d79f2fef51e2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088898"
---
# <a name="locationdisplatlongreportfactorystatus-property"></a>LocationDisp.LatLongReportFactory.Status-Eigenschaft

\[Das Objektmodell der Standort-API ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen die [W3C-Geolocation-API,](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))um von einer Website aus auf den Standort zuzugreifen. Verwenden Sie die [**Windows.Devices.Geolocation-API,**](/uwp/api/Windows.Devices.Geolocation) um von einer Desktopanwendung aus auf den Standort zuzugreifen.\]

Der aktuelle Berichtsstatus.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
Status = LocationDisp.LatLongReportFactory.Status
```



## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (unsigned long).



| Status                                                                                               | Bedeutung                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Bericht wird nicht unterstützt.<br/> |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Fehler.<br/>                |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Der Zugriff wurde verweigert.<br/>        |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Initialisierung.<br/>         |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Wird ausgeführt.<br/>              |



 

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieser Eigenschaft finden Sie unter [Lauschen auf LatLong-Berichtsereignisse.](/uwp/api/Windows.Devices.Geolocation)

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|--------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ 7-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                  |



 

