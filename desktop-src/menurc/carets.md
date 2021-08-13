---
title: Carets
description: In diesem Abschnitt werden Carets erläutert, bei denen es sich um blinkende Linien, Blöcke oder Bitmaps im Clientbereich eines Fensters handelt.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\carets.htm
keywords:
- resources,carets
- Carets,about
- blinkende Linien
- blinkende Blöcke
- blinkende Bitmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ed77a9d7fe315f5cef1be501c6392cce5fcfc3e79c5994f197a9fe6e254d8f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118734855"
---
# <a name="carets"></a>Carets

Ein *Caretstrich* ist eine blinkende Linie, ein Block oder eine Bitmap im Clientbereich eines Fensters. Das Caret-Zeichen gibt in der Regel die Stelle an, an der Text oder Grafiken eingefügt werden.

Die folgende Abbildung zeigt einige häufige Variationen in der Darstellung des Caret-Zeichens.

![Zeigt fünf verschiedene Möglichkeiten an, wie ein Caret-Caret-Format angezeigt werden kann.](images/cscrt-01.png)

Anwendungen können ein Caret-Caret-Caret-Paar erstellen, dessen Blinkzeit ändern und das Caret-Bzw. -Caret anzeigen, ausblenden oder ändern.

### <a name="in-this-section"></a>In diesem Abschnitt



| Name                                   | Beschreibung                                                               |
|----------------------------------------|---------------------------------------------------------------------------|
| [Informationen zu Carets](about-carets.md)       | Erläutert Carets.<br/>                                              |
| [Verwenden von Carets](using-carets.md)       | Codebeispiele, die zeigen, wie Aufgaben im Zusammenhang mit Carets durchgeführt werden.<br/> |
| [Caretreferenz](caret-reference.md) | Enthält die API-Referenz.<br/>                                    |



 

### <a name="caret-functions"></a>Caretfunktionen



| Name                                           | Beschreibung                                                                                                                                                                                                                                                   |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret)             | Erstellt eine neue Form für das System caret und weist dem angegebenen Fenster den Besitz des Caret-Carets zu. Die Caretform kann eine Linie, ein Block oder eine Bitmap sein. <br/>                                                                                         |
| [**DestroyCaret**](/windows/desktop/api/Winuser/nf-winuser-destroycaret)           | Zerstört die aktuelle Form des Caret-Carets, gibt das Caret-Caret-Caret aus dem Fenster frei und entfernt das Caret-Caret vom Bildschirm. <br/>                                                                                                                                       |
| [**GetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) | Ruft die Zeit ab, die erforderlich ist, um die Pixel des Caret-Carets zurück zu wenden. Der Benutzer kann diesen Wert festlegen. <br/>                                                                                                                                                            |
| [**GetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-getcaretpos)             | Kopiert die Position des Caret-Carets in die angegebene [**POINT-Struktur.**](/previous-versions//dd162805(v=vs.85)) <br/>                                                                                                                                                                    |
| [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret)                 | Entfernt das Caret-Caret vom Bildschirm. Das Ausblenden eines Caret-Zeichens zerstört nicht seine aktuelle Form und macht die Einfügemarke nicht ungültig. <br/>                                                                                                                           |
| [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) | Legt die Blinkzeit des Caretzeichens auf die angegebene Anzahl von Millisekunden fest. Die Blinkzeit ist die verstrichene Zeit in Millisekunden, die zum Umdrehen der Pixel des Caretstrichs erforderlich ist. <br/>                                                                                    |
| [**SetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos)             | Verschiebt das Caret-Caret auf die angegebenen Koordinaten. Wenn das Fenster, das das Caretmenü besitzt, mit dem **KLASSENstil CS \_ OWNDC** erstellt wurde, unterliegen die angegebenen Koordinaten dem Zuordnungsmodus des Gerätekontexts, der diesem Fenster zugeordnet ist. <br/> |
| [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret)                 | Macht das Caret-Zeichen an der aktuellen Position des Caret-Zeichens auf dem Bildschirm sichtbar. Wenn das Caret-Zeichen sichtbar wird, wird es automatisch blinken. <br/>                                                                                                          |



 

 

