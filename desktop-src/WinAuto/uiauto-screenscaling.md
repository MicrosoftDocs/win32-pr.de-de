---
title: Grundlegendes zu Problemen bei der Bildschirmskalierung
description: Windows Mit Vista und höheren Versionen des Betriebssystems können Benutzer die DPI-Einstellung (Dots per Inch) so ändern, dass die meisten Benutzeroberflächenelemente auf dem Bildschirm größer erscheinen.
ms.assetid: 27dc49e7-2466-4ea3-a6d9-5ea86d6b4c60
keywords:
- Clients,Benutzeroberflächenautomatisierung Bildschirmskalierung
- Clients, Bildschirmskalierung
- Clients,Skalierung
- Benutzeroberflächenautomatisierung,Bildschirmskalierung
- Benutzeroberflächenautomatisierung,Skalierung
- Bildschirmskalierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4dcdc8d586b4320e4da04dfdd7e0264f36074cc59fa53f42333ec5a6c3dd135
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614290"
---
# <a name="understanding-screen-scaling-issues"></a>Grundlegendes zu Problemen bei der Bildschirmskalierung

Windows Mit Vista und höheren Versionen des Betriebssystems können Benutzer die DPI-Einstellung (Dots per Inch) so ändern, dass die meisten Benutzeroberflächenelemente auf dem Bildschirm größer erscheinen. In früheren Versionen von Windows musste die Skalierung von Anwendungen implementiert werden. In Windows Vista und höher führt der Desktopfenster-Manager (DWM) die Standardskalierung für alle Anwendungen aus, die ihre eigene Skalierung nicht verarbeiten. Microsoft Benutzeroberflächenautomatisierung-Clientanwendungen müssen dieses Feature berücksichtigen.

Dieses Thema enthält folgende Abschnitte:

-   [Skalierung in Windows Vista und höher](#scaling-in-windows-vista-and-later)
-   [Skalierung in Benutzeroberflächenautomatisierungs-Clients](#scaling-in-ui-automation-clients)

## <a name="scaling-in-windows-vista-and-later"></a>Skalierung in Windows Vista und höher

Die dpi-Standardeinstellung ist 96, was bedeutet, dass 96 Pixel eine Breite oder Höhe von einem nominalen Zoll belegen. Das genaue Maß für ein „Zoll“ ist abhängig von der Größe und der physischen Auflösung des Monitors. Auf einem Monitor mit einer Breite von 12 Zoll bei einer horizontalen Auflösung von 1280 Pixel erstreckt sich eine horizontale Linie von 96 Pixeln beispielsweise über etwas 9/10 eines Zolls.

Das Ändern der dpi-Einstellung ist nicht mit dem Ändern der Bildschirmauflösung identisch. Bei der DPI-Skalierung bleibt die Anzahl der physischen Pixel auf dem Bildschirm unverändert. Die Skalierung wird jedoch auf die Größe und Position von Benutzeroberflächenelementen angewendet. Diese Skalierung kann automatisch vom DWM für den Desktop und für Anwendungen ausgeführt werden, die nicht explizit fordern, nicht skaliert zu werden.

Wenn der Benutzer den Skalierungsfaktor auf 120 dpi fest legt, wird ein vertikaler oder horizontaler Zoll auf dem Bildschirm um 25 Prozent größer. Alle Dimensionen werden entsprechend skaliert. Der Offset eines Anwendungsfensters vom oberen und linken Rand des Bildschirms erhöht sich um 25 Prozent. Wenn die Anwendungsskalierung aktiviert ist und die Anwendung nicht dpi-fähig ist, erhöht sich die Fenstergröße im gleichen Verhältnis zusammen mit den Offsets und Größen aller elemente der Benutzeroberfläche, die sie enthält.

> [!Note]  
> Standardmäßig führt das DWM keine Skalierung für nicht dpi-orientierte Anwendungen durch, wenn der Benutzer den dpi-Wert auf 120 festgelegt hat, führt aber eine Skalierung durch, wenn der dpi-Wert auf einen benutzerdefinierten Wert von 144 oder höher festgelegt ist. Das Standardverhalten kann vom Benutzer jedoch außer Kraft gesetzt werden.

 

Die Bildschirmskalierung stellt an Anwendungen neue Herausforderungen, die sich in irgendeiner Weise mit Bildschirmkoordinaten befassen. Der Bildschirm enthält jetzt zwei Koordinatensysteme: ein physisches und ein logisches. Die physischen Koordinaten eines Punkts sind der tatsächliche Offset in Pixeln von der oberen linken Seite des Ursprungspunkts. Die logischen Koordinaten sind die Offsets, die sich ergeben würden, wenn die Pixel selbst skaliert würden.

Angenommen, Sie entwerfen ein Dialogfeld mit einer Schaltfläche an den Koordinaten (100, 48). Wenn dieses Dialogfeld mit dem Standardwert von 96 dpi angezeigt wird, befindet sich die Schaltfläche an physischen Koordinaten von (100, 48). Bei 120 dpi befindet es sich an physischen Koordinaten von (125, 60). Die logischen Koordinaten sind jedoch bei jeder dpi-Einstellung identisch: (100, 48).

Logische Koordinaten sind wichtig, da sie das Verhalten des Betriebssystems und der Anwendungen unabhängig von der dpi-Einstellung konsistent machen. Beispielsweise gibt die [**GetCursorPos-Funktion**](/windows/desktop/api/winuser/nf-winuser-getcursorpos) in der Regel die logischen Koordinaten zurück. Wenn Sie den Cursor über ein Element in einem Dialogfeld bewegen, werden unabhängig von der dpi-Einstellung die gleichen Koordinaten zurückgegeben. Wenn Sie ein Steuerelement bei (100, 100) zeichnen, wird es auf diese logischen Koordinaten gezeichnet und nimmt bei jeder dpi-Einstellung die gleiche relative Position ein.

## <a name="scaling-in-ui-automation-clients"></a>Skalierung in Benutzeroberflächenautomatisierungs-Clients

Die Benutzeroberflächenautomatisierung-API verwendet keine logischen Koordinaten. Die folgenden Methoden und Eigenschaften geben physische Koordinaten zurück oder nehmen physische Koordinaten als Parameter an.

-   [**IUIAutomation::ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)
-   [**IUIAutomation::ElementFromPointBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompointbuildcache)
-   [**IUIAutomationElement::GetClickablePoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getclickablepoint)
-   [**IUIAutomationElement::CurrentBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentboundingrectangle)
-   [**IUIAutomationElement::CachedBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedboundingrectangle)
-   [**IRawElementProviderFragment::BoundingRectangle**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-get_boundingrectangle)

Standardmäßig erhalten Benutzeroberflächenautomatisierung Anwendungen, die in einer Umgebung ausgeführt werden, die nicht auf 96 dpi festgelegt ist, nicht die richtigen Ergebnisse von diesen Methoden und Eigenschaften. Da sich die Cursorposition beispielsweise in logischen Koordinaten befindet, kann der Client diese Koordinaten nicht an [**IUIAutomation::ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint) übergeben, um das Element unter dem Cursor zu erhalten. Darüber hinaus ist die Anwendung nicht in der Lage, Fenster außerhalb seines Clientbereichs ordnungsgemäß zu platzieren.

Die Lösung besteht aus zwei Teilen.

Machen Sie zunächst die Clientanwendung dpi-bewusst. Rufen Sie hierzu beim Start die [**Funktion SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) auf. Diese Funktion macht den gesamten Prozess dpi-bewusst, was bedeutet, dass alle Fenster, die zum Prozess gehören, nicht skaliert sind.

Rufen Sie zweitens die [**GetPhysicalCursorPos-Funktion**](/windows/desktop/api/winuser/nf-winuser-getphysicalcursorpos) auf, um Cursorkoordinaten zu erhalten.

 

 