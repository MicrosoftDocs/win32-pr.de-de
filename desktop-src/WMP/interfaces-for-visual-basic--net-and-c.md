---
title: Schnittstellen für Visual Basic .NET und C
description: Schnittstellen für Visual Basic .NET und C\
ms.assetid: c66f1e03-20eb-45b1-8710-be9eae63e7ad
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
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a7024c60235b0a545463826fc8948adf3716c9c2d5b491414212d788087404b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862580"
---
# <a name="interfaces-for-visual-basic-net-and-c"></a>Schnittstellen für Visual Basic .NET und C #

In diesem Abschnitt werden die Schnittstellen dokumentiert, die vom Windows Media Player ActiveX-Steuerelement verfügbar gemacht werden.

Mehrere Eigenschaften und Methoden des [AxWindowsMediaPlayer-Objekts](axwindowsmediaplayer-object--vb-and-c.md) werden verwendet, um bestimmte Schnittstellen abzurufen. Diese Schnittstellen verfügen wiederum möglicherweise über Eigenschaften und Zugriffsmethoden zum Abrufen weiterer Schnittstellen.

Das Windows Media Player-Steuerelement macht die folgenden Schnittstellen verfügbar.



| Schnittstelle                                                      | BESCHREIBUNG                                                                                                                                                       |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IWMPCählen](iwmpcdrom--vb-and-c.md)                           | Greift auf eine CD oder DVD auf einem Laufwerk zu.                                                                                                                                  |
| [IWMPCaku Überschreiben](iwmpcdromburn--vb-and-c.md)                   | Stellt Eigenschaften und Methoden zum Verwalten der Erstellung von Audio-CDs bereit.                                                                                                     |
| [IWMPCcollection](iwmpcdromcollection--vb-and-c.md)       | Greift auf eine Sammlung von CD- oder DVD-Laufwerken zu.                                                                                                                        |
| [IWMPCpinRip](iwmpcdromrip--vb-and-c.md)                     | Stellt Eigenschaften und Methoden zum Verwalten von Kopier- oder *Löschspuren* von einer Audio-CD bereit.                                                                         |
| [IWMPClosedCaption](iwmpclosedcaption--vb-and-c.md)           | Bietet eine Möglichkeit zum Einschließen von Untertiteln in eine digitale Mediendatei.                                                                                                     |
| [IWMPClosedCaption2](iwmpclosedcaption2--vb-and-c.md)         | Stellt zusätzliche Untertiteleigenschaften und -methoden bereit.                                                                                                     |
| [IWMPControls](iwmpcontrols--vb-and-c.md)                     | Stellt die Transportsteuerelemente von Windows Media Player dar, z. B. Wiedergabe, Beenden und Anhalten.                                                                         |
| [IWMPControls2](iwmpcontrols2--vb-and-c.md)                   | Stellt eine zusätzliche Steuerelementmethode bereit, um die Wiedergabe auf dem nächsten oder vorherigen Frame einzufrieren.                                                                           |
| [IWMPControls3](iwmpcontrols3--vb-and-c.md)                   | Stellt zusätzliche Steuerelementeigenschaften und -methoden für die Auswahl und Unterstützung der Audiosprache bereit.                                                                      |
| [IWMPDVD](iwmpdvd--vb-and-c.md)                               | Stellt Eigenschaften und Methoden für die Arbeit mit DVDs bereit.                                                                                                            |
| [IWMPError](iwmperror--vb-and-c.md)                           | Greift auf eine Auflistung von [IWMPErrorItem-Schnittstellen](iwmperroritem--vb-and-c.md) zum Abrufen von Fehlerinformationen zu.                                                |
| [IWMPErrorItem](iwmperroritem--vb-and-c.md)                   | Bietet Zugriff auf Fehlerinformationen.                                                                                                                             |
| [IWMPErrorItem2](iwmperroritem2--vb-and-c.md)                 | Stellt eine zusätzliche Fehlerelementeigenschaft zum Abrufen eines Fehlerbedingungscodes bereit.                                                                                   |
| **IWMPFolderMonitorServices**                                  | Wird für die .NET-Programmierung nicht unterstützt.                                                                                                                               |
| [IWMPLibrary](iwmplibrary--vb-and-c.md)                       | Stellt eine Bibliothek dar.                                                                                                                                             |
| [IWMPLibraryServices](iwmplibraryservices--vb-and-c.md)       | Stellt Methoden zum Aufzählen von Bibliotheken bereit.                                                                                                                          |
| **IWMPLibrarySharingServices**                                 | Wird für die .NET-Programmierung nicht unterstützt.                                                                                                                               |
| [IWMPMedia](iwmpmedia--vb-and-c.md)                           | Bietet eine Möglichkeit zum Festlegen und Abrufen der Eigenschaften eines Medienelements.                                                                                                |
| [IWMPMedia2](iwmpmedia2--vb-and-c.md)                         | Ermöglicht den Zugriff auf eine zusätzliche Medienelementeigenschaft.                                                                                                             |
| [IWMPMedia3](iwmpmedia3--vb-and-c.md)                         | Stellt zusätzliche Methoden für den Zugriff auf die Eigenschaften eines Medienelements bereit.                                                                                             |
| [IWMPMediaCollection](iwmpmediacollection--vb-and-c.md)       | Stellt Methoden bereit, die verwendet werden können, um eine große Sammlung von Medienelementen zu organisieren.                                                                                  |
| [IWMPMediaCollection2](iwmpmediacollection2--vb-and-c.md)     | Stellt Methoden bereit, die die **IWMPMediaCollection-Schnittstelle** ergänzen.                                                                                           |
| [IWMPMetadataPicture](iwmpmetadatapicture--vb-and-c.md)       | Stellt Eigenschaften zum Abrufen von Informationen über das Bild bereit, das in einer digitalen Mediendatei enthalten ist, die durch ein **WM/Picture-Metadatenattribut** dargestellt wird.         |
| [IWMPMetadataText](iwmpmetadatatext--vb-and-c.md)             | Stellt Eigenschaften zum Abrufen von Informationen zu komplexen Textmetadatenattributen bereit.                                                                            |
| [IWMPNetwork](iwmpnetwork--vb-and-c.md)                       | Stellt Eigenschaften und Methoden bereit, um auf Statistiken im Zusammenhang mit der Qualität einer Netzwerkverbindung zuzugreifen und die Netzwerkproxyeinstellungen anzugeben und abzurufen.     |
| **IWMPPlayerApplication**                                      | Wird für die .NET-Programmierung nicht unterstützt.                                                                                                                               |
| **IWMPPlayerServices**                                         | Wird für die .NET-Programmierung nicht unterstützt.                                                                                                                               |
| **IWMPPlayerServices2**                                        | Wird für die .NET-Programmierung nicht unterstützt.                                                                                                                               |
| [IWMPPlaylist](iwmpplaylist--vb-and-c.md)                     | Stellt Eigenschaften und Methoden zum Organisieren, Verwalten und Bearbeiten von Medienelementen in einer Wiedergabeliste bereit.                                                                    |
| [IWMPPlaylistArray](iwmpplaylistarray--vb-and-c.md)           | Greift auf eine Auflistung von [IWMPPlaylist-Schnittstellen](iwmpplaylist--vb-and-c.md) nach Indexnummer zu.                                                                   |
| [IWMPPlaylistCollection](iwmpplaylistcollection--vb-and-c.md) | Stellt Methoden zum Bearbeiten von [IWMPPlaylist-](iwmpplaylist--vb-and-c.md) und [IWMPPlaylistArray-Schnittstellen](iwmpplaylistarray--vb-and-c.md) in einer Auflistung bereit. |
| [IWMPQuery](iwmpquery--vb-and-c.md)                           | Stellt eine zusammengesetzte Abfrage dar.                                                                                                                                      |
| [IWMPSettings](iwmpsettings--vb-and-c.md)                     | Stellt Eigenschaften und Methoden bereit, die die Werte Windows Media Player Einstellungen abrufen oder festlegen.                                                                      |
| [IWMPSettings2](iwmpsettings2--vb-and-c.md)                   | Stellt Eigenschaften und eine Methode bereit, die die **IWMPSettings-Schnittstelle** ergänzen.                                                                                  |
| [IWMPStringCollection](iwmpstringcollection--vb-and-c.md)     | Stellt eine Eigenschaft und eine Methode für den Zugriff auf eine Auflistung von Zeichenfolgen nach Indexnummer bereit.                                                                           |
| [IWMPStringCollection2](iwmpstringcollection2--vb-and-c.md)   | Stellt Methoden bereit, die die **IWMPStringCollection-Schnittstelle** ergänzen.                                                                                          |
| **IWMPSyncDevice**                                             | Wird für die .NET-Programmierung nicht unterstützt.                                                                                                                               |
| **IWMPSyncDevice2**                                            | Wird für die .NET-Programmierung nicht unterstützt.                                                                                                                               |
| **IWMPSyncServices**                                           | Wird für die .NET-Programmierung nicht unterstützt.                                                                                                                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Objektmodellreferenz für Visual Basic .NET und C #**](object-model-reference-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 




