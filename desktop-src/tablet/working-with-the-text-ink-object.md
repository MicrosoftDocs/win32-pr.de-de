---
description: Um die Unterstützung von frei Hand Eingaben in-Anwendungen zu unterstützen, gibt es zwei Objekte, die beide eingebettet werden können und von jedem OLE-Container, dem Text Ink-Objekt (Tink) und dem Sketch Ink-Objekt (Senke) unterstützt werden.
ms.assetid: 0202e91c-c7a0-4e7b-a1c6-a2f58c11c0be
title: Arbeiten mit dem Text Ink-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 082323f7e67e76f7ae39c6b592a86f2be0945a86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360077"
---
# <a name="working-with-the-text-ink-object"></a>Arbeiten mit dem Text Ink-Objekt

Um die Unterstützung von frei Hand Eingaben in-Anwendungen zu unterstützen, gibt es zwei Objekte, die beide eingebettet werden können und von jedem OLE-Container, dem Text Ink-Objekt (Tink) und dem Sketch Ink-Objekt (Senke) unterstützt werden.

Das Text Ink-Objekt ist ein OLE-Objekt, das frei Hand Eingaben darstellt, die als Wörter erwartet werden. Ein Text frei Hand Objekt ermöglicht, dass das handschriftliche frei Handzeichen in Text konvertiert werden kann, indem es aus einer Liste von Alternativen ausgewählt wird. Die Farbe und Größe des Text frei Hand Objekts können Programm gesteuert festgelegt werden, und Sie können auf den Attributen des Texts um das Objekt basieren. Das Text frei Hand Objekt soll ein einzelnes Wort enthalten.

Das Text Ink-Objekt unterstützt den Standardsatz von OLE-Schnittstellen, die zum Einbetten und Zwischenspeichern von zwischen Die [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) -Schnittstelle liest aus einem Stream und schreibt ihn in einen Stream im frei Hand Format (Ink serialisiert Format, ISF) Das Text Ink-Objekt stellt die [**iinklineinfo**](/windows/desktop/api/msinkaut/nn-msinkaut-iinklineinfo) -Schnittstelle für den Zugriff auf die Anzeigeeigenschaften und die Erkennungs Ergebnisliste bereit.

Das Text frei Hand Objekt kann für die Interoperabilität zwischen Anwendungen verwendet werden, indem es in den OLE-Objekt Slot in der Zwischenablage platziert wird, indem es in RTF eingebettet oder in einem ISF-Datenstrom gespeichert wird.

Ein Text-Ink-Objekt kann auf folgende Weise generiert werden.

-   Das [InkEdit](inkedit-control-reference.md) -Steuerelement nutzt das Text-Ink-Objekt. Die Funktionalität des InkEdit-Steuer Elements ist eine Obermenge der standardmäßigen RichEdit-Steuerelement Funktionalität. Ink wird als Text frei Hand Objekt in den RTF-Stream des InkEdit-Steuer Elements eingefügt.
-   Wenn eine Anwendung ein [inkstriche](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) oder ein [InkEdit](inkedit-control-reference.md) -Objekt in die Zwischenablage kopiert und das [**Aufzählungs Format InkClipboardFormats**](/windows/desktop/api/msinkaut/ne-msinkaut-inkclipboardformats) festgelegt ist, enthält das OLE-Objekt Zwischenablage Slot ein Text-Ink-OLE-Objekt.
-   Der Tablet PC-Eingabebereich kann Text frei Hand Objekte generieren.

Die Anwendung kann z. b. Handschrift erkennen und den Strichen das Erkennungs Ergebnis hinzufügen. Wenn Sie dann die Striche kopieren und in Microsoft Word als Text frei Hand Objekt einfügen, ist die Alternative zu diesem Wort in Word 2003 und höheren Versionen verfügbar.

Um Text frei Hand Objekte erfolgreich zu enthalten, muss eine Anwendung Unterstützung für OLE-Container für eingebettete Objekte implementieren. Damit der Container Text Freihand vollständig unterstützt, müssen Sie Folgendes erstellen:

-   Änderungen an der Anwendung zum Suchen und ersetzen. Anstatt eingebettete Objekte in der Suche zu überspringen, müssen diese Objekte für den Typ abgefragt werden. Wenn es sich um ein Text frei Hand Objekt handelt, müssen Sie instanziiert und nach dem entsprechenden Text abgefragt werden.
-   Änderungen am Auswahl Verhalten. Die Auswahl von Text frei Hand Objekten darf nie mit den Zieh Punkten der Größe angezeigt werden. Sie sollten auf die gleiche Weise ausgewählt werden, wie Text im Dokument ausgewählt wird. Der Auswahl Code für-Objekte muss erkennen, ob der Typ Text frei ist, und die Auswahl entsprechend anzeigen.
-   Verwendung von Umgebungs Eigenschaften. Ambient-Eigenschaften wie Schriftart Größe, Farbe und Fett Formatierung müssen an das Text frei Hand Objekt übertragen werden. Durch die Anwendung dieser Eigenschaften wird die Breite der handschriftlichen frei Hand Eingaben geändert, sodass ein Größen Update erforderlich ist, indem die [**iinklineinfo:: getinkblock**](/windows/desktop/api/msinkaut/nf-msinkaut-iinklineinfo-getinkextent) -oder [**IOleObject:: GetExtent**](/windows/win32/api/oleidl/nf-oleidl-ioleobject-getextent) -Methode aufgerufen wird.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Umrechnen eines Text frei Hand Objekts in frei Hand Eingaben](converting-a-text-ink-object-to-ink.md)
-   [Textink-APIs](text-ink-apis.md)
-   [sInk-und Tink-Objekte](sink-and-tink-objects.md)

 

 
