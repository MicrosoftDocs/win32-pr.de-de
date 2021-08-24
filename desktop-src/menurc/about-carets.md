---
title: Informationen zu Carets
description: In diesem Thema werden Carets erläutert.
ms.assetid: 4487c93c-9a0f-467c-86b1-969f664d5526
keywords:
- resources,carets
- Carets,Entfernen
- Blinkende Linien
- Blinkende Blöcke
- Blinkende Bitmaps
- Carets, Sichtbarkeit
- Carets, Blinkzeiten
- Blinkzeiten
- Carets, Positionen
- Entfernen von Carets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65ed2cbe50771b893c7a2ccc0874a882aabb23a1d0b4ba27822d7ce0ec47a18b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461320"
---
# <a name="about-carets"></a>Informationen zu Carets

Das System stellt ein Caretzeichen pro Nachrichtenwarteschlange bereit. Ein Fenster sollte nur dann ein Caretfeld erstellen, wenn es über den Tastaturfokus verfügt oder aktiv ist. Das Fenster sollte den Caretpunkt zerstören, bevor der Tastaturfokus verloren geht oder inaktiv wird. Weitere Informationen zur Tastatureingabe finden Sie unter [Tastatureingabe.](/windows/desktop/inputdev/keyboard-input)

Verwenden Sie die [**CreateCaret-Funktion,**](/windows/desktop/api/Winuser/nf-winuser-createcaret) um die Parameter für ein Carett anzugeben. Das System bildet ein Caretelement durch Umkehren der Pixelfarbe innerhalb des Rechtecks, das durch Position, Breite und Höhe des Caretelements angegeben wird. Breite und Höhe werden in logischen Einheiten angegeben. daher unterliegt die Darstellung eines Carets dem Zuordnungsmodus des Fensters.

Die folgenden Themen werden in diesem Abschnitt erläutert.

-   [Sichtbarkeit von Caret](#caret-visibility)
-   [Caret Blink Time](#caret-blink-time)
-   [Caretposition](#caret-position)
-   [Entfernen eines Carets](#removing-a-caret)

## <a name="caret-visibility"></a>Sichtbarkeit von Caret

Verwenden Sie nach dem Definieren des Carets die [**ShowCaret-Funktion,**](/windows/desktop/api/Winuser/nf-winuser-showcaret) um das Carett-Füllungs-Kit sichtbar zu machen. Wenn das Caretzeichen angezeigt wird, beginnt es automatisch mit dem Blinken. Um ein durchgezogenes Caretelement anzuzeigen, stellt das System jedes Pixel im Rechteck um. um ein graues Caretelement anzuzeigen, wird jedes andere Pixel vom System umgekehrt. Um ein Bitmap-Caretmuster anzuzeigen, stellt das System nur die weißen Bits der Bitmap invertiert.

## <a name="caret-blink-time"></a>Caret Blink Time

Die verstrichene Zeit in Millisekunden, die zum Umkehren des Caretstrichs erforderlich ist, wird als *Blinkzeit* bezeichnet. Das Caretzeichen blinkt, solange der Thread, der die Nachrichtenwarteschlange besitzt, über eine Nachrichtenpump verfügt, die die Nachrichten verarbeitet.

Der Benutzer kann die Blinkzeit des Carets mithilfe des Systemsteuerung festlegen, und Anwendungen sollten die einstellungen berücksichtigen, die der Benutzer ausgewählt hat. Eine Anwendung kann die Blinkzeit des Carets mithilfe der [**GetCaretBlinkTime-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) bestimmen. Wenn Sie eine Anwendung schreiben, die es dem Benutzer ermöglicht, die Blinkzeit anzupassen, z. B. ein Systemsteuerung Applet, verwenden Sie die [**SetCaretBlinkTime-Funktion,**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) um die Rate der Blinkzeit auf eine angegebene Anzahl von Millisekunden festzulegen.

Die *Flashzeit* ist die verstrichene Zeit in Millisekunden, die zum Anzeigen, Umkehren und Wiederherstellen der Anzeige des Carets erforderlich ist. Die Flashzeit eines Carets ist doppelt so hoch wie die Blinkzeit.

## <a name="caret-position"></a>Caretposition

Sie können die Position des Carets mithilfe der [**GetCaretPos-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getcaretpos) bestimmen. Die Position in Clientkoordinaten wird in eine Struktur kopiert, die von einem Parameter in **GetCaretPos** angegeben wird. Eine Anwendung kann einen Caret in einem Fenster mithilfe der [**SetCaretPos-Funktion**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos) verschieben. Ein Fenster kann ein Carett nur verschieben, wenn es bereits im Besitz des Carets ist. **SetCaretPos** kann das Caretset unabhängig davon verschieben, ob es sichtbar ist oder nicht.

## <a name="removing-a-caret"></a>Entfernen eines Carets

Sie können ein Caretchen vorübergehend entfernen, indem Sie es ausblenden, oder Sie können es dauerhaft entfernen, indem Sie es zerstören. Verwenden Sie zum Ausblenden des Carets die [**HideCaret-Funktion.**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) Dies ist nützlich, wenn Ihre Anwendung den Bildschirm während der Verarbeitung einer Nachricht neu zeichnen muss, das Caretzeichen jedoch nicht im Weg halten muss. Wenn die Anwendung das Zeichnen abgeschlossen hat, kann sie das Caretzeichen mithilfe der [**ShowCaret-Funktion**](/windows/desktop/api/Winuser/nf-winuser-showcaret) erneut anzeigen. Das Ausblenden des Caretzeichens zerstört nicht seine Form oder macht die Einfügemarke ungültig. Das Ausblenden des Caretpunkts ist kumulativ. Das heißt, wenn die Anwendung **HideCaret** fünfmal aufruft, muss sie **ShowCaret** auch fünfmal aufrufen, bevor das Caretbeispiel wieder angezeigt wird.

Verwenden Sie die [**DestroyCaret-Funktion,**](/windows/desktop/api/Winuser/nf-winuser-destroycaret) um den Caretbildschirm zu entfernen und seine Form zu zerstören. **DestroyCaret** zerstört das Carett nur, wenn das an der aktuellen Aufgabe beteiligte Fenster das Carett-Leiste besitzt.

 

 