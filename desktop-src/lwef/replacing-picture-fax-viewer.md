---
title: Ersetzen der Windows Bild-und Faxviewer-Anwendung mithilfe des Vorschau Verbs
description: Ab Windows XP können Benutzer Bilder anzeigen, drehen, Drucken und Zoomen.
ms.assetid: cb08756b-6a5d-424d-ab6d-2e34d180ec4e
keywords:
- Windows-Bild-und-Faxviewer
- Vorschau Verb
- bewährte Methoden, Windows Bild-und Faxviewer
- bewährte Methoden, Vorschau Verb
- Leistung, Windows Bild-und Faxanzeige
- Leistung, Vorschau Verb
- registrieren, Vorschau Verb
- registrieren, Bildschirm Verb
- Bildschirm Verb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e6769e13aaea41b3b05bbf674ea95d7f88fb646
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948745"
---
# <a name="replacing-the-windows-picture-and-fax-viewer-application-using-the-preview-verb"></a>Ersetzen der Windows Bild-und Faxviewer-Anwendung mithilfe des Vorschau Verbs

\[Das Bild-und Faxviewer-Feature wird nur unter Windows XP unterstützt. \]

Ab Windows XP können Benutzer Bilder anzeigen, drehen, Drucken und Zoomen. Einige dieser Features werden über die Windows-Shell und andere über die Windows-Bild-und Faxviewer-Anwendung bereitgestellt. Obwohl Windows Bild-und Faxviewer eine hervorragende Baseline von Features bietet und ein wichtiger Bestandteil der Abbild Erstellung ist, können Sie Sie problemlos durch eine andere Anwendung ersetzen, wenn Sie sich dafür entscheiden. Dieses Dokument soll Sie dabei unterstützen, die Windows-Bild-und Faxviewer-Anwendung effektiv zu ersetzen, ohne wichtige Features zu verlieren oder die Benutzer Leistung zu verringern.

-   [Bewährte Methoden](#best-practices)
    -   [Leistung](#performance)
    -   [Funktionen](#features)
    -   [Format Unterstützung](#format-support)
-   [Registrieren für das Vorschau Verb](#registering-for-the-preview-verb)
-   [Registrieren für das Bearbeitungs Verb](#registering-for-the-edit-verb)
-   [Registrieren für das Diashow-Verb](#registering-for-the-slideshow-verb)
-   [Zugehörige Themen](#related-topics)

## <a name="best-practices"></a>Bewährte Methoden

In Windows XP und höher enthält die Shell ein Verb, das Sie verwenden können, um Benutzern das Anzeigen von Bildern zu ermöglichen. Sie wird als *Vorschau* bezeichnet. In diesem Verb wird die Hauptbenutzer Aufgabe für Bilder hervorgehoben, die angezeigt wird. Damit diese Funktionsweise funktioniert, ist die Windows-Bild-und Faxviewer-Anwendung standardmäßig für die Vorschau Zuordnung zuständig.

Der Windows Bild-und Faxviewer bzw. eine beliebige Anwendung, die eine Datei Zuordnung besitzt, enthält ein Element, das die Bearbeitungs Anwendung des Benutzers aufruft. Da das Vorschau Verb nur für die Vorschau von Images verwendet wird, anstatt diese zu bearbeiten, muss Ihre Anwendung darauf achten, die Empfehlungen in diesem Dokument zu befolgen, wenn Sie diese Zuordnung anfordern.

Sie möchten sicherstellen, dass eine Anwendung, die Images bearbeitet, das Bearbeitungs Verb übernehmen kann. Wenn ein Benutzer beispielsweise Microsoft Picture! installiert, wenn Sie auf eine JPG-Datei doppelklicken, sollte der Computer die Windows Bild-und Faxviewer-Anwendung starten. Wenn Sie jedoch auf der Symbolleiste auf " **Bearbeiten** " klicken, sollte der Computer das Bild starten! mit dieser JPG-Datei.

Beim Ersetzen von Windows-Bild und Fax-Viewer sollten Sie drei Aspekte berücksichtigen. Diese lauten wie folgt:

-   [Leistung](#performance)
-   [Funktionen](#features)
-   [Format Unterstützung](#format-support)

### <a name="performance"></a>Leistung

Der Hauptaspekt bei der Leistung ist die Geschwindigkeit, mit der Bilder geladen werden. Es ist zwar keine Leistungs Metrik vorhanden, Sie sollten jedoch versuchen, Windows Bild-und Faxviewer durch eine Anwendung zu ersetzen, die der Leistung entspricht oder diese steigert.

Die Anwendung selbst sollte schnell geladen werden. Eines der wichtigsten Probleme, die Benutzer bei Anwendungen haben, die Bild Zuordnungen übernehmen, ist die Wartezeit, während die Anwendung geladen wird. Dies ist häufig darauf zurückzuführen, dass eine leistungsstarke Bearbeitungs Anwendung geladen wird, wenn Sie auf eine Bilddatei doppelklicken, auch wenn der Benutzer die Datei einfach anzeigen möchte. Es ist für den Benutzer am besten geeignet, wenn Sie Optionen bereitstellen, die diese schnell zu einer Anwendung machen, in der Sie das Abbild nur dann bearbeiten können, wenn dies der Wunsch ist.

### <a name="features"></a>Features

Es gibt eine minimale Anzahl von Features, die Ihre Anwendung bereitstellen sollte, wenn Sie die Windows-Bild-und Faxviewer-Anwendung ersetzen. Dies sind:



| Funktion                            | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bild am besten anpassen             | Dadurch wird dem Benutzer die Option angezeigt, das gesamte Bild auf die Größe skalieren zu können, in der ich am besten in den sichtbaren Bereich des Anwendungsfensters passt. Auf diese Weise kann das gesamte Bild angezeigt werden, auch wenn es durch Zoomen etwas beeinträchtigt wird. Dabei sollte es sich um die Standardeinstellung handeln, wenn ein Bild geladen wird, das größer als der sichtbare Bereich ist. Andernfalls sollte das Bild in der tatsächlichen Größe angezeigt werden. Beispielsweise sollte ein 64 x 64 Pixel-Bild nicht auf die Größe 600 x 600 skaliert werden, einfach weil dies die Fenstergröße der Anwendung ist. |
| Bild in tatsächlicher Größe anzeigen          | Dadurch erhält der Benutzer die Möglichkeit, das gesamte Bild bei der eigentlichen Auflösung anzuzeigen. Dies ermöglicht es Ihnen, Sie mit der entsprechenden Größe und der entsprechenden Größe des Bilds anzuzeigen. Dies sollte nicht die Standardansicht sein, es sei denn, das Bild ist kleiner als der Anzeige Bare Bereich in der Anwendung.                                                                                                                                                                                                                                                              |
| Bild zoomen                    | Dadurch kann der Benutzer einen Teil des Bilds vergrößern, um genauere Details zu untersuchen, oder einfach ein kleines Bild vergrößern. Dies ähnelt dem Anzeigen der tatsächlichen Größe des Bilds, ermöglicht es dem Benutzer jedoch zu steuern, wie genau das Bild angezeigt wird.                                                                                                                                                                                                                                                                                            |
| Bild verkleinern                  | Dies ermöglicht es dem Benutzer, eine umfassendere Ansicht zu vergrößern und zu erhalten. Dies ähnelt der Anzeige des Bilds am besten, aber ermöglicht es dem Benutzer, die Anzeige des Bilds zu steuern.                                                                                                                                                                                                                                                                                                                                                          |
| Nächstes Bild                         | Dies ermöglicht dem Benutzer, das nächste Bild in der Liste anzuzeigen. Diese Liste kann alle Bilder im aktuellen Ordner oder alle Images sein, die der Benutzer als Teil eines Mehrfachauswahl Vorgangs auswählt. Das heißt, wenn er auf die Maus klickt und Sie zieht, um Bilder hervorzuheben, oder die Schaltfläche "Control" gedrückt hält und auf einzelne Dateien klickt.                                                                                                                                                                                                                       |
| Vorheriges Bild                     | Dadurch kann der Benutzer das vorherige Bild in der Liste anzeigen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Drehen um 90 Grad im Uhrzeigersinn        | Dadurch kann der Benutzer das Bild im Uhrzeigersinn um Quartale drehen. Windows XP speichert das Abbild automatisch, wenn es rotiert wird, um den Verlust der Bildqualität zu verringern. Die Anwendung kann auch kleinere Inkremente drehen, aber 90 Grad ist der Standardwert für die häufigste Drehung digitaler Bilder.                                                                                                                                                                                                                                 |
| Gegen den Uhrzeigersinn um 90 Grad drehen | Dadurch kann der Benutzer das Bild gegen den Uhrzeigersinn um Quartale drehen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Drucken                              | Dadurch kann der Benutzer das Bild drucken, das momentan angezeigt wird.                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Speichern unter                            | Dies ermöglicht dem Benutzer das Speichern des Bilds in einem angegebenen Ordner.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Bild löschen                       | Dadurch kann der Benutzer das Bild löschen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Hilfe                               | Dadurch erhält der Benutzerhilfe bei der Verwendung der Anzeigeanwendung.                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Eigenschaften                         | Dies ermöglicht es dem Benutzer, die Eigenschaften des Bilds anzuzeigen oder zu bearbeiten, in der Regel die in jedem Image gespeicherten Informationen zur austauschbaren Bilddatei (EXIF).                                                                                                                                                                                                                                                                                                                                                                                      |
| Bearbeiten                               | Dadurch kann der Benutzer sein bevorzugtes Bearbeitungsprogramm starten, das für das Bearbeitungs Verb für das Bild registriert ist.                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

### <a name="format-support"></a>Format Unterstützung

Da es für eine Anwendung schwierig ist, alle unterschiedlichen Images zu unterstützen, wird empfohlen, dass die Anwendung Windows GDI+ zur Unterstützung von Bildformaten verwendet. Wenn Sie sich jedoch für die Verwendung von GDI+ entscheiden, sollte Ihre Anwendung nur die Dateizuordnungen übernehmen, für die Sie getestet wurde und funktioniert. Wenn der Benutzer dann ein Format anzeigen muss, das Sie nicht behandeln, kann Windows Bild-und Faxviewer weiterhin Zugriff bereitstellen.

Beispielsweise bietet Windows Bild-und Faxviewer eine Reihe von Tools zum Bearbeiten von Anmerkungen in TIFF-Bildern. Wenn diese Funktionalität nicht in Ihrer Anwendung dupliziert ist, sollten Sie Ihre Anwendung nicht registrieren, um TIFF-Images zu verarbeiten. Das Fahr Prinzip sollte darin bestehen, sicherzustellen, dass der Benutzer keinerlei Funktionalität verliert.

## <a name="registering-for-the-preview-verb"></a>Registrieren für das Vorschau Verb

Die Registrierung einer Anwendung für die Handhabung des Vorschau Verbs ist recht einfach. Suchen Sie den folgenden Wert der Anwendung in der Registrierung, wobei "Application. JPEG" den Namen des Datei Zuordnungs Schlüssels der Anwendung darstellt (Weitere Informationen finden Sie unter " [Standardprogramme](/windows/desktop/shell/default-programs) "):

```
HKEY_CLASSES_ROOT
   Application.Jpeg
      shell
         open
            command
               (Default) = app.exe %1
```

Ändern Sie den Namen des unter Schlüssels **Open** in "Preview", wie hier gezeigt.

```
HKEY_CLASSES_ROOT
   Application.Jpeg
      shell
         preview
            command
               (Default) = app.exe %1
```

Dadurch wird die Anwendung registriert und als Standardanwendung für das vorschauverb für eine JPG-Datei definiert. Folgendes ist ebenfalls erforderlich.

**HKEY \_ Klassen \_ root** \\ **. jpg** \( Default) = Application. JPEG

## <a name="registering-for-the-edit-verb"></a>Registrieren für das Bearbeitungs Verb

Dadurch wird eine Anwendung für das Bearbeitungs Verb registriert und zur neuen Standardanwendung für die Bearbeitung eines Bilds. Die registrierte Anwendung sollte die Bearbeitungsfunktion der vorhandenen Standardanwendung zur Installationszeit übernehmen und Sie zum Zeitpunkt der Deinstallation als Handler installieren. Dies kann erreicht werden, indem die neue Anwendung in der Zuordnungs Liste kleiner als die Standardanwendung registriert wird. Die Standardanwendung wird hier registriert:

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      image
         shell
            edit
               command
                  (Default) = app.exe %1
```

Die neue Anwendung sollte sich hier registrieren:

```
HKEY_CLASSES_ROOT
   Application.Jpeg
      shell
         edit
            command
               (Default) = app.exe %1
```

## <a name="registering-for-the-slideshow-verb"></a>Registrieren für das Diashow-Verb

Ab Windows Vista kann eine Anwendung auch das **Diashow** -Verb registrieren. Anwendungen, die eine Folien Anzeige implementieren, können sich registrieren, um aufgerufen zu werden, wenn das Bildschirm Verb ausgewählt wird. Diese Registrierung erfolgt auf genau dieselbe Weise wie das oben beschriebene Vorschau Verb. Es wird dringend empfohlen, dass Anwendungen das DropTarget-Formular des Verbs implementieren. Auf diese Weise kann ein kompletter Satz von Elementen an Sie übermittelt werden. Die DropTarget-Implementierung wird wie folgt registriert:

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

[Informationen zu GDI+](../gdiplus/-gdiplus-about-gdi--about.md)
</dt> </dl>

 

 