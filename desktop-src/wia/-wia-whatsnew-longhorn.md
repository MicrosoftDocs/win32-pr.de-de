---
description: Viele neue WIA-APIs (Windows Image Acquisition) sind in Windows-Abbild Beschaffung (WIA) 2,0 enthalten.
ms.assetid: d8e85c34-d8ce-4512-af71-102a21393fdf
title: Neues bei der Windows-Abbild Beschaffung (WIA) 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97f9d225185b8f1ff2d6441a7ddf0e8fd919ac98
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106363896"
---
# <a name="whats-new-in-windows-image-acquisition-wia-20"></a>Neues bei der Windows-Abbild Beschaffung (WIA) 2,0

Viele neue WIA-APIs (Windows Image Acquisition) sind in Windows-Abbild Beschaffung (WIA) 2,0 enthalten. Außerdem gibt es einige vorwärts-und abwärts Inkompatibilitäten zwischen der Windows-Abbild Beschaffung (WIA) 1,0 und dem WIA 2,0-Dienst, der im Lieferumfang von Windows Vista enthalten ist. Einige Schnittstellen, Strukturen, Eigenschaften und Eigenschaftswerte von WIA 1,0 werden von nicht unterstützt, und Anwendungen, die Sie verwenden, können unter, Windows Vista und höher nicht ausgeführt werden. Ebenso können Anwendungen, die die neuen Schnittstellen, Strukturen, Eigenschaften und Eigenschaftswerte verwenden, die mit WIA 2,0 eingeführt wurden (siehe unten), nicht auf Betriebssystemversionen vor Windows Vista ausgeführt werden.

## <a name="new-api-for-wia-20"></a>Neue API für WIA 2,0

### <a name="constants-lists-updated-for-wia-20"></a>Konstanten: für WIA 2,0 aktualisierte Listen

-   [**Allgemeine WIA-Element Eigenschaften Konstanten**](-wia-wiaitempropcommonitem.md)
-   [**Eigenschaften Konstanten für Geräteinformationen**](-wia-wiadeviceinfoprop.md)
-   [**Eigenschaften Konstanten für Scanner-Geräte**](-wia-wiaitempropscannerdevice.md)
-   [**Eigenschaften Konstanten für Scanner-WIA-Elemente**](-wia-wiaitempropscanneritem.md)
-   [**WIA 2,0-Element Kategorie-GUIDs**](-wia-wia2-itemcategoryguids.md)
-   [**WIA 2,0 Seitengrößen Konstanten**](-wia-wia2-pagesizeconstants.md)
-   [**WIA-Elementtyp-Flags**](-wia-wia-item-type-flags.md)

### <a name="new-structures-in-wia-20"></a>Neue Strukturen in WIA 2,0



| Thema                                               | Inhalte                                                                                                                                                                                                                                                          |
|-----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DEVICEDIALOGDATA2**](-wia-devicedialogdata2.md) | Definiert die Daten, die zum Abrufen eines Geräte Dialogfelds erforderlich sind.<br/>                                                                                                                                                                                                       |
| [**WIA \_ - \_ rohheader**](-wia-wia-raw-header.md)     | Die [**WIA \_ - \_ rohheaderstruktur**](-wia-wia-raw-header.md) definiert ein Bild im Rohdaten Format eines Geräts und ermöglicht Anwendungen das Verwenden des RAW-Formats in WIA-Übertragungen.<br/>                                                                         |
| [**Wiatransferparameams**](-wia-wiatransferparams.md) | Der [**wiatransferparameams**](-wia-wiatransferparams.md) wird während einer Datenübertragung durch das WIA-Laufzeitsystem an die [**iwiatransfercallback:: transfercallback**](-wia-iwiatransfercallback-transfercallback.md) -Methode an eine Anwendung übertragen.<br/> |



 

### <a name="new-interfaces-in-wia-20"></a>Neue Schnittstellen in WIA 2,0



| Thema                                                         | Inhalte                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)                   | Wird von Anwendungen verwendet, um [**IWiaItem2**](-wia-iwiaitem2.md) -Objekte im aktuellen Ordner der Elementstruktur aufzulisten.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| [**Iscanprofile**](-wia-iscanprofile.md)                     | Die [**iscanprofile**](-wia-iscanprofile.md) -Schnittstelle stellt ein einzelnes Überprüfungs Profil dar und ermöglicht Anwendungen das Festlegen und Abrufen der Eigenschaften des Profils. <br/>                                                                                                                                                                                                                                                                                                                                   |
| [**Iscanprofilemgr**](-wia-iscanprofilemgr.md)               | Die [**iscanprofilemgr**](-wia-iscanprofilemgr.md) -Schnittstelle stellt Methoden zum Erstellen, öffnen, löschen und Verwalten von Scan Profilen bereit. <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**Iscanprofileui**](-wia-iscanprofileui.md)                 | Mithilfe der [**iscanprofileui**](-wia-iscanprofileui.md) -Schnittstelle können Anwendungen ein Dialogfeld anzeigen, sodass Benutzer Scan Profile erstellen, ändern und löschen können.<br/>                                                                                                                                                                                                                                                                                                                               |
| [**Iwiaapperrorhandler**](-wia-iwiaapperrorhandler.md)       | Mithilfe der [**iwiaapperrorhandler**](-wia-iwiaapperrorhandler.md) -Schnittstelle können Anwendungen Fehler Fenster (während der Datenübertragungen) anzeigen, von denen der Benutzer auswählen kann, ob die Übertragung fortgesetzt, abgebrochen oder abgebrochen werden soll.<br/>                                                                                                                                                                                                                                                                     |
| [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)                       | Die [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) -Schnittstelle wird verwendet, um Abbild Erfassungsgeräte zu erstellen und zu verwalten sowie zum Empfangen von Geräte Ereignissen zu registrieren.<br/>                                                                                                                                                                                                                                                                                                                                             |
| [**Iwiaerrorhandler**](-wia-iwiaerrorhandler.md)             | Die [**iwiaerrorhandler**](-wia-iwiaerrorhandler.md) -Schnittstelle stellt Methoden bereit, um Fehler zu behandeln, die auftreten können, wenn eine Anwendung Bilddaten anfordert, ob für die Vorschau oder die endgültige Bits. <br/>                                                                                                                                                                                                                                                                                                      |
| [**Iwiaimagefilter**](-wia-iwiaimagefilter.md)               | Die [**iwiaimagefilter**](-wia-iwiaimagefilter.md) -Schnittstelle ist eine durch Bild Verarbeitungs Filter-Entwickler implementierte Erweiterungsschnittstelle, die von WIA 2,0 aufgerufen wird. <br/>                                                                                                                                                                                                                                                                                                                                  |
| [**IWiaItem2**](-wia-iwiaitem2.md)                           | Die [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstelle bietet Anwendungen die gleiche Funktionalität wie die [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -Schnittstelle (die Möglichkeit zum Abfragen von Geräten, um ihre Funktionen zu ermitteln, auf Datenübertragungs Schnittstellen und Element Eigenschaften zuzugreifen und das Gerät zu steuern). Außerdem bietet die Anwendung die Möglichkeit, Bild Verarbeitungs Filter dynamisch zu erstellen und zu verwenden, die als Erweiterungen der WIA 2,0-Gerätetreiber in Windows Vista bereitgestellt werden können.<br/> |
| [**Iwiapreview**](-wia-iwiapreview.md)                       | Die [**iwiapreview**](-wia-iwiapreview.md) -Schnittstelle speichert ungefilterte Bilder intern zwischen und übergibt sie durch Bild Verarbeitungs Filter. <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**Iwiasegmentationfilter**](-wia-iwiasegmentationfilter.md) | Die [**iwiasegmentationfilter**](-wia-iwiasegmentationfilter.md) -Schnittstelle erkennt Unterbereiche eines bildstreams und stellt separate [**IWiaItem2**](-wia-iwiaitem2.md) Items für jede dar. <br/>                                                                                                                                                                                                                                                                                                         |
| [**Iwiatransfer**](-wia-iwiatransfer.md)                     | Die [**iwiatransfer**](-wia-iwiatransfer.md) -Schnittstelle stellt Datenstrom basierte Übertragung von Daten bereit. <br/>                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**Iwiatransfercallback**](-wia-iwiatransfercallback.md)     | Die [**iwiatransfercallback**](-wia-iwiatransfercallback.md) -Schnittstelle empfängt Rückrufe während einer Datenübertragung. <br/>                                                                                                                                                                                                                                                                                                                                                                                |
| [**IWiaUIExtension2**](-wia-iwiauiextension2.md)             | Die IWiaUIExtension2-Schnittstelle stellt Methoden bereit, die die vom System bereitgestellte Standardbenutzer Oberfläche durch eine benutzerdefinierte Benutzeroberfläche ersetzen und ein benutzerdefiniertes Gerätesymbol bereitstellen. Gerätehersteller können diese Schnittstelle implementieren, um benutzerdefinierte Benutzeroberflächen für Ihre Geräte bereitzustellen.<br/>                                                                                                                                                                                                                     |



 

### <a name="new-and-changed-overviews-for-wia-20"></a>Neue und geänderte Übersichten für WIA 2,0



| Thema                                                                          | Inhalte |
|--------------------------------------------------------------------------------|----------|
| [Konstanten](-wia-constants.md)                                                |          |
| [Funktionen](-wia-functions.md)                                                |          |
| [Schnittstellen](-wia-interfaces.md)                                              |          |
| [Profil Schema überprüfen](-wia-scan-profile-schema.md)                            |          |
| [Strukturen](-wia-structures.md)                                              |          |
| [Übertragen von Bilddaten in WIA 2,0](-wia-transferring-image-data-in-wia2.md) |          |
| [WIA-Gerätetyp spezifiker](-wia-wia-device-type-specifiers.md)              |          |
| [WIA-Eigenschafts Konstanten](-wia-wia-property-constants.md)                      |          |



 

## <a name="leave-feedback"></a>Feedback hinterlassen

Senden **sdkfdbk@microsoft.com** Sie eine E-Mail, um Fehlerberichte und Featureanforderungen direkt an Microsoft zu senden.

 

 




