---
description: Stellt einen breiten-/Längen Grad dar.
ms.assetid: efa8d805-8546-4bab-95a0-69e1edc28753
title: LocationDisp. displatlongreport-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1b9629f22aee33670463b2a0832c12d520a9b8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352363"
---
# <a name="locationdispdisplatlongreport-object"></a>LocationDisp. displatlongreport-Objekt

\[Das Location-API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen die [W3C-geolozierungs-API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)), um auf den Standort von einer Website zuzugreifen. Verwenden Sie die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API, um auf den Speicherort einer Desktop Anwendung zuzugreifen.\]

Stellt einen breiten-/Längen Grad dar.

## <a name="members"></a>Member

Das **LocationDisp. displatlongreport** -Objekt verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **LocationDisp. displatlongreport** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                                         | Zugriffstyp          | BESCHREIBUNG                                                                                                                                                                                       |
|:---------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Höhe**](locationdisp-displatlongreport-altitude.md)<br/>           | Schreibgeschützt<br/> | Aktuelle Höhe in Meter.<br/>                                                                                                                                                           |
| [**"Altitudebug Error"**](locationdisp-displatlongreport-altitudeerror.md)<br/> | Schreibgeschützt<br/> | Höhen Fehler in Meter.<br/>                                                                                                                                                             |
| [**Errorradius**](locationdisp-displatlongreport-errorradius.md)<br/>     | Schreibgeschützt<br/> | Eine Entfernung vom gemeldeten Speicherort in Meter. In Kombination mit dem gemeldeten Speicherort als Ursprung beschreibt dieser RADIUS den Kreis, in dem sich der tatsächliche Speicherort befindet.<br/> |
| [**Breiten**](locationdisp-displatlongreport-latitude.md)<br/>           | Schreibgeschützt<br/> | Aktueller Breitengrad in Grad.<br/>                                                                                                                                                          |
| [**Längengrad**](locationdisp-displatlongreport-longitude.md)<br/>         | Schreibgeschützt<br/> | Aktueller Längengrad in Grad.<br/>                                                                                                                                                         |
| [**Timestamp**](locationdisp-displatlongreport-timestamp.md)<br/>         | Schreibgeschützt<br/> | Das Datum und die Uhrzeit, zu der der Bericht generiert wurde.<br/>                                                                                                                                       |



 

## <a name="remarks"></a>Bemerkungen

Sie können dieses Objekt über die [**latlongreport**](locationdisp-latlongreportfactory-latlongreport.md) -Eigenschaft des [**latlongreportfactory**](locationdisp-latlongreportfactory.md) -Objekts abrufen. Sie können dieses Objekt über das [**newlatlongreport**](newlatlongreport.md) -Ereignis empfangen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                  |



 

