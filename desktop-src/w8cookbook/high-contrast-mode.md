---
title: Modus mit hohem Kontrast
description: Modus mit hohem Kontrast
ms.assetid: 817F2BBD-3744-4D34-927F-EBF9F7894CC0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae8c53d3e92bb97dd9e2f5fa34bad9f901920cc7
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "103730744"
---
# <a name="high-contrast-mode"></a>Modus mit hohem Kontrast

## <a name="platforms"></a>Plattformen

 **Clients** -Windows 8  
**Server** -Windows Server 2012  



## <a name="description"></a>BESCHREIBUNG

In früheren Windows-Betriebssystemen war der Modus für hohe Kontraste auf Designs beschränkt, die unter klassischen Themen ausgeführt werden, die nicht visuell formatiert wurden. In Windows 8 und Windows Server 2012 wurde der klassische Modus entfernt und durch visuell formatierte Designs mit hohem Kontrast ersetzt. Einer der Hauptvorteile für diese Änderung ist das Entfernen eines separaten Codepfads für apps, die im klassischen Modus ausgeführt werden.

Entwickler müssen immer noch in der Art und Weise geschult werden, wie sich der Modus für hohe Kontraste auf Ihre APP auswirken kann, und wie Sie eine App entwickeln, die wirklich Stil agnostisch ist. Dies ist wichtig, denn während die falsche Verwendung oder die Annahme von Design Farben bewirken kann, dass apps in einem visuellen Stil wie Aero ordnungsgemäß Verhalten, reagieren dieselben apps unter hohem Kontrast falsch. Beispielsweise ist der Text in Aero immer schwarz, und die Hervorhebungs Farbe ist hell blau. Im hohen Kontrast schwarz ist die Hervorhebungs Farbe jedoch schwarz. Wenn Sie den schwarzen Text annehmen, wie dies in vielen in-Box-apps vor Windows 8 der Fall war, und die Standardeinstellung des Systems für die Hervorhebung verwenden, wird dem Benutzer schwarzer Text in schwarzem Hintergrund angezeigt. In diesen Situationen ist es erforderlich, dass Sie verstehen, wie Designs und Systemmetriken ordnungsgemäß verwendet werden, damit die APP über Stile hinweg korrekt aussieht.

## <a name="manifestations"></a>Kundgebungen

-   Die Design Funktion ist nicht im Client Bereich von apps aktiviert, die kein Windows 8- <supportedOS> Tag in Ihrem App-Manifest enthalten. Daher müssen die apps den Client Bereich Renderern, indem Sie den Codepfad verwenden, der erforderlich ist, um im Modus mit hohem Kontrast des klassischen Designs zu rendieren.
-   Die Design Funktion ist nicht sowohl in den nicht-Client-als auch in den Client Bereichen von apps in Designs mit hohem Kontrast aktiviert. Sie ist auch nicht in apps aktiviert, die kein Windows 8 <supportedOS> -Tag in Ihrem App-Manifest enthalten, und das im nicht-Client Bereich eines Fensters mithilfe der dwniscompositionaktivierten ()-API gezeichnet wird. Die gesamte APP wird im Modus mit hohem Kontrast zum klassischen Design gerendert.
-   Apps, die Unterstützung für Windows 8 in ihrem Manifest hinzufügen, aber keine visuellen Stile zum Rendern verwenden, d. h., dass Sie Farben oder Bilder in ihren apps hart codieren, werden möglicherweise in Designs mit hohem Kontrast nicht ordnungsgemäß gerendert. Möglicherweise ist es schwierig, Text zu lesen, oder Bilder werden im Modus mit hohem Kontrast nicht angezeigt.

## <a name="mitigation"></a>Minderung

Die Textfarben in den Designs mit hohem Kontrast wurden so verfasst, dass Sie mit den Microsoft-Richtlinien für Barrierefreiheit kompatibel sind. Wir behalten ein 14:1-Verhältnis mit hohem Kontrast zwischen Vordergrund und Hintergrund. Wenn die standardmäßig aktivierten Farben für einen bestimmten Endbenutzer nicht geeignet sind, können Sie problemlos über die System Steuerungseinstellungen für "Window Color" in diesen Designs mit hohem Kontrast angepasst werden.

Diese UI-Komponenten sind in Designs mit hohem Kontrast anpassbar:

-   Hintergrundfarbe des Fensters
-   Textfarbe
-   Hyperlinks-Farbe
-   Deaktivierter Text
-   Ausgewählte Text Vordergrund-und Hintergrundfarben
-   Vordergrund-und Hintergrundfarben der Titel des aktiven Fensters
-   Inaktive Fenstertitel Vordergrund-und Hintergrundfarben
-   Schaltflächen Vordergrund-und Hintergrundfarben

## <a name="solution"></a>Lösung

Wenn ein unerwartetes Verhalten in apps in High-Contrast-Designs auftritt, könnte eine dieser Lösungen hilfreich sein:

-   **Manifestieren einer APP für Windows 8:**

    Für apps, die das Windows 8- <supportedOS> Tag nicht im App-Manifest enthalten, werden die Client Bereiche ohne Design gerendert. In-Box-apps sollten alle diesen Eintrag im App-Manifest enthalten. Fügen Sie den Wert 4a2s28e3-53b9-4441-ba9c-d69d4a4a6e38 GUID für Windows 8 hinzu.

-   **Verwenden visueller Stile mit vom Besitzer gezeichneten UIs:**

    Vom Besitzer gezeichnete Steuerelemente müssen die Anweisungen auf [MSDN](/windows/desktop/Controls/using-visual-styles) befolgen, um Steuerelement Teile und-Zustände, einschließlich Text, korrekt zu rendern. Entwickler sollten sich nicht darauf verlassen, dass die in einem Gerätekontext angegebene Text-oder Hintergrundfarbe verwendet wird, um nicht-uxtheme-Methoden zum Rendern zu verwenden. Wenn kein Design Teil für das betreffende Steuerelement vorhanden ist, verwenden Sie getthemesyscolor mit der [entsprechenden Metrik](/windows/desktop/api/winuser/nf-winuser-getsyscolor) , und zeichnen Sie den Text mithilfe der Standard-GDI-Methoden. Wenn keiner der uxtheme-Aufrufe geeignet ist, verwenden Sie die GetSysColor-Methode, um die entsprechende Metrik zu erhalten.

-   **Auswählen der Textfarbe:**

    Verwenden Sie keine hart codierte Textfarbe, auch wenn davon ausgegangen wird, dass Sie in allen gängigen Szenarien problemlos aussieht. Die Versand Designs werden auf eine Weise erstellt, die hohe Sichtbarkeit mit zugeordneten Metriken unterstützt. Beispielsweise soll Color \_ HighlightText mit Color- \_ Hervorhebung als Hintergrund verwendet werden, und \_ WindowText ist für die Verwendung mit Farb \_ Fenstern als Hintergrund gedacht. Wenn es Ausnahmen zu diesen Zuordnungen gibt, arbeiten Sie mit Ihnen in den Design teilen und Zustands Definitionen selbst und nicht im Code. Beim Entwerfen von UIs mit hohem Kontrast ist es von entscheidender Bedeutung, dass die Benutzeroberfläche für das aktuell angewendete Design mit hohem Kontrast agnostisch ist, da Benutzer mit hohem Kontrast ihre Farben anpassen können.

-   **Reaktion auf das WM- \_ Änderungs Ereignis:**

    Wenn Ihre APP die aus dem Design abgerufenen Farben zwischenspeichert oder Farben auf eine nicht standardmäßige Weise anwendet, fügen Sie einen Meldungs Handler für WM-Programmcode hinzu, \_ der die gespeicherten Farbwerte neu berechnet und die Benutzeroberfläche neu zeichnet.

-   **Schreiben einer WWA-App mit hohem Kontrast:**

    Web-Apps haben keinen Zugriff auf die uxtheme-APIs, sollten aber trotzdem mit den aktuellen Systemmetriken als Grundlage für die Benutzeroberfläche geschrieben werden. Es gibt einige Ressourcen, die WWA-Entwickler nutzen können, um eine kompatible App mit hohem Kontrast sicherzustellen:

    -   Die [W3C-CSS-Farbspezifikation](https://www.w3.org/TR/css3-color/) gibt die Syntax für die Verwendung von Systemmetriken anstelle spezifischer Farben an.
    -   Unterstützung für Medien Abfragen mit hohem Kontrast wird Internet Explorer 10 hinzugefügt
    -   Wwas kann die iaccessibilityfunktionalitäten:: get \_ HighContrast ()-Methode nutzen, um den Status von hohem Kontrast zu überprüfen.

    Für Windows Store-Apps gibt es nicht viele der gleichen Probleme mit Design teilen, die in klassischen Windows-Anwendungen vorhanden sind, aber Sie müssen trotzdem eine hohe Kontrast Konformität sicherstellen. Standardmäßig ignoriert Internet Explorer bestimmte benutzerdefinierte Stile und ersetzt diese durch kontrastreiche kompatible Werte. Beispielsweise werden die CSS-Eigenschaften "background-image", "Background" und "Color" ignoriert.

    Wenn Sie nicht möchten, dass Internet Explorer Eigenschaften ignoriert, die Sie festgelegt haben, und Sie sichergestellt haben, dass die Benutzeroberfläche mit hohem Kontrast kompatibel ist, können Sie die neue Eigenschaft "M3 CSS" – MS-High-Contrast: off für ein übergeordnetes Element festlegen.

-   **Schreiben einer Windows Store-App mit hohem Kontrast:**

    Die Windows Store-App sollte die Klasse " [System Colors](/dotnet/api/system.windows.systemcolors) " verwenden, um die ordnungsgemäße Farbgebung von Benutzeroberflächen Elementen zu bestimmen. dabei ist zu beachten, dass bestimmte System metrikfarben für die Verwendung in Verbindung stehen, wie z. b. System Colors. WindowColor und SystemColors. WindowText Dadurch wird eine bessere Ober Kontrast Funktion ermöglicht.

-   **Ordnungsgemäßes Erkennen von hohem Kontrast in früheren Windows-Versionen:**

    Apps, die in früheren Versionen von Windows ausgeführt werden, haben keinen Zugriff auf die neuen Designs mit hohem Kontrast, auch wenn das Manifest die Kompatibilität mit der fraglichen Windows-Version angibt. Daher kann es erforderlich sein, zusätzliche Codepfade einzufügen, um das Rendering in der klassischen Umgebung zu verarbeiten, die in früheren Versionen von Windows verwendet wurde. Das vorhanden sein von hohem Kontrast sollte in diesem Fall durch Aufrufen der [SystemParametersInfo](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) -Funktion mit dem SPI \_ gethighcontrast-Flag geprüft werden. Dies ist die einzige unterstützte Methode zum Überprüfen des Vorhandenseins von hohem Kontrast.

## <a name="tests"></a>Tests

Stellen Sie beim Testen einer APP sicher, dass Sie in allen von Windows 8 bereitgestellten Standarddesigns ordnungsgemäß gerendert wird: Aero, Basic, hoher Kontrast 1, hoher Kontrast 2, hoher Kontrast Black und hoher Kontrast weiß. Stellen Sie sicher, dass der Text in den Designs mit hohem Kontrast eindeutig sichtbar und leicht lesbar ist.

## <a name="resources"></a>Ressourcen

-   [Klassen, Teile und Zustände im Aero-Stil](../controls/aero-style-classes-parts-and-states.md) (das neue grundlegende Design und das Design mit hohem Kontrast verwenden auch diese Zustände)
-   [Teile und Zustände, die für alle visuellen Stile gemeinsam sind](../controls/parts-and-states.md)
-   [Verwenden visueller Stile mit benutzerdefinierten Steuerelementen und Owner-Drawn Steuerelementen](../controls/using-visual-styles.md)
-   [GetSysColor-Funktion](/windows/win32/api/winuser/nf-winuser-getsyscolor)
-   [W3C-CSS-Farb Modulebene 3](https://www.w3.org/TR/css3-color/)
-   [System Colors-Klasse](/dotnet/api/system.windows.systemcolors?view=netcore-3.1)
-   [SystemParametersInfo-Funktion](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
-   [Microsoft Accessibility (Microsoft-Barrierefreiheit)](https://www.microsoft.com/enable/)

 

 