---
title: Implementieren einer Benutzeroberfläche
description: In diesem Abschnitt werden einige der Aufgaben beschrieben, die mit der Implementierung einer Benutzeroberfläche für eine Windows-Anwendung verknüpft sind.
ms.assetid: 889791a7-d12c-4ec6-9b04-8fed14ecdb2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0941458e046a85dc6e27a684d8aa3a7ea609e889
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315734"
---
# <a name="implementing-a-user-interface"></a>Implementieren einer Benutzeroberfläche

In diesem Abschnitt werden einige der Aufgaben beschrieben, die mit der Implementierung einer Benutzeroberfläche für eine Windows-Anwendung verknüpft sind.

-   [Prototyp](#prototype)
-   [Erstellen](#construct)
-   [Vereinfachen](#simplify)
    -   [Reduzieren, wieder verwenden, überhäufen](#reduce-reuse-declutter)
    -   [Die beste Benutzeroberfläche ist keine Benutzeroberfläche.](#the-best-ui-is-no-ui)
    -   [Weniger Benutzeroberfläche ist eine bessere Benutzeroberfläche](#less-ui-is-better-ui)
    -   [Konsistente Benutzeroberfläche ist eine gute Benutzeroberfläche](#consistent-ui-is-good-ui)

## <a name="prototype"></a>Prototyp

Benutzeroberflächen (UI) sollten aus der Liste der Benutzer Szenarios und Anforderungen entworfen werden, die im Schritt zur Benutzer Analyse identifiziert wurden.

Prototypen können so einfach wie Stift Skizzen oder so komplex sein wie interaktive Bildschirm-Mockups. Behalten Sie alle vorherigen Aufgaben bei, da dies hilfreich sein kann, wenn Sie den beteiligten Alternativen zeigen, warum Sie verworfen wurden.

Versuchen Sie, diesen Schritt höchstens auf zwei oder drei Prototypen zu beschränken. Prototypen müssen nicht vollständig sein. Sie müssen lediglich die Verwendung der realen Anwendung effektiv simulieren.

Veranschaulichen Sie die Prototypen, und verfolgen Sie das Benutzer Feedback, um die allgemeinen Verb Nutzbarkeits Trends zu ermitteln. Verwerfen Sie ggf. die am wenigsten erfolgreichen Prototypen, und integrieren Sie so viel nützliches Feedback wie möglich in einen oder mehrere der verbleibenden Prototypen. Wiederholen Sie diesen Vorgang als Zeit und Ressourcen zulassen.

Es gibt verschiedene prototyptools, einschließlich " [schrägerflow](/previous-versions/visualstudio/design-tools/expression-studio-3/ee341458(v=expression.30)) " in Microsoft Expression Studio 3, den Layout-Editor in Microsoft Visual Studio und sogar Microsoft Paint.

## <a name="construct"></a>Konstrukt

Beachten Sie Folgendes, wenn Sie die Benutzeroberfläche für eine Anwendung implementieren:

-   Befehlsstruktur

    Bestimmen Sie, ob eine herkömmliche Befehlsstruktur auf der Grundlage von Menüs und Symbolleisten implementiert werden soll, oder eine Alternative Befehlsstruktur, die auf dem Windows-Menü Band Framework basiert. Weitere Informationen finden Sie unter [Menüs](../menurc/menus.md), [Symbolleisten](../controls/toolbar-control-reference.md)und Windows-Menü [Band Framework](../windowsribbon/-uiplat-windowsribbon-entry.md).

-   Fenster und Dialogfelder

    Implementieren Sie basierend auf dem Design der Benutzeroberfläche und der prototypenarbeit die Anwendungsfenster, einschließlich des Hauptfensters, der untergeordneten Fenster, Dialogfelder und Meldungs Felder. Befolgen Sie die UX-Richtlinien, um zu bestimmen, welche Stile und Steuerelemente in den Fenstern und Dialogfeldern verwendet werden sollen. Weitere Informationen finden Sie unter [Fenster](../winmsg/windows.md), [Dialog Felder](../dlgbox/dialog-boxes.md)und Windows-Steuer [Elemente](../controls/window-controls.md).

-   Benutzerdefinierte Steuerelemente

    Erstellen Sie neue benutzerdefinierte Steuerelemente nur dann, wenn Sie die gewünschte Funktionalität von einem der standardmäßigen Windows-Steuerelemente nicht erhalten können. Neue benutzerdefinierte Steuerelemente sind sehr kostspielig zu entwickeln und erfordern zusätzliche Arbeit, um Sie zugänglich zu machen. Wenn Ihre Anwendung benutzerdefinierte Steuerelemente erfordert, stellen Sie sicher, dass Sie den Hilfstechnologien angemessen ausgesetzt sind. Weitere Informationen finden Sie unter [benutzerdefinierte Steuerelemente](../controls/user-controls-intro.md) und [Windows-Automatisierungs-API](../winauto/windows-automation-api-portal.md).

-   Unterstützung für Standardbenutzer-Eingabegeräte

    Die meisten Windows-Anwendungen müssen Benutzereingaben über die Tastatur und die Maus unterstützen. Die Möglichkeit, nur über die Tastatur zu navigieren und auf alle Anwendungsfunktionen zuzugreifen, ist besonders wichtig für Benutzer, die sich sehbehindert oder Probleme mit der Mobilität haben. Weitere Informationen finden Sie unter [User Input](../inputdev/user-input.md) und The [Engineering Software for Barrierefreiheits](https://www.microsoft.com/download/details.aspx?id=19262)-e-book.

-   Visuelle Stile, Animationen und visuelle Effekte

    Windows umfasst verschiedene Technologien, mit denen Sie visuelle Interessen hinzufügen und die Benutzeroberfläche von anderen Anwendungen trennen können. Hierzu gehören das Angeben der visuellen Stile von Steuerelementen, das Hinzufügen von Animationen zu Benutzeroberflächen Elementen und das Implementieren verschiedener visueller Effekte in der Benutzeroberfläche. Weitere Informationen finden Sie unter [visuelle Stile](../controls/themes-overview.md), [Windows Animation Manager](../uianimation/-main-portal.md)und [Desktopfenster-Manager](../dwm/dwm-overview.md).

## <a name="simplify"></a>Vereinfachen von 

Eine erfolgreiche Benutzer Leistung hängt von dem Ansatz, der Perspektive und den Annahmen des Entwicklers während des Entwurfsprozesses ab. Wenn Sie ein grundlegendes Verständnis dafür haben, wie eine Anwendung von der Zielgruppe verwendet werden kann, müssen Sie sich über die Einschränkungen der Anforderungen des Entwicklers im allgemeinen Gedanken machen. Wenn Sie diese Zeit, den Aufwand und die Untersuchung am Anfang eines Projekts investieren, fallen am Ende Dividenden an.

### <a name="reduce-reuse-declutter"></a>Reduzieren, wieder verwenden, überhäufen

Features verbessern nur ein Produkt, wenn Sie tatsächlich verwendet werden. In vielen Fällen kann die Verbreitung von Features eine Komplexität mit sich bringen, indem weitere Symbole, Menü Elemente, Symbolleisten und Dialogfelder hinzugefügt werden, die die Effizienz und Produktivität beeinträchtigen, anstatt einen Wert hinzuzufügen.

### <a name="the-best-ui-is-no-ui"></a>Die beste Benutzeroberfläche ist keine Benutzeroberfläche.

Die Benutzeroberfläche impliziert, dass der Benutzer mit der Anwendung interagieren muss, damit etwas passiert. Im Idealfall ist keine Interaktion erforderlich. Aus Sicht des Benutzers funktioniert das nur. Wenn eine Funktion hinzugefügt werden kann, mit der eine Benutzerinteraktion sicher entfernt wird, ist die Benutzer Funktionalität deutlich besser.

### <a name="less-ui-is-better-ui"></a>Weniger Benutzeroberfläche ist eine bessere Benutzeroberfläche

In vielen Fällen ist es nicht möglich, die UI-Interaktion vollständig aus der Benutzeroberfläche zu entfernen. Der weniger Benutzereingriff, der von einer Anwendung benötigt wird, ist jedoch besser.

Identifizieren Sie die gängigsten und wichtigsten Aktivitäten, die Benutzer mit der Anwendung durchführen, und machen Sie diese Funktionen in der Benutzeroberfläche am prominentesten. Setzen Sie andere Funktionen und Aktivitäten entweder visuell, hierarchisch oder durch optionale Anwendungseinstellungen und Benutzereinstellungen auf einen niedrigeren Status um.

-   Anstelle von "Add" ersetzen

    Die Erhaltung der UI-Regel gibt an, dass Sie etwas nur dann hinzufügen, wenn Sie etwas entfernen können. Diese Regel zwingt einen Entwickler, eine neue Funktion in Erwägung zu ziehen, indem er die Auswirkungen der Funktion auf die gesamte Benutzer Funktionalität berücksichtigt.

    Neue Features sollten nicht höher gestuft werden, da Sie neu sind: Marketing nicht mit Nutzbarkeit verwechseln. Um Benutzern zu helfen, neue Funktionen in Ihrem Produkt zu finden, fügen Sie dem Menü **Hilfe** ein Element hinzu, das die Änderungen beschreibt, die seit der letzten Version der Anwendung aufgetreten sind.

-   Der Benutzer ist eine eingeschränkte Ressource.

    Die mehr Funktionalität, die zu einem beliebigen Zeitpunkt verfügbar gemacht wird, desto schwieriger ist es, dass ein Benutzer die benötigte Funktionalität findet.

-   Das unterbrechen ist grob.

    Wenn eine Anwendung ein Dialogfeld anzeigt, zwingt Sie den Benutzer, den Vorgang zu beenden, den Sie tatsächlich durchgeführt haben, und muss auf etwas anderes achten. Wenn möglich, entfernen Sie ein Dialogfeld vollständig, indem Sie Fehlerfälle und andere Benutzeroberflächen vermeiden. Weitere Informationen zu Nachrichten Richtlinien finden Sie unter [Nachrichten](https://msdn.microsoft.com/library/dd535525.aspx).

-   Einfach kann leistungsfähig sein

    Eine einfache Benutzeroberfläche impliziert keine fehlende Funktionalität. In der Regel ist das Ergebnis einer einfacheren Benutzeroberfläche eine verkürzte Lernkurve, eine höhere Effizienz und eine verbesserte Produktivität. Dies ermöglicht es einem Benutzer, seine Kenntnisse mit der Anwendung zu erhöhen.

### <a name="consistent-ui-is-good-ui"></a>Konsistente Benutzeroberfläche ist eine gute Benutzeroberfläche

Im Allgemeinen wird empfohlen, Konsistenz in einer Anwendungs Benutzeroberfläche zu gewährleisten. Durch die Bereitstellung einer konsistenten Benutzeroberfläche kann ein Benutzer in viel kürzerer Zeit mit einer Anwendung besser vertraut werden. Sie sind in der Lage, Ihre vorhandenen Kenntnisse der Anwendung auf unterschiedliche Situationen anzuwenden und mit vertrauenswürdiger Funktionalität zu verwenden.

In seltenen Fällen bietet die Konsistenz keinen Vorteil für den Benutzer und kann sogar die Benutzer Leistung beeinträchtigen. Machen Sie die Benutzeroberfläche nicht konsistent, wenn diese Konsistenz die Fähigkeit zum Ausführen einer Aufgabe beeinträchtigt. Die Konsistenz in sich selbst garantiert nicht die Verwendbarkeit. Es ist ein Fehler, zu bedenken, dass die Konsistenz in der Schnittstelle zu einem guten Entwurf führt.

Beispielsweise ist die Videospiel-Benutzeroberfläche in der Regel sehr spezifisch für die Art des Spiels. Wenn Sie versuchen, eine generische Benutzeroberfläche zu entwerfen, die für zwei spezialisierte Spiele geeignet ist, eine, die ein Mausrad erfordert, und eine andere, die am besten mit einem Joystick und Schaltflächen funktioniert, wird für jedes Spiel wahrscheinlich nicht erfolgreich sein. Es ist wahrscheinlich, dass ein mittlerer Grund wahrscheinlich erreicht wird, der für beides nicht geeignet ist.

Wenn Sie gute Daten darüber haben, wie Dinge verwendet werden, können Sie diese Entscheidung treffen. Machen Sie sich mit den vor-und Nachteile der einzelnen Kompromisse vertraut (Geschwindigkeit und Zuverlässigkeit, einfaches lernen im Vergleich zu Fachkenntnissen, globale Konsistenz und lokale Optimierung), und treffen Sie die besten Entscheidungen für das Feature im Zusammenhang mit dem gesamten Produkt.

Der Entwurf wählt, wie ein Fehler auftritt: die Optimierung für ein anderes bedeutet, dass er fehlschlägt. Der Schlüssel zu gutem Design der Benutzeroberfläche ist die Entscheidung, welche Merkmale der Anwendung am wichtigsten sind und welche ausgeschnitten werden können.

 

 