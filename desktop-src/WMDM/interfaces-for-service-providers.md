---
title: Schnittstellen für Dienstanbieter
description: Schnittstellen für Dienstanbieter
ms.assetid: bd61c5fa-047c-4d93-bae1-f3433696b95b
keywords:
- Windows Media Device Manager, Dienstanbieter Schnittstellen
- Device Manager, Dienstanbieter Schnittstellen
- Dienstanbieter, Schnittstellen
- Programmier Referenz, Dienstanbieter Schnittstellen
- Referenz für Windows Media Device Manager, Dienstanbieter Schnittstellen
- Dienstanbieter Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 019d31f05674f0d9e492f8a73748500bc1d9d514
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711406"
---
# <a name="interfaces-for-service-providers"></a>Schnittstellen für Dienstanbieter

In diesem Abschnitt werden die von Windows Media Device Manager Service-Anbietern implementierten Schnittstellen beschrieben. Dienstanbieter führen den größten Teil der eigentlichen Arbeit der Kommunikation mit einem Gerät durch, da Sie die meisten der Windows Media Device Manager SDK-Methoden implementieren, die von der Anwendung aufgerufen werden.

Dienstanbieter müssen nicht alle in diesem Abschnitt aufgeführten Schnittstellen implementieren. Beispielsweise werden von einem Medien Gerät, das nicht über einen-Board-Speicher verfügt, keine Schnittstellen implementiert, die zum Steuern oder verfügbar machen von Inhalten verwendet werden. Ob eine Methode oder Schnittstelle erforderlich ist, wird auf der entsprechenden Referenzseite angezeigt.



| Schnittstelle oder Klasse                                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Csecurechannelserver](csecurechannelserver-class.md) | Eine Hilfsklasse, die einem Dienstanbieter oder einem sicheren Inhaltsanbieter ermöglicht, eine Anwendung zu authentifizieren und Mac-Signaturen für sichere Parameter zu erstellen.                                                                                                                                                         |
| [**Imdserviceprovider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider)       | Stellt den Client (normalerweise Windows Media Device Manager) mit einem Geräte Enumerator für die Geräte bereit, die dieser Dienstanbieter unterstützt.                                                                                                                                                                          |
| [**IMDServiceProvider2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider2)     | Erweitert **imdserviceprovider** durch Bereitstellen einer Methode zum Erstellen des Geräts mithilfe des Geräte Pfads.                                                                                                                                                                                                            |
| [**IMDServiceProvider3**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider3)     | Erweitert **IMDServiceProvider2** durch Bereitstellen einer Methode zum Festlegen der geräteenumerationseinstellungen.                                                                                                                                                                                                             |
| [**Imdspdevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice)                     | Stellt eine instanzbasierte Zuordnung zu einem Medien Gerät bereit. Mithilfe dieser Schnittstelle kann der Client die Speichermedien-Enumeratoren für das Gerät auflisten, Informationen zum Gerät erhalten und nicht transparente (Pass-Through-) Befehle an das Gerät senden.                                                                 |
| [**IMDSPDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2)                   | Erweitert **imdspdevice** durch Bereitstellen von Methoden zum erhalten erweiterter Videoformate, zum erhalten von Plug & Play (PNP)-Gerätenamen, zum Aktivieren der Verwendung von Eigenschaften Seiten und zum Erstellen eines Zeigers auf ein Speichermedium aus dem Namen. Diese Schnittstelle ist für den Dienstanbieter optional, wird jedoch empfohlen. |
| [**IMDSPDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice3)                   | Erweitert **IMDSPDevice2** durch die Möglichkeit, Eigenschaften und Funktionen des Geräts in Bezug auf ein Objekt Format abzufragen.                                                                                                                                                                                 |
| [**Imdspde vicecontrol**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevicecontrol)       | Stellt Methoden zum Steuern von Geräten bereit.                                                                                                                                                                                                                                                                         |
| [**Imdspdirecttransfer**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdirecttransfer)     | Ermöglicht Windows Media Device Manager das Delegieren der Inhalts Übertragung an den Dienstanbieter. In diesem Fall verarbeitet Windows Media Device Manager keinen Inhalt vor dem Senden an den Dienstanbieter. Der Dienstanbieter erhält die vollständige Kontrolle über die Quelle.                                   |
| [**Imdspenum Device**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice)             | Listet die Mediengeräte auf, die von diesem Dienstanbieter unterstützt werden.                                                                                                                                                                                                                                                  |
| [**Imdspenum Storage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage)           | Listet die Speichermedien auf einem Gerät und die Inhalte auf einem Speichermedium auf.                                                                                                                                                                                                                                    |
| [**Imdspobject**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject)                     | Enthält Methoden für Datenübertragungs Vorgänge für ein Speicher Objekt.                                                                                                                                                                                                                                                |
| [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2)                   | Erweitert **imdspobject** durch Bereitstellen einer effizienteren Übertragung von DRM-fähigen Daten.                                                                                                                                                                                                                             |
| [**Imdspobjectinfo**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobjectinfo)             | Legt die Wiedergabe Länge, die Wiedergabe Position, den Wiedergabe Offset oder die Gesamtlänge von Wiedergabe baren Objekten auf einem Speichermedium fest oder ruft Sie ab.                                                                                                                                                                                                    |
| [**Imdstaked**](/windows/desktop/api/mswmdm/nn-mswmdm-imdsprevoked)                   | Ruft die URL ab, von der aktualisierte Komponenten heruntergeladen werden können.                                                                                                                                                                                                                                                |
| [**Imdspstorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage)                   | Stellt eine Instanziierung auf der Grundlage eines Speichermediums auf einem Gerät bereit. Diese Schnittstelle erstellt Speicher Objekte, ruft Informationen darüber ab und ermöglicht den Zugriff auf die **imdspenumstorage** -Schnittstelle zum Auflisten der Unterordner, die im aktuellen Speicher geschachtelt sind.                                      |
| [**IMDSPStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2)                 | Erweitert **imdspstorage** , indem erweiterte Attribute erhalten und festgelegt werden, und es ist möglich, einen Zeiger auf den Speicher aus seinem Namen zu erhalten.                                                                                                                                                                             |
| [**IMDSPStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage3)                 | Erweitert **IMDSPStorage2** durch Unterstützung von Metadaten.                                                                                                                                                                                                                                                                 |
| [**IMDSPStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage4)                 | Erweitert **IMDSPStorage3** durch Unterstützung von Wiedergabelisten Objekten.                                                                                                                                                                                                                                                         |
| [**Imdspstorageglobals**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals)     | Ruft globale Informationen zu einem Speichermedium ab, z. b. die Menge an freiem Speicherplatz und die Gesamtanzahl der Dateien.                                                                                                                                                                                              |



 

Im folgenden Diagramm wird veranschaulicht, wie die verschiedenen Schnittstellen, die von einem Dienstanbieter implementiert werden, angezeigt werden. In diesem Diagramm werden abgeleitete Schnittstellen im selben Tag für die Kompaktheit angezeigt, daher stellt imdserviceprovider/2/3 drei Schnittstellen dar: **imdserviceprovider**, **IMDServiceProvider2** und **IMDServiceProvider3**. Die angezeigten Methoden werden durch nur eine dieser Schnittstellen erweitert. Abgeleitete Schnittstellen werden abgerufen, indem **QueryInterface** für die Basisschnittstelle des erstellten Objekts aufgerufen wird.

![Diagramm, das zeigt, wie der Windows Media-Geräte-Manager erwartet, Schnittstellen von einem Dienstanbieter abzurufen.](images/wmdm-sp-interfaces.gif)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> <dt>

[**Windows Media DRM-Implemented-Schnittstellen**](windows-media-drm-implemented-interfaces.md)
</dt> </dl>

 

 




