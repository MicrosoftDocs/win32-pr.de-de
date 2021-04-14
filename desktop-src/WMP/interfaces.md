---
title: WMP-SDK-Schnittstellen
description: WMP-SDK-Schnittstellen
ms.assetid: 68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd
keywords:
- Windows Media Player, Schnittstellen
- Windows Media Player Mobile, Schnittstellen
- Windows Media Player-Objektmodell, Schnittstellen
- Objektmodell, Schnittstellen
- ActiveX-Steuerelement, Schnittstellen
- Windows Media Player ActiveX-Steuerelement, Schnittstellen
- Windows Media Player Mobile ActiveX-Steuerelement, Schnittstellen
- Verweis für Objektmodell, Schnittstellen
- Schnittstellen Objektmodell-Verweis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffff5a4c609d13d84972989ac32dae1600f5f02d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391362"
---
# <a name="wmp-sdk-interfaces"></a>WMP-SDK-Schnittstellen

In diesem Abschnitt werden die vom Windows Media Player ActiveX-Steuerelement und dem Windows Media Player Mobile ActiveX-Steuerelement verfügbar gemachten com-Schnittstellen dokumentiert.

Die Accessor-Methoden der **iwmpcore** -oder **iwmpplayer** -Schnittstelle werden verwendet, um bestimmte Schnittstellen abzurufen. Diese Schnittstellen können wiederum Zugriffsmethoden zum Abrufen weiterer Schnittstellen aufweisen. Das Aufrufen von **QueryInterface** für eine dieser Schnittstellen ist nur erforderlich, wenn Sie die Basisversion einer Schnittstelle abrufen und eine Methode in einer neueren Version derselben Schnittstelle aufrufen möchten.

> [!Note]  
> Alle Methoden und Ereignisse werden in Windows Media Player 10 Mobile und höher vollständig unterstützt, sofern nicht ausdrücklich anders angegeben.

Das Windows Media Player-Steuerelement macht die folgenden Schnittstellen verfügbar.

| Schnittstelle                                                    | BESCHREIBUNG                                                                                                                                                                               |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_Wmpocxevents](-wmpocxevents-interface.md)                | Stellt Ereignisse aus dem Windows Media Player-Steuerelement bereit, auf das ein Einbett Ende Programm reagieren kann.                                                                              |
| [Iwmpcdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom)                                   | Greift auf eine CD oder DVD in einem Laufwerk zu.                                                                                                                                                          |
| [Iwmpcdromburn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)                           | Stellt Methoden zum Verwalten der Erstellung von AudioCDs bereit.                                                                                                                                            |
| [Iwmpcdromcollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)               | Greift auf eine Auflistung von CD-oder DVD-Laufwerken zu.                                                                                                                                                |
| [Iwmpcdromrip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)                             | Stellt Methoden zum Verwalten des Kopiervorgangs von einer AudioCD bereit.                                                                                                                               |
| [Iwmpclosedcaption](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpclosedcaption)                   | Enthält Beschriftungen mit einem Medien Clip.                                                                                                                                                      |
| [IWMPClosedCaption2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpclosedcaption2)                 | Stellt zusätzliche Methoden für geschlossene Untertitel bereit.                                                                                                                                            |
| [Iwmpcontrols](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols)                             | Stellt die Transport Steuerelemente von Windows-Media Player dar, z. b. Wiedergabe, anhalten und anhalten.                                                                                                 |
| [IWMPControls2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2)                           | Stellt zusätzliche Steuerungsmethoden bereit.                                                                                                                                                      |
| [IWMPControls3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols3)                           | Stellt zusätzliche Steuerungsmethoden bereit.                                                                                                                                                      |
| [Iwmpcore](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore)                                     | Ruft Zeiger auf andere Schnittstellen ab und greift auf grundlegende Funktionen des-Steuer Elements zu. Dies ist die Stamm Schnittstelle für das Windows Media Player-Objektmodell.                                  |
| [IWMPCore2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore2)                                   | Stellt zusätzliche Kern Methoden bereit.                                                                                                                                                         |
| [IWMPCore3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore3)                                   | Stellt zusätzliche Kern Methoden bereit.                                                                                                                                                         |
| [Iwmpdvd](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpdvd)                                       | Greift auf das Inhalts Menü einer DVD zu.                                                                                                                                                       |
| [Iwmperror](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperror)                                   | Greift auf eine Auflistung von [iwmperroritem](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperroritem) -Zeigern zu.                                                                                                                     |
| [Iwmperroritem](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperroritem)                           | Stellt Informationen zu Fehlern bereit.                                                                                                                                                        |
| [IWMPErrorItem2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperroritem2)                         | Stellt zusätzliche Fehler Element Methoden bereit.                                                                                                                                                   |
| [Iwmpevents](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)                       | Macht Ereignisse verfügbar, die aus dem Windows Media Player-Steuerelement stammen, auf das ein Einbettungs Programm reagieren kann.                                                                            |
| [IWMPEvents2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)                     | Macht Ereignisse verfügbar, die vom Windows Media Player 10-Steuerelement stammen, auf das ein Einbettungs Programm reagieren kann. Diese Ereignisse werden speziell für Geräte Synchronisierungs Programme verwendet. |
| [IWMPEvents3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)                               | Stellt Ereignisse im Zusammenhang mit CD-Ripping, CD-brennen, Ordner Überwachung und Remote Bibliotheksdiensten bereit.                                                                                        |
| [Iwmpfoldermonitorservices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)   | Stellt Methoden zum Aufzählen, Scannen und Ändern von Datei Ordnern bereit, die von Windows Media Player für den Inhalt digitaler Medien überwacht werden.                                                                |
| [Iwmpgraphcreation](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpgraphcreation)                   | Verwaltet das DirectShow-Diagramm.                                                                                                                                                             |
| [Iwmplibrary](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)                               | Stellt eine Bibliothek dar.                                                                                                                                                                     |
| [Iwmplibraryservices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)               | Stellt Methoden zum Aufzählen von Bibliotheken bereit.                                                                                                                                                  |
| [Iwmplibrarysharingservices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrarysharingservices) | Stellt Methoden zum Verwalten der Bibliotheks Freigabe bereit.                                                                                                                                               |
| [Iwmpmedia](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)                                   | Legt die Eigenschaften eines Medien Elements fest und ruft Sie ab.                                                                                                                                        |
| [IWMPMedia2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia2)                                 | Stellt zusätzliche Methoden zum Festlegen und Abrufen der Eigenschaften eines Medien Elements bereit.                                                                                                           |
| [IWMPMedia3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia3)                                 | Stellt zusätzliche Methoden zum Festlegen und Abrufen der Eigenschaften eines Medien Elements bereit.                                                                                                           |
| [Iwmpmediacollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection)               | Greift auf eine Auflistung von [iwmpmedia](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) -Zeigern zu.                                                                                                                             |
| [IWMPMediaCollection2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2)             | Stellt Methoden bereit, die die **iwmpmediacollection** -Schnittstelle ergänzen.                                                                                                                   |
| [IWMPMetadataPicture](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmetadatapicture)               | Ruft Informationen zum **WM/Bild-** Metadatenattribut ab.                                                                                                                        |
| [IWMPMetadataText](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmetadatatext)                     | Ruft Informationen zu komplexen textmetadatenattributen ab.                                                                                                                          |
| [Iwmpnetwork](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpnetwork)                               | Legt die Eigenschaften der von Windows Media Player verwendeten Netzwerkverbindung fest und ruft Sie ab.                                                                                                 |
| [Iwmpplayer](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer)                                 | Steuert das Verhalten der Benutzeroberfläche des Windows Media Player-Steuer Elements.                                                                                                                 |
| [IWMPPlayer2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer2)                               | Stellt zusätzliche Methoden zum Steuern von Windows-Media Player bereit.                                                                                                                         |
| [IWMPPlayer3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer3)                               | Stellt zusätzliche Methoden zum Steuern von Windows-Media Player bereit.                                                                                                                         |
| [IWMPPlayer4](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer4)                               | Stellt zusätzliche Methoden zum Steuern von Windows-Media Player bereit.                                                                                                                         |
| [Iwmpplayerapplication](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerapplication)           | Wechselt zwischen einem remoten Windows Media Player-Steuerelement und dem vollständigen Modus des Players. Entwickelt für die Verwendung durch C++-Programme, die das-Steuerelement im Remote Modus einbetten.                          |
| [Iwmpplayerservices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)                 | Wird vom Host eines remoten Steuer Elements verwendet, um den vollständigen Modus von Windows-Media Player zu bearbeiten. Entwickelt für die Verwendung mit C++.                                                                     |
| [IWMPPlayerServices2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices2)               | Legt die Priorität der Hintergrundverarbeitung fest.                                                                                                                                                  |
| [Iwmpwiedergabe](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)                             | Erstellt und verwaltet Wiedergabelisten.                                                                                                                                                            |
| [Iwmpplaylistarray](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylistarray)                   | Greift über die Indexnummer auf eine Auflistung von [iwmpwiedergabe](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist) Zeigern zu.                                                                                                       |
| [Iwmpplaylistcollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylistcollection)         | Bearbeitet die Zeiger [iwmpwiedergabe](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist) und [iwmpplaylistarray](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylistarray) .                                                                                     |
| [Iwmpquery](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)                                   | Stellt eine Verbund Abfrage dar.                                                                                                                                                              |
| [Iwmpremotemediaservices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)       | Stellt Dienste für Windows-Media Player von einem Programm bereit, das das Player-Steuerelement hostet. Entwickelt für die Verwendung mit C++.                                                                        |
| [Iwmprenderconfig](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmprenderconfig)                     | Stellt Methoden bereit, um einen Wert anzugeben oder abzurufen, der angibt, ob die Wiedergabe nur im aktuellen Prozess stattfindet.                                                                          |
| [Iwmpsettings](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings)                             | Legt Windows Media Player Einstellungen fest oder ruft diese ab.                                                                                                                                          |
| [IWMPSettings2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings2)                           | Legt Windows Media Player Einstellungen fest oder ruft diese ab.                                                                                                                                          |
| [Iwmpskinmanager](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpskinmanager)                       | Gibt die mit Windows-Media Player verwendete Skin an.                                                                                                                                        |
| [Iwmpstringcollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection)             | Greift auf eine Auflistung von Zeichen folgen zu.                                                                                                                                                         |
| [IWMPStringCollection2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2)           | Stellt Methoden bereit, die die **iwmpstringcollection** -Schnittstelle ergänzen.                                                                                                                  |
| [Iwmpsyncdevice](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)                         | Stellt ein Gerät dar, das digitale Mediendateien mit Windows Media Player 10 synchronisieren kann.                                                                                                |
| [IWMPSyncDevice2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice2)                       | Stellt eine Methode bereit, die die **iwmpsyncdevice** -Schnittstelle ergänzt.                                                                                                                      |
| [Iwmpsyncservices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)                     | Listet die verfügbaren Geräte auf, die digitale Mediendateien mit Windows Media Player 10 synchronisieren können.                                                                                       |
| [Iwmptranscodepolicy](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmptranscodepolicy)               | Stellt eine Methode bereit, die von DirectShow-Quell Filtern implementiert wird, um das Ändern des Formats digitaler Mediendateien zu verwalten.                                                                          |
| [Iwmpvideorenderconfig](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig)           | Stellt eine Methode bereit, mit der der von Windows Media Player verwendete erweiterte Videorenderer konfiguriert wird.                                                                                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Objektmodell Referenz für C++**](object-model-reference-for-c.md)
</dt> </dl>

 

 




