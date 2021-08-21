---
description: 'Um die Unterstützung von Ink in Anwendungen zu unterstützen, gibt es zwei Objekte, die beide eingebettet werden können und von jedem OLE-Container unterstützt werden: das Text-Ink-Objekt (tInk) und das Sketch-Ink-Objekt (sInk).'
ms.assetid: 0202e91c-c7a0-4e7b-a1c6-a2f58c11c0be
title: Arbeiten mit dem Text Ink-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 938d7e68795147913b64cad399f70ac6c1d2fdb06edc19e6d0c0b6c64add6422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449263"
---
# <a name="working-with-the-text-ink-object"></a>Arbeiten mit dem Text Ink-Objekt

Um die Unterstützung von Ink in Anwendungen zu unterstützen, gibt es zwei Objekte, die beide eingebettet werden können und von jedem OLE-Container unterstützt werden: das Text-Ink-Objekt (tInk) und das Sketch-Ink-Objekt (sInk).

Das Text-Ink-Objekt ist ein OLE-Objekt, das Ink darstellt, von dem erwartet wird, dass es Wörter bildet. Mit einem Text-Ink-Objekt kann die handschriftliche Ink-Datei in Text konvertiert werden, indem aus einer Liste alternativer Objekte eine Auswahl erstellt wird. Die Farbe und Größe des Freitextobjekts kann programmgesteuert festgelegt werden und kann auf den Attributen des Texts um das Objekt basieren. Das Text-Ink-Objekt soll ein einzelnes Wort enthalten.

Das Text-Ink-Objekt unterstützt den Standardsatz von OLE-Schnittstellen, die für das Einbetten und die Unterstützung der Zwischenablage erforderlich sind. Die [**IPersistStream-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-ipersiststream) liest aus einem Datenstrom und schreibt in einen Stream im isf-Serialisierungsformat (Ink Serialized Format). Das Text-Ink-Objekt stellt die [**IInkLineInfo-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinklineinfo) für den Zugriff auf die Anzeigeeigenschaften und die Liste der Erkennungsergebnis bereit.

Das Text-Ink-Objekt kann für die Interoperabilität zwischen Anwendungen verwendet werden, indem es entweder im OLE-Objektslot in der Zwischenablage platziert, in RTF eingebettet oder in einem ISF-Stream beibehalten wird.

Ein Text-Ink-Objekt kann auf folgende Weise generiert werden.

-   Das [InkEdit-Steuerelement](inkedit-control-reference.md) verwendet das Text-Ink-Objekt. Die Funktionalität des InkEdit-Steuerelements ist ein Obersatz der RichEdit-Standardsteuerfunktionen. Ink wird als Text-Ink-Objekt in den RTF-Stream des InkEdit-Steuerelements eingefügt.
-   Wenn eine Anwendung ein [InkStrokes-](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) oder [InkEdit-Objekt](inkedit-control-reference.md) in die Zwischenablage kopiert und [**das InkClipboardFormats-Enumerationsformat**](/windows/desktop/api/msinkaut/ne-msinkaut-inkclipboardformats) festgelegt ist, enthält der OLE-Objektslot Zwischenablage ein TEXT-Ink-OLE-Objekt.
-   Der Tablet PC-Eingabebereich kann Text-Ink-Objekte generieren.

Ihre Anwendung kann z. B. Handschrift erkennen und den Strichen das Erkennungsergebnis hinzufügen. Wenn Sie dann die Striche kopieren und in Microsoft Word als Text-Freitextobjekt einfügen, ist eine Alternative für dieses Wort in Word 2003 und höher verfügbar.

Um Text-Ink-Objekte erfolgreich enthalten zu können, muss eine Anwendung OLE-Containerunterstützung für eingebettete Objekte implementieren. Damit der Container Text-Ink vollständig unterstützt, müssen Sie anschließend:

-   Änderungen an der Anwendung für Suchen und Ersetzen. Anstatt eingebettete Objekte in der Suche zu überspringen, müssen diese Objekte für den Typ verhört werden. Wenn es sich um ein Text-Ink-Objekt handelt, müssen sie instanziiert und nach dem entsprechenden Text abgefragt werden.
-   Änderungen am Auswahlverhalten. Die Auswahl von Text-Ink-Objekten sollte nie mit Größenziehpunkten angezeigt werden. Sie sollten auf die gleiche Weise ausgewählt werden wie Text im Dokument. Der Auswahlcode für Objekte muss erkennen, ob es sich bei dem Typ um Eine-Text-Ink handelt, und die Auswahl entsprechend anzeigen.
-   Verwendung von Umgebungseigenschaften. Umgebungseigenschaften wie Schriftgrad, Farbe und Fettformatierung müssen an das Text-Ink-Objekt übertragen werden. Die Anwendung dieser Eigenschaften ändert die Breite der handschriftlichen Freihandschrift, sodass eine Größenaktualisierung erforderlich ist, indem die [**IInkLineInfo::GetInkExtent-**](/windows/desktop/api/msinkaut/nf-msinkaut-iinklineinfo-getinkextent) oder [**IOleObject::GetExtent-Methode aufruft.**](/windows/win32/api/oleidl/nf-oleidl-ioleobject-getextent)

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Konvertieren eines Text-Ink-Objekts in Ink](converting-a-text-ink-object-to-ink.md)
-   [Text-Ink-APIs](text-ink-apis.md)
-   [sInk- und tInk-Objekte](sink-and-tink-objects.md)

 

 
