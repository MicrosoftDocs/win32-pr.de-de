---
description: Verwaltet Breiten-/Längengradberichte.
ms.assetid: 66025874-32dd-4494-a9ad-12fe3afa60f9
title: LocationDisp.LatLongReportFactory-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory
api_type:
- COM
api_location: ''
ms.openlocfilehash: 18f8fddd675cc25a78deaf9acf46c41c3d002a4ba394288116020c0d5241d903
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117809547"
---
# <a name="locationdisplatlongreportfactory-object"></a>LocationDisp.LatLongReportFactory-Objekt

\[Das Location API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen die [W3C-Geolocation-API,](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))um von einer Website aus auf den Standort zuzugreifen. Um von einer Desktopanwendung aus auf den Speicherort zuzugreifen, verwenden Sie die [**Windows. Devices.Geolocation-API.**](/uwp/api/Windows.Devices.Geolocation)\]

Verwaltet Breiten-/Längengradberichte.

## <a name="members"></a>Member

Das **LocationDisp.LatLongReportFactory-Objekt** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **LocationDisp.LatLongReportFactory-Objekt** verfügt über diese Methoden.



| Methode                                                                                       | Beschreibung                                                                                   |
|:---------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [**ListenForReports**](locationdisp-latlongreportfactory-listenforreports.md)               | Fordert Breiten-/Längengradberichtsereignisse an.<br/>                                         |
| [**RequestPermissions**](locationdisp-latlongreportfactory-requestpermissions.md)           | Öffnet ein Systemdialogfeld, in dem Benutzerberechtigungen für standortfähige Geräte angefordert werden.<br/> |
| [**StopListeningForReports**](/previous-versions/windows/desktop/legacy/dd317718(v=vs.85)) | Bricht Anforderungen für Breiten-/Längengradberichtsereignisse ab.<br/>                             |



 

### <a name="properties"></a>Eigenschaften

Das **LocationDisp.LatLongReportFactory-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                | Zugriffstyp           | Beschreibung                                                                                      |
|:----------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [**DesiredAccuracy**](locationdisp-latlongreportfactory-desiredaccuracy.md)<br/> | Lesen/Schreiben<br/> | Der aktuelle Wert für die gewünschte Genauigkeit.<br/>                                                   |
| [**LatLongReport**](locationdisp-latlongreportfactory-latlongreport.md)<br/>     | Schreibgeschützt<br/>  | Der aktuelle [**LocationDisp.DispLatLongReport**](locationdisp-displatlongreport.md).<br/> |
| [**ReportInterval**](locationdisp-latlongreportfactory-reportinterval.md)<br/>   | Lesen/Schreiben<br/> | Das aktuelle Breiten-/Längengrad-Berichtsereignisintervall in Millisekunden.<br/>                 |
| [**Status**](locationdisp-latlongreportfactory-status.md)<br/>                   | Schreibgeschützt<br/>  | Der aktuelle Berichtsstatus.<br/>                                                            |



 

## <a name="examples"></a>Beispiele

Der folgende Beispielcode zeigt, wie dieses Objekt im HTML-Code erstellt wird.


```
<object id="latlongfactory" 
    classid="clsid:9DCC3CC8-8609-4863-BAD4-03601F4C65E8"
    type="application/x-oleobject">
</object>
```



Der folgende Beispielcode zeigt, wie Sie dieses Objekt in JScript mithilfe Windows Skripthosts erstellen.


```JScript
var latlongfactory = WScript.CreateObject("LocationDisp.LatLongReportFactory");
```



Der folgende Beispielcode zeigt, wie dieses Objekt in VBScript mithilfe Windows Skripthosts erstellt wird.


```VB
Dim latlongfactory
Set latlongfactory = WScript.CreateObject("LocationDisp.LatLongReportFactory")
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LocationDisp.DispLatLongReport**](locationdisp-displatlongreport.md)
</dt> </dl>

 

