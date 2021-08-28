---
title: Schnittstellen für Anwendungen
description: Schnittstellen für Anwendungen
ms.assetid: bea867d6-a875-4150-9958-7f683cd215b9
keywords:
- Windows Medien Geräte-Manager, Anwendungsschnittstellen
- Geräte-Manager, Anwendungsschnittstellen
- Desktopanwendungen, Schnittstellen
- Programmierreferenz, Anwendungsschnittstellen
- Referenz für Windows Media Geräte-Manager,Anwendungsschnittstellen
- Plug-Ins, Schnittstellen
- Anwendungsschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 690b8419a7f04ef2b4eab1db65266027bdf5bcf3a102e59a95030a290e3747ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619955"
---
# <a name="interfaces-for-applications"></a>Schnittstellen für Anwendungen

In diesem Abschnitt werden Schnittstellen beschrieben, die von Anwendungen verwendet oder implementiert werden, die das Windows Media Geräte-Manager SDK für die Kommunikation mit Geräten verwenden. Der hier verwendete Begriff "Anwendung" bezeichnet alle ausführbaren Dateien, Plug-Ins oder COM-Objekte, die auf einem Desktopcomputer vorhanden sind und eine kommunikation auf hoher Ebene mit einem verbundenen portablen Gerät benötigen. Dies kann eine Media Player-Anwendung, ein Windows Media Player Plug-In (wenn es direkten Zugriff auf ein portables Gerät benötigt) oder ein COM-Objekt zur Messung der Wiedergabeanzahl umfassen.

Einige dieser Schnittstellen werden von der Anwendung implementiert, während andere von der Anwendung aufgerufen werden. Die Dokumentation für jede Schnittstelle gibt an, ob sie implementiert oder aufgerufen wird (und ob sie optional oder erforderlich ist, wenn sie implementiert ist).

Die folgenden Schnittstellen oder Klassen werden von Anwendungen verwendet.



| Schnittstelle oder Klasse                                           | BESCHREIBUNG                                                                                                                                                                                                         |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CSecureChannelClient-Klasse](csecurechannelclient-class.md) | Eine Hilfsklasse, die es Anwendungen ermöglicht, sich selbst zu authentifizieren, Daten zu verschlüsseln und zu entschlüsseln und MACs zu erstellen.                                                                                                     |
| [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager)                 | Die Geräte-Manager-Schnittstelle der obersten Ebene Windows Media für Anwendungen.                                                                                                                                              |
| [**IWMDeviceManager2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2)               | Erweitert **IWMDeviceManager** durch die Bereitstellung erweiterter Enumerationsmethoden und anderer Methoden.                                                                                                                           |
| [**IWMDeviceManager3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager3)               | Erweitert die **IWMDeviceManager2-Schnittstelle,** indem eine Methode angegeben wird, die die Einstellung für die Geräteenumeration festlegt.                                                                                                      |
| [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)                           | Stellt Methoden zum Untersuchen und Untersuchen eines einzelnen portablen Geräts bereit.                                                                                                                                                   |
| [**IWMDMDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice2)                         | Erweitert **IWMDMDevice,** indem es möglich wird, die von einem Gerät unterstützten Videoformate abzurufen, einen Speicher anhand des Namens zu suchen und Eigenschaftenseiten zu verwenden.                                                                       |
| [**IWMDMDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3)                         | Erweitert **IWMDMDevice2** durch die Bereitstellung von Methoden zum Abfragen von Eigenschaften für ein Gerät, zum Senden von Geräte-E/A-Steuerungscodes und zum Bereitstellen aktualisierter Methoden zum Suchen nach Speicher und Abrufen von Geräteformatfunktionen. |
| [**IWMDMDeviceControl**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevicecontrol)             | Stellt Methoden zum Steuern von Geräten bereit.                                                                                                                                                                           |
| [**IWMDMDeviceSession**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevicesession)             | Verbessert die Effizienz von Gerätevorgängen, indem mehrere Vorgänge in einer Sitzung gebündelt werden                                                                                                                       |
| [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice)                   | Listet portable Geräte auf, die an einen Computer angefügt sind.                                                                                                                                                                 |
| [**IWMDMEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage)                 | Listet Speicher auf einem Gerät auf.                                                                                                                                                                                    |
| [**IWMDMMetaData**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata)                       | Legt Metadateneigenschaften (z. B. Interpret, Album, Genre usw.) eines Speichers fest und ruft sie ab.                                                                                                                      |
| [**IWMDMObjectInfo**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmobjectinfo)                   | Ruft Informationen ab, die steuern, wie abspielbare Dateien auf dem Gerät von der **IWMDMDeviceControl-Schnittstelle** verarbeitet werden, und legt diese fest.                                                                                            |
| [**IWMDMRevoked**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmrevoked)                         | Ruft die URL ab, von der aktualisierte Komponenten heruntergeladen werden können, wenn bei einer Übertragung ein Sperrfehler auftritt.                                                                                                     |
| [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage)                         | Stellt Methoden zum Untersuchen und Untersuchen eines Speichers (Datei, Ordner, Wiedergabeliste) auf einem Gerät bereit.                                                                                                                             |
| [**IWMDMStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage2)                       | Erweitert **IWMDMStorage,** indem es möglich wird, einen untergeordneten Speicher anhand des Namens abzurufen und erweiterte Attribute abzurufen und festzulegen.                                                                                              |
| [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3)                       | Erweitert **IWMDMStorage2** durch Verfügbarmachen von Metadaten.                                                                                                                                                                     |
| [**IWMDMStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4)                       | Erweitert **IWMDMStorage3** durch die Bereitstellung von Methoden zum Abrufen einer Teilmenge der verfügbaren Metadaten für einen Speicher sowie zum Festlegen und Abrufen einer Liste von Verweisen auf andere Speicher.                                  |
| [**IWMDMStorageControl**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol)           | Wird zum Einfügen, Löschen oder Verschieben von Dateien innerhalb eines Geräts oder zwischen einem Gerät und dem Computer verwendet.                                                                                                                        |
| [**IWMDMStorageControl2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol2)         | Erweitert **IWMDMStorageControl,** indem es möglich ist, den Namen der Zieldatei festzulegen, wenn Inhalt in einen Speicher eingefügt wird.                                                                                |
| [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3)         | Erweitert **IWMDMStorageControl2,** indem es möglich ist, einen **IWMDMMetaData-Schnittstellenzeiger** zu übergeben.                                                                                                           |
| [**IWMDMStorageGlobals**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorageglobals)           | Stellt Methoden zum Abrufen globaler Informationen über ein Speichermedium (z. B. eine Flash-ROM-Karte) auf einem Gerät bereit.                                                                                                   |
| [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md)                   | Ermöglicht einer Anwendung das Durchführen der Messung, Lizenzsynchronisierung und Aktualisierung der DRM-Komponenten eines Geräts.                                                                                                       |
| [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md)                 | Erweitert **IWMDRMDeviceApp** durch Bereitstellen einer neuen Version der **QueryDeviceStatus-Methode.**                                                                                                                         |



 

Rückrufschnittstellen

Die folgenden optionalen Schnittstellen werden von einer Anwendung implementiert, um den Fortschritt einer asynchronen Anforderung, z. B. einer Lese- oder Schreibanforderung, nachzuverfolgen.



| Schnittstelle                                      | BESCHREIBUNG                                                                                                                                                             |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification) | Ermöglicht Anwendungen und Dienstanbietern den Empfang von Benachrichtigungen, wenn Geräte oder Speicher (z. B. RAM-Karten) mit dem Computer verbunden oder getrennt sind. |
| [**IWMDMOperation2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation2)     | Erweitert **IWMDMOperation** durch die Bereitstellung von Methoden zum Abrufen und Festlegen erweiterter Attribute.                                                                                     |
| [**IWMDMOperation3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation3)     | Erweitert **IWMDMOperation,** indem eine neue Methode zum unverschlüsselten Übertragen von Daten zur Effizienzsteigerung zur Verfügung gestellt wird.                                                            |
| [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation)       | Ermöglicht einer Anwendung, zu steuern, wie Daten während einer Dateiübertragung vom Computer gelesen oder auf den Computer geschrieben werden.                                                               |
| [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)       | Erweitert die **IWMDMProgress::End-Methode** durch Angabe eines Statusindikators.                                                                                              |
| [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)       | Erweitert **IWMDMProgress2** durch die Bereitstellung zusätzlicher Eingabeparameter, um die Ereignis-ID und kontextspezifische Informationen anzugeben.                                           |
| [**IWMDMProgress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress)         | Ermöglicht einer Anwendung das Nachverfolgen des Fortschritts von Vorgängen, z. B. das Formatieren von Medien oder Dateiübertragungen.                                                                  |



 

Das folgende Diagramm zeigt, wie die meisten wichtigen Anwendungsschnittstellen von der **IWMDeviceManager-Stammschnittstelle** bezogen werden. Eine Anwendung ruft diese Stammschnittstelle ab, indem sie das MediaDevMgr-Objekt erstellt, die **IComponentAuthenticate-Schnittstelle** anfordert, die Komponente authentifiziert und dann den **IWMDeviceManager** anfordert (diese Schritte werden unter [Authentifizieren der Anwendung](authenticating-the-application.md)beschrieben). Nachdem diese Stammschnittstelle abgerufen wurde, wird [**IWMDeviceManager::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) aufgerufen, um ein Objekt zu erstellen, das [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice)implementiert. Andere Schnittstellen werden abgerufen, indem Methoden für Schnittstellen in der angezeigten Reihenfolge aufgerufen werden. Abgeleitete Schnittstellen wie [**IWMDMDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice2) werden abgerufen, indem **QueryInterface** für die Basisschnittstelle aufgerufen wird.

Im folgenden Diagramm sind abgeleitete Schnittstellen mit Schrägstrichen gekennzeichnet, sodass "IWMDMStorage/2/3" **IWMDMStorage,** **IWMDMStorage2** und **IWMDMStorage3** angibt.

![Diagramm, das zeigt, wie die wichtigsten Anwendungsschnittstellen im Windows-Mediengeräte-Manager angezeigt werden.](images/wmdm-app-interfaces.gif)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> </dl>

 

 




