---
title: Modus für hohen Kontrast
description: Modus für hohen Kontrast
ms.assetid: 817F2BBD-3744-4D34-927F-EBF9F7894CC0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a288447dda8d3a76278ad695459d2c15598b328
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883893"
---
# <a name="high-contrast-mode"></a>Modus für hohen Kontrast

## <a name="platforms"></a>Plattformen

 **Clients** – Windows 8  
**Server** – Windows Server 2012  



## <a name="description"></a>Beschreibung

In Windows Betriebssystemen war der Modus mit hohem Kontrast auf Designs beschränkt, die unter klassischen Designs ausgeführt wurden, die nicht visuell formatiert waren. In Windows 8 und Windows Server 2012 wurde der klassische Modus entfernt und durch visuell formatierte Designs mit hohem Kontrast ersetzt. Einer der Hauptvorteile dieser Änderung ist das Entfernen eines separaten Codepfads für Apps, die im klassischen Modus ausgeführt werden.

Entwickler müssen immer noch wissen, wie sich der Modus mit hohem Kontrast auf ihre App auswirken kann und wie sie eine App entwickeln, die wirklich stilunabhängig ist. Dies ist wichtig, da die falsche Verwendung oder Annahme von Designfarben dazu führen kann, dass sich Apps unter einem visuellen Stil wie Etwa Als richtig verhalten, diese Apps jedoch bei hohem Kontrast falsch reagieren. Beispielsweise ist text in Einer immer schwarz, und die Hervorhebungsfarbe ist hellblau. In Schwarz mit hohem Kontrast ist die Hervorhebungsfarbe jedoch schwarz. Wenn Sie wie bei vielen integrierten Apps vor Windows 8 von schwarzem Text ausgehen und die Systemeinstellung für die Hervorhebung verwenden, wird dem Benutzer schwarzer Text auf schwarzem Hintergrund angezeigt. In diesen Situationen ist es erforderlich, zu verstehen, wie Designs und Systemmetriken ordnungsgemäß verwendet werden, damit die App stilübergreifend korrekt aussieht.

## <a name="manifestations"></a>Manifestationen

-   Das Theming ist im Clientbereich von Apps nicht aktiviert, die kein Windows 8 &lt; supportedOS-Tag &gt; in ihrem App-Manifest enthalten. Daher müssen die Apps den Clientbereich mithilfe des Codepfads rendern, der zum Rendern im Modus mit hohem Kontrast des klassischen Designs erforderlich ist.
-   Das Theming ist nicht sowohl im Nicht-Client- als auch im Clientbereich von Apps in Designs mit hohem Kontrast aktiviert. Sie ist auch nicht in Apps aktiviert, die kein Windows 8 supportedOS-Tag in ihrem App-Manifest enthalten und die im Nicht-Clientbereich eines Fensters mithilfe der &lt; &gt; DwnIsCompositionEnabled()-API zeichnen. Die gesamte App wird im Modus mit hohem Kontrast des klassischen Designs gerendert.
-   Apps, die unterstützung für Windows 8 in ihrem Manifest hinzufügen, aber keine visuellen Stile für das Rendering verwenden, d.&a; sie hartcodieren Farben oder Bilder in ihren Apps, werden in Designs mit hohem Kontrast möglicherweise nicht ordnungsgemäß gerendert. Text kann schwierig zu lesen sein, oder Bilder werden möglicherweise nicht wie im Modus mit hohem Kontrast angezeigt.

## <a name="mitigation"></a>Minderung

Die Textfarben in den Designs mit hohem Kontrast wurden so erstellt, dass sie mit den Microsoft-Richtlinien für Barrierefreiheit konform sind. Wir behalten ein 14:1-Verhältnis mit hohem Kontrast zwischen Vordergrund und Hintergrund bei. Wenn die standardmäßig aktivierten Farben für einen bestimmten Endbenutzer nicht geeignet sind, können sie problemlos über die Systemsteuerungseinstellungen für "Fensterfarbe" in diesen Designs mit hohem Kontrast angepasst werden.

Diese Benutzeroberflächenkomponenten können in Designs mit hohem Kontrast angepasst werden:

-   Hintergrundfarbe des Fensters
-   Textfarbe
-   Hyperlinksfarbe
-   Deaktivierter Text
-   Ausgewählte Textgrund- und Hintergrundfarben
-   Vordergrund- und Hintergrundfarben des aktiven Fenstertitels
-   Vordergrund- und Hintergrundfarben des inaktiven Fenstertitels
-   Vordergrund- und Hintergrundfarben der Schaltfläche

## <a name="solution"></a>Lösung

Wenn in Apps in Designs mit hohem Kontrast unerwartetes Verhalten zu sehen ist, kann eine der folgenden Lösungen helfen:

-   **Manifestieren einer App für Windows 8:**

    Bei Apps, die nicht das Windows 8 supportedOS-Tag im App-Manifest enthalten, werden ihre Clientbereiche &lt; &gt; ohne Design gerendert. In-Box-Apps sollten alle diesen Eintrag im App-Manifest enthalten. Fügen Sie den GUID-Wert 4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38 GUID für Windows 8.

-   **Verwenden von visuellen Stilen mit vom Besitzer gezeichneten Beschriftungstypen:**

    Vom Besitzer gezeichnete Steuerelemente sollten die Anweisungen auf [MSDN](/windows/desktop/Controls/using-visual-styles) befolgen, um Steuerelementteile und -zustände, einschließlich Text, ordnungsgemäß zu rendern. Entwickler sollten sich nicht auf die in einem Gerätekontext angegebene Text- oder Hintergrundfarbe verlassen, um Nicht-UxTheme-Methoden für das Rendering zu verwenden. Falls kein Designteil für das entsprechende Steuerelement vorkommt, verwenden Sie [](/windows/desktop/api/winuser/nf-winuser-getsyscolor) GetThemeSysColor mit der entsprechenden Metrik, und zeichnen Sie den Text mithilfe von GDI-Standardmethoden. Wenn keiner der UxTheme-Aufrufe geeignet ist, verwenden Sie die GetSysColor-Methode, um die entsprechende Metrik zu erhalten.

-   **Auswählen der Textfarbe:**

    Verwenden Sie keine hartcodierte Textfarbe, auch wenn davon ausgegangen wird, dass sie in allen gängigen Szenarien gut aussingt. Die Versandthemen werden auf eine Weise erstellt, die eine hohe Sichtbarkeit mit zugeordneten Metriken unterstützt. Beispielsweise ist COLOR HIGHLIGHTTEXT für die Verwendung mit COLOR HIGHLIGHT als Hintergrund und COLOR WINDOWTEXT für die Verwendung mit COLOR WINDOW als \_ \_ Hintergrund \_ \_ gedacht. Wenn Ausnahmen für diese Zuordnungen gelten, arbeiten Sie mit ihnen in den Designteilen und Zustandsdefinitionen selbst und nicht im Code. Beim Entwerfen von Benutzeroberflächen mit hohem Kontrast ist es wichtig, dass die Benutzeroberfläche unabhängig vom aktuell angewendeten Design mit hohem Kontrast ist, da Benutzer mit hohem Kontrast ihre Farben anpassen können.

-   **Reagieren auf das WM \_ ThemeChange-Ereignis:**

    Wenn Ihre App die vom Design abgerufenen Farben zwischenspeichert oder Farben auf nicht standardmäßige Weise angewendet, fügen Sie einen Meldungshandler für WM THEMECHANGE hinzu, der die gespeicherten Farbwerte neu berechnet und die Benutzeroberfläche neu \_ formatiert.

-   **Schreiben einer WWA-App mit hohem Kontrast:**

    Web-Apps haben keinen Zugriff auf die UxTheme-APIs, sollten aber dennoch mit den aktuellen Systemmetriken als Grundlage für die Benutzeroberfläche geschrieben werden. Es gibt einige Ressourcen, die WWA-Entwickler nutzen können, um eine konforme App mit hohem Kontrast sicherzustellen:

    -   Die [W3C CSS-Farbspezifikation gibt](https://www.w3.org/TR/css3-color/) die Syntax für die Verwendung von Systemmetriken anstelle bestimmter Farben an.
    -   Unterstützung für Medienabfragen mit hohem Kontrast wird hinzugefügt, um Internet Explorer 10
    -   WWAs können die IAccessibilityCapabilities::get HighContrast()-Methode nutzen, um den Zustand des \_ hohen Kontrasts zu überprüfen.

    Windows Store-Apps haben nicht viele der gleichen Probleme mit Designteilen, die in klassischen Windows-Anwendungen vorhanden sind, aber Sie müssen trotzdem die Konformität mit hohem Kontrast sicherstellen. Standardmäßig ignoriert Internet Explorer bestimmte benutzerdefinierte Stile und ersetzt sie durch mit hohem Kontrast kompatible Werte. Css-Eigenschaften für Hintergrundbild, Hintergrund und Farbe werden beispielsweise ignoriert.

    Wenn Sie nicht möchten, dass Internet Explorer von Ihnen festgelegten Eigenschaften ignoriert und sichergestellt haben, dass die Benutzeroberfläche mit hohem Kontrast kompatibel ist, können Sie die neue CSS-Eigenschaft M3 –ms-high-contrast: für ein übergeordnetes Element deaktivieren.

-   **Schreiben einer App mit hohem Windows Store:**

    Windows Store-App sollte die [SystemColors-Klasse](/dotnet/api/system.windows.systemcolors) verwenden, um die richtige Färbung von Benutzeroberflächenelements zu bestimmen. Beachten Sie dabei, dass bestimmte Systemmetrikfarben für die Verwendung in Verbindung konzipiert sind, z. B. SystemColors.WindowColor und SystemColors.WindowTextColor. Dies ermöglicht eine bessere Erfahrung mit hohem Kontrast.

-   **Ordnungsgemäße Erkennung von hohem Kontrast in früheren Versionen Windows:**

    Apps, die in früheren Versionen von Windows ausgeführt werden, haben keinen Zugriff auf die neuen Designs mit hohem Kontrast, auch wenn das Manifest die Kompatibilität mit der Windows angibt. Daher kann es erforderlich sein, zusätzliche Codepfade für das Rendering in der klassischen Umgebung, die in früheren Versionen von verwendet wurde, Windows. Das Vorhandensein eines hohen Kontrasts sollte in diesem Fall überprüft werden, indem die [SystemParametersInfo-Funktion](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) mit dem SPI \_ GETHIGHCONTRAST-Flag aufgerufen wird. Dies ist die einzige unterstützte Methode, um das Vorhandensein von hohem Kontrast zu überprüfen.

## <a name="tests"></a>Tests

Stellen Sie beim Testen einer App sicher, dass sie in allen von Windows 8 bereitgestellten In-Box-Designs ordnungsgemäß gerendert wird: "Zwischen", "Basic", "hoher Kontrast 1", "hoher Kontrast 2", "hoher Kontrast Black" und "hoher Kontrast White". Stellen Sie sicher, dass der Text in den Designs mit hohem Kontrast klar sichtbar und leicht zu lesen ist.

## <a name="resources"></a>Ressourcen

-   [Style Classes, Parts, and States](../controls/aero-style-classes-parts-and-states.md) (die neuen grundlegenden Designs und Designs mit hohem Kontrast verwenden auch diese Zustände)
-   [Teile und Zustände, die allen visuellen Stilen gemeinsam sind](../controls/parts-and-states.md)
-   [Verwenden von visuellen Stilen mit benutzerdefinierten und Owner-Drawn Steuerelementen](../controls/using-visual-styles.md)
-   [GetSysColor-Funktion](/windows/win32/api/winuser/nf-winuser-getsyscolor)
-   [W3C CSS Color Module Level 3](https://www.w3.org/TR/css3-color/)
-   [SystemColors-Klasse](/dotnet/api/system.windows.systemcolors?view=netcore-3.1)
-   [SystemParametersInfo-Funktion](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
-   [Microsoft Accessibility (Microsoft-Barrierefreiheit)](https://www.microsoft.com/enable/)

 

 
