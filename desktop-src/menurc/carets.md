---
title: Caretzeichen
description: In diesem Abschnitt werden die Caretzeichen erläutert, die Zeilen, Blöcke oder Bitmaps im Client Bereich eines Fensters blinken.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\carets.htm
keywords:
- Ressourcen, Caretzeichen
- Caretzeichen, Info
- blinkende Linien
- blinkende Blöcke
- blinken von Bitmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50cb99dfc324aa039924fa26683ab0a7674706ea
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "104393826"
---
# <a name="carets"></a>Caretzeichen

Ein *Caretzeichen* ist eine blinkende Zeile, ein Block oder eine Bitmap im Client Bereich eines Fensters. Die Einfügemarke gibt in der Regel den Ort an, an dem Text oder Grafiken eingefügt werden.

In der folgenden Abbildung werden einige allgemeine Variationen der Darstellung der Einfügemarke veranschaulicht.

![Zeigt fünf unterschiedliche Möglichkeiten, wie ein Caretzeichen angezeigt werden kann.](images/cscrt-01.png)

Anwendungen können eine Einfügemarke erstellen, die Blinkzeit ändern und die Einfügemarke anzeigen, ausblenden oder verschieben.

### <a name="in-this-section"></a>In diesem Abschnitt



| Name                                   | BESCHREIBUNG                                                               |
|----------------------------------------|---------------------------------------------------------------------------|
| [Informationen zu Caretzeichen](about-carets.md)       | Erläutert Caretzeichen.<br/>                                              |
| [Verwenden von Caretzeichen](using-carets.md)       | Code Beispiele, die das Ausführen von Aufgaben im Zusammenhang mit Caretzeichen veranschaulichen.<br/> |
| [Verweis auf Caretzeichen](caret-reference.md) | Enthält die API-Referenz.<br/>                                    |



 

### <a name="caret-functions"></a>Caretzeichen



| Name                                           | BESCHREIBUNG                                                                                                                                                                                                                                                   |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Auflistungs Daten Satz**](/windows/desktop/api/Winuser/nf-winuser-createcaret)             | Erstellt eine neue Form für die System Einfügemarke und weist dem angegebenen Fenster den Besitz der Einfügemarke zu. Die Form des Caretzeichen kann eine Linie, ein Block oder eine Bitmap sein. <br/>                                                                                         |
| [**DestroyCaret**](/windows/desktop/api/Winuser/nf-winuser-destroycaret)           | Zerstört die aktuelle Form des Caretzeichen, gibt die Einfügemarke aus dem Fenster frei und entfernt die Einfügemarke aus dem Bildschirm. <br/>                                                                                                                                       |
| [**Getcaretblinktime**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) | Ruft die Zeit ab, die zum Umkehren der Pixel der Einfügemarke benötigt wird. Der Benutzer kann diesen Wert festlegen. <br/>                                                                                                                                                            |
| [**Getcaretpos**](/windows/desktop/api/Winuser/nf-winuser-getcaretpos)             | Kopiert die Position der Einfügemarke in die angegebene [**Punkt**](/previous-versions//dd162805(v=vs.85)) Struktur. <br/>                                                                                                                                                                    |
| [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret)                 | Entfernt die Einfügemarke aus dem Bildschirm. Beim Ausblenden einer Einfügemarke wird die aktuelle Form nicht zerstört, oder die Einfügemarke wird ungültig. <br/>                                                                                                                           |
| [**Setcaretblinktime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) | Legt die Blinkzeit des Caretzeichen auf die angegebene Anzahl von Millisekunden fest. Die Blink Zeit ist die verstrichene Zeit (in Millisekunden), die erforderlich ist, um die Pixel des Caretzeichen umzukehren. <br/>                                                                                    |
| [**SetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos)             | Verschiebt die Einfügemarke zu den angegebenen Koordinaten. Wenn das Fenster, das die Einfügemarke besitzt, mit dem **CS- \_ owndc** -Klassen Stil erstellt wurde, unterliegen die angegebenen Koordinaten dem Kartenmodus des Geräte Kontexts, der diesem Fenster zugeordnet ist. <br/> |
| [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret)                 | Macht das Caretzeichen auf dem Bildschirm an der aktuellen Position des Caretzeichen sichtbar. Wenn das Caretzeichen sichtbar wird, beginnt es automatisch mit dem blinken. <br/>                                                                                                          |



 

 

