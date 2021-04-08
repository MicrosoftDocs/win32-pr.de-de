---
description: Fordert Berichts Ereignisse mit breiten-/Längen Grad an.
ms.assetid: c26a388b-e042-43da-a220-e3ecfcbd03a8
title: LocationDisp. latlongreportfactory. listenforreports-Methode (locationapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.ListenForReports
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: 7e822595339fa499aaf469336ca3580acb2815bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757338"
---
# <a name="locationdisplatlongreportfactorylistenforreports-method"></a>LocationDisp. latlongreportfactory. listenforreports-Methode

\[Das Location-API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen die [W3C-geolozierungs-API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)), um auf den Standort von einer Website zuzugreifen. Verwenden Sie die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API, um auf den Speicherort einer Desktop Anwendung zuzugreifen.\]

Fordert Berichts Ereignisse mit breiten-/Längen Grad an.

## <a name="syntax"></a>Syntax


```JScript
LocationDisp.LatLongReportFactory.ListenForReports(
  requestedReportInterval
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*requestedreportinterval* 
</dt> <dd> Number (**doppeltes Wort**), das die angeforderte Zeit zwischen Breiten-/Längengrad-Berichts Ereignissen in Millisekunden darstellt. Siehe Hinweise.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Es ist nicht erforderlich, dass der standortanbieter Berichte in dem von Ihnen angeforderten Intervall bereitstellt. Lesen Sie den Wert der [**reportinterval**](locationdisp-latlongreportfactory-reportinterval.md) -Eigenschaft, um die Einstellung für das tatsächliche Berichts Intervall zu ermitteln.

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieser Methode finden Sie unter [lauschen auf latlong-Bericht Ereignisse](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                |
| Header<br/>                   | <dl> <dt>Locationapi. h</dt> </dl> |



 

