---
title: Präsentation
description: Präsentation ist der letzte Schritt im UPnP-Prozess.
ms.assetid: e8d20ae6-2dd8-4de2-b07b-6cf4e725735e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 195399316882de71c148f2369dd2978c4cfbd728
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855959"
---
# <a name="presentation"></a>Präsentation

Präsentation ist der letzte Schritt im UPnP-Prozess. Wenn ein Gerät über eine URL zur Darstellung verfügt, kann ein Kontrollpunkt eine Seite aus dieser URL abrufen und die Seite in einen Browser laden. Abhängig von den Funktionen der Präsentationsseite und des Geräts kann der Steuerungspunkt das Gerät steuern und den Status des Geräts anzeigen.

Der Ressourcen Pfad, der während der Registrierung an [**iupnpregistrinar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) übermittelt wird, ist der Ort, an dem alle für die Darstellung des Geräts relevanten Dateien gefunden werden. Geräte Entwickler können für jedes eingebettete Gerät separate Seiten bereitstellen. Die Präsentations-URL in der Geräte Beschreibungs Vorlage kann entweder ein absolute URL oder ein relative URL sein. Bei relativen URLs, die relativ zum Ressourcen Pfad sind, sollte die Vorlage für die Geräte Beschreibung einen Dateinamen enthalten. **Iupnpregistrinar** konvertiert diese in eine URL mit dem tatsächlichen Speicherort. Bei absoluten URLs wird der Speicherort nicht geändert.

Zur Unterstützung von Client seitigen Skripts auf einer Präsentationsseite werden in der Regel zusätzliche Informationen in Form einer "Abfrage Zeichenfolge" an die URL angehängt. Die zusätzlichen Informationen, die angefügt werden, sind die URL zum Dokument mit der Geräte Beschreibung und der udn des Geräts oder eingebetteten Geräts. Die URL für die Geräte Beschreibung kann verwendet werden, um ein Beschreibungs Dokument in das Skript zu laden und das Gerät dann über seine Dienste zu steuern. Der udn wird verwendet, um ein eingebettetes Gerät aus dem Stamm Gerät auszuwählen.

Das Format der geänderten Präsentations-URL lautet: die tatsächliche Präsentations-URL, ein Fragezeichen ("?"), die URL für die Geräte Beschreibung, ein Pluszeichen ("+"), das udn des Geräts. Das Fragezeichen gibt den Anfang der Abfrage Zeichenfolge an.

Wenn die Präsentations-URL in der Geräte Beschreibungs Vorlage eine absolute URL ist, die bereits ein Fragezeichen ("?") enthielt, werden die zusätzlichen Informationen nicht der Präsentations-URL hinzugefügt.



| BESCHREIBUNG                        | URL                                                                                                                                               |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| In der Vorlage Geräte Beschreibung | **presentationurl** MyDevice.html **/presentationURL**                                                                                              |
| Vom Geräte Host generiert       | **presentationurl** https://machinename/deviceID/MyDevice.html/?https://machine/upnphost/udhisapi.dll?content=uuid:487394 ... + Udn **/presentationURL** |



 

Ein Client seitiges Skript muss möglicherweise die URL der Geräte Beschreibung aus der Präsentations-URL extrahieren, um das [**iupnpdescriptiondocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) -Objekt zu laden. Dies erfolgt durch das übernehmen der Abfrage Zeichenfolge und das Beenden des Plus Zeichens ("+").


```VB
Dim QueryString
QueryString = window.location.search
Dim DescURLString
DescURLString = Trim(Mid(QueryString,2,Instr(QueryString,"+")-2))& vbCrLf

    Dim LightDesc
    Set LightDesc = CreateObject("UPnP.DescriptionDocument.1")
    LightDesc.Load(DescURLString)
```



Im Fall einer Präsentationsseite für ein eingebettetes Gerät sind einige zusätzliche Arbeitsschritte erforderlich. Nach dem Laden von [**upnpdescriptiondocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument)muss das Skript die Sammlung eingebetteter Geräte abrufen und dann das Gerät auswählen, das mit dem udn in der Abfrage Zeichenfolge übereinstimmt. Das folgende Skript zeigt, wie Sie das eingebettete Gerät für die aktuelle Präsentationsseite auswählen. Es wird davon ausgegangen, dass lightdesc bereits geladen wurde.


```VB
Dim LightDevice
Set LightDevice = LightDesc.RootDevice

Dim EmbeddedDevices 
set EmbeddedDevices = LightDevice.Children

Dim DeviceUdnString
DeviceUdnString = Trim(Mid(QueryString,Instr(QueryString,"+")+1,Len(QueryString)))

Dim Item
set Item = EmbeddedDevices.Item(DeviceUdnString)
```



 

 




