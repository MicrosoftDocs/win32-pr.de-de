---
title: Informationen zu Caretzeichen
description: In diesem Thema werden Carets erläutert.
ms.assetid: 4487c93c-9a0f-467c-86b1-969f664d5526
keywords:
- Ressourcen, Caretzeichen
- Caretzeichen, entfernen
- blinkende Linien
- blinkende Blöcke
- blinken von Bitmaps
- Caretzeichen, Sichtbarkeit
- Caretzeichen, blinkende Zeiten
- blinkende Zeiten
- Caretzeichen, Positionen
- Entfernen von Caretzeichen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a19eb3895ada13297f090a09529b2bcb7c75dee
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106337650"
---
# <a name="about-carets"></a>Informationen zu Caretzeichen

Das System stellt eine Einfügemarke pro Nachrichten Warteschlange bereit. Ein Fenster sollte nur dann eine Einfügemarke erstellen, wenn es den Tastaturfokus besitzt oder aktiv ist. Das Fenster muss die Einfügemarke zerstören, bevor der Tastaturfokus verloren geht oder inaktiv wird. Weitere Informationen zur Tastatureingabe finden Sie unter [Tastatureingabe](/windows/desktop/inputdev/keyboard-input).

Verwenden Sie die Funktion " [**kreatecaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) ", um die Parameter für eine Einfügemarke anzugeben. Das System bildet eine Einfügemarke, indem die Pixelfarbe innerhalb des Rechtecks, das durch die Position, Breite und Höhe der Einfügemarke angegeben wird, umgekehrt wird. Breite und Höhe werden in logischen Einheiten angegeben. Daher wird die Darstellung einer Einfügemarke dem Kartenmodus des Fensters unterzogen.

Die folgenden Themen werden in diesem Abschnitt erläutert.

-   [Sichtbarkeit von Textcursor](#caret-visibility)
-   [Blinkzeit des Caretzeichen](#caret-blink-time)
-   [Position des Caretzeichen](#caret-position)
-   [Entfernen einer Einfügemarke](#removing-a-caret)

## <a name="caret-visibility"></a>Sichtbarkeit von Textcursor

Nachdem die Einfügemarke definiert ist, verwenden Sie die [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) -Funktion, um das Caretzeichen sichtbar zu machen. Wenn die Einfügemarke angezeigt wird, beginnt Sie automatisch mit dem blinken. Um einen Einfügemarke anzuzeigen, kehrt das System jedes Pixel im Rechteck um. zum Anzeigen eines grauen Caretzeichen kehrt das System alle anderen Pixel um. um ein Bitmap-Caretzeichen anzuzeigen, kehrt das System nur die weißen Bits der Bitmap um.

## <a name="caret-blink-time"></a>Blinkzeit des Caretzeichen

Die verstrichene Zeit in Millisekunden, die zum Umkehren der Einfügemarke erforderlich ist, wird als *Blinkzeit* bezeichnet. Die Einfügemarke blinkt, solange der Thread, der die Nachrichten Warteschlange besitzt, über ein nachrichtenpump verfügt, das die Nachrichten verarbeitet.

Der Benutzer kann die blinkende Zeit der Einfügemarke mithilfe der Systemsteuerung festlegen, und Anwendungen sollten die vom Benutzer ausgewählten Einstellungen berücksichtigen. Eine Anwendung kann die Blinkzeit des Caretzeichen mithilfe der [**getcaretblinktime**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) -Funktion bestimmen. Wenn Sie eine Anwendung schreiben, die es dem Benutzer ermöglicht, die Blink Zeit anzupassen (z. b. ein System Steuerungs Applet), verwenden Sie die [**setcaretblinktime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) -Funktion, um die Rate der Blink Zeit auf eine angegebene Anzahl von Millisekunden festzulegen.

Die *Flash Zeit* ist die verstrichene Zeit in Millisekunden, die zum Anzeigen, umkehren und Wiederherstellen der Anzeige des Caretzeichen benötigt wird. Die Flash Zeit eines Caretzeichen ist doppelt so groß wie die Blink Zeit.

## <a name="caret-position"></a>Position des Caretzeichen

Sie können die Position der Einfügemarke mithilfe der [**getcaretpos**](/windows/desktop/api/Winuser/nf-winuser-getcaretpos) -Funktion ermitteln. Die Position in Client Koordinaten wird in eine Struktur kopiert, die von einem Parameter in **getcaretpos** angegeben wird. Eine Anwendung kann mithilfe der [**SetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos) -Funktion eine Einfügemarke in ein Fenster verschieben. Ein Fenster kann eine Einfügemarke nur verschieben, wenn Sie die Einfügemarke bereits besitzt. **SetCaretPos** können die Einfügemarke verschieben, unabhängig davon, ob Sie sichtbar ist.

## <a name="removing-a-caret"></a>Entfernen einer Einfügemarke

Sie können eine Einfügemarke vorübergehend entfernen, indem Sie Sie ausblenden, oder Sie können die Einfügemarke dauerhaft entfernen, indem Sie sie zerstören. Um das Caretzeichen auszublenden, verwenden Sie die [**hideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) -Funktion. Dies ist hilfreich, wenn die Anwendung den Bildschirm bei der Verarbeitung einer Nachricht neu zeichnen muss, aber die Einfügemarke nicht auf dem Weg halten muss. Nachdem die Anwendung das Zeichnen abgeschlossen hat, kann Sie die Einfügemarke mithilfe der [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) -Funktion erneut anzeigen. Durch das Ausblenden der Einfügemarke wird die Form nicht zerstört, oder die Einfügemarke wird ungültig. Das Ausblenden der Einfügemarke ist kumulativ. Das heißt, wenn die Anwendung " **hideCaret** " fünfmal aufruft, muss Sie " **ShowCaret** " auch fünfmal aufrufen, bevor die Einfügemarke wieder angezeigt wird.

Wenn Sie die Einfügemarke aus dem Bildschirm entfernen und deren Form zerstören möchten, verwenden Sie die Funktion [**DestroyCaret**](/windows/desktop/api/Winuser/nf-winuser-destroycaret) . **DestroyCaret** zerstört die Einfügemarke nur, wenn das Fenster, das an der aktuellen Aufgabe beteiligt ist, das Caretzeichen besitzt.

 

 