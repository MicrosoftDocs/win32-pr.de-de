---
description: Um die Unterstützung von frei Hand Eingaben in Anwendungen zu unterstützen, gibt es zwei Objekte, die beide eingebettet werden können und von jedem OLE-Container unterstützt werden.
ms.assetid: fbd7bdf0-63b4-48d1-be91-eabbbb3f1618
title: sInk-und Tink-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ef7ed1c06d256fe8eda9fad4bf15afa19fcb833
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366483"
---
# <a name="sink-and-tink-objects"></a>sInk-und Tink-Objekte

Um die Unterstützung von frei Hand Eingaben in Anwendungen zu unterstützen, gibt es zwei Objekte, die beide eingebettet werden können und von jedem OLE-Container unterstützt werden. Sie werden entweder durch Aufrufen der **Ink. ClipboardCopy-Methode (Rechteck, InkClipboardFormats, InkClipboardModes)** oder der **Ink. ClipboardCopy-Methode (Striche, InkClipboardFormats, InkClipboardModes)** -Methode erstellt und lauten:

-   Text frei Hand Objekt (Tink). Dabei handelt es sich um ein OLE-Objekt, das frei Hand Eingaben darstellt. Mit einem Tink-Objekt können die handschriftlichen frei Hand Eingaben in Text konvertiert werden, entweder als Text, der von einer Erkennung zurückgegeben wurde, oder aus einer Liste von Erkennungs Alternativen. Die Farbe und die Größe der frei Hand Eingaben können Programm gesteuert festgelegt werden, und Sie können auf den Attributen des Texts um das Objekt basieren. Das Tink-Objekt soll ein einzelnes Wort enthalten. Das Tink-Objekt ist ein kleines, einfaches Objekt, das einfache Vorgänge wie das Rendern (bei einem Handle für einen Gerätekontext (HDC) und ein Rect) und das persistente Speichern selbst (bei einem gegebenen Stream) ausführen kann. Die Verwendung eines Tink-Objekts ermöglicht eine nahtlose Benutzererfahrung bei der Arbeit in einer Anwendung, die sowohl Handschrift als auch Text verwendet.
-   Sketch Ink-Objekt (Senke). Dies ist ein OLE-Objekt, das frei Hand Eingaben darstellt, für die keine Wörter erwartet werden. Ein sInk-Objekt wird als Zeichnung interpretiert. Ein sInk-Objekt ist auch nützlich für die Darstellung mehrerer Wörter.

Diese Objekte können für die Interoperabilität zwischen Anwendungen verwendet werden, indem Sie entweder in den OLE-objektslot in der Zwischenablage platziert werden oder durch Einbetten in das Rich-Text-Format (RTF).

Tink-und sInk-Objekte können wie folgt verwendet werden:

-   Sowohl Tink-als auch sInk-Objekte werden in Microsoft Word 2002 unterstützt. Benutzer können frei Hand Eingaben in ein Word-Dokument einfügen, indem Sie die in Word 2002 bereitgestellten Schreib-und Zeichnungs Texteingabe Bereiche verwenden. Diese frei Hand Eingabe wird als OLE-Objekt mit der CLSID des sInk-oder Tink-Objekts in die Word-Datei eingebettet.
-   Das Tablet PC [InkEdit](/previous-versions/ms552265(v=vs.100)) -Steuerelement nutzt das Tink-Objekt. Das InkEdit-Steuerelement ist eine Unterklasse des standardmäßigen [RichTextBox](/dotnet/api/system.windows.forms.richtextbox?view=netcore-3.1) -Steuer Elements. Ink wird in den RTF-Stream des InkEdit-Steuer Elements als Tink-Objekt eingefügt.
-   Wenn eine Anwendung ein ausgewähltes frei Hand Objekt in die Zwischenablage verschiebt, enthält das OLE-Objekt Zwischenablage Slot ein Tink-oder sInk-OLE [-Objekt.](/previous-versions/aa515768(v=msdn.10))

Beispielsweise kann Ihre Anwendung die Handschrift erkennen und jedes frei Hand Objekt als Tink [-Objekt markieren](/previous-versions/aa515768(v=msdn.10)) . Wenn Sie dann ein Wort in Ink auswählen und es kopieren und in Word einfügen, werden die Alternativen für dieses Wort in Word 2002 angezeigt.

> [!Note]  
> Die Unterstützung der Zwischenablage der Tablet PC-Plattform wählt automatisch das EMF-Flag (Enhanced Metafile) für Sie aus, wenn Sie ein sInk-oder Tink-Objekt als OLE-Objekt in der Zwischenablage platzieren. Das Objekt selbst wird in der Zwischenablage in den Slots Einbettungs Quelle und Objekt Deskriptor gespeichert.

 

Ein weiteres Beispiel: mit dem sInk-Objekt können Sie eine frei Hand Skizze in eine Anwendung ziehen, die Skizze kopieren und in Word 2002 einfügen und dann die Zeichnung mithilfe des Tablet PC-Eingabe Bereichs in Word bearbeiten.

Um Tink-Objekte erfolgreich zu enthalten, muss eine Anwendung Unterstützung für OLE-Container für eingebettete Objekte implementieren. Damit der Container Tink vollständig unterstützt, müssen Sie Folgendes erstellen:

-   Änderungen am Code für "suchen und ersetzen". Anstatt eingebettete Objekte in der Suche zu überspringen, müssen diese Objekte für den Typ abgefragt werden. Handelt es sich um ein Tink-Objekt, müssen diese instanziiert und nach dem entsprechenden Text abgefragt werden.
-   Änderungen am Auswahl Verhalten. Die Auswahl von Tink-Objekten darf nie mit den Zieh Punkten der Größe angezeigt werden. Sie sollten auf die gleiche Weise ausgewählt werden, wie Text im Dokument ausgewählt wird. Der Auswahl Code für-Objekte muss erkennen, ob der Typ Tink ist, und die Auswahl entsprechend anzeigen.
-   Verwendung von Umgebungs Eigenschaften. Ambient-Eigenschaften wie Schriftart Größe, Farbe und Fett Formatierung müssen an das Tink-Objekt übertragen werden. Durch die Anwendung dieser Eigenschaften wird die Breite der handschriftlichen frei Hand Eingaben geändert, sodass ein Größen Update erforderlich ist, indem die [**getinkblock-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinklineinfo-getinkextent) oder die [IOleObject:: GetExtent](/windows/win32/api/oleidl/nf-oleidl-ioleobject-getextent) -Methode aufgerufen wird.
-   Überschreiben Sie die Standard [mäßige IOleObject::D overb](/windows/win32/api/oleidl/nf-oleidl-ioleobject-doverb) -Methoden Verarbeitung. Dies ermöglicht die Konvertierung in Text, um einen Batch von Tink-Objekten an die Erkennung zu übergeben, der dann die Wörter in Erkennungs Segmente unterteilen kann.

Weitere Informationen über das Unterbrechen von Wörtern in Erkennungs Segmente finden Sie unter [Erkennungs Segmente](recognition-segments.md).

 

 
