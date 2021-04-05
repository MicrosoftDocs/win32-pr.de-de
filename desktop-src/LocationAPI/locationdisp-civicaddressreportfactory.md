---
description: Verwaltet die Berichte zu öffentlichen Adressen.
ms.assetid: 46c2d001-409a-4a0a-9006-1c2c9d327c13
title: LocationDisp. civicaddressreportfactory-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory
api_type:
- COM
api_location: ''
ms.openlocfilehash: 451bb21822d1b56e4c7a45f1587df04761b67690
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758280"
---
# <a name="locationdispcivicaddressreportfactory-object"></a>LocationDisp. civicaddressreportfactory-Objekt

\[Das Location-API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen die [W3C-geolozierungs-API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)), um auf den Standort von einer Website zuzugreifen. Verwenden Sie die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API, um auf den Speicherort einer Desktop Anwendung zuzugreifen.\]

Verwaltet die Berichte zu öffentlichen Adressen.

## <a name="members"></a>Member

Das **LocationDisp. civicaddressreportfactory** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **LocationDisp. civicaddressreportfactory** -Objekt verfügt über diese Methoden.



| Methode                                                                                            | BESCHREIBUNG                                                                                   |
|:--------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [**Listenforreports**](locationdisp-civicaddressreportfactory-listenforreports.md)               | Fordert Ereignisse für den Bericht "Civic Address" an<br/>                                              |
| [**Requestberechtigungs Berechtigungen**](locationdisp-civicaddressreportfactory-requestpermissions.md)           | Öffnet ein System Dialogfeld zum Anfordern von Benutzerberechtigungen für Geräte, die für den Standort aktiviert sind.<br/> |
| [**Stoplisteningforreports**](locationdisp-civicaddressreportfactory-stoplisteningforreports.md) | Bricht die Ereignis Anforderungen für den Bericht "Civic Address" ab<br/>                                       |



 

### <a name="properties"></a>Eigenschaften

Das **LocationDisp. civicaddressreportfactory** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                                                        | Zugriffstyp           | BESCHREIBUNG                                                                                                |
|:------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------|
| [**Civicaddressreport**](locationdisp-dispcivicaddressreport-civicaddressreport.md)<br/> | Schreibgeschützt<br/>  | Der aktuelle [**LocationDisp. dispcivicaddressreport**](locationdisp-dispcivicaddressreport.md).<br/> |
| [**Desiredaccuracy**](locationdisp-civicaddressreportfactory-desiredaccuracy.md)<br/>    | Lesen/Schreiben<br/> | Die aktuelle Einstellung für die gewünschte Genauigkeit.<br/>                                                           |
| [**Report Interval**](locationdisp-civicaddressreportfactory-reportinterval.md)<br/>      | Lesen/Schreiben<br/> | Das aktuelle Ereignis Intervall für das Berichts Ereignis in Millisekunden.<br/>                                |
| [**Status**](locationdisp-civicaddressreportfactory-status.md)<br/>                      | Schreibgeschützt<br/>  | Der aktuelle Status des Berichts.<br/>                                                                      |



 

## <a name="examples"></a>Beispiele

Der folgende Beispielcode zeigt, wie Sie dieses Objekt in HTML-Code erstellen.


```Text
<object id="civicfactory" 
    classid="clsid:2A11F42C-3E81-4ad4-9CBE-45579D89671A"
    type="application/x-oleobject">
</object>
```



Der folgende Beispielcode zeigt, wie dieses Objekt in JScript mithilfe von Windows Script Host erstellt wird.


```JScript
var civicfactory = WScript.CreateObject("LocationDisp.CivicAddressReportFactory");
```



Der folgende Beispielcode zeigt, wie dieses Objekt in VBScript mithilfe von Windows Script Host erstellt wird.


```VB
Dim civicfactory
Set civicfactory = WScript.CreateObject("LocationDisp.CivicAddressReportFactory")
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LocationDisp. civicaddressreport**](locationdisp-dispcivicaddressreport.md)
</dt> </dl>

 

