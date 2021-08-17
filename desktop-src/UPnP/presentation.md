---
title: Präsentation
description: Die Präsentation ist der letzte Schritt im UPnP-Prozess.
ms.assetid: e8d20ae6-2dd8-4de2-b07b-6cf4e725735e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c92f8457a881dc0414713e996d230261330c10911f2aea285a2e365ad0d59320
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137193"
---
# <a name="presentation"></a>Präsentation

Die Präsentation ist der letzte Schritt im UPnP-Prozess. Wenn ein Gerät über eine URL für die Präsentation verfügt, kann ein Kontrollpunkt eine Seite aus dieser URL abrufen und die Seite in einen Browser laden. Abhängig von den Funktionen der Präsentationsseite und des Geräts kann der Steuerungspunkt das Gerät steuern und den Status des Geräts anzeigen.

Im Ressourcenpfad, der während der Registrierung [**an IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) übergeben wird, befinden sich alle Dateien, die für die Darstellung des Geräts relevant sind. Geräteentwickler können separate Seiten für jedes eingebettete Gerät bereitstellen. Die Präsentations-URL in der Gerätebeschreibungsvorlage kann entweder ein absolute URL oder ein relative URL. Für relative URLs, die relativ zum Ressourcenpfad sind, sollte die Gerätebeschreibungsvorlage einen Dateinamen enthalten. **IUPnPRegistrar** konvertiert dies in eine URL mit dem tatsächlichen Speicherort. Bei absoluten URLs wird der Speicherort nicht geändert.

Zur Unterstützung clientseitiger Skripts auf einer Präsentationsseite werden normalerweise zusätzliche Informationen in Form einer "Abfragezeichenfolge" an die URL angefügt. Die zusätzlichen Informationen, die angefügt werden, sind die URL zum Dokument mit der Gerätebeschreibung und die UDN des Geräts oder eingebetteten Geräts. Die URL der Gerätebeschreibung kann verwendet werden, um ein Beschreibungsdokument in das Skript zu laden und dann das Gerät über seine Dienste zu steuern. Der UDN wird verwendet, um ein eingebettetes Gerät aus dem Stammgerät auszuwählen.

Das Format der geänderten Präsentations-URL lautet: die tatsächliche Präsentations-URL, ein Fragezeichen ("?"), die URL der Gerätebeschreibung, ein Pluszeichen ("+"), die Geräte-UDN. Das Fragezeichen gibt den Anfang der Abfragezeichenfolge an.

Wenn die Präsentations-URL in der Gerätebeschreibungsvorlage ein absolute URL und bereits ein Fragezeichen ("?") enthielt, werden die zusätzlichen Informationen nicht zur Präsentations-URL hinzugefügt.



| Beschreibung                        | URL                                                                                                                                               |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| In der Gerätebeschreibungsvorlage | **presentationURL** MyDevice.html **/presentationURL**                                                                                              |
| Vom Gerätehost generiert       | **presentationURL** https://machinename/deviceID/MyDevice.html/?https://machine/upnphost/udhisapi.dll?content=uuid:487394 ... + UDN **/presentationURL** |



 

Ein clientseitiges Skript muss möglicherweise die URL der Gerätebeschreibung aus der Präsentations-URL extrahieren, um das [**IUPnPDescriptionDocument-Objekt zu**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) laden. Dazu wird die Abfragezeichenfolge verwendet und am Pluszeichen ("+") beendet.


```VB
Dim QueryString
QueryString = window.location.search
Dim DescURLString
DescURLString = Trim(Mid(QueryString,2,Instr(QueryString,"+")-2))& vbCrLf

    Dim LightDesc
    Set LightDesc = CreateObject("UPnP.DescriptionDocument.1")
    LightDesc.Load(DescURLString)
```



Im Fall einer Präsentationsseite für ein eingebettetes Gerät ist einige zusätzliche Arbeit erforderlich. Nach dem Laden [**von UPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument)muss das Skript die Sammlung eingebetteter Geräte abrufen und dann das Gerät auswählen, das mit dem UDN in der Abfragezeichenfolge übereinstimmen soll. Das folgende Skript zeigt, wie Sie das eingebettete Gerät für die aktuelle Präsentationsseite auswählen. Es wird davon ausgegangen, dass LightDesc bereits geladen ist.


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



 

 




