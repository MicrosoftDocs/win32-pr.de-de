---
title: Unterstützung für benutzerdefinierte Images für Geräte
description: Unterstützung für benutzerdefinierte Images für Geräte
ms.assetid: 0ccc327c-e953-4348-9802-705331b574ac
keywords:
- Windows Media Player, Unterstützung für benutzerdefinierte Images für Geräte
- Windows Media Player, Abbild Unterstützung für Geräte
- Unterstützung für benutzerdefinierte Geräte Images
- Unterstützung für benutzerdefinierte Images für Geräte
- imageunterstützung für Geräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ffdf318df39935e844cc84919bb4d6e50cc259a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106342358"
---
# <a name="custom-image-support-for-devices"></a>Unterstützung für benutzerdefinierte Images für Geräte

> [!Note]  
> In diesem Abschnitt wird ein Feature von Windows Media Player 10 dokumentiert, das verfügbar ist, wenn das Betriebssystem Windows XP verwendet wird. Er ist möglicherweise in nachfolgenden Versionen nicht verfügbar.

 

Gerätehersteller können zwei spezielle Bilddateien bereitstellen, um die Art und Weise anzupassen, wie ein Gerät in der Windows Media Player 10-Benutzeroberfläche dargestellt wird. Diese beiden Dateien lauten:

-   "Debug". Eine Windows-Symbol Format Datei, die die Gerätehardware darstellt. Dieses Bild wird in Windows Media Player 10 angezeigt, wo ein Symbol zur Darstellung eines Geräts verwendet wird, z. b. die Geräteliste in der **Synchronisierungs** Funktion.
-   Devlogo. fil. Eine PNG-Format Datei, die das Firmenlogo des Geräteherstellers darstellt. Dieses Bild wird in Windows Media Player 10, wo das Unternehmens Branding verwendet wird, z. b. im Dialogfeld " **Geräte Einrichtung** ", angezeigt.

## <a name="general-guidelines-for-images"></a>Allgemeine Richtlinien für Images

Die folgenden Richtlinien gelten für die Unterstützung für benutzerdefinierte Images im allgemeinen:

-   Dieses Feature ist optional. Geräte, die keine Abbilder bereitstellen, werden standardmäßig dargestellt.
-   Diese Funktion wird nur für MTP-aktivierte Geräte unterstützt.
-   Um Änderungen an den Dateien zu verhindern, empfiehlt es sich, die Bilddateien in der Firmware oder einem geschützten Speichermedium (nicht mit vom Benutzer erstellten Dateien) zu speichern.
-   Die Dateien sollten nicht an Windows Media Device Manager-Clients zurückgegeben werden, die den Stamm Speicher des Geräts auflisten. Außerdem sollte das Löschen, verschieben oder Umbenennen der Dateien fehlschlagen.
-   Wenn das Gerät mehr als ein Speichermedium bereitstellt, sollte das Gerät die Bilddateien als Reaktion auf Datei Öffnungs Anforderungen von einem beliebigen Medium zurückgeben. Verschiedene Geräte Symbole können von jedem Speichermedium zurückgegeben werden.
-   Bei Windows Media Device Manager 1,2-fähigen Clients haben diese Images Vorrang vor Symbol Eigenschaften, die von Windows-Setup Mechanismen, z. b. Geräteknoten Eigenschaften, bereitgestellt werden.
-   Die Bilder dürfen keine Informationen enthalten, die eine Lokalisierung erfordern.
-   Bei Geräten mit mehreren Funktionen werden diese Images nur für die Musikwiedergabe Features von Windows XP verwendet.

## <a name="creating-the-device-icon-image"></a>Erstellen des Gerätesymbol Bilds

Die Gerätesymbol-Bilddatei Devicon. fil muss eine Datei im Windows-Symbol Format enthalten. In den MSDN-Artikel [Symbolen in Win32](/previous-versions/ms997538(v=msdn.10)) wird beschrieben, wie eine solche Datei erstellt wird. Der MSDN-Artikel [Erstellen von Windows XP-Symbolen](/previous-versions/ms997636(v=msdn.10)) bietet Stilrichtlinien für Windows XP-Symbole. Die Gerätesymbol-Bilddatei enthält zwölf Bilder in einer einzelnen Datei, indem vier verschiedene Größen mit jeweils drei unterschiedlichen Farbtiefen bereitgestellt werden.

Achten Sie besonders auf die folgenden Richtlinien:

-   Empfohlene Größen (in Pixel) sind 16x16, 32x32, 48x48 und 256x256.
-   Empfohlene Farbtiefe sind 24 Bit mit 8-Bit-Alphakanal, 8-Bit-Transparenz und 1-Bit-Transparenz und 4 Bit mit 1-Bit-Transparenz.
-   Verwenden Sie die in den zuvor erwähnten MSDN-Artikeln beschriebenen Empfehlungen Perspektive Angle und Drop Shadow.

Nachdem Sie die Symbol Datei erstellt haben, benennen Sie Sie einfach Devicon. fil um.

## <a name="creating-the-corporate-logo-image"></a>Erstellen des Firmen Logo Bilds

Die Bilddatei für das Firmenlogo, devlogo. fil, muss eine Datei im PNG-Format enthalten. Beachten Sie beim Erstellen des Images die folgenden Richtlinien:

-   Die maximalen Abmessungen für das Bild sind 150 x 32 Pixel.
-   Das Bild sollte Alpha Blending unterstützen, um einen reibungslosen Übergang zwischen der Windows Media Player 10-Benutzeroberfläche und dem Logo zu ermöglichen.

Nachdem Sie die Firmenlogo Datei erstellt haben, benennen Sie Sie einfach "devlogo. fil" um.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Windows Media Player**](windows-media-player.md)
</dt> </dl>

 

 