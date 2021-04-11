---
title: Schnittstellen für Anwendungen
description: Schnittstellen für Anwendungen
ms.assetid: bea867d6-a875-4150-9958-7f683cd215b9
keywords:
- Windows Media Device Manager, Anwendungsschnittstellen
- Device Manager, Anwendungsschnittstellen
- Desktop Anwendungen, Schnittstellen
- Programmier Referenz, Anwendungsschnittstellen
- Referenz für Windows Media Device Manager, Anwendungsschnittstellen
- Plug-ins, Schnittstellen
- Anwendungsschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49d66272c42679fd38d01b0114a834ee6f33e92
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310231"
---
# <a name="interfaces-for-applications"></a>Schnittstellen für Anwendungen

In diesem Abschnitt werden Schnittstellen beschrieben, die von Anwendungen verwendet oder implementiert werden, die das Windows Media Device Manager SDK zum kommunizieren mit Geräten verwenden. Der hier verwendete Begriff "Anwendung" bezieht sich auf alle ausführbaren Dateien, Plug-ins oder COM-Objekte, die auf einem Desktop Computer vorhanden sind und eine übergeordnete Kommunikation mit einem verbundenen tragbaren Gerät benötigen. Dies kann eine Media Player-Anwendung, ein Windows Media Player-Plug-in (wenn es einen direkten Zugriff auf ein tragbares Gerät benötigt) oder ein COM-Objekt zur Erfassung der Wiedergabe Anzahl enthalten.

Einige dieser Schnittstellen werden von der Anwendung implementiert, während andere von der Anwendung aufgerufen werden. Die Dokumentation für jede Schnittstelle gibt an, ob Sie implementiert oder aufgerufen wird (und ob Sie optional oder erforderlich ist).

Die folgenden Schnittstellen oder Klassen werden von Anwendungen verwendet.



| Schnittstelle oder Klasse                                           | BESCHREIBUNG                                                                                                                                                                                                         |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Csecurechannelclient-Klasse](csecurechannelclient-class.md) | Eine Hilfsklasse, die es Anwendungen ermöglicht, sich selbst zu authentifizieren, Daten zu verschlüsseln und zu entschlüsseln und Macs zu erstellen.                                                                                                     |
| [**Iwmdebug Manager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager)                 | Die Windows Media Device Manager-Schnittstelle der obersten Ebene für-Anwendungen.                                                                                                                                              |
| [**IWMDeviceManager2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2)               | Erweitert **iwmdevicemanager** durch Bereitstellen erweiterter Enumerationsmethoden und anderer Methoden.                                                                                                                           |
| [**IWMDeviceManager3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager3)               | Erweitert die **IWMDeviceManager2** -Schnittstelle durch Bereitstellen einer Methode, mit der die Geräte Enumeration festgelegt wird.                                                                                                      |
| [**Iwmdmdevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)                           | Bietet Methoden zum Überprüfen und untersuchen eines einzelnen tragbaren Geräts.                                                                                                                                                   |
| [**IWMDMDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice2)                         | Erweitert **iwmdmdevice** , indem es das Abrufen der von einem Gerät unterstützten Videoformate, das Suchen nach einem Speicher nach Namen und das Verwenden von Eigenschaften Seiten ermöglicht.                                                                       |
| [**IWMDMDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3)                         | Erweitert **IWMDMDevice2** durch die Bereitstellung von Methoden zum Abfragen eines Geräts nach Eigenschaften, zum Senden von e/a-Steuerungs Codes von Geräten und zum Bereitstellen aktualisierter Methoden, um nach Speicher zu suchen und Geräte Formatierungsfunktionen abzurufen. |
| [**Iwmdmde vicecontrol**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevicecontrol)             | Stellt Methoden zum Steuern von Geräten bereit.                                                                                                                                                                           |
| [**Iwmdmde vicesession**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevicesession)             | Verbesserung der Effizienz von Geräte Vorgängen durch bündeln mehrerer Vorgänge in einer Sitzung                                                                                                                       |
| [**Iwmdmenumschlag Device**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice)                   | Listet tragbare Geräte auf, die mit einem Computer verbunden sind.                                                                                                                                                                 |
| [**Iwmdmenumschlag**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage)                 | Listet Speicher auf einem Gerät auf.                                                                                                                                                                                    |
| [**Iwmdmmetadata**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata)                       | Legt Metadateneigenschaften (z. b. "Artist", "Album", "Genre" usw.) eines Speichers fest und ruft Sie ab.                                                                                                                      |
| [**Iwmdmubjectinfo**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmobjectinfo)                   | Dient zum Abrufen und Festlegen von Informationen, die Steuern, wie Wiedergabe Bare Dateien auf Geräten von der **iwmdmdevicecontrol** -Schnittstelle verarbeitet werden.                                                                                            |
| [**Iwmdmgesperrt**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmrevoked)                         | Ruft die URL ab, von der aktualisierte Komponenten heruntergeladen werden können, wenn eine Übertragung mit einem Sperr Fehler fehlschlägt.                                                                                                     |
| [**Iwmdmstorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage)                         | Stellt Methoden zum Überprüfen und untersuchen eines Speichers (Datei, Ordner, Wiedergabeliste) auf einem Gerät bereit.                                                                                                                             |
| [**IWMDMStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage2)                       | Erweitert **iwmdmstorage** , indem es ermöglicht wird, einen untergeordneten Speicher nach Namen zu erhalten und erweiterte Attribute zu erhalten und festzulegen.                                                                                              |
| [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3)                       | Erweitert **IWMDMStorage2** durch das verfügbar machen von Metadaten.                                                                                                                                                                     |
| [**IWMDMStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4)                       | Erweitert **IWMDMStorage3** durch Bereitstellen von Methoden zum Abrufen einer Teilmenge der verfügbaren Metadaten für einen Speicher und zum Festlegen und Abrufen einer Liste von Verweisen auf andere Storages.                                  |
| [**Iwmdmstoragecontrol**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol)           | Wird verwendet, um Dateien innerhalb eines Geräts oder zwischen einem Gerät und dem Computer einzufügen, zu löschen oder zu verschieben.                                                                                                                        |
| [**IWMDMStorageControl2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol2)         | Erweitert **iwmdmstoragecontrol** , indem es ermöglicht wird, den Namen der Zieldatei festzulegen, wenn Inhalte in einen Speicher eingefügt werden.                                                                                |
| [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3)         | Erweitert **IWMDMStorageControl2** , indem es ermöglicht wird, einen **iwmdmmetadata** -Schnittstellen Zeiger zu übergeben.                                                                                                           |
| [**Iwmdmstorageglobals**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorageglobals)           | Stellt Methoden zum Abrufen von globalen Informationen über ein Speichermedium (z. b. eine Flash-Rom-Karte) auf einem Gerät bereit.                                                                                                   |
| [**Iwmdrmdeviceapp**](iwmdrmdeviceapp.md)                   | Ermöglicht einer Anwendung die Durchführung von Messungen, Lizenz Synchronisierungen und Aktualisierungen der DRM-Komponenten eines Geräts.                                                                                                       |
| [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md)                 | Erweitert **iwmdrmdeviceapp** durch Bereitstellen einer neuen Version der **querydevicestatus** -Methode.                                                                                                                         |



 

Rückruf Schnittstellen

Die folgenden optionalen Schnittstellen werden von einer Anwendung implementiert, um den Fortschritt einer asynchronen Anforderung, z. b. eine Lese-oder Schreib Anforderung, zu verfolgen.



| Schnittstelle                                      | BESCHREIBUNG                                                                                                                                                             |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iwmdmnotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification) | Ermöglicht Anwendungen und Dienstanbietern das Empfangen von Benachrichtigungen, wenn Geräte oder Speicher Speicher (z. b. RAM-Karten) verbunden sind oder vom Computer getrennt werden. |
| [**IWMDMOperation2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation2)     | Erweitert **iwmdmoperation** durch Bereitstellen von Methoden zum Abrufen und Festlegen erweiterter Attribute.                                                                                     |
| [**IWMDMOperation3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation3)     | Erweitert **iwmdmoperation** durch Bereitstellen einer neuen Methode für die unverschlüsselte Übertragung von Daten, um zusätzliche Effizienz zu erzielen.                                                            |
| [**Iwmdmoperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation)       | Ermöglicht es einer Anwendung, zu steuern, wie Daten während einer Dateiübertragung vom Computer gelesen oder auf diesen geschrieben werden.                                                               |
| [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)       | Erweitert die **iwmdmprogress:: End** -Methode durch Bereitstellen eines Status Indikators.                                                                                              |
| [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)       | Erweitert **IWMDMProgress2** , indem zusätzliche Eingabeparameter bereitgestellt werden, um die Ereignis-ID und kontextspezifische Informationen anzugeben.                                           |
| [**Iwmdmprogress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress)         | Ermöglicht einer Anwendung, den Fortschritt von Vorgängen zu verfolgen, z. b. das Formatieren von Medien oder Dateiübertragungen                                                                  |



 

Im folgenden Diagramm wird gezeigt, wie die meisten wichtigen Anwendungsschnittstellen von der Stamm- **iwmdevicemanager** -Schnittstelle abgerufen werden. Eine Anwendung ruft diese Stamm Schnittstelle durch koerstellen des mediadevmgr-Objekts ab, fordert die **icomponentauthenticate** -Schnittstelle an, authentifiziert die Komponente und fordert dann den **iwmdevicemanager** an (diese Schritte werden unter [Authentifizieren der Anwendung](authenticating-the-application.md)beschrieben). Nachdem diese Stamm Schnittstelle abgerufen wurde, wird [**iwmtvicemanager:: enumdevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) aufgerufen, um ein Objekt zu erstellen, das [**iwmdmenumdevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice)implementiert. Andere Schnittstellen werden abgerufen, indem Methoden für Schnittstellen in der angezeigten Reihenfolge aufgerufen werden. Abgeleitete Schnittstellen, z. b. [**IWMDMDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice2) , werden durch Aufrufen von **QueryInterface** in der Basisschnittstelle abgerufen.

Im folgenden Diagramm werden abgeleitete Schnittstellen durch Schrägstriche gekennzeichnet, sodass "iwmdmstorage/2/3" **iwmdmstorage**, **IWMDMStorage2** und **IWMDMStorage3** angeben würde.

![Diagramm, das zeigt, wie Sie die wichtigsten Anwendungsschnittstellen in Windows Media Device Manager erhalten.](images/wmdm-app-interfaces.gif)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> </dl>

 

 




