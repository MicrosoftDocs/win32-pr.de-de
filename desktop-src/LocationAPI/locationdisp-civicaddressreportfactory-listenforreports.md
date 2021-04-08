---
description: Fordert Ereignisse für den Bericht "Civic Address" an
ms.assetid: cb02f611-7cda-405f-aeee-833b7385a4be
title: LocationDisp. civicaddressreportfactory. listenforreports-Methode (locationapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.ListenForReports
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: 02315f8b2f7fced76c3d0d1330df246af6bad4b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960839"
---
# <a name="locationdispcivicaddressreportfactorylistenforreports-method"></a>LocationDisp. civicaddressreportfactory. listenforreports-Methode

\[Das Location-API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen die [W3C-geolozierungs-API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)), um auf den Standort von einer Website zuzugreifen. Verwenden Sie die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API, um auf den Speicherort einer Desktop Anwendung zuzugreifen.\]

Fordert Ereignisse für den Bericht "Civic Address" an

## <a name="syntax"></a>Syntax


```JScript
LocationDisp.CivicAddressReportFactory.ListenForReports(
  requestedReportInterval
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*requestedreportinterval* 
</dt> <dd> Number (**doppeltes Wort**), das die angeforderte Zeit zwischen den Ereignissen des öffentlichen Adress Berichts (in Millisekunden) darstellt. Siehe Hinweise.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der Speicherort Anbieter ist nicht erforderlich, um die gewünschte Genauigkeit anzugeben. Lesen Sie den Wert der [**reportinterval**](locationdisp-civicaddressreportfactory-reportinterval.md) -Eigenschaft, um die Einstellung für das tatsächliche Berichts Intervall zu ermitteln.

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieser Methode finden Sie unter Überwachen von [Ereignissen zu öffentlichen Adress Berichten](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                |
| Header<br/>                   | <dl> <dt>Locationapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Newcivicaddressreport-Ereignis**](newcivicaddressreport.md)
</dt> </dl>

 

