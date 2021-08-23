---
title: Ersetzen der Windows Bild- und Faxanzeigeanwendung mithilfe des Vorschauverbs
description: Ab dem Windows XP können Benutzer Bilder anzeigen, drehen, drucken und zoomen.
ms.assetid: cb08756b-6a5d-424d-ab6d-2e34d180ec4e
keywords:
- Windows Bild- und Faxanzeige
- Vorschauverb
- Bewährte Methoden,Windows Bild- und Faxanzeige
- Bewährte Methoden,Vorschauverb
- Leistung, Windows Bild- und Faxanzeige
- Leistung, Vorschauverb
- register,Preview-Verb
- register,Slideshow verb
- Slideshow-Verb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 518e32f7b7bf33db26e534c92cfe2fb46c9a51bc444f04f4881f18fb1fe6c738
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608520"
---
# <a name="replacing-the-windows-picture-and-fax-viewer-application-using-the-preview-verb"></a>Ersetzen der Windows Bild- und Faxanzeigeanwendung mithilfe des Vorschauverbs

\[Das Bild- und Faxanzeigefeature wird nur unter xp Windows unterstützt. \]

Ab dem Windows XP können Benutzer Bilder anzeigen, drehen, drucken und zoomen. Einige dieser Features werden über die Windows Shell und andere über die Anwendung Windows Bild- und Faxanzeige bereitgestellt. Während Windows Bild- und Faxanzeige eine hervorragende Basislinie von Features bietet und ein wichtiger Bestandteil der Bildverarbeitungserfahrung ist, können Sie sie bei Wahl einfach durch eine andere Anwendung ersetzen. Dieses Dokument soll Ihnen helfen, die Anwendung Windows Bild- und Faxanzeige effektiv zu ersetzen, ohne wichtige Features zu verlieren oder die Benutzerfreundlichkeit zu verbessern.

-   [Bewährte Methoden](#best-practices)
    -   [Leistung](#performance)
    -   [Funktionen](#features)
    -   [Formatunterstützung](#format-support)
-   [Registrieren für das Vorschauverb](#registering-for-the-preview-verb)
-   [Registrieren für das Edit-Verb](#registering-for-the-edit-verb)
-   [Registrieren für das Slideshow-Verb](#registering-for-the-slideshow-verb)
-   [Zugehörige Themen](#related-topics)

## <a name="best-practices"></a>Empfehlungen

In Windows XP und höher enthält die Shell ein Verb, mit dem Sie Benutzern die Vorschau von Bildern ermöglichen können. Sie heißt *Vorschauversion.* Dieses Verb hebt die Hauptbenutzeraufgabe für Bilder hervor, die angezeigt wird. Damit diese Erfahrung gut funktioniert, besitzt Windows Anwendung Bild- und Faxanzeige standardmäßig die Vorschau-Zuordnung.

Die Windows Bild- und Faxanzeige oder eine beliebige Anwendung, die eine Dateiassozierung besitzt, enthält ein Element, das die Bearbeitungsanwendung des Benutzers startet. Da das Vorschauverb nur verwendet wird, um Bilder in der Vorschau anzuzeigen, anstatt sie zu bearbeiten, muss Ihre Anwendung beim Beanspruchen dieser Zuordnung darauf achten, die Empfehlungen in diesem Dokument zu befolgen.

Sie möchten sicherstellen, dass eine Anwendung, die Bilder bearbeitet, weiterhin das Verb Bearbeiten übernehmen kann. Beispiel: Ein Benutzer hat Microsoft Picture It! Installiert: Wenn sie auf eine Datei doppelklicken.jpg sollte der Computer die Anwendung Windows Bild- und Faxanzeige starten. Wenn sie jedoch auf der **Symbolleiste auf** Bearbeiten klicken, sollte der Computer Picture It! starten. mit dieser .jpg Datei.

Es gibt drei Überlegungen, die Sie berücksichtigen sollten, wenn Sie Windows Bild- und Faxanzeige ersetzen. Diese sind:

-   [Leistung](#performance)
-   [Funktionen](#features)
-   [Formatunterstützung](#format-support)

### <a name="performance"></a>Leistung

Der wichtigste Aspekt bei der Leistung ist die Geschwindigkeit, mit der Bilder geladen werden. Obwohl hier keine Leistungsmetrik bereitgestellt wird, sollten Sie versuchen, Windows Picture and Fax Viewer durch eine Anwendung zu ersetzen, die die Leistung ab- oder erhöht.

Die Anwendung selbst sollte schnell geladen werden. Eines der hauptprobleme, die Benutzer mit Anwendungen haben, die Bildzuordnungen übernehmen, ist die Wartezeit beim Laden der Anwendung. Dies liegt häufig an einer leistungsstarken Anwendungsauslastung beim Bearbeiten, wenn sie auf eine Bilddatei doppelklicken, auch wenn der Benutzer die Datei einfach anzeigen möchte. Es ist für den Benutzer am besten, Optionen zur Verfügung zu stellen, die ihn schnell zu einer Anwendung bringen, in der er das Bild nur bearbeiten kann, wenn dies gewünscht ist.

### <a name="features"></a>Features

Es gibt eine minimale Reihe von Features, die Ihre Anwendung bereitstellen sollte, wenn Sie Windows Bild- und Faxanzeigeanwendung ersetzen. Dies sind:



| Feature                            | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bild am besten anzeigen             | Dadurch kann der Benutzer das gesamte Bild auf die Größe skalieren, in der ich am besten in den anzeigebaren Bereich des Anwendungsfensters passt. Auf diese Weise können sie das gesamte Bild sehen, auch wenn es durch Verkleinern leicht heruntergestuft wird. Dies sollte die Standardeinstellung sein, wenn ein Bild geladen wird, das größer als der angezeigte Platz ist. Andernfalls sollte das Bild in seiner tatsächlichen Größe angezeigt werden. Beispielsweise sollte ein Bild mit 64 x 64 Pixeln nicht einfach auf eine Größe von 600 x 600 skaliert werden, da dies die Fenstergröße der Anwendung ist. |
| Bild in tatsächlicher Größe anzeigen          | Dies gibt dem Benutzer die Möglichkeit, das gesamte Bild in seiner tatsächlichen Auflösung zu sehen. Dies ermöglicht es ihnen, sie in der richtigen Größe zu sehen und um das Bild zu schwenken. Dies sollte nicht die Standardansicht sein, es sei denn, das Bild ist kleiner als der in der Anwendung angezeigte Platz.                                                                                                                                                                                                                                                              |
| Vergrößern des Bilds                    | Dadurch kann der Benutzer einen Teil des Bilds vergrößern, um detailliertere Details zu untersuchen oder einfach ein kleines Bild zu vergrößern. Dies ähnelt der Anzeige der tatsächlichen Größe des Bilds, ermöglicht dem Benutzer jedoch, zu steuern, wie genau er das Bild sieht.                                                                                                                                                                                                                                                                                            |
| Verkleinern des Bilds                  | Dadurch kann der Benutzer verkleinern und eine umfassendere Ansicht erhalten. Dies ähnelt der Anzeige des Bilds am besten, ermöglicht es dem Benutzer jedoch, zu steuern, wie weit das Bild zurück angezeigt wird.                                                                                                                                                                                                                                                                                                                                                          |
| Nächste Abbildung                         | Dadurch kann der Benutzer das nächste Bild in der Liste sehen. Diese Liste kann alle Bilder im aktuellen Ordner oder alle Bilder sein, die der Benutzer im Rahmen eines Mehrfachauswahl-Vorgangs auswählt. Das heißt, wenn er klickt und zieht, um Bilder hervorzuheben, oder hält die Steuerschaltfläche gedrückt und klickt auf einzelne Dateien.                                                                                                                                                                                                                       |
| Vorherige Abbildung                     | Dadurch kann der Benutzer das vorherige Bild in der Liste anzeigen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Drehen im Uhrzeigersinn um 90 Grad        | Dadurch kann der Benutzer das Bild im Uhrzeigersinn um Quartale drehen. Windows XP speichert das Bild automatisch, wenn es gedreht wird, um den Verlust der Imagequalität zu verringern. Die Anwendung kann auch kleinere Inkremente drehen, aber 90 Grad ist der Standard als häufigste Drehung für digitale Bilder.                                                                                                                                                                                                                                 |
| Drehen gegen den Uhrzeigersinn um 90 Grad | Dadurch kann der Benutzer das Bild gegen den Uhrzeigersinn um Quartale drehen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Drucken                              | Dadurch kann der Benutzer das derzeit angezeigte Bild drucken.                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Speichern unter                            | Dadurch kann der Benutzer das Bild in einem angegebenen Ordner speichern.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Bild löschen                       | Dadurch kann der Benutzer das Image löschen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Hilfe                               | Dadurch erhalten Benutzer Hilfedokumentationen zur Verwendung der Anzeigeanwendung.                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Eigenschaften                         | Dadurch kann der Benutzer die Eigenschaften des Bilds anzeigen oder bearbeiten, in der Regel die in jedem Bild gespeicherten EXIF-Informationen (Exchangeable Image File).                                                                                                                                                                                                                                                                                                                                                                                      |
| Bearbeiten                               | Dadurch kann der Benutzer sein bevorzugtes Bearbeitungsprogramm starten, das für das Verb Bearbeiten auf dem Bild registriert ist.                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

### <a name="format-support"></a>Formatunterstützung

Da es für eine Anwendung schwierig ist, alle verschiedenen Images zu unterstützen, wird empfohlen, dass die Anwendung Windows GDI+ Bildformate unterstützt. Wenn Sie sich jedoch gegen die Verwendung von GDI+ entscheiden, sollte Ihre Anwendung nur die Dateizuordnungen übernehmen, für die sie getestet wurde und die bekannterd funktionieren. Wenn der Benutzer dann ein Format anzeigen muss, das Sie nicht verarbeiten, können Windows Bild- und Faxanzeige weiterhin Zugriff bereitstellen.

Beispielsweise stellt Windows Bild- und Faxanzeige eine Reihe von Tools zum Bearbeiten von Anmerkungen in TIFF-Bildern zur Verfügung. Sofern diese Funktionalität in Ihrer Anwendung nicht dupliziert ist, sollten Sie Ihre Anwendung nicht registrieren, um TIFF-Images zu verarbeiten. Das Fahrprinzip sollte sein, sicherzustellen, dass der Benutzer keinerlei Funktionalität verliert.

## <a name="registering-for-the-preview-verb"></a>Registrieren für das Vorschauverb

Das Registrieren einer Anwendung zur Handhabung des Vorschauverbs ist recht einfach. Suchen Sie den folgenden Wert der Anwendung in der Registrierung, wobei Application.Jpeg den [](/windows/desktop/shell/default-programs) Namen des Dateiassozschlüssels der Anwendung darstellt (weitere Informationen finden Sie unter Standardprogramme):

```
HKEY_CLASSES_ROOT
   Application.Jpeg
      shell
         open
            command
               (Default) = app.exe %1
```

Ändern Sie den Namen des **geöffneten Unterschlüssels** in "Vorschau", wie hier gezeigt.

```
HKEY_CLASSES_ROOT
   Application.Jpeg
      shell
         preview
            command
               (Default) = app.exe %1
```

Dadurch wird die Anwendung registriert und als Standardanwendung für das Vorschauverb für eine .jpg festgelegt. Außerdem ist Folgendes erforderlich.

**HKEY \_ CLASSES \_ ROOT** \\ **.jpg** \( Default) = Application.Jpeg

## <a name="registering-for-the-edit-verb"></a>Registrieren für das Edit-Verb

Dadurch wird eine Anwendung für das Edit Verb registriert und zur neuen Standardanwendung zum Bearbeiten eines Bilds. Die registrierte Anwendung sollte die Bearbeitungsfunktion der vorhandenen Standardanwendung zum Zeitpunkt der Installation übernehmen und sie zum Zeitpunkt der Deinstallation als Handler wieder installieren. Dies kann erreicht werden, indem die neue Anwendung in der Zuordnungsliste niedriger registriert wird als die Standardanwendung. Die Standardanwendung wird hier registriert:

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      image
         shell
            edit
               command
                  (Default) = app.exe %1
```

Eine neue Anwendung sollte hier registriert werden:

```
HKEY_CLASSES_ROOT
   Application.Jpeg
      shell
         edit
            command
               (Default) = app.exe %1
```

## <a name="registering-for-the-slideshow-verb"></a>Registrieren für das Slideshow-Verb

Ab Windows Vista kann eine Anwendung auch  das Diashowverb registrieren. Anwendungen, die eine Bildschirmpräsentation implementieren, können sich registrieren, um aufgerufen zu werden, wenn das Slideshow-Verb ausgewählt wird. Diese Registrierung erfolgt auf die gleiche Weise wie für das oben beschriebene Vorschauverb. Es wird dringend empfohlen, dass Anwendungen die DropTarget-Form des Verbs implementieren. Auf diese Weise können sie einen vollständigen Satz von Elementen übergeben. Die DropTarget-Implementierung wird wie hier gezeigt registriert:

```
HKEY_CLASSES_ROOT
   Application.Jpeg
      shell
         slideshow
            DropTarget
               CLSID = {CLSID of the implementation}
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einführung in Dateizuordnungen](/windows/desktop/shell/fa-intro)
</dt> <dt>

[Informationen GDI+](../gdiplus/-gdiplus-about-gdi--about.md)
</dt> </dl>

 

 