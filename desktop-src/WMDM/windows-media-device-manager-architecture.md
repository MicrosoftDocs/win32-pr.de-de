---
title: Windows Medienarchitektur Geräte-Manager Medienarchitektur
description: Windows Medienarchitektur Geräte-Manager Medienarchitektur
ms.assetid: 3c1b2da4-559d-427b-b502-5ef8dc055a8e
keywords:
- Windows Medien Geräte-Manager,Architektur
- Geräte-Manager,Architektur
- Architektur für Windows Media Geräte-Manager
- Windows Medien Geräte-Manager,Desktopanwendungen
- Geräte-Manager,Desktopanwendungen
- Windows Medien Geräte-Manager,Dienstanbieter
- Geräte-Manager,Dienstanbieter
- Windows Medien Geräte-Manager,Plug-Ins
- Geräte-Manager,Plug-Ins
- Desktopanwendungen,Windows Media Geräte-Manager Architektur
- Dienstanbieter,Windows Media Geräte-Manager Architektur
- Plug-Ins, Windows Media Geräte-Manager architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deadb7e5a85c4d7331a276a515add2ace30e566c2b683404b7b4466bf891dbbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055600"
---
# <a name="windows-media-device-manager-architecture"></a>Windows Medienarchitektur Geräte-Manager Medienarchitektur

Windows Media Geräte-Manager ermöglicht einer Anwendung oder einem Plug-In die Kommunikation mit einem Gerät. Anwendungen können Gerätemetadaten anfordern, angefügte Geräte auflisten und untersuchen sowie Objekte (Ordner, Dateien, Wiedergabelisten und so weiter) senden oder empfangen. Windows Media Geräte-Manager stellt eine einzelne API für die aufrufende Anwendung bereit, unabhängig davon, welcher Gerätetyp aufgerufen wird (MTP oder Massen-Storage-Klasse, auf Version 10 aufgebaute Dienstanbieter oder Dienstanbieter, die auf früheren Versionen von Windows Media Geräte-Manager) basiert.

Windows Media Geräte-Manager fungiert als Go-Between für die drei Hauptkomponenten des Systems: die Anwendung, die Anforderungen stellt (für Informationen, zum Lesen oder Schreiben von Daten und so weiter). ein sicherer Inhaltsanbieter, bei dem es sich um eine Komponente handelt, die die Kommunikation mit DRM-geschützten Dateien verarbeitet. und ein Dienstanbieter, der Anforderungen von der Anwendung empfängt und mit dem Gerät kommuniziert, um diese Anforderungen zu erfüllen. Sowohl die Anwendung als auch der Dienstanbieter bauen auf dem Windows Media Geräte-Manager SDK auf.

Das folgende Diagramm zeigt, wie eine Desktopanwendung mithilfe von Media Windows Media Geräte-Manager 11 mit einem Gerät kommuniziert.

![Diagramm, das eine Anwendung zeigt, die mit vier verschiedenen Gerätetypen kommuniziert.](images/wmdm-device-communication.gif)

Das obige Diagramm zeigt eine Anwendung, die mit vier verschiedenen Gerätetypen kommuniziert, die jeweils über einen eigenen Dienstanbieter kommunizieren. Jeder Dienstanbieter ist für die Kommunikation mit einem bestimmten Gerätetyp konzipiert. Dieses Diagramm zeigt die drei von Microsoft bereitgestellten Dienstanbieter (generische Klassentreiber für Massen-Storage-Klassengeräte, RAPI-Geräte und MTP-Geräte) sowie einen benutzerdefinierten Dienstanbieter für ein proprietäres Gerät, das von einem Drittanbieter erstellt wurde. Wenn ein Gerät eine Verbindung herstellt, Windows Media Geräte-Manager instanziiert eine Instanz des Dienstanbieters, der für dieses Gerät registriert ist. Die Dienstanbieter erhalten Anforderungen von der Anwendung über Windows Media Geräte-Manager-Schnittstellen, die sie implementieren, verwenden geeignete Treiber für die Kommunikation mit dem Gerät und geben entsprechende Ergebnisse zurück. Die Kommunikation zwischen dem Dienstanbieter und dem Gerät liegt außerhalb der Domäne des Windows Media Geräte-Manager.

Dienstanbieter sind für die Anwendung nicht sichtbar. Eine Anwendung sieht nur eine Liste von "Geräten", da Windows Media Geräte-Manager einen Standardsatz von Methoden und Schnittstellen für alle Geräte verfügbar macht. Wenn ein Hersteller einen benutzerdefinierten Dienstanbieter erstellt, muss er alle Windows Media Geräte-Manager-Standardmethoden verarbeiten, wenn Anwendungen das Gerät verwenden können sollen.

Dieses Diagramm zeigt auch ein SCP-Modul (Secure Content Provider). Dieses Modul ist für die Verarbeitung von drM-geschützten Inhalten (Digital Rights Management) verantwortlich. Microsoft stellt ein SCP-Modul zur Verfügung, das DRM-geschützte WMA- und WMV-Dateien verarbeiten kann. Wenn eine Anwendung oder ein Gerät andere geschützte Formate verarbeiten möchte, muss sie ein eigenes SCP-Modul bereitstellen. Weder die Anwendung noch der Dienstanbieter kümmert sich direkt um den SCP.

Sowohl die Anwendung als auch der Dienstanbieter bauen auf Windows Media Geräte-Manager auf, der Aufrufe zwischen der Anwendung und dem entsprechenden Dienstanbieter für ein Gerät weiter leitet. der Dienstanbieter ist für die direkte Kommunikation mit dem Gerät verantwortlich. Windows Media Geräte-Manager führt einige Aktionen selbst aus (z. B. das Aufzählen verbundener Geräte, das Weiterleiten von Aufrufen und das Behandeln der Komponentenüberprüfung). der Größte Teil der Arbeit wird jedoch vom Dienstanbieter erledigt, der Anforderungen von der Anwendung empfängt und mit dem Gerät kommuniziert.

Eine Anwendung, die auf Windows Media Geräte-Manager basiert, kann mit Geräten und Dienstanbietern kommunizieren, die auf früheren Versionen von Windows Media Geräte-Manager; Diese älteren Geräte werden jedoch durch Komponenten der 9er Serie (nicht angezeigt) ausgeführt und unterstützen nicht die neuesten Features, insbesondere die erweiterte Technologie für die Verwaltung digitaler Rechte.

Architektur eines Geräts

Das folgende Diagramm zeigt eine vereinfachte Hierarchie von Geräten und Speichern, wie sie von einer Anwendung mithilfe Windows Media Geräte-Manager.

![Diagramm, das Speicher auf einem Gerät zeigt.](images/wmdm-basic-device-layout.gif)

Das obige Diagramm zeigt eine vereinfachte Version eines verbundenen Flashlaufwerks, wie von einer Windows Media Geräte-Manager angezeigt. Der Flashlaufwerk verfügt über Attribute und Eigenschaften, z. B. eine Seriennummer und unterstützte Formatkonfigurationen. Ein unmittelbar untergeordnetes Gerät des Flashgeräts ist das Stammspeicherobjekt, das einen Ordner enthält, der selbst ein Bild und einen Song enthält.

Eine Anwendung listet die Liste der angeschlossenen Geräte auf, indem sie eine Enumerationsmethode aufruft, die von der [**Stammschnittstelle IWMDeviceManager verfügbar gemacht**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) wird. Geräte werden durch [**eine IWMDMDevice-Schnittstelle**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) (oder eine abgeleitete Schnittstelle) dargestellt. Diese Schnittstelle macht Methoden zum Abrufen von Gerätename, Formatfunktionen, Seriennummern und so weiter sowie  eine Methode verfügbar, die Speicher auf dem Gerät aufzählt. In Windows Media Geräte-Manager ist ein Speicher jede Art von Objekt auf dem Gerät, unabhängig davon, ob es sich um ein tatsächliches Datenblob handelt. Beispielsweise werden Audiodateien, Textdateien, Ordner, Wiedergabelisten, die als Dateien gespeichert sind, und Wiedergabelisten, die als Metadaten gespeichert sind, als Speicher betrachtet, obwohl Ordner und Metadatenelemente wahrscheinlich keine physische Datei darstellen. Der Typ (oder das Format) eines Speichers kann abgerufen werden, indem [**GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) (oder [**GetMetadata)**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata)aufgerufen und das Format des Speichers abgerufen wird.

Speicher auf einem Gerät werden hierarchisch gespeichert, und alle Geräte verfügen über einen Stammspeicher. Jeder Speicher kann null oder mehr untergeordnete Objekte enthalten, die durch Aufrufen der [**IWMDMStorage::EnumStorage-Methode**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage) dieses Speichers aufzählt.

Beachten Sie, dass jedem Speicher im Diagramm Attribute und Metadaten zugeordnet sind (nicht alle Werte werden angezeigt). Attribute sind einfache, boolesche Informationen, die häufig Verwaltungs- oder Navigationsinformationen beschreiben (z. B. "has folders" oder "can delete"), während Metadaten Zeichenfolgenwerte, Zahlen oder komplexe Informationen (z. B. Renderingfunktionen) sein können. Attribute werden durch einen relativ begrenzten Satz von Flags beschrieben, die vom SDK definiert und durch Aufrufen von [**IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) oder [**IWMDMStorage2::GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2)abgerufen werden. Metadatenwerte werden durch einen eindeutigen Namen abgerufen. Das SDK definiert eine Reihe von Metadatenwerten, die Geräte unterstützen sollten, aber Geräte können ihre eigenen [Metadatenkonst constants definieren.](metadata-constants.md) Wenn ein Gerät oder ein Dienstanbieter jedoch eine neue Metadatenkonst constant definiert, können Anwendungen diesen Wert nur anfordern oder festlegen, wenn die Anwendungsentwickler diese neue Konstante kennen. Ein Dienstanbieter muss [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3) oder höher unterstützen, um das Abrufen oder Festlegen von Metadaten zu unterstützen. Weitere Informationen finden Sie unter [Abrufen und Festlegen von Metadaten und Attributen.](getting-and-setting-metadata-and-attributes.md)

Dienstanbieter

Der Dienstanbieter fungiert als Mittelman zwischen der Anwendung und dem Gerät. Der Dienstanbieter ist für den Anwendungsentwickler nicht sichtbar, sodass ein Anwendungsentwickler nichts über die Entwicklung eines Dienstanbieters wissen muss. Es ist jedoch der Dienstanbieter, der die Kommunikation mit einem Gerät übernimmt.

Ein Dienstanbieter ist eine COM-DLL, die auf Windows Media Geräte-Manager basiert, die Anforderungen von einer Anwendung empfängt und mit dem Gerät kommuniziert, um sie durchzuführen. Die Kommunikation mit der Desktopanwendung wird durch Windows Media Geräte-Manager; Die Kommunikation mit dem Gerät wird vom Dienstanbieter kontrolliert.

Ein Dienstanbieter empfängt Anforderungen von der Anwendung zum Aufzählen von Geräteinhalten, Anforderungen für Gerätefunktionen, Anforderungen zum Lesen oder Schreiben von Daten und so weiter. Er muss den Entwurf eines Geräts so gut kennen, dass es Befehle im richtigen Format und Protokoll senden kann. Es sollte auch gerätespezifische Anforderungen ausblenden können, z. B. eine erforderliche Dateierweiterung für Wiedergabelisten, damit Anwendungen diese Anforderungen nicht kennen müssen, um das Gerät zu verwenden.

Microsoft stellt eine Reihe von Dienstanbietern für Standardgerätetypen zur Verfügung, darunter generische MTP-Geräte, Massengeräte Storage-Klasse und RAPI-Geräte. Der einzige Grund, warum ein Geräte-Designer einen benutzerdefinierten Dienstanbieter erstellen muss, ist, wenn ein Gerät über bestimmte oder ungewöhnliche Datenspeicheranforderungen verfügt, die von den Standarddienstanbietern nicht verarbeitet werden, z. B. wenn Dateien an bestimmten Speicherorten gespeichert werden müssen und das Gerätebetriebssystem dies nicht automatisch verarbeitet.

Wenn ein Gerät mit dem Computer verbunden ist, erstellt das Betriebssystem eine Instanz des entsprechenden Dienstanbieters für jede Windows Media Geräte-Manager Anwendung. Wenn eine zweite Windows Media Geräte-Manager startet, wird eine zweite Instanz des Dienstanbieters geladen. Jeder Dienstanbieter kann jedoch mehrere Geräte verarbeiten. Dies wird im folgenden Diagramm veranschaulicht.

![Diagramm, das zwei MTP-Geräte zeigt, die mit zwei Anwendungen kommunizieren.](images/wmdm-sp-to-device.gif)

Das obige Diagramm zeigt zwei verschiedene Anwendungen, die mit zwei MTP-Geräten kommunizieren. Die Geräte verwenden dieselbe Dienstanbieterklasse, aber jede Anwendung verfügt über eine eigene Instanz desselben Dienstanbieters. Jede Dienstanbieterinstanz kommuniziert mit Geräten. Die verschiedenen Instanzen des Dienstanbieters kennen sich nicht.

Viele Anwendungsmethoden verfügen über eine entsprechend benannte Dienstanbietermethode. Wenn die Anwendung eine -Methode aufruft, leitet Windows Media Geräte-Manager den Aufruf an die entsprechende Methode für den Dienstanbieter weiter (obwohl möglicherweise zuerst einige zusätzliche interne Aktionen durchgeführt werden). Wenn die Anwendung beispielsweise [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty)aufruft, leitet Windows Media Geräte-Manager diesen Aufruf an die Implementierung von [**IMDSPDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice3-getproperty)des Dienstanbieters weiter. (Die meisten Anwendungsschnittstellen beginnen mit IWMDM, und die entsprechende Dienstanbieterschnittstelle beginnt mit IMDSP.) Es wird erwartet, dass der Dienstanbieter diesen Methodenaufruf verarbeitet und ein entsprechendes Ergebnis zurück gibt.

Eine Anwendung untersucht oder kommuniziert nie direkt mit einem Gerät (es sei denn, sie ruft [**IWMDMDevice3::D eviceIoControl**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol) oder [**IWMDMStorage::SendOpaqueCommand**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-sendopaquecommand)auf). Die Anwendung kommuniziert mit dem Dienstanbieter, der ein Gerät auf die logischste und einfachste Weise darstellen muss. Wenn die Anwendung Informationen über das Gerät anfragt oder Objekte auf dem Gerät aufzählt, fragt der Dienstanbieter das Gerät auf geeignete Weise ab und erhält und gibt die entsprechenden Informationen zurück. Es kann die Dateiorganisation auf dem Gerät anders verfügbar machen als die physische Speicherung auf dem Gerät, falls dies angemessen ist. Das Gerät sollte jedoch auf konsistente, logische Weise verfügbar sein, damit die Anwendung die benötigten Daten finden und die von ihr übermittelten Befehle verarbeiten kann. Ein guter Dienstanbieter blendet gerätespezifische Ähnlichkeiten aus. Wenn das Gerät beispielsweise physisch eine Wiedergabeliste als Datei mit einer benutzerdefinierten Dateierweiterung speichert, sollte der Dienstanbieter diese Erweiterung automatisch hinzufügen, wenn die Anwendung eine Wiedergabeliste auf dem Gerät erstellt. Es sollte nicht erwartet werden, dass die Anwendung beim Erstellen eines Wiedergabelistenobjekts die richtige Erweiterung kennt.

Dienstanbieter werden innerhalb des Prozesses der aufrufenden Anwendung ausgeführt. Die einzige Ausnahme ist der MTP-Dienstanbieter, der in einem eigenen Prozess ausgeführt wird. Aus diesem Grund besteht ein gewisses Risiko, dass ein blockierter Dienstanbieter die aufrufende Anwendung blockiert. Daher sollten Dienstanbieter so konzipiert sein, dass sie robust sind und Blockierung verhindern, und Anwendungen sollten so entworfen werden, dass sie nicht mehr reagieren, wenn ein bestimmter Methodenaufruf nicht schnell zurückkehrt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erste Schritte**](getting-started.md)
</dt> </dl>

 

 




