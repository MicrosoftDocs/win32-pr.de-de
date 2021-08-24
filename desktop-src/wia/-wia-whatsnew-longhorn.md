---
description: Viele neue Windows WIA-API (Image Acquisition) sind in Windows Image Acquisition (WIA) 2.0 enthalten.
ms.assetid: d8e85c34-d8ce-4512-af71-102a21393fdf
title: Neues bei Windows Image Acquisition (WIA) 2.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fef5fdc2f70c7b0a7c25e3e9df68b82d05b7fd1a53eb7ec3613962f975e5c1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592950"
---
# <a name="whats-new-in-windows-image-acquisition-wia-20"></a>Neues bei Windows Image Acquisition (WIA) 2.0

Viele neue Windows WIA-API (Image Acquisition) sind in Windows Image Acquisition (WIA) 2.0 enthalten. Darüber hinaus gibt es einige Vorwärts- und Abwärtsinkompatibilitäten zwischen Windows Image Acquisition (WIA) 1.0 und dem WIA 2.0-Dienst, der mit Windows Vista Windows wird. Einige Schnittstellen, Strukturen, Eigenschaften und Eigenschaftswerte von WIA 1.0 werden von nicht unterstützt, und Anwendungen, die sie verwenden, werden nicht unter Windows Vista und höher ausgeführt. Ebenso werden Anwendungen, die die neuen Schnittstellen, Strukturen, Eigenschaften und Eigenschaftswerte verwenden, die mit WIA 2.0 eingeführt wurden (siehe unten), nicht unter Betriebssystemversionen vor Windows Vista ausgeführt.

## <a name="new-api-for-wia-20"></a>Neue API für WIA 2.0

### <a name="constants-lists-updated-for-wia-20"></a>Konstanten: Für WIA 2.0 aktualisierte Listen

-   [**Allgemeine WIA-Elementeigenschaftskonst constants**](-wia-wiaitempropcommonitem.md)
-   [**Eigenschaftenkonst constants für Geräteinformationen**](-wia-wiadeviceinfoprop.md)
-   [**Eigenschaftenkonst constants des Scannergeräts**](-wia-wiaitempropscannerdevice.md)
-   [**WiA-Elementeigenschaftskonst constants (WIA-Elementeigenschaftskonst constants) für**](-wia-wiaitempropscanneritem.md)
-   [**WIA 2.0-Elementkategorie-GUIDs**](-wia-wia2-itemcategoryguids.md)
-   [**WIA 2.0-Seitengrößenkonst constants**](-wia-wia2-pagesizeconstants.md)
-   [**WIA-Elementtypflags**](-wia-wia-item-type-flags.md)

### <a name="new-structures-in-wia-20"></a>Neue Strukturen in WIA 2.0



| Thema                                               | Inhalte                                                                                                                                                                                                                                                          |
|-----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DEVICEDIALOGDATA2**](-wia-devicedialogdata2.md) | Definiert die Daten, die zum Aufrufen eines Gerätedialogfelds erforderlich sind.<br/>                                                                                                                                                                                                       |
| [**\_ \_ WIA-RAW-HEADER**](-wia-wia-raw-header.md)     | Die [**WIA \_ RAW \_ HEADER-Struktur**](-wia-wia-raw-header.md) definiert ein Bild im RAW-Datenformat eines Geräts und ermöglicht Anwendungen die Verwendung des RAW-Formats bei WIA-Übertragungen.<br/>                                                                         |
| [**WiaTransferParams**](-wia-wiatransferparams.md) | [**WiaTransferParams**](-wia-wiatransferparams.md) wird während einer Datenübertragung durch das WIA-Laufzeitsystem an die [**IWiaTransferCallback::TransferCallback-Methode an eine Anwendung**](-wia-iwiatransfercallback-transfercallback.md) übertragen.<br/> |



 

### <a name="new-interfaces-in-wia-20"></a>Neue Schnittstellen in WIA 2.0



| Thema                                                         | Inhalte                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)                   | Wird von Anwendungen zum Aufzählen von [**IWiaItem2-Objekten**](-wia-iwiaitem2.md) im aktuellen Ordner der Elementstruktur verwendet.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| [**IScanProfile**](-wia-iscanprofile.md)                     | Die [**IScanProfile-Schnittstelle**](-wia-iscanprofile.md) stellt ein einzelnes Scanprofil dar und ermöglicht Anwendungen das Festlegen und Erhalten der Eigenschaften des Profils. <br/>                                                                                                                                                                                                                                                                                                                                   |
| [**IScanProfileMgr**](-wia-iscanprofilemgr.md)               | Die [**IScanProfileMgr-Schnittstelle**](-wia-iscanprofilemgr.md) stellt Methoden zum Erstellen, Öffnen, Löschen und Verwalten von Scanprofilen bereit. <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**IScanProfileUI**](-wia-iscanprofileui.md)                 | Mit [**der IScanProfileUI-Schnittstelle**](-wia-iscanprofileui.md) können Anwendungen ein Dialogfeld anzeigen, sodass Benutzer Scanprofile erstellen, ändern und löschen können.<br/>                                                                                                                                                                                                                                                                                                                               |
| [**IWiaAppErrorHandler**](-wia-iwiaapperrorhandler.md)       | Mit [**der IWiaAppErrorHandler-Schnittstelle**](-wia-iwiaapperrorhandler.md) können Anwendungen Fehlerfenster (während Datenübertragungen) anzeigen, aus denen der Benutzer auswählen kann, ob die Übertragung fortgesetzt, abgebrochen oder abgebrochen werden soll.<br/>                                                                                                                                                                                                                                                                     |
| [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)                       | Die [**IWiaDevMgr2-Schnittstelle**](-wia-iwiadevmgr2.md) wird verwendet, um Geräte für die Bilderfassung zu erstellen und zu verwalten und sich für den Empfang von Geräteereignissen zu registrieren.<br/>                                                                                                                                                                                                                                                                                                                                             |
| [**IWiaErrorHandler**](-wia-iwiaerrorhandler.md)             | Die [**IWiaErrorHandler-Schnittstelle**](-wia-iwiaerrorhandler.md) stellt Methoden zur Verfügung, um Fehler zu behandeln, die auftreten können, wenn eine Anwendung Bilddaten an fordert, unabhängig davon, ob es sich um Vorschau- oder endgültige Bits geht. <br/>                                                                                                                                                                                                                                                                                                      |
| [**IWiaImageFilter**](-wia-iwiaimagefilter.md)               | Die [**IWiaImageFilter-Schnittstelle**](-wia-iwiaimagefilter.md) ist eine Erweiterungsschnittstelle, die von Entwicklern von Bildverarbeitungsfiltern implementiert und von WIA 2.0 aufgerufen wird. <br/>                                                                                                                                                                                                                                                                                                                                  |
| [**IWiaItem2**](-wia-iwiaitem2.md)                           | Die [**IWiaItem2-Schnittstelle**](-wia-iwiaitem2.md) bietet Anwendungen die gleiche Funktionalität wie die [**IWiaItem-Schnittstelle**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) (die Möglichkeit, Geräte zu abfragen, um ihre Funktionen zu entdecken, auf Datenübertragungsschnittstellen und Elementeigenschaften zu zugreifen und das Gerät zu steuern). Darüber hinaus bietet sie der Anwendung die Möglichkeit, Bildverarbeitungsfilter dynamisch zu erstellen und zu verwenden, die als Erweiterungen der wia 2.0-Gerätetreiber in Windows Vista bereitgestellt werden können.<br/> |
| [**IWiaPreview**](-wia-iwiapreview.md)                       | Die [**IWiaPreview-Schnittstelle**](-wia-iwiapreview.md) speichert ungefilterte Bilder intern zwischen und übergibt sie über Bildverarbeitungsfilter. <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md) | Die [**IWiaSegmentationFilter-Schnittstelle**](-wia-iwiasegmentationfilter.md) erkennt Unterregionen eines Bilddatenstroms und macht jeweils separate [**IWiaItem2-Elemente.**](-wia-iwiaitem2.md) <br/>                                                                                                                                                                                                                                                                                                         |
| [**IWiaTransfer**](-wia-iwiatransfer.md)                     | Die [**IWiaTransfer-Schnittstelle**](-wia-iwiatransfer.md) ermöglicht die streambasierte Übertragung von Daten. <br/>                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**IWiaTransferCallback**](-wia-iwiatransfercallback.md)     | Die [**IWiaTransferCallback-Schnittstelle**](-wia-iwiatransfercallback.md) empfängt Rückrufe während einer Datenübertragung. <br/>                                                                                                                                                                                                                                                                                                                                                                                |
| [**IWiaUIExtension2**](-wia-iwiauiextension2.md)             | Die IWiaUIExtension2-Schnittstelle stellt Methoden bereit, die die vom System bereitgestellte Standard-Benutzeroberfläche durch eine benutzerdefinierte Benutzeroberfläche ersetzen und ein benutzerdefiniertes Gerätesymbol bereitstellen. Gerätehersteller können diese Schnittstelle implementieren, um benutzerdefinierte Benutzeroberflächen für ihre Geräte zur Verfügung zu stellen.<br/>                                                                                                                                                                                                                     |



 

### <a name="new-and-changed-overviews-for-wia-20"></a>Neue und geänderte Übersichten für WIA 2.0



| Thema                                                                          | Inhalte |
|--------------------------------------------------------------------------------|----------|
| [Konstanten](-wia-constants.md)                                                |          |
| [Funktionen](-wia-functions.md)                                                |          |
| [Schnittstellen](-wia-interfaces.md)                                              |          |
| [Scan Profile Schema](-wia-scan-profile-schema.md)                            |          |
| [Strukturen](-wia-structures.md)                                              |          |
| [Übertragen von Bilddaten in WIA 2.0](-wia-transferring-image-data-in-wia2.md) |          |
| [WIA-Gerätetypspezifizierer](-wia-wia-device-type-specifiers.md)              |          |
| [WIA-Eigenschaftenkonst constants](-wia-wia-property-constants.md)                      |          |



 

## <a name="leave-feedback"></a>Feedback hinterlassen

Senden Sie eine **sdkfdbk@microsoft.com** E-Mail, um Fehlerberichte und Featureanforderungen direkt an Microsoft zu senden.

 

 




