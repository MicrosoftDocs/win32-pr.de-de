---
description: Verwaltet Berichte mit breiten-und Längengrad.
ms.assetid: 66025874-32dd-4494-a9ad-12fe3afa60f9
title: LocationDisp. latlongreportfactory-Objekt
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
ms.openlocfilehash: 9fad1ca0f4605f1167f9b86b0df5bc8f20e46285
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868892"
---
# <a name="locationdisplatlongreportfactory-object"></a>LocationDisp. latlongreportfactory-Objekt

\[Das Location-API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen die [W3C-geolozierungs-API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)), um auf den Standort von einer Website zuzugreifen. Verwenden Sie die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API, um auf den Speicherort einer Desktop Anwendung zuzugreifen.\]

Verwaltet Berichte mit breiten-und Längengrad.

## <a name="members"></a>Member

Das **LocationDisp. latlongreportfactory** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **LocationDisp. latlongreportfactory** -Objekt verfügt über diese Methoden.



| Methode                                                                                       | BESCHREIBUNG                                                                                   |
|:---------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [**Listenforreports**](locationdisp-latlongreportfactory-listenforreports.md)               | Fordert Berichts Ereignisse mit breiten-/Längen Grad an.<br/>                                         |
| [**Requestberechtigungs Berechtigungen**](locationdisp-latlongreportfactory-requestpermissions.md)           | Öffnet ein System Dialogfeld zum Anfordern von Benutzerberechtigungen für Geräte, die für den Standort aktiviert sind.<br/> |
| [**Stoplisteningforreports**](/previous-versions/windows/desktop/legacy/dd317718(v=vs.85)) | Bricht Anforderungen für Berichts Ereignisse mit breiten-und Längengrad ab.<br/>                             |



 

### <a name="properties"></a>Eigenschaften

Das **LocationDisp. latlongreportfactory** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                                                | Zugriffstyp           | BESCHREIBUNG                                                                                      |
|:----------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [**Desiredaccuracy**](locationdisp-latlongreportfactory-desiredaccuracy.md)<br/> | Lesen/Schreiben<br/> | Der aktuelle Wert für die gewünschte Genauigkeit.<br/>                                                   |
| [**Latlongreport**](locationdisp-latlongreportfactory-latlongreport.md)<br/>     | Schreibgeschützt<br/>  | Der aktuelle [**LocationDisp. displatlongreport**](locationdisp-displatlongreport.md).<br/> |
| [**Report Interval**](locationdisp-latlongreportfactory-reportinterval.md)<br/>   | Lesen/Schreiben<br/> | Das aktuelle Berichts Ereignis Intervall (breiten-/Längen Grad) in Millisekunden.<br/>                 |
| [**Status**](locationdisp-latlongreportfactory-status.md)<br/>                   | Schreibgeschützt<br/>  | Der aktuelle Status des Berichts.<br/>                                                            |



 

## <a name="examples"></a>Beispiele

Der folgende Beispielcode zeigt, wie Sie dieses Objekt in HTML-Code erstellen.


```
<object id="latlongfactory" 
    classid="clsid:9DCC3CC8-8609-4863-BAD4-03601F4C65E8"
    type="application/x-oleobject">
</object>
```



Der folgende Beispielcode zeigt, wie dieses Objekt in JScript mithilfe von Windows Script Host erstellt wird.


```JScript
var latlongfactory = WScript.CreateObject("LocationDisp.LatLongReportFactory");
```



Der folgende Beispielcode zeigt, wie dieses Objekt in VBScript mithilfe von Windows Script Host erstellt wird.


```VB
Dim latlongfactory
Set latlongfactory = WScript.CreateObject("LocationDisp.LatLongReportFactory")
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LocationDisp. displatlongreport**](locationdisp-displatlongreport.md)
</dt> </dl>

 

