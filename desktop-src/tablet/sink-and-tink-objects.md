---
description: Um die Unterstützung von Ink in Anwendungen zu unterstützen, gibt es zwei -Objekte, die beide eingebettet werden können und von jedem OLE-Container unterstützt werden.
ms.assetid: fbd7bdf0-63b4-48d1-be91-eabbbb3f1618
title: sInk- und tInk-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8e25e1f258ac789382475666878c986f5053323a1b19bf8f4b6110c096f2fd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091302"
---
# <a name="sink-and-tink-objects"></a>sInk- und tInk-Objekte

Um die Unterstützung von Ink in Anwendungen zu unterstützen, gibt es zwei -Objekte, die beide eingebettet werden können und von jedem OLE-Container unterstützt werden. Sie werden entweder durch Aufrufen der **Ink.ClipboardCopy-Methode (Rectangle, InkClipboardFormats, InkClipboardModes)** oder der **Ink.ClipboardCopy-Methode (Strokes, InkClipboardFormats, InkClipboardModes)** erstellt und sind:

-   Text-Ink-Objekt (tInk). Dies ist ein OLE-Objekt, das Ink darstellt, das Wörter bilden soll. Mit einem tInk-Objekt kann die handschriftliche Ink-Funktion in Text konvertiert werden, entweder als der von einer Erkennung zurückgegebene Text oder die Auswahl aus einer Liste von Erkennungswechseln. Die Farbe und Größe der Freitextfarbe kann programmgesteuert festgelegt werden und kann auf den Attributen des Texts um das Objekt basieren. Das tInk-Objekt soll ein einzelnes Wort enthalten. Das tInk-Objekt ist ein kleines, einfaches Objekt, das einfache Vorgänge wie das Rendern (mit einem Handle für einen Gerätekontext (HDC) und ein RECT) und das Beibehalten selbst (bei einem Stream) ausführen kann. Die Verwendung eines tInk-Objekts ermöglicht eine nahtlose Benutzererfahrung bei der Arbeit in einer Anwendung, die Sowohl Handschrift als auch Texteingaben verwendet.
-   Skizzieren eines Ink-Objekts (sInk). Dies ist ein OLE-Objekt, das Ink darstellt, die keine Wörter bilden soll. Ein sInk-Objekt wird als Zeichnung interpretiert. Ein sInk-Objekt ist auch nützlich, um mehrere Wörter zu darstellen.

Diese Objekte können für die Interoperabilität zwischen Anwendungen verwendet werden, indem sie entweder im OLE-Objektslot in der Zwischenablage platziert oder in das Rich Text Format (RTF) eingebettet werden.

Sie können tInk- und sInk-Objekte wie folgt verwenden:

-   Sowohl tInk- als auch sInk-Objekte werden in Microsoft Word 2002 unterstützt. Benutzer können Ink in ein Word-Dokument einfügen, indem sie die in Word 2002 bereitgestellten Eingabepanels zum Schreiben und Zeichnen von Text verwenden. Diese Ink-Datei wird als OLE-Objekt mit der CLSID des sInk- oder tInk-Objekts in die Word-Datei eingebettet.
-   Das Tablet PC [InkEdit-Steuerelement](/previous-versions/ms552265(v=vs.100)) nutzt das tInk-Objekt. Das InkEdit-Steuerelement ist eine Unterklasse des [RichTextBox-Standardsteuerfelds.](/dotnet/api/system.windows.forms.richtextbox?view=netcore-3.1) Ink wird als tInk-Objekt in den RTF-Stream des InkEdit-Steuerelements eingefügt.
-   Wenn eine Anwendung ein ausgewähltes [Ink-Objekt in](/previous-versions/aa515768(v=msdn.10)) die Zwischenablage verschiebt, enthält der Zwischenablageslot des OLE-Objekts ein tInk- oder sInk-OLE-Objekt.

Ihre Anwendung kann z. B. Handschrift erkennen und jedes [Ink-Objekt](/previous-versions/aa515768(v=msdn.10)) als tInk-Objekt markieren. Wenn Sie dann ein Wort in Ink auswählen und kopieren und in Word einfügen, werden Alternativen für dieses Wort in Word 2002 angezeigt.

> [!Note]  
> Die Unterstützung der Zwischenablage der Tablet PC-Plattform wählt automatisch das EMF-Flag (Enhanced Metafile) aus, wenn Sie ein sInk- oder tInk-Objekt als OLE-Objekt in der Zwischenablage platzieren. Das Objekt selbst wird in der Zwischenablage in den Einbettungsquelle- und Objektdeskriptorslots gespeichert.

 

Als weiteres Beispiel können Sie mithilfe des sInk-Objekts einen Ink-Sketch in einer Anwendung zeichnen, den Sketch kopieren und in Word 2002 einfügen und dann die Zeichnung mithilfe des Tablet PC-Eingabebereichs in Word bearbeiten.

Um tInk-Objekte erfolgreich enthalten zu können, muss eine Anwendung OLE-Containerunterstützung für eingebettete Objekte implementieren. Damit der Container tInk vollständig unterstützt, müssen Sie dann:

-   Änderungen am Code für Suchen und Ersetzen. Anstatt eingebettete Objekte in der Suche zu überspringen, müssen diese Objekte für den Typ verhört werden. Wenn es sich um ein tInk-Objekt handelt, müssen sie instanziiert und nach dem entsprechenden Text abgefragt werden.
-   Änderungen am Auswahlverhalten. Die Auswahl von tInk-Objekten sollte nie mit Größenziehpunkten angezeigt werden. Sie sollten auf die gleiche Weise ausgewählt werden wie Text im Dokument. Der Auswahlcode für Objekte muss erkennen, ob der Typ tInk ist, und die Auswahl entsprechend anzeigen.
-   Verwendung von Umgebungseigenschaften. Umgebungseigenschaften wie Schriftgrad, Farbe und Fettformatierung müssen an das tInk-Objekt übertragen werden. Die Anwendung dieser Eigenschaften ändert die Breite der handschriftlichen Freihandschrift, sodass eine Größenaktualisierung durch Aufrufen der [**GetInkExtent-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinklineinfo-getinkextent) oder [der IOleObject::GetExtent-Methode erforderlich](/windows/win32/api/oleidl/nf-oleidl-ioleobject-getextent) ist.
-   Überschreiben Sie die Standardmäßige Verarbeitung der [IOleObject::D oVerb-Methode.](/windows/win32/api/oleidl/nf-oleidl-ioleobject-doverb) Dies ermöglicht die Konvertierung in Text, um einen Batch von tInk-Objekten an die Erkennung zu übergeben, die die Wörter dann in Erkennungssegmente unterteilen kann.

Weitere Informationen zum Aufteilen von Wörtern in Erkennungssegmente finden Sie unter [Erkennungssegmente.](recognition-segments.md)

 

 
