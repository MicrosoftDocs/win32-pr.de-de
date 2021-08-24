---
title: Schnittstellen für Dienstanbieter
description: Schnittstellen für Dienstanbieter
ms.assetid: bd61c5fa-047c-4d93-bae1-f3433696b95b
keywords:
- Windows Medien Geräte-Manager,Dienstanbieterschnittstellen
- Geräte-Manager,Dienstanbieterschnittstellen
- Dienstanbieter,Schnittstellen
- Programmierreferenz,Dienstanbieterschnittstellen
- Referenz für Windows Media Geräte-Manager,Dienstanbieterschnittstellen
- Dienstanbieterschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73a7b178ec0f3ab70f0a133a2286a97e294d449264061681fec540ae9b434c94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766705"
---
# <a name="interfaces-for-service-providers"></a>Schnittstellen für Dienstanbieter

In diesem Abschnitt werden Schnittstellen beschrieben, die von Windows Media Geräte-Manager implementiert werden. Dienstanbieter führen den Großteil der eigentlichen Kommunikation mit einem Gerät durch, da sie die meisten der Windows Media Geräte-Manager SDK-Methoden implementieren, die von der Anwendung aufgerufen werden.

Dienstanbieter müssen nicht alle in diesem Abschnitt aufgeführten Schnittstellen implementieren. Beispielsweise implementiert ein Mediengerät ohne On-Board-Speicher nicht die Schnittstellen, die zum Steuern oder Verfügbar machen von Inhalten verwendet werden. Ob eine Methode oder Schnittstelle erforderlich ist, wird auf der entsprechenden Referenzseite angegeben.



| Schnittstelle oder Klasse                                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CSecureChannelServer](csecurechannelserver-class.md) | Eine Hilfsklasse, die es einem Dienstanbieter oder einem sicheren Inhaltsanbieter ermöglicht, eine Anwendung zu authentifizieren und MAC-Signaturen für sichere Parameter zu erstellen.                                                                                                                                                         |
| [**IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider)       | Stellt dem Client (normalerweise Windows Media Geräte-Manager) einen Geräteenumerator für die Geräte zur Verfügung, die dieser Dienstanbieter unterstützt.                                                                                                                                                                          |
| [**IMDServiceProvider2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider2)     | Erweitert **IMDServiceProvider,** indem eine Methode zum Erstellen des Geräts mithilfe des Gerätepfads zur Verfügung stellt.                                                                                                                                                                                                            |
| [**IMDServiceProvider3**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider3)     | Erweitert **IMDServiceProvider2,** indem eine Methode zum Festlegen der Einstellungen für die Geräteenumeration bereitgestellt wird.                                                                                                                                                                                                             |
| [**IMDSPDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice)                     | Stellt eine instanzbasierte Zuordnung zu einem Mediengerät zur Über diese Schnittstelle kann der Client die Speichermedien-Enumeratoren für das Gerät aufzählen, Informationen zum Gerät erhalten und nicht transparente (Pass-Through)-Befehle an das Gerät senden.                                                                 |
| [**IMDSPDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2)                   | Extends **IMDSPDevice** by providing methods for getting extended video formats, getting Plug and Play (PnP) device names, enabling the use of property pages, and making it possible to get a pointer to a storage medium from its name. Diese Schnittstelle ist für den Dienstanbieter optional, wird jedoch empfohlen. |
| [**IMDSPDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice3)                   | Erweitert **IMDSPDevice2** durch die Möglichkeit, Eigenschaften und Funktionen des Geräts in Bezug auf ein Objektformat abfragen zu können.                                                                                                                                                                                 |
| [**IMDSPDeviceControl**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevicecontrol)       | Stellt Methoden zum Steuern von Geräten zur Verfügung.                                                                                                                                                                                                                                                                         |
| [**IMDSPDirectTransfer**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdirecttransfer)     | Ermöglicht Windows Media Geräte-Manager, die Inhaltsübertragung an den Dienstanbieter zu delegieren. In diesem Fall Windows Media Geräte-Manager keine Verarbeitung des Inhalts vor dem Senden an den Dienstanbieter. Der Dienstanbieter erhält die vollständige Kontrolle über die Quelle.                                   |
| [**IMDSPEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice)             | Hier werden die von diesem Dienstanbieter unterstützten Mediengeräte aufzählt.                                                                                                                                                                                                                                                  |
| [**IMDSPEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage)           | Aufzählt die Speichermedien auf einem Gerät und den Inhalt auf einem Speichermedium.                                                                                                                                                                                                                                    |
| [**IMDSPObject**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject)                     | Enthält Methoden für Datenübertragungsvorgänge für ein Speicherobjekt.                                                                                                                                                                                                                                                |
| [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2)                   | Erweitert **IMDSPObject** durch eine effizientere Übertragung von DRM-fähigen Daten.                                                                                                                                                                                                                             |
| [**IMDSPObjectInfo**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobjectinfo)             | Legt die Wiedergabelänge, die Wiedergabeposition, den Wiedergabeoffset oder die Gesamtlänge von wieder playable-Objekten auf einem Speichermedium fest oder ruft sie ab.                                                                                                                                                                                                    |
| [**IMDSPRevoked**](/windows/desktop/api/mswmdm/nn-mswmdm-imdsprevoked)                   | Ruft die URL ab, von der aktualisierte Komponenten heruntergeladen werden können.                                                                                                                                                                                                                                                |
| [**IMDSPStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage)                   | Stellt eine instanzbasierte Zuordnung zu einem Speichermedium auf einem Gerät zur Seite. Diese Schnittstelle erstellt Speicherobjekte, ruft Informationen darüber ab und bietet Zugriff auf die **IMDSPEnumStorage-Schnittstelle** zum Aufzählen von Unterordnern, die im aktuellen Speicher geschachtelt sind.                                      |
| [**IMDSPStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2)                 | Erweitert **IMDSPStorage** durch Abrufen und Festlegen erweiterter Attribute und ermöglicht es, einen Zeiger auf den Speicher aus seinem Namen zu erhalten.                                                                                                                                                                             |
| [**IMDSPStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage3)                 | Erweitert **IMDSPStorage2 durch Unterstützung** von Metadaten.                                                                                                                                                                                                                                                                 |
| [**IMDSPStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage4)                 | Erweitert **IMDSPStorage3 durch Die** Unterstützung von Wiedergabelistenobjekten.                                                                                                                                                                                                                                                         |
| [**IMDSPStorageGlobals**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals)     | Ruft globale Informationen zu einem Speichermedium ab, z. B. die Menge des freien Speicherplatzes und die Gesamtzahl der Dateien.                                                                                                                                                                                              |



 

Das folgende Diagramm zeigt, wie die verschiedenen Schnittstellen von einem Dienstanbieter implementiert werden. In diesem Diagramm werden abgeleitete Schnittstellen zur Dichte im selben Tag angezeigt, sodass IMDServiceProvider/2/3 drei Schnittstellen darstellen würde: **IMDServiceProvider,** **IMDServiceProvider2** und **IMDServiceProvider3**. Die gezeigten Methoden werden nur durch eine dieser Schnittstellen erweitert. Abgeleitete Schnittstellen werden durch Aufrufen von **QueryInterface** auf der Basisschnittstelle des erstellten Objekts ermittelt.

![Diagramm, das zeigt, wie windows media device manager erwartet, Schnittstellen von einem Dienstanbieter zu erhalten.](images/wmdm-sp-interfaces.gif)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> <dt>

[**Windows Medienschnittstellen DRM-Implemented Medienschnittstellen**](windows-media-drm-implemented-interfaces.md)
</dt> </dl>

 

 




