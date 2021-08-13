---
description: 'Um die Unterstützung von Freihand in Anwendungen zu unterstützen, gibt es zwei Objekte, die beide eingebettet werden können und von jedem OLE-Container unterstützt werden: das Text-Freihandobjekt (tInk) und das Sketch-Freihandobjekt (sInk).'
ms.assetid: 0202e91c-c7a0-4e7b-a1c6-a2f58c11c0be
title: Arbeiten mit dem Text-Ink-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 938d7e68795147913b64cad399f70ac6c1d2fdb06edc19e6d0c0b6c64add6422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449263"
---
# <a name="working-with-the-text-ink-object"></a>Arbeiten mit dem Text-Ink-Objekt

Um die Unterstützung von Freihand in Anwendungen zu unterstützen, gibt es zwei Objekte, die beide eingebettet werden können und von jedem OLE-Container unterstützt werden: das Text-Freihandobjekt (tInk) und das Sketch-Freihandobjekt (sInk).

Das Text-Ink-Objekt ist ein OLE-Objekt, das Ink darstellt, von dem erwartet wird, dass es Wörter bildet. Mit einem Text-Ink-Objekt kann die handschriftliche Ink in Text konvertiert werden, indem aus einer Liste alternativer Objekte ausgewählt wird. Farbe und Größe des Freihandtextobjekts können programmgesteuert festgelegt werden und auf den Attributen des Texts um das Objekt basieren. Das Text-Ink-Objekt soll ein einzelnes Wort enthalten.

Das Text-Freihandobjekt unterstützt den Standardsatz von OLE-Schnittstellen, der für die Unterstützung von Einbettung und Zwischenablage erforderlich ist. Die [**IPersistStream-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-ipersiststream) liest aus und schreibt in einen Stream im serialisierten Freihandformat (ISF). Das Text-Freihandobjekt stellt die [**IInkLineInfo-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinklineinfo) bereit, um auf die Anzeigeeigenschaften und die Erkennungsergebnisliste zuzugreifen.

Das Freihandtextobjekt kann für die Interoperabilität zwischen Anwendungen verwendet werden, indem es entweder im OLE-Objektslot in der Zwischenablage platziert, in RTF eingebettet oder in einem ISF-Stream gespeichert wird.

Ein Text-Ink-Objekt kann auf folgende Weise generiert werden.

-   Das [InkEdit-Steuerelement](inkedit-control-reference.md) verwendet das Text-Ink-Objekt. Die Funktionalität des InkEdit-Steuerelements ist eine Obermenge der standardmäßigen RichEdit-Steuerelementfunktionalität. Ink wird als Text-Ink-Objekt in den RTF-Datenstrom des InkEdit-Steuerelements eingefügt.
-   Wenn eine Anwendung ein [InkStrokes-](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) oder ein [InkEdit-Objekt](inkedit-control-reference.md) in die Zwischenablage kopiert und das [**Enumerationsformat InkClipboardFormats**](/windows/desktop/api/msinkaut/ne-msinkaut-inkclipboardformats) festgelegt ist, enthält der Zwischenablageslot des OLE-Objekts ein TEXT-Freihand-OLE-Objekt.
-   Der Tablet PC-Eingabebereich kann Texteingabeobjekte generieren.

Beispielsweise kann Ihre Anwendung Handschrift erkennen und den Strichen das Erkennungsergebnis hinzufügen. Wenn Sie dann die Striche kopieren und in Microsoft Word als Freihandtextobjekt einfügen, stehen alternative Striche für dieses Wort in Word 2003 und höher zur Verfügung.

Um Text-Ink-Objekte erfolgreich enthalten zu können, muss eine Anwendung OLE-Containerunterstützung für eingebettete Objekte implementieren. Damit der Container Freihandtext vollständig unterstützt, müssen Sie folgendes inserieren:

-   Änderungen an der Anwendung für Suchen und Ersetzen. Anstatt eingebettete Objekte in der Suche zu überspringen, müssen diese Objekte nach Typ abgefragt werden. Wenn es sich um ein Text-Ink-Objekt handelt, müssen sie instanziiert und nach dem entsprechenden Text abgefragt werden.
-   Änderungen am Auswahlverhalten. Die Auswahl von Text-Ink-Objekten sollte nie mit Größenziehpunkten angezeigt werden. Sie sollten auf die gleiche Weise ausgewählt werden, wie text im Dokument ausgewählt wird. Auswahlcode für Objekte muss erkennen, ob es sich bei dem Typ um Text ink handelt, und die Auswahl entsprechend anzeigen.
-   Verwendung von Umgebungseigenschaften. Umgebungseigenschaften wie Schriftgrad, Farbe und Fettformatierung müssen an das Text-Ink-Objekt übertragen werden. Die Anwendung dieser Eigenschaften ändert die Breite der handschriftlichen Freihand, sodass eine Größenaktualisierung erforderlich ist, indem die [**IInkLineInfo::GetInkExtent-**](/windows/desktop/api/msinkaut/nf-msinkaut-iinklineinfo-getinkextent) oder [**IOleObject::GetExtent-Methode**](/windows/win32/api/oleidl/nf-oleidl-ioleobject-getextent) aufgerufen wird.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Konvertieren eines Text-Ink-Objekts in eine Ink-Datei](converting-a-text-ink-object-to-ink.md)
-   [Text-Ink-APIs](text-ink-apis.md)
-   [sInk- und tInk-Objekte](sink-and-tink-objects.md)

 

 
