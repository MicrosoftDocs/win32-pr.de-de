---
title: Neuerungen in Windows Media Player 11
description: In diesem Thema sind die neuen Features von Windows Media Player 11 und dem Windows Media Player 11 SDK aufgeführt.
ms.assetid: d2a6b6ce-a924-4b55-9dc7-68cc57e5651f
keywords:
- Windows Media Player, Neuerungen
- Windows Media Player, neue Features
- Software Development Kit (SDK), Windows Media Player 11
- SDK (Software Development Kit), Windows Media Player 11
- Dokumentation, Windows Media Player 11 SDK
- Neuerungen, Windows Media Player 11
- neue Features, Windows Media Player 11
- Schnittstellen, neue Features in Windows Media Player 11
- Attribute, neue Features in Windows Media Player 11
- Windows Media Player ActiveX-Steuerelement, neue Features in Version 11
- ActiveX-Steuerelement, neue Features in Version 11
- Skins, neue Features in Windows Media Player 11
- Windows Media Player Skins, neue Features in Version 11
- Plug-ins, neue Features in Windows Media Player 11
- Windows Media Player-Plug-ins, neue Features in Version 11
- Online Stores, neue Features in Windows Media Player 11
- Windows Media Player Online Stores, neue Features in Version 11
- Beispiele, neue Features in Windows Media Player 11
- Versionen von Windows Media Player, neue Features in Version 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12aa728aa1552ac0e65f5825cad62d8e9e0c7300
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104038683"
---
# <a name="what-was-new-in-windows-media-player-11"></a>Neuerungen in Windows Media Player 11

In diesem Thema sind die neuen Features von Windows Media Player 11 und dem Windows Media Player 11 SDK aufgeführt.

## <a name="windows-media-player-control"></a>Windows Media Player-Steuerelement

Die folgenden Schnittstellen waren im Windows Media Player 11-ActiveX-Steuerelement neu.

-   [**Iwmplibrary-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)
-   [**Iwmplibraryservices-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)
-   [**Iwmplibrarysharingservices-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrarysharingservices)
-   [**IWMPMediaCollection2-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2)
-   [**Iwmpquery-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)
-   [**IWMPStringCollection2-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2)
-   [**Mediacollection-Objekt**](mediacollection-object.md)
-   [**Query-Objekt**](query-object.md)
-   [**StringCollection-Objekt**](stringcollection-object.md)
-   [**Iwmpcdromrip-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)
-   [**Iwmpcdromburn-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)
-   [**Iwmpfoldermonitorservices-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
-   [**IWMPSyncDevice2-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice2)
-   [**Iwmpvideorenderconfig-Schnittstelle**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig)
-   [**Iwmpusereventsink**](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpusereventsink)
-   [**IWMPEvents3-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)

## <a name="windows-media-player-skins"></a>Windows Media Player Skins

Die folgenden Skin-Features waren in Windows Media Player 11 neu.

-   Neue Attribute zum Positionieren von Steuerelementen. Weitere Informationen finden Sie unter [**ambientattribute. Right**](ambientattributes-right.md) und [**ambientattribute. Bottom**](ambientattributes-bottom.md).
-   Neue Attribute für die Verschiebung und Größenanpassung von Steuerelementen. Weitere Informationen finden Sie unter [**ambientattribute. muvesizeto**](ambientattributes-movesizeto.md) und [**ambientattribute. slideto**](ambientattributes-slideto.md).
-   Ein neues Attribut zum Angeben des Verhaltens der Bild Größe für die Anpassung. Siehe [**ambientattribute. resizeimages**](ambientattributes-resizeimages.md).
-   Ein neues Attribut zum Angeben der nicht einheitlichen Skalierung eines Skin-Elements. Siehe [**ambientattribute. ninegridmargin**](ambientattributes-ninegridmargins.md).

## <a name="windows-media-player-plug-ins"></a>Windows Media Player-Plug-ins

Das Windows Media Player 11 SDK hat einen neuen Plug-in-Typ zum umrechnen digitaler Mediendatei Formate eingeführt. Weitere Informationen finden Sie unter [Windows Media Player Conversion Plug-ins](windows-media-player-conversion-plug-ins.md)

DSP-Plug-ins, die vor der Veröffentlichung des Windows Media Player 11 SDK erstellt wurden, müssen aktualisiert werden, damit Sie mit Windows Media Player 11 funktionieren. Siehe [Aktualisieren vorhandener DSP-Plug-ins](updating-existing-dsp-plug-ins.md).

Der Windows Media Player-Plug-in-Assistent wurde aktualisiert, um DSP-Plug-ins zu erstellen, die in Windows Media Player 11 funktionieren. Weitere Informationen finden [Sie unter Updates für den DSP-Plug-in-Assistenten für Windows Media Player 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).

## <a name="windows-media-player-online-stores"></a>Windows Media Player Online Stores

In Windows Media Player 11 wurde ein neues Modell für die Integration von Online-Store-Katalogen in das Windows Media Player Library-Feature eingeführt. Siehe [Typ 1 Online Stores](type-1-online-stores.md).

## <a name="windows-media-player"></a>Windows Media Player

Die folgenden Features waren in Windows Media Player 11 neu.

-   [Geräte Erweiterungen für die Berichterstellung über den Inhalt](device-extensions-for-reporting-acquired-content.md)
-   [Geräte Erweiterungen für Wiedergabelisten Objekt Einstellungen](device-extensions-for-playlist-object-preferences.md)

## <a name="windows-media-player-sdk-samples"></a>Windows Media Player SDK-Beispiele

Das c#-Beispiel mit dem Namen schemareader war im Windows Media Player 11 SDK neu. Im Beispiel wird ein Tool erstellt, das das Windows Media Player-Objektmodell verwendet, um Informationen zu Metadaten in der Windows Media Player-Bibliothek oder in einer digitalen Mediendatei abzurufen und anzuzeigen. Das Tool kann die Ergebnisse in einer Textdatei speichern. Das Tool listet die in der Bibliothek gespeicherten metadatenattributnamen für jedes unterstützte Schema (Audiodatei, Video, Wiedergabeliste, Foto usw.) auf. Das Tool kann auch Informationen über verfügbare Attribute für Wiedergabelisten in der Wiedergabelisten Auflistung, CD-Spuren, CD-Inhaltsverzeichnis, DVD-Titel, DVD-Kapitel, DVD-Inhaltsverzeichnis und einzelne Mediendateien bereitstellen.

Das C++-Beispiel namens wmpml wurde im Windows Media Player 11 SDK aktualisiert, um die folgenden Features zu veranschaulichen:

-   Verwenden der neuen [**IWMPStringCollection2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2) -Schnittstelle zum Erstellen einer Benutzeroberfläche ähnlich der Windows Media Player-Bibliotheksfunktion.
-   Verwenden der [**iwmpquery**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery) -und [**IWMPMediaCollection2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2) -Schnittstellen, um zusammengesetzte Abfragen zu erstellen und die Ergebnisse anzuzeigen.

 

 




