---
title: Informationen zu Statusanzeige-Steuerelementen
description: Eine Statusanzeige ist ein Fenster, mit dem eine Anwendung den Fortschritt eines langwierigen Vorgangs angeben kann. Sie besteht aus einem Rechteck, das während des Vorgangs fortgesetzt wird.
ms.assetid: 1db7a5c9-71cd-4ebc-86b8-8159f30348fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f00c80b1f9e97cec1657fe979a19437f607251b8
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730449"
---
# <a name="about-progress-bar-controls"></a>Informationen zu Statusanzeige-Steuerelementen

Eine Statusanzeige ist ein Fenster, mit dem eine Anwendung den Fortschritt eines langwierigen Vorgangs angeben kann.

Sie besteht aus einem Rechteck, das während des Vorgangs fortgesetzt wird.

Die folgende Abbildung zeigt eine Statusanzeige, in der keine visuellen Stile verwendet werden.

![Screenshot einer Statusanzeige, die Rechtecke in einer Zeile hinzufügt, um den Fortschritt anzuzeigen](images/pb-oldstyle.png)

Die folgende Abbildung zeigt eine Statusanzeige mit visuellen Stilen. Die Darstellung des Steuer Elements variiert je nach Betriebssystem und ausgewähltem Design. Weitere Informationen finden Sie unter [visuelle Stile](themes-overview.md).

![Screenshot einer Statusanzeige, die ein animiertes grünes Rechteck verlängert, um den Fortschritt anzuzeigen](images/pb-newstyle.png)

Weitere Informationen finden Sie unter den folgenden Überschriften.

-   [Verwenden von Status leisten](#using-progress-bars)
    -   [Bereich und aktuelle Position](#range-and-current-position)
    -   [Standard Verarbeitung der Statusanzeige Nachricht](#default-progress-bar-message-processing)
    -   [Marquee-Stil](#marquee-style)

## <a name="using-progress-bars"></a>Verwenden von Status leisten

Sie können eine Statusanzeige erstellen, indem Sie die Funktion " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " verwenden und die Fenster Klasse " [**Progress \_ Class**](common-control-window-classes.md) " angeben. Diese Fenster Klasse wird registriert, wenn die dll der allgemeinen Steuerelemente geladen wird. Weitere Informationen finden Sie unter Informationen [zu allgemeinen Steuerelementen](common-controls-intro.md).

Das-Steuerelement steht auch in der Microsoft Visual Studio Toolbox zur Verfügung, wo es als Fortschrittskontrolle bezeichnet wird.

### <a name="range-and-current-position"></a>Bereich und aktuelle Position

Der *Bereich* der Statusanzeige stellt die gesamte Dauer des Vorgangs dar, und die *aktuelle Position* stellt den Fortschritt dar, den die Anwendung zum Abschließen des Vorgangs durchgeführt hat. Die Fenster Prozedur verwendet den Bereich und die aktuelle Position, um den Prozentsatz der Statusanzeige zu ermitteln, der mit der Hervorhebungs Farbe aufgefüllt werden soll.

Wenn Sie die Bereichs Werte nicht festlegen, legt das System den Minimalwert auf 0 und den maximalen Wert auf 100 fest. Mithilfe der [**PBM- \_ SetRange**](pbm-setrange.md) -Nachricht können Sie den Bereich auf bequeme ganze Zahlen anpassen.

Eine Statusanzeige stellt mehrere Meldungen bereit, die Sie zum Festlegen der aktuellen Position verwenden können. Die [**PBM- \_ SetPos**](pbm-setpos.md) -Nachricht legt die Position auf einen angegebenen Wert fest. Die [**PBM- \_ Delta POS**](pbm-deltapos.md) -Nachricht erhöht die Position, indem der aktuellen Position ein angegebener Wert hinzugefügt wird.

Mithilfe der [**PBM- \_ SetStep**](pbm-setstep.md) -Nachricht können Sie ein schrittweises Inkrement für eine Statusanzeige angeben. Wenn Sie anschließend die [**PBM- \_ StepIt**](pbm-stepit.md) -Nachricht an die Statusanzeige senden, wird die aktuelle Position um das angegebene Inkrement erweitert. Standardmäßig ist das Schritt Inkrement auf 10 festgelegt.

### <a name="default-progress-bar-message-processing"></a>Standard Verarbeitung der Statusanzeige Nachricht

In diesem Abschnitt werden die Meldungen beschrieben, die von der Fenster Prozedur für die Klasse " [**Progress \_ Class**](common-control-window-classes.md) " verarbeitet werden.



| `Message`            | Verarbeitung wird ausgeführt                                                                                                                                                               |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WM \_ Erstellen**     | Ordnet eine anfängliche Struktur zu und initialisiert sie.                                                                                                                                    |
| **WM \_ zerstören**    | Gibt alle der Statusanzeige zugeordneten Ressourcen frei.                                                                                                                              |
| **WM- \_ erasebkgnd** | Zeichnet den Hintergrund und die Rahmen der Statusanzeige.                                                                                                                              |
| **WM- \_ getFont**    | Gibt das Handle für die aktuelle Schriftart zurück. Die Statusanzeige zeichnet derzeit keinen Text, sodass das Senden dieser Nachricht keine Auswirkung auf das Steuerelement hat.                                       |
| **WM- \_ Paint**      | Zeichnet die Statusanzeige. Wenn der *wParam* -Parameter ungleich **null** ist, geht das Steuerelement davon aus, dass es sich bei dem Wert um einen HDC handelt und zeichnet sich durch den Gerätekontext aus.                              |
| **WM- \_ setFont**    | Speichert das Handle in der neuen Schriftart und gibt das Handle für die vorherige Schriftart zurück. Die Statusanzeige zeichnet derzeit keinen Text, sodass das Senden dieser Nachricht keine Auswirkung auf das Steuerelement hat. |



 

### <a name="marquee-style"></a>Marquee-Stil

Durch das Erstellen des Statusanzeige-Steuer Elements mit dem [**PSB- \_ Marquee**](progress-bar-control-styles.md) -Stil können Sie es auf eine Weise animieren, die Aktivität anzeigt, aber nicht angibt, welcher Anteil der Aufgabe abgeschlossen ist. Der markierte Teil der Statusanzeige wird wiederholt entlang der Länge der Leiste verschoben. Sie können die Animation starten und Abbrechen und die Geschwindigkeit steuern, indem Sie die [**PBM- \_ setmarquee**](pbm-setmarquee.md) -Nachricht senden. Marquee-Status leisten verfügen nicht über einen Bereich oder eine Position.

Die folgende Abbildung zeigt eine Statusanzeige im Marquee-Modus. Der hervorgehobene Teil wird in der Leiste verschoben.

![Screenshot einer Statusanzeige, die eine grüne Hervorhebung über ein graues Rechteck bewegt, um den Fortschritt anzuzeigen](images/pb-marquee.png)

 

 