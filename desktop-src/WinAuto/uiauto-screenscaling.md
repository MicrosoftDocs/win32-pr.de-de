---
title: Grundlegendes zur Bildschirm Skalierung
description: Windows Vista und höhere Versionen des Betriebssystems ermöglichen Benutzern das Ändern der dpi-Einstellung (dots per inch), sodass die meisten Elemente der Benutzeroberfläche auf dem Bildschirm größer erscheinen.
ms.assetid: 27dc49e7-2466-4ea3-a6d9-5ea86d6b4c60
keywords:
- Clients, Bildschirm Skalierung der Benutzeroberflächen Automatisierung
- Clients, Bildschirm Skalierung
- Clients, Skalierung
- Benutzeroberflächen Automatisierung, Bildschirm Skalierung
- Benutzeroberflächen Automatisierung, Skalierung
- Bildschirm Skalierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05d790ee7747f258847cd23aea8bbbe8c25813fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390825"
---
# <a name="understanding-screen-scaling-issues"></a>Grundlegendes zur Bildschirm Skalierung

Windows Vista und höhere Versionen des Betriebssystems ermöglichen Benutzern das Ändern der dpi-Einstellung (dots per inch), sodass die meisten Elemente der Benutzeroberfläche auf dem Bildschirm größer erscheinen. In früheren Versionen von Windows musste die Skalierung von Anwendungen implementiert werden. In Windows Vista und höher führt die Desktopfenster-Manager (DWM) die Standard Skalierung für alle Anwendungen aus, die ihre eigene Skalierung nicht verarbeiten. Microsoft UI Automation-Client Anwendungen müssen dieses Feature berücksichtigen.

Dieses Thema enthält folgende Abschnitte:

-   [Skalierung in Windows Vista und höher](#scaling-in-windows-vista-and-later)
-   [Skalierung in Benutzeroberflächenautomatisierungs-Clients](#scaling-in-ui-automation-clients)

## <a name="scaling-in-windows-vista-and-later"></a>Skalierung in Windows Vista und höher

Die dpi-Standardeinstellung ist 96. Dies bedeutet, dass 96 Pixel eine Breite oder Höhe von einem einzelnen Zoll belegen. Das genaue Maß für ein „Zoll“ ist abhängig von der Größe und der physischen Auflösung des Monitors. Auf einem Monitor mit einer Breite von 12 Zoll bei einer horizontalen Auflösung von 1280 Pixel erstreckt sich eine horizontale Linie von 96 Pixeln beispielsweise über etwas 9/10 eines Zolls.

Das Ändern der dpi-Einstellung ist nicht dasselbe wie das Ändern der Bildschirmauflösung. Bei der DPI-Skalierung bleibt die Anzahl der physischen Pixel auf dem Bildschirm unverändert. Die Skalierung wird jedoch auf die Größe und den Speicherort der Benutzeroberflächen Elemente angewendet. Diese Skalierung kann automatisch durch die DWM für den Desktop und für Anwendungen ausgeführt werden, die nicht explizit die Skalierung der Skalierung anfordern.

Wenn der Benutzer den Skalierungsfaktor auf 120 DPI festlegt, wird ein vertikaler oder horizontaler Zoll auf dem Bildschirm um 25 Prozent vergrößert. Alle Dimensionen werden entsprechend skaliert. Der Offset eines Anwendungsfensters vom oberen und linken Rand des Bildschirms wird um 25 Prozent vergrößert. Wenn die Anwendungs Skalierung aktiviert ist und die Anwendung nicht mit dpi-Werten kompatibel ist, vergrößert sich die Größe des Fensters zusammen mit den Offsets und Größen aller darin enthaltenen UI-Elemente im selben Verhältnis.

> [!Note]  
> Standardmäßig führt die DWM keine Skalierung für Anwendungen ohne dpi-Unterstützung durch, wenn der Benutzer den dpi-Wert auf 120 festlegt, aber die Skalierung durchführt, wenn der dpi-Wert auf einen benutzerdefinierten Wert von 144 oder höher festgelegt ist. Das Standardverhalten kann vom Benutzer jedoch außer Kraft gesetzt werden.

 

Die Bildschirmskalierung stellt an Anwendungen neue Herausforderungen, die sich in irgendeiner Weise mit Bildschirmkoordinaten befassen. Der Bildschirm enthält jetzt zwei Koordinatensysteme: ein physisches und ein logisches. Die physischen Koordinaten eines Punkts stellen den tatsächlichen Offset in Pixel von der linken oberen Ecke des Ursprungs Punkts dar. Die logischen Koordinaten sind die Offsets, die sich ergeben würden, wenn die Pixel selbst skaliert würden.

Angenommen, Sie entwerfen ein Dialogfeld mit einer Schaltfläche an den Koordinaten (100, 48). Wenn dieses Dialogfeld mit dem 96-Standard dpi angezeigt wird, befindet sich die Schaltfläche an den physischen Koordinaten von (100, 48). Bei 120 dpi befindet er sich an physischen Koordinaten von (125, 60). Aber die logischen Koordinaten sind bei jeder dpi-Einstellung identisch: (100, 48).

Logische Koordinaten sind wichtig, da Sie das Verhalten des Betriebssystems und der Anwendungen unabhängig von der dpi-Einstellung konsistent machen. In der Regel gibt die [**GetCursor**](/windows/desktop/api/winuser/nf-winuser-getcursorpos) -Funktion z. b. die logischen Koordinaten zurück. Wenn Sie den Cursor über ein Element in einem Dialogfeld bewegen, werden unabhängig von der dpi-Einstellung dieselben Koordinaten zurückgegeben. Wenn Sie ein Steuerelement bei (100, 100) zeichnen, wird es auf diese logischen Koordinaten gezeichnet und nimmt dieselbe relative Position bei jeder dpi-Einstellung an.

## <a name="scaling-in-ui-automation-clients"></a>Skalierung in Benutzeroberflächenautomatisierungs-Clients

Die Benutzeroberflächenautomatisierungs-API verwendet keine logischen Koordinaten. Die folgenden Methoden und Eigenschaften geben physische Koordinaten zurück oder verwenden physische Koordinaten als Parameter.

-   [**Iuiautomation:: elementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)
-   [**Iuiautomation:: elementfrompointbuildcache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompointbuildcache)
-   [**Iuiautomationelement:: GetClickablePoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getclickablepoint)
-   [**Iuiautomationelement:: currentboundingrechteck**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentboundingrectangle)
-   [**Iuiautomationelement:: cachedboundingrechteck**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedboundingrectangle)
-   [**IRawElementProviderFragment:: boundingrechteck**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-get_boundingrectangle)

Standardmäßig erhalten Benutzeroberflächenautomatisierungs-Anwendungen, die in einer Umgebung ausgeführt werden, die nicht auf 96 dpi festgelegt ist, die richtigen Ergebnisse von diesen Methoden und Eigenschaften. Da die Cursorposition z. b. in logischen Koordinaten angegeben ist, kann der Client diese Koordinaten nicht an [**iuiautomation:: elementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint) übergeben, um das Element zu erhalten, das sich unter dem Cursor befindet. Darüber hinaus ist die Anwendung nicht in der Lage, Fenster außerhalb seines Clientbereichs ordnungsgemäß zu platzieren.

Die Lösung besteht aus zwei Teilen.

Legen Sie für die Client Anwendung zunächst dpi-fähig. Um dies zu erreichen, müssen Sie die Funktion [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) beim Start aufrufen. Diese Funktion macht den gesamten Prozess dpi-fähig, was bedeutet, dass alle Fenster, die dem Prozess angehören, nicht skaliert werden.

Zum Abrufen von Cursor Koordinaten müssen Sie die [**GetPhysicalCursorPos**](/windows/desktop/api/winuser/nf-winuser-getphysicalcursorpos) -Funktion aufrufen.

 

 