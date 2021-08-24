---
title: Implementieren eines Benutzeroberfläche
description: In diesem Abschnitt werden einige der Aufgaben beschrieben, die mit der Implementierung einer Benutzeroberfläche für eine Windows Anwendung verbunden sind.
ms.assetid: 889791a7-d12c-4ec6-9b04-8fed14ecdb2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7967474781e180ab29a42fce6884cc391515eef0211107852659eace3490e712
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702340"
---
# <a name="implementing-a-user-interface"></a>Implementieren eines Benutzeroberfläche

In diesem Abschnitt werden einige der Aufgaben beschrieben, die mit der Implementierung einer Benutzeroberfläche für eine Windows Anwendung verbunden sind.

-   [Prototyp](#prototype)
-   [Erstellen](#construct)
-   [Vereinfachen](#simplify)
    -   [Reduce, Reuse, Declutter](#reduce-reuse-declutter)
    -   [Die beste Benutzeroberfläche ist keine Benutzeroberfläche.](#the-best-ui-is-no-ui)
    -   [Weniger Benutzeroberfläche ist bessere Benutzeroberfläche](#less-ui-is-better-ui)
    -   [Konsistente Benutzeroberfläche ist gute Benutzeroberfläche](#consistent-ui-is-good-ui)

## <a name="prototype"></a>Prototyp

Benutzeroberflächen (UI) sollten aus der Liste der Benutzerszenarien und Anforderungen entworfen werden, die im Schritt zur Benutzeranalyse identifiziert wurden.

Prototypen können so einfach wie Stiftzeichnungen oder so komplex wie interaktive Bildschirmmodelle sein. Behalten Sie alle vorherigen Arbeiten bei, da dies hilfreich sein kann, wenn Die beteiligten Personen die alternativen Alternativen zeigen, die berücksichtigt wurden, und erklären, warum sie verworfen wurden.

Versuchen Sie, diesen Schritt auf maximal zwei oder drei Prototypen zu beschränken. Prototypen müssen nicht vollständig sein. Sie müssen lediglich die Erfahrung mit der Verwendung der echten Anwendung effektiv simulieren.

Zeigen Sie die Prototypen, und verfolgen Sie Benutzerfeedback nach, um die allgemeinen Benutzerfreundlichkeitstrends zu identifizieren. Wenn möglich, verwerfen Sie die am wenigsten erfolgreichen Prototypen, und integrieren Sie so viel nützliches Feedback wie möglich in einen oder mehrere der verbleibenden Prototypen. Wiederholen Sie diesen Vorgang, wenn Zeit und Ressourcen dies zulassen.

Es stehen verschiedene Prototyptools zur Verfügung, darunter [SketchFlow](/previous-versions/visualstudio/design-tools/expression-studio-3/ee341458(v=expression.30)) in Microsoft Expression Studio 3, der Layout-Editor in Microsoft Visual Studio und sogar Microsoft Paint.

## <a name="construct"></a>Konstrukt

Berücksichtigen Sie beim Implementieren der Benutzeroberfläche für eine Anwendung Folgendes:

-   Befehlsstruktur

    Bestimmen Sie, ob eine herkömmliche Befehlsstruktur basierend auf Menüs und Symbolleisten oder eine alternative Befehlsstruktur basierend auf dem Windows Menübandframework implementiert werden soll. Weitere Informationen finden Sie unter [Menüs,](../menurc/menus.md) [Symbolleisten](../controls/toolbar-control-reference.md)und [Windows Menübandframework.](../windowsribbon/-uiplat-windowsribbon-entry.md)

-   Windows und Dialogfelder

    Implementieren Sie basierend auf dem Benutzeroberflächenentwurf und der Prototyperstellung die Anwendungsfenster, einschließlich hauptfenster, untergeordneter Fenster, Dialogfelder und Meldungsfelder. Befolgen Sie die UX-Richtlinien, um zu bestimmen, welche Stile und Steuerelemente in den Fenstern und Dialogfeldern verwendet werden sollen. Weitere Informationen finden Sie unter [Windows](../winmsg/windows.md), [Dialogfeldern](../dlgbox/dialog-boxes.md)und [Windows-Steuerelementen.](../controls/window-controls.md)

-   Benutzerdefinierte Steuerelemente

    Erstellen Sie neue benutzerdefinierte Steuerelemente nur, wenn Sie die gewünschte Funktionalität nicht von einem der Standardsteuerelemente Windows abrufen können. Die Entwicklung neuer benutzerdefinierter Steuerelemente ist sehr kostspielig und erfordert zusätzlichen Aufwand, um sie zugänglich zu machen. Wenn Ihre Anwendung benutzerdefinierte Steuerelemente erfordert, stellen Sie sicher, dass sie ausreichend für Hilfstechnologien verfügbar gemacht werden. Weitere Informationen finden Sie unter [Benutzerdefinierte Steuerelemente](../controls/user-controls-intro.md) und [Windows Automation-API.](../winauto/windows-automation-api-portal.md)

-   Unterstützung für Standardbenutzereingabegeräte

    Die meisten Windows Anwendungen müssen Benutzereingaben über Tastatur und Maus unterstützen. Die Möglichkeit, allein über die Tastatur zu navigieren und auf alle Anwendungsfunktionen zuzugreifen, ist besonders wichtig für Benutzer mit Sehbehinderung oder Mobilitätsproblemen. Weitere Informationen finden Sie unter [Benutzereingabe](../inputdev/user-input.md) und Engineering [Software for Accessibility eBook](https://www.microsoft.com/download/details.aspx?id=19262).

-   Visuelle Stile, Animationen und visuelle Effekte

    Windows enthält mehrere Technologien, mit denen Sie visuelles Interesse hinzufügen und die Benutzeroberfläche von denen anderer Anwendungen unterscheiden können. Dazu gehören das Angeben der visuellen Stile von Steuerelementen, das Hinzufügen von Animationen zu Benutzeroberflächenelementen und das Implementieren verschiedener visueller Effekte in der Benutzeroberfläche. Weitere Informationen finden Sie unter [Visual Styles](../controls/themes-overview.md), Windows [Animation Manager](../uianimation/-main-portal.md)und [Desktopfenster-Manager](../dwm/dwm-overview.md).

## <a name="simplify"></a>Vereinfachen von 

Eine erfolgreiche Benutzererfahrung hängt vom Ansatz, der Perspektive und den Annahmen des Entwicklers während des Entwurfsprozesses ab. Um ein grundlegendes Verständnis dafür zu erlangen, wie eine Anwendung von der Zielgruppe verwendet werden kann, müssen Sie über die Einschränkungen der Anforderungen des Entwicklers hinaus umfassend denken können. Wenn Sie diese Zeit, den Aufwand und die Forschung am Anfang eines Projekts investieren, zahlen Sie am Ende einen Gewinn aus.

### <a name="reduce-reuse-declutter"></a>Reduce, Reuse, Declutter

Features verbessern ein Produkt nur, wenn sie tatsächlich verwendet werden. In vielen Fällen kann die Verbreitung von Features zu Komplexität führen, da mehr Symbole, Menüelemente, Symbolleisten und Dialogfelder die Effizienz und Produktivität beeinträchtigen, anstatt einen Mehrwert zu schaffen.

### <a name="the-best-ui-is-no-ui"></a>Die beste Benutzeroberfläche ist keine Benutzeroberfläche.

Die Benutzeroberfläche impliziert, dass der Benutzer mit der Anwendung interagieren muss, um etwas zu bewirken. Im Idealfall ist keine Interaktion erforderlich. Aus Sicht des Benutzers funktioniert dies einfach. Wenn ein Feature hinzugefügt werden kann, das eine Benutzerinteraktion sicher entfernt, wird die Benutzerfreundlichkeit erheblich verbessert.

### <a name="less-ui-is-better-ui"></a>Weniger Benutzeroberfläche ist bessere Benutzeroberfläche

In vielen Fällen ist es nicht möglich, die Benutzeroberflächeninteraktion vollständig aus der Benutzeroberfläche zu entfernen. Je weniger Benutzerinteraktion von einer Anwendung benötigt wird, desto besser ist es jedoch.

Identifizieren Sie die gängigsten und wichtigsten Aktivitäten, die Benutzer mit der Anwendung ausführen, und machen Sie diese Funktionen in der Benutzeroberfläche zu den wichtigsten. Verwerfen Sie andere Funktionen und Aktivitäten entweder visuell, hierarchisch oder über optionale Anwendungseinstellungen und Benutzereinstellungen in einen niedrigeren Status.

-   Ersetzen statt Hinzufügen

    Die Ui-Regel besagt, dass Sie etwas nur hinzufügen, wenn Sie etwas wegnehmen können. Diese Regel zwingt einen Entwickler, kritisch über ein neues Feature nachzudenken, indem er die Auswirkungen berücksichtigt, die das Feature auf die gesamte Benutzeroberfläche hat.

    Neue Features sollten nicht heraufgestuft werden, da sie neu sind: Verwechseln Sie Marketing nicht mit Benutzerfreundlichkeit. Damit Benutzer neue Features in Ihrem Produkt finden können, fügen Sie dem **Menü Hilfe** ein Element hinzu, das die Änderungen beschreibt, die seit der letzten Version der Anwendung aufgetreten sind.

-   Der Benutzer ist eine eingeschränkte Ressource.

    Je mehr Funktionen gleichzeitig verfügbar gemacht werden, desto schwieriger ist es für einen Benutzer, die benötigte Funktionalität zu finden.

-   Es ist nur schwer zu unterbrechen.

    Wenn eine Anwendung ein Dialogfeld anzeigt, zwingt sie den Benutzer, das zu beenden, was er gerade tut, und auf etwas anderes zu achten. Wenn möglich, entfernen Sie die Notwendigkeit eines Dialogfelds vollständig, indem Sie Fehlerfälle und andere unterbrechungsfreie Benutzeroberflächen vermeiden. Weitere Informationen zu Nachrichtenrichtlinien finden Sie unter [Meldungen.](https://msdn.microsoft.com/library/dd535525.aspx)

-   Einfach kann leistungsstark sein

    Eine einfache Benutzeroberfläche impliziert keine fehlende Funktionalität. In der Regel ist das Ergebnis einer einfacheren Benutzeroberfläche eine verkürzte Lernkurve, eine höhere Effizienz und eine verbesserte Produktivität. Dies ermöglicht es einem Benutzer, seine Kenntnisse über die Anwendung zu verbessern.

### <a name="consistent-ui-is-good-ui"></a>Konsistente Benutzeroberfläche ist gute Benutzeroberfläche

Im Allgemeinen wird empfohlen, die Konsistenz in der gesamten Benutzeroberfläche einer Anwendung zu gewährleisten. Durch die Bereitstellung einer konsistenten Benutzeroberfläche kann ein Benutzer in viel kürzerer Zeit mit einer Anwendung vertrauter werden. Sie sind in der Lage, ihre vorhandenen Kenntnisse der Anwendung auf verschiedene Situationen anzuwenden und unbekannte Funktionen mit Zuverlässigkeit zu nutzen.

In seltenen Fällen bietet Konsistenz dem Benutzer keinen Vorteil und kann sogar die Benutzerfreundlichkeit beeinträchtigen. Machen Sie die Benutzeroberfläche nicht konsistent, wenn diese Konsistenz die Fähigkeit beeinträchtigt, eine Aufgabe auszuführen. Die Konsistenz an sich garantiert keine Benutzerfreundlichkeit. Es ist ein Fehler zu glauben, dass Konsistenz in der Schnittstelle zu einem guten Design führt.

Beispielsweise ist die Benutzeroberfläche von Spielen in der Regel sehr spezifisch für die Art des Spiels. Der Versuch, eine generische Benutzeroberfläche zu entwerfen, die gut für zwei spezialisierte Spiele geeignet ist, eines, das ein reifes Rad erfordert, und ein anderes, das am besten mit einem Kasten und Schaltflächen funktioniert, wird wahrscheinlich für beide Spiele nicht erfolgreich sein. Bestnfalls wird ein Mittelweg erreicht, der auch nicht gut geeignet ist.

Gute Daten zur Verwendung der Dinge sind der Schlüssel für diese Entscheidung. Machen Sie sich mit den Vor- und Nachteilen der einzelnen Kompromisse (Geschwindigkeit und Zuverlässigkeit, Einfaches Lernen im Vergleich zu Expertenkenntnissen, globale Konsistenz und lokale Optimierung) klar, und treffen Sie die besten Entscheidungen für das Feature in Bezug auf das gesamte Produkt.

Der Entwurf wählt aus, wie ein Fehler vorliegt: Die Optimierung für eine Sache bedeutet, dass ein Fehler bei einem anderen fehlschlägt. Der Schlüssel zu einem guten Benutzeroberflächenentwurf besteht darin, entscheiden zu können, welche Merkmale der Anwendung am wichtigsten sind und welche ausgeschnitten werden können.

 

 