---
title: WMP-SDK-Schnittstellen
description: WMP-SDK-Schnittstellen
ms.assetid: 68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd
keywords:
- Windows Media Player,Schnittstellen
- Windows Media Player Mobil, Schnittstellen
- Windows Media Player Objektmodell, Schnittstellen
- Objektmodell, Schnittstellen
- ActiveX-Steuerelement, Schnittstellen
- Windows Media Player ActiveX-Steuerelement, Schnittstellen
- Windows Media Player Mobiles ActiveX-Steuerelement, Schnittstellen
- Referenz für Objektmodell, Schnittstellen
- Referenz zum Schnittstellenobjektmodell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7db8e5ebe29e38da9f92370f60a622fad70f36395b271eb7bd86ef49f49a3d49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123500"
---
# <a name="wmp-sdk-interfaces"></a>WMP-SDK-Schnittstellen

In diesem Abschnitt werden die COM-Schnittstellen dokumentiert, die vom Windows Media Player ActiveX-Steuerelement und dem Windows Media Player Mobile ActiveX-Steuerelement verfügbar gemacht werden.

Die Accessormethoden der **IWMPCore-** oder **IWMPPlayer-Schnittstelle** werden verwendet, um bestimmte Schnittstellen abzurufen. Diese Schnittstellen verfügen wiederum möglicherweise über Accessormethoden zum Abrufen weiterer Schnittstellen. Das Aufrufen von **QueryInterface** für eine dieser Schnittstellen ist nur erforderlich, wenn Sie die Basisversion einer Schnittstelle abrufen und eine Methode für eine höhere Version derselben Schnittstelle aufrufen möchten.

> [!Note]  
> Alle Methoden und Ereignisse werden in Windows Media Player 10 Mobile und höher vollständig unterstützt, sofern nicht explizit anders angegeben.

Das Windows Media Player-Steuerelement macht die folgenden Schnittstellen verfügbar.

| Schnittstelle                                                    | BESCHREIBUNG                                                                                                                                                                               |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_WMPOCXEvents](-wmpocxevents-interface.md)                | Stellt Ereignisse bereit, die vom Windows Media Player-Steuerelement stammen, auf das ein Einbettungsprogramm reagieren kann.                                                                              |
| [IWMPCählen](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom)                                   | Greift auf eine CD oder DVD auf einem Laufwerk zu.                                                                                                                                                          |
| [IWMPCaku Überschreiben](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)                           | Stellt Methoden zum Verwalten der Erstellung von Audio-CDs bereit.                                                                                                                                            |
| [IWMPCcollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)               | Greift auf eine Sammlung von CD- oder DVD-Laufwerken zu.                                                                                                                                                |
| [IWMPCpinRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)                             | Stellt Methoden zum Verwalten des Kopierens von Spuren von einer Audio-CD bereit.                                                                                                                               |
| [IWMPClosedCaption](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpclosedcaption)                   | Schließt Untertitel mit einem Medienclip ein.                                                                                                                                                      |
| [IWMPClosedCaption2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpclosedcaption2)                 | Stellt zusätzliche Untertitelmethoden bereit.                                                                                                                                            |
| [IWMPControls](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols)                             | Stellt die Transportsteuerelemente von Windows Media Player dar, z. B. Wiedergabe, Beenden und Anhalten.                                                                                                 |
| [IWMPControls2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2)                           | Stellt zusätzliche Steuerungsmethoden bereit.                                                                                                                                                      |
| [IWMPControls3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols3)                           | Stellt zusätzliche Steuerungsmethoden bereit.                                                                                                                                                      |
| [IWMPCore](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore)                                     | Ruft Zeiger auf andere Schnittstellen ab und greift auf grundlegende Features des Steuerelements zu. Dies ist die Stammschnittstelle für das Windows Media Player-Objektmodell.                                  |
| [IWMPCore2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore2)                                   | Stellt zusätzliche Kernmethoden bereit.                                                                                                                                                         |
| [IWMPCore3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore3)                                   | Stellt zusätzliche Kernmethoden bereit.                                                                                                                                                         |
| [IWMPDVD](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpdvd)                                       | Greift auf das Inhaltsmenü einer DVD zu.                                                                                                                                                       |
| [IWMPError](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperror)                                   | Greift auf eine Auflistung von [IWMPErrorItem-Zeigern](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperroritem) zu.                                                                                                                     |
| [IWMPErrorItem](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperroritem)                           | Stellt Informationen zu Fehlern bereit.                                                                                                                                                        |
| [IWMPErrorItem2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperroritem2)                         | Stellt zusätzliche Fehlerelementmethoden bereit.                                                                                                                                                   |
| [IWMPEvents](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)                       | Macht Ereignisse verfügbar, die aus dem Windows Media Player-Steuerelement stammen, auf das ein Einbettungsprogramm reagieren kann.                                                                            |
| [IWMPEvents2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)                     | Macht Ereignisse verfügbar, die vom Windows Media Player 10-Steuerelement stammen, auf das ein Einbettungsprogramm reagieren kann. Diese Ereignisse werden speziell für Gerätesynchronisierungsprogramme verwendet. |
| [IWMPEvents3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)                               | Stellt Ereignisse im Zusammenhang mit CD-Vorgängen, CD-Löschvorgängen, Ordnerüberwachung und Remotebibliotheksdiensten bereit.                                                                                        |
| [IWMPFolderMonitorServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)   | Stellt Methoden zum Aufzählen, Überprüfen und Ändern von Dateiordnern bereit, die Windows Media Player auf digitale Medieninhalte überwachen.                                                                |
| [IWMPGraphCreation](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpgraphcreation)                   | Verwaltet das DirectShow-Diagramm.                                                                                                                                                             |
| [IWMPLibrary](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)                               | Stellt eine Bibliothek dar.                                                                                                                                                                     |
| [IWMPLibraryServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)               | Stellt Methoden zum Aufzählen von Bibliotheken bereit.                                                                                                                                                  |
| [IWMPLibrarySharingServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrarysharingservices) | Stellt Methoden zum Verwalten der Bibliotheksfreigabe bereit.                                                                                                                                               |
| [IWMPMedia](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)                                   | Legt die Eigenschaften eines Medienelements fest und ruft sie ab.                                                                                                                                        |
| [IWMPMedia2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia2)                                 | Stellt zusätzliche Methoden zum Festlegen und Abrufen der Eigenschaften eines Medienelements bereit.                                                                                                           |
| [IWMPMedia3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia3)                                 | Stellt zusätzliche Methoden zum Festlegen und Abrufen der Eigenschaften eines Medienelements bereit.                                                                                                           |
| [IWMPMediaCollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection)               | Greift auf eine Auflistung von [IWMPMedia-Zeigern](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) zu.                                                                                                                             |
| [IWMPMediaCollection2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2)             | Stellt Methoden bereit, die die **IWMPMediaCollection-Schnittstelle** ergänzen.                                                                                                                   |
| [IWMPMetadataPicture](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmetadatapicture)               | Ruft Informationen zum **WM/Picture-Metadatenattribut** ab.                                                                                                                        |
| [IWMPMetadataText](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmetadatatext)                     | Ruft Informationen zu komplexen Textmetadatenattributen ab.                                                                                                                          |
| [IWMPNetwork](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpnetwork)                               | Legt die Eigenschaften der von Windows Media Player verwendeten Netzwerkverbindung fest und ruft sie ab.                                                                                                 |
| [IWMPPlayer](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer)                                 | Steuert das Verhalten der Windows Media Player Steuerelement-Benutzeroberfläche.                                                                                                                 |
| [IWMPPlayer2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer2)                               | Stellt zusätzliche Methoden zum Steuern Windows Media Player bereit.                                                                                                                         |
| [IWMPPlayer3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer3)                               | Stellt zusätzliche Methoden zum Steuern Windows Media Player bereit.                                                                                                                         |
| [IWMPPlayer4](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer4)                               | Stellt zusätzliche Methoden zum Steuern Windows Media Player bereit.                                                                                                                         |
| [IWMPPlayerApplication](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerapplication)           | Wechselt zwischen einem Remotesteuerelement Windows Media Player und dem vollständigen Modus des Players. Entwickelt für die Verwendung durch C++-Programme, die das Steuerelement in den Remotemodus einbetten.                          |
| [IWMPPlayerServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)                 | Wird vom Host eines Remotesteuer steuerelements verwendet, um den vollständigen Modus der Windows Media Player. Für die Verwendung mit C++ entwickelt.                                                                     |
| [IWMPPlayerServices2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices2)               | Legt die Hintergrundverarbeitungspriorität fest.                                                                                                                                                  |
| [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)                             | Erstellt und verwaltet Wiedergabelisten.                                                                                                                                                            |
| [IWMPPlaylistArray](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylistarray)                   | Zugriff auf eine Auflistung von [IWMPPlaylist-Zeigern](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist) nach Indexnummer.                                                                                                       |
| [IWMPPlaylistCollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylistcollection)         | Bearbeitet [IWMPPlaylist- und](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist) [IWMPPlaylistArray-Zeiger.](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylistarray)                                                                                     |
| [IWMPQuery](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)                                   | Stellt eine zusammengesetzte Abfrage dar.                                                                                                                                                              |
| [IWMPRemoteMediaServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)       | Stellt Dienste zum Windows Media Player eines Programms zur Hostung des Player-Steuerelements zur Verfügung. Für die Verwendung mit C++ entwickelt.                                                                        |
| [IWMPRenderConfig](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmprenderconfig)                     | Stellt Methoden zum Angeben oder Abrufen eines Werts zur Auswahl, der angibt, ob die Wiedergabe nur im aktuellen Prozess erfolgt.                                                                          |
| [IWMPSettings](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings)                             | Legt die Einstellungen Windows Media Player oder ruft sie ab.                                                                                                                                          |
| [IWMPSettings2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings2)                           | Legt die Einstellungen Windows Media Player oder ruft sie ab.                                                                                                                                          |
| [IWMPSkinManager](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpskinmanager)                       | Gibt die mit dem -Element verwendete Windows Media Player.                                                                                                                                        |
| [IWMPStringCollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection)             | Zugriff auf eine Auflistung von Zeichenfolgen.                                                                                                                                                         |
| [IWMPStringCollection2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2)           | Stellt Methoden bereit, die die **IWMPStringCollection-Schnittstelle** ergänzen.                                                                                                                  |
| [IWMPSyncDevice](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)                         | Stellt ein Gerät dar, das digitale Mediendateien mit Windows Media Player 10 synchronisieren kann.                                                                                                |
| [IWMPSyncDevice2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice2)                       | Stellt eine Methode bereit, die die **IWMPSyncDevice-Schnittstelle** ergänzt.                                                                                                                      |
| [IWMPSyncServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)                     | Aufzählen verfügbarer Geräte, die digitale Mediendateien mit Windows Media Player 10 synchronisieren können.                                                                                       |
| [IWMPTranscodePolicy](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmptranscodepolicy)               | Stellt eine von DirectShow-Quellfiltern implementierte Methode zum Verwalten der Änderung des Formats digitaler Mediendateien zur Verfügung.                                                                          |
| [IWMPVideoRenderConfig](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig)           | Stellt eine Methode zur Konfiguration des erweiterten Videorenderers zur Verwendung durch Windows Media Player.                                                                                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Objektmodellreferenz für C++**](object-model-reference-for-c.md)
</dt> </dl>

 

 




