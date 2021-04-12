---
title: Architektur von Windows Media Device Manager
description: Architektur von Windows Media Device Manager
ms.assetid: 3c1b2da4-559d-427b-b502-5ef8dc055a8e
keywords:
- Windows Media-Device Manager, Architektur
- Device Manager, Architektur
- Architektur für Windows Media Device Manager
- Windows Media Device Manager, Desktop Anwendungen
- Device Manager, Desktop Anwendungen
- Windows Media Device Manager, Dienstanbieter
- Device Manager, Dienstanbieter
- Windows Media Device Manager, Plug-ins
- Device Manager, Plug-ins
- Desktop Anwendungen, Windows Media Device Manager-Architektur
- Dienstanbieter, Windows Media Device Manager-Architektur
- Plug-ins, Windows Media Device Manager-Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fda87e4ed4bce2c82bbb9c0863c119851965940
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206488"
---
# <a name="windows-media-device-manager-architecture"></a>Architektur von Windows Media Device Manager

Mithilfe von Windows Media Device Manager kann eine Anwendung oder ein Plug-in mit einem Gerät kommunizieren. Anwendungen können Geräte Metadaten anfordern, angeschlossene Geräte aufzählen und durchsuchen und Objekte (Ordner, Dateien, Wiedergabelisten usw.) senden oder empfangen. Windows Media Device Manager stellt eine einzelne API für die aufrufende Anwendung bereit, unabhängig davon, welche Art von Gerät aufgerufen wird (MTP-oder Massenspeicher Klasse, auf Version 10 basierende Dienstanbieter oder Dienstanbieter, die auf früheren Versionen von Windows Media Device Manager basieren).

Windows Media Device Manager fungiert als Ganzes für die drei Hauptkomponenten des Systems: die Anwendung, die Anforderungen (Informationen zum Lesen und Schreiben von Daten usw.) ausführt. ein sicherer Inhaltsanbieter, bei dem es sich um eine Komponente handelt, die die Kommunikation mit DRM-geschützten Dateien behandelt. und ein Dienstanbieter, der Anforderungen von der Anwendung empfängt und mit dem Gerät kommuniziert, um diese Anforderungen auszuführen. Die Anwendung und der Dienstanbieter werden auf dem Windows Media Device Manager SDK erstellt.

Das folgende Diagramm zeigt, wie eine Desktop Anwendung mithilfe von Windows Media Device Manager 11 mit einem Gerät kommuniziert.

![Diagramm, das zeigt, wie eine Anwendung mit vier verschiedenen Arten von Geräten kommuniziert.](images/wmdm-device-communication.gif)

Das obige Diagramm zeigt eine Anwendung, die mit vier verschiedenen Gerätetypen kommuniziert, die jeweils über einen eigenen Dienstanbieter verfügen. Jeder Dienstanbieter ist für die Kommunikation mit einem bestimmten Gerätetyp konzipiert. Dieses Diagramm zeigt die drei von Microsoft bereitgestellten Dienstanbieter (generische Klassen Treiber für Massenspeicher Klassen-Geräte, RAPI-Geräte und MTP-Geräte) sowie einen benutzerdefinierten Dienstanbieter für ein proprietäres Gerät, das von einem Drittanbieter erstellt wurde. Wenn ein Gerät eine Verbindung herstellt, instanziiert Windows Media Device Manager eine Instanz des Dienstanbieters, der für dieses Gerät registriert ist. Die Dienstanbieter erhalten Anforderungen von der Anwendung über Windows Media Device Manager Schnittstellen, die Sie implementieren, verwenden Sie die geeigneten Treiber für die Kommunikation mit dem Gerät, und geben Sie entsprechende Ergebnisse zurück. Die Kommunikation zwischen dem Dienstanbieter und dem Gerät erfolgt außerhalb der Domäne von Windows Media Device Manager.

Dienstanbieter sind für die Anwendung nicht sichtbar. in einer Anwendung wird nur eine Liste der Geräte angezeigt, da Windows Media Device Manager einen Standardsatz von Methoden und Schnittstellen für alle Geräte verfügbar macht. Wenn ein Hersteller einen benutzerdefinierten Dienstanbieter erstellt, muss er alle standardmäßigen Windows Media Device Manager-Methoden verarbeiten, wenn Anwendungen in der Lage sein sollen, das Gerät zu verwenden.

Dieses Diagramm zeigt auch ein Modul des Typs Secure Content Provider (SCP). Dieses Modul ist für die Behandlung von Digital Rights Management geschützten Inhalten (DRM) verantwortlich. Microsoft stellt ein SCP-Modul bereit, das von DRM geschützte WMA-und WMV-Dateien verarbeiten kann. Wenn eine Anwendung oder ein Gerät andere geschützte Formate verarbeiten soll, muss es ein eigenes SCP-Modul bereitstellen. Weder die Anwendung noch der Dienstanbieter verarbeitet direkt den SCP.

Sowohl die Anwendung als auch der Dienstanbieter werden auf Windows Media Device Manager erstellt, die Aufrufe zwischen der Anwendung und dem entsprechenden Dienstanbieter für ein Gerät weiterleitet. der Dienstanbieter ist für die direkte Kommunikation mit dem Gerät verantwortlich. Windows Media Device Manager führt bestimmte Aktionen aus (z. b. das Auflisten verbundener Geräte, Routing Aufrufe und die Verarbeitung der Komponenten Überprüfung). der größte Teil der Arbeit erfolgt jedoch durch den Dienstanbieter, der Anforderungen von der Anwendung empfängt und mit dem Gerät kommuniziert.

Eine auf Windows Media Device Manager basierende Anwendung kann mit Geräten und Dienstanbietern kommunizieren, die auf früheren Versionen von Windows Media Device Manager basieren; diese älteren Geräte werden jedoch über 9-Serie-Komponenten ausgeführt (nicht angezeigt) und unterstützen nicht die neuesten Features, insbesondere die erweiterte Digital Rights Management Technologie.

Architektur eines Geräts

Das folgende Diagramm zeigt eine vereinfachte Hierarchie von Geräten und Speicher, die von einer Anwendung verwendet wird, die Windows Media Device Manager verwendet.

![das Diagramm zeigt die Speicher auf einem Gerät.](images/wmdm-basic-device-layout.gif)

Das obige Diagramm zeigt eine vereinfachte Version eines verbundenen Flash Laufwerks, wie von einer Windows Media Device Manager-Anwendung dargestellt. Das Flash Laufwerk verfügt über Attribute und Eigenschaften, z. b. eine Seriennummer und unterstützte Format Konfigurationen. Ein unmittelbar untergeordnetes Element des Flash-Geräts ist das Stamm Speicher Objekt, das einen Ordner enthält, der selbst ein Bild und einen Song enthält.

Eine Anwendung listet die Liste der angefügten Geräte durch Aufrufen einer Enumerationsmethode auf, die von der Stamm- [**iwmdevicemanager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) -Schnittstelle verfügbar gemacht wird. Geräte werden durch eine [**iwmdmdevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) (oder eine abgeleitete) Schnittstelle dargestellt. Diese Schnittstelle stellt Methoden zum Abrufen des Geräte namens, der Formatierungsfunktionen, der Seriennummer usw. und einer Methode zur Verfügung, die auf dem Gerät *Speicher* auflistet. In Windows Media Device Manager ist ein Speicher eine beliebige Art von Objekt auf dem Gerät, unabhängig davon, ob es sich um ein tatsächliches BLOB von Daten handelt. Beispiel: Audiodateien, Textdateien, Ordner, Wiedergabelisten, die als Dateien gespeichert sind, und als Metadaten gespeicherte Wiedergabelisten gelten als Speicher, auch wenn Ordner und Metadatenelemente wahrscheinlich keine physische Datei darstellen. Der Typ (oder das Format) eines Speichers kann abgerufen werden, indem [**GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) aufgerufen wird (oder [**GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata), um das Format des Speichers anzufordern).

Storages auf einem Gerät werden hierarchisch gespeichert, und alle Geräte verfügen über einen Stamm Speicher. Jeder Speicher kann NULL oder mehr untergeordnete Objekte enthalten, die durch den Aufruf der [**iwmdmstorage:: enumstorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage) -Methode des Speichers aufgezählt werden.

Beachten Sie, dass jedem Speicher im Diagramm Attribute und Metadaten zugeordnet sind (es werden nicht alle Werte angezeigt). Attribute sind einfache, boolesche Informationen, die häufig Verwaltungs-oder Navigationsinformationen beschreiben (z. b. "hat Ordner&quot; oder &quot;kann gelöscht werden"), wohingegen Metadaten Zeichen folgen Werte, Zahlen oder komplexe Informationen sein können (z. b. Renderingfunktionen). Attribute werden durch einen relativ begrenzten Satz von Flags beschrieben, die vom SDK definiert und durch Aufrufen von [**iwmdmstorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) oder [**IWMDMStorage2:: GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2)abgerufen werden. Metadatenwerte werden durch einen eindeutigen Namen abgerufen. Das SDK definiert eine Reihe von Metadatenwerten, die von Geräten unterstützt werden sollen. Geräte können jedoch eigene [metadatenkonstanten](metadata-constants.md)definieren. Wenn ein Gerät oder ein Dienstanbieter jedoch eine neue metadatenkonstante definiert, können Anwendungen diesen Wert nur dann anfordern oder festlegen, wenn die Anwendungsentwickler diese neue Konstante kennen. Ein Dienstanbieter muss [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3) oder höher unterstützen, um das Abrufen oder Festlegen von Metadaten zu unterstützen. Weitere Informationen finden Sie unter [erhalten und Festlegen von Metadaten und Attributen](getting-and-setting-metadata-and-attributes.md).

Dienstanbieter

Der Dienstanbieter fungiert als middlemann zwischen der Anwendung und dem Gerät. Der Dienstanbieter ist für den Anwendungsentwickler unsichtbar, sodass ein Anwendungsentwickler nichts über das Entwickeln eines Dienstanbieters wissen muss. Es ist jedoch der Dienstanbieter, der die Kommunikation mit einem Gerät durchführt.

Ein Dienstanbieter ist eine com-dll, die auf Windows Media Device Manager basiert und Anforderungen von einer Anwendung empfängt und mit dem Gerät kommuniziert, um Sie auszuführen. Die Kommunikation mit der Desktop Anwendung wird von Windows Media Device Manager vermittelt; die Kommunikation mit dem Gerät unterliegt der Kontrolle des Dienstanbieters.

Ein Dienstanbieter empfängt Anforderungen von der Anwendung zum Aufzählen von Geräte Inhalten, Anforderungen an Gerätefunktionen, Anforderungen zum Lesen und Schreiben von Daten usw. Er muss wissen, dass ein Gerät gut genug ist, damit Befehle im richtigen Format und Protokoll gesendet werden können. Er sollte auch gerätespezifische Anforderungen ausblenden können, wie z. b. eine erforderliche Dateierweiterung für Wiedergabelisten, damit Anwendungen diese Anforderungen nicht kennen müssen, damit das Gerät verwendet werden kann.

Microsoft stellt eine Reihe von Dienstanbietern für Standardgeräte Typen bereit, einschließlich generischer MTP-Geräte, Massenspeicher Klassen-Geräte und RAPI-Geräten. Der einzige Grund, warum ein Geräte-Designer einen benutzerdefinierten Dienstanbieter erstellen muss, ist, wenn ein Gerät bestimmte oder ungewöhnliche Datenspeicher Anforderungen hat, die von den Standard Dienstanbietern nicht behandelt werden – z. b. wenn Dateien an bestimmten Speicherorten gespeichert werden müssen und das Betriebssystem das Betriebssystem nicht automatisch verarbeitet.

Wenn ein Gerät mit dem Computer verbunden ist, erstellt das Betriebssystem eine Instanz des entsprechenden Dienstanbieters für jede Windows Media Device Manager-Anwendung. Wenn eine zweite Windows Media Device Manager-Anwendung gestartet wird, wird eine zweite Instanz des Dienstanbieters geladen. Jeder Dienstanbieter kann jedoch mehrere Geräte verarbeiten. Dies wird im folgenden Diagramm veranschaulicht.

![das Diagramm zeigt zwei MTP-Geräte, die mit zwei Anwendungen kommunizieren.](images/wmdm-sp-to-device.gif)

Das obige Diagramm zeigt zwei verschiedene Anwendungen, die mit zwei MTP-Geräten kommunizieren. Die Geräte verwenden die gleiche Dienstanbieter Klasse, aber jede Anwendung verfügt über eine eigene Instanz desselben Dienstanbieters. Jede Instanz des Dienstanbieters kommuniziert mit Geräten. Die verschiedenen Instanzen des Dienstanbieters sind einander nicht bewusst.

Viele Anwendungsmethoden verfügen über eine entsprechend benannte Dienstanbieter Methode. Wenn die Anwendung eine-Methode aufruft, leitet Windows Media Device Manager den Aufruf an die entsprechende-Methode für den Dienstanbieter weiter. (allerdings werden möglicherweise einige zusätzliche interne Aktionen zuerst durchgeführt.) Wenn die Anwendung z. b. [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty)aufruft, leitet Windows Media Device Manager diesen Aufruf an die Implementierung von [**IMDSPDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice3-getproperty)des Dienstanbieters weiter. (Die meisten Anwendungsschnittstellen beginnen mit iwmdm, und die zugehörige Dienstanbieter Schnittstelle beginnt mit imdsp). Der Dienstanbieter wird erwartet, dass dieser Methodenaufrufe behandelt und ein entsprechendes Ergebnis zurückgegeben wird.

Eine Anwendung untersucht oder kommuniziert nicht direkt mit einem Gerät (es sei denn, es wird [**IWMDMDevice3 aufgerufen::D eviceiocontrol**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol) oder [**iwmdmstorage:: sendopaquecommand**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-sendopaquecommand)); die Anwendung kommuniziert mit dem Dienstanbieter, der ein Gerät auf logischere und einfache Weise darstellen muss. Wenn die Anwendung Informationen über das Gerät anfordert oder Objekte auf dem Gerät auflistet, fragt der Dienstanbieter das Gerät entsprechend ab und ruft die entsprechenden Informationen ab und gibt diese zurück. Wenn dies der Fall ist, kann die Dateiorganisation auf dem Gerät anders verfügbar sein als auf dem Gerät. Allerdings wird das Gerät verfügbar gemacht. es sollte einheitlich und logisch sein, damit die Anwendung die Anforderungen ermitteln und die Befehle verarbeiten kann, die Sie sendet. Ein guter Dienstanbieter verbirgt gerätespezifische Besonderheiten – wenn das Gerät z. b. physisch eine Wiedergabeliste als Datei mit einer benutzerdefinierten Dateierweiterung speichert, sollte der Dienstanbieter diese Erweiterung automatisch hinzufügen, wenn die Anwendung eine Wiedergabeliste auf dem Gerät erstellt. Es sollte nicht erwartet werden, dass die Anwendung die richtige Erweiterung kennt, wenn ein Wiedergabelisten Objekt erstellt wird.

Dienstanbieter werden innerhalb des Prozesses der aufrufenden Anwendung ausgeführt. Die einzige Ausnahme ist der MTP-Dienstanbieter, der in einem eigenen Prozess ausgeführt wird. Aus diesem Grund besteht das Risiko, dass ein blockierter Dienstanbieter die aufrufenden Anwendung blockiert. Daher sollten Dienstanbieter so entworfen werden, dass Sie robust sind und Blockierungen verhindern, und Anwendungen sollten so entworfen werden, dass das stecken bleiben vermieden wird, wenn ein bestimmter Methoden Aufrufwert nicht schnell zurückgegeben wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Einstieg**](getting-started.md)
</dt> </dl>

 

 




