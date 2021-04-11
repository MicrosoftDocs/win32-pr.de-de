---
title: Schnittstellen für Visual Basic .net und C
description: Schnittstellen für Visual Basic .net und C \
ms.assetid: c66f1e03-20eb-45b1-8710-be9eae63e7ad
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
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a301cb075ccee049272f1db9b2582aeae6697fa3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207030"
---
# <a name="interfaces-for-visual-basic-net-and-c"></a>Schnittstellen für Visual Basic .net und C #

In diesem Abschnitt werden die vom Windows Media Player ActiveX-Steuerelement verfügbar gemachten Schnittstellen dokumentiert.

Zum Abrufen bestimmter Schnittstellen werden verschiedene Eigenschaften und Methoden des [AxWindowsMediaPlayer-Objekts](axwindowsmediaplayer-object--vb-and-c.md) verwendet. Diese Schnittstellen können wiederum Eigenschaften und Accessormethoden aufweisen, um weitere Schnittstellen abzurufen.

Das Windows Media Player-Steuerelement macht die folgenden Schnittstellen verfügbar.



| Schnittstelle                                                      | BESCHREIBUNG                                                                                                                                                       |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Iwmpcdrom](iwmpcdrom--vb-and-c.md)                           | Greift auf eine CD oder DVD in einem Laufwerk zu.                                                                                                                                  |
| [Iwmpcdromburn](iwmpcdromburn--vb-and-c.md)                   | Stellt Eigenschaften und Methoden zum Verwalten der Erstellung von AudioCDs bereit.                                                                                                     |
| [Iwmpcdromcollection](iwmpcdromcollection--vb-and-c.md)       | Greift auf eine Auflistung von CD-oder DVD-Laufwerken zu.                                                                                                                        |
| [Iwmpcdromrip](iwmpcdromrip--vb-and-c.md)                     | Stellt Eigenschaften und Methoden zum Verwalten von Kopier-oder *einreißen*-Spuren von einer AudioCD bereit.                                                                         |
| [Iwmpclosedcaption](iwmpclosedcaption--vb-and-c.md)           | Bietet eine Möglichkeit zum Einschließen von Untertiteln in eine digitale Mediendatei.                                                                                                     |
| [IWMPClosedCaption2](iwmpclosedcaption2--vb-and-c.md)         | Stellt zusätzliche Eigenschaften und Methoden für Untertitel bereit.                                                                                                     |
| [Iwmpcontrols](iwmpcontrols--vb-and-c.md)                     | Stellt die Transport Steuerelemente von Windows-Media Player dar, z. b. Wiedergabe, anhalten und anhalten.                                                                         |
| [IWMPControls2](iwmpcontrols2--vb-and-c.md)                   | Stellt eine zusätzliche Steuerungsmethode zum Fixieren der Wiedergabe für den nächsten oder vorherigen Frame bereit.                                                                           |
| [IWMPControls3](iwmpcontrols3--vb-and-c.md)                   | Stellt zusätzliche Steuerungseigenschaften und-Methoden für die Auswahl und Unterstützung der Audiosprache bereit.                                                                      |
| [Iwmpdvd](iwmpdvd--vb-and-c.md)                               | Stellt Eigenschaften und Methoden zum Arbeiten mit DVDs bereit.                                                                                                            |
| [Iwmperror](iwmperror--vb-and-c.md)                           | Greift auf eine Auflistung von [iwmperroritem](iwmperroritem--vb-and-c.md) -Schnittstellen zum Abrufen von Fehlerinformationen zu.                                                |
| [Iwmperroritem](iwmperroritem--vb-and-c.md)                   | Bietet Zugriff auf Fehlerinformationen.                                                                                                                             |
| [IWMPErrorItem2](iwmperroritem2--vb-and-c.md)                 | Stellt eine zusätzliche Fehler Element Eigenschaft zum erhalten eines Fehler Bedingungs Codes bereit.                                                                                   |
| **Iwmpfoldermonitorservices**                                  | Wird für die .NET-Programmierung nicht unterstützt.                                                                                                                               |
| [Iwmplibrary](iwmplibrary--vb-and-c.md)                       | Stellt eine Bibliothek dar.                                                                                                                                             |
| [Iwmplibraryservices](iwmplibraryservices--vb-and-c.md)       | Stellt Methoden zum Aufzählen von Bibliotheken bereit.                                                                                                                          |
| **Iwmplibrarysharingservices**                                 | Wird für die .NET-Programmierung nicht unterstützt.                                                                                                                               |
| [Iwmpmedia](iwmpmedia--vb-and-c.md)                           | Bietet eine Möglichkeit zum Festlegen und Abrufen der Eigenschaften eines Medien Elements.                                                                                                |
| [IWMPMedia2](iwmpmedia2--vb-and-c.md)                         | Ermöglicht den Zugriff auf eine zusätzliche Medien Element Eigenschaft.                                                                                                             |
| [IWMPMedia3](iwmpmedia3--vb-and-c.md)                         | Stellt zusätzliche Methoden für den Zugriff auf die Eigenschaften eines Medien Elements bereit.                                                                                             |
| [Iwmpmediacollection](iwmpmediacollection--vb-and-c.md)       | Stellt Methoden bereit, die verwendet werden können, um eine große Auflistung von Medien Elementen zu organisieren.                                                                                  |
| [IWMPMediaCollection2](iwmpmediacollection2--vb-and-c.md)     | Stellt Methoden bereit, die die **iwmpmediacollection** -Schnittstelle ergänzen.                                                                                           |
| [IWMPMetadataPicture](iwmpmetadatapicture--vb-and-c.md)       | Stellt Eigenschaften bereit, mit denen Informationen zu dem Bild, das in einer digitalen Mediendatei enthalten ist, die durch ein **WM/Bild-** Metadatenattribut dargestellt wird, erhalten         |
| [IWMPMetadataText](iwmpmetadatatext--vb-and-c.md)             | Stellt Eigenschaften zum erhalten von Informationen zu komplexen textmetadatenattributen bereit.                                                                            |
| [Iwmpnetwork](iwmpnetwork--vb-and-c.md)                       | Stellt Eigenschaften und Methoden für den Zugriff auf Statistiken in Bezug auf die Qualität einer Netzwerkverbindung sowie zum angeben und Abrufen der Netzwerk Proxy Einstellungen bereit.     |
| **Iwmpplayerapplication**                                      | Wird für die .NET-Programmierung nicht unterstützt.                                                                                                                               |
| **Iwmpplayerservices**                                         | Wird für die .NET-Programmierung nicht unterstützt.                                                                                                                               |
| **IWMPPlayerServices2**                                        | Wird für die .NET-Programmierung nicht unterstützt.                                                                                                                               |
| [Iwmpwiedergabe](iwmpplaylist--vb-and-c.md)                     | Stellt Eigenschaften und Methoden bereit, um Medienelemente in einer Wiedergabeliste zu organisieren, zu verwalten und zu bearbeiten.                                                                    |
| [Iwmpplaylistarray](iwmpplaylistarray--vb-and-c.md)           | Greift nach Indexnummer auf eine Auflistung von [iwmpwiedergabe](iwmpplaylist--vb-and-c.md) -Schnittstellen zu.                                                                   |
| [Iwmpplaylistcollection](iwmpplaylistcollection--vb-and-c.md) | Stellt Methoden zum Bearbeiten von [iwmpwiedergabe](iwmpplaylist--vb-and-c.md) -und [iwmpplaylistarray](iwmpplaylistarray--vb-and-c.md) -Schnittstellen in einer-Auflistung bereit. |
| [Iwmpquery](iwmpquery--vb-and-c.md)                           | Stellt eine Verbund Abfrage dar.                                                                                                                                      |
| [Iwmpsettings](iwmpsettings--vb-and-c.md)                     | Stellt Eigenschaften und Methoden bereit, mit denen die Werte von Windows Media Player-Einstellungen angezeigt oder festgelegt werden.                                                                      |
| [IWMPSettings2](iwmpsettings2--vb-and-c.md)                   | Stellt Eigenschaften und eine Methode bereit, die die **iwmpsettings** -Schnittstelle ergänzen.                                                                                  |
| [Iwmpstringcollection](iwmpstringcollection--vb-and-c.md)     | Stellt eine Eigenschaft und eine Methode für den Zugriff auf eine Auflistung von Zeichen folgen anhand der Indexnummer bereit.                                                                           |
| [IWMPStringCollection2](iwmpstringcollection2--vb-and-c.md)   | Stellt Methoden bereit, die die **iwmpstringcollection** -Schnittstelle ergänzen.                                                                                          |
| **Iwmpsyncdevice**                                             | Wird für die .NET-Programmierung nicht unterstützt.                                                                                                                               |
| **IWMPSyncDevice2**                                            | Wird für die .NET-Programmierung nicht unterstützt.                                                                                                                               |
| **Iwmpsyncservices**                                           | Wird für die .NET-Programmierung nicht unterstützt.                                                                                                                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Objektmodell Referenz für Visual Basic .net und C #**](object-model-reference-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 




