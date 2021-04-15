---
title: Active Accessibility-und Windows Vista-Bildschirm Skalierung
description: Windows Vista ermöglicht es Benutzern, die dpi-Einstellung (dots per inch) so zu ändern, dass die meisten Elemente der Benutzeroberfläche auf dem Bildschirm größer erscheinen.
ms.assetid: c781fefd-09f0-4340-b3d3-f4e57308f392
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6db8e192dc01d4c7d75f19741cdfac7b3b08d22c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473788"
---
# <a name="active-accessibility-and-windows-vista-screen-scaling"></a>Active Accessibility-und Windows Vista-Bildschirm Skalierung

Windows Vista ermöglicht es Benutzern, die dpi-Einstellung (dots per inch) so zu ändern, dass die meisten Elemente der Benutzeroberfläche auf dem Bildschirm größer erscheinen. Obwohl dieses Feature seit langem in Microsoft Windows verfügbar ist, musste die Skalierung in früheren Versionen von Anwendungen implementiert werden. In Windows Vista führt die Desktopfenster-Manager eine Standard Skalierung für alle Anwendungen aus, die ihre eigene Skalierung nicht verarbeiten. Microsoft Active Accessibility-Client Anwendungen müssen dieses Feature berücksichtigen.

## <a name="scaling-in-windows-vista"></a>Skalierung in Windows Vista

Die dpi-Standardeinstellung ist 96. Dies bedeutet, dass 96 Pixel eine Breite oder Höhe von einem einzelnen Zoll belegen. Das genaue Maß für ein „Zoll“ ist abhängig von der Größe und der physischen Auflösung des Monitors. Auf einem Monitor mit einer Breite von 12 Zoll bei einer horizontalen Auflösung von 1280 Pixel erstreckt sich eine horizontale Linie von 96 Pixeln beispielsweise über etwas 9/10 eines Zolls.

Das Ändern der dpi-Einstellung ist nicht dasselbe wie das Ändern der Bildschirmauflösung. Bei der DPI-Skalierung bleibt die Anzahl der physischen Pixel auf dem Bildschirm unverändert. Die Skalierung wird jedoch auf die Größe und den Speicherort der Benutzeroberflächen Elemente angewendet. Diese Skalierung kann vom Desktopfenster-Manager (DWM) für den Desktop und für Anwendungen automatisch durchgeführt werden , die nicht ausdrücklich danach verlangen, nicht skaliert zu werden.

Wenn der Benutzer den Skalierungsfaktor auf 120 DPI festlegt, wird ein vertikaler oder horizontaler Zoll auf dem Bildschirm um 25 Prozent vergrößert. Alle Dimensionen werden entsprechend skaliert. Der Offset eines Fensters vom oberen und linken Rand des Bildschirms wird um 25 Prozent vergrößert. Die Größe des Fensters wird im selben Anteil zusammen mit den Offsets und Größen aller darin enthaltenen Benutzeroberflächen Elemente vergrößert.

Standardmäßig führt der DWM keine Skalierung für Anwendungen ohne dpi-Unterstützung durch, wenn der Benutzer den dpi-Wert auf 120 festlegt, er aber ausführt, wenn der dpi-Wert auf einen benutzerdefinierten Wert von 144 oder höher festgelegt ist. Das Standardverhalten kann vom Benutzer jedoch außer Kraft gesetzt werden.

Die Bildschirmskalierung stellt an Anwendungen neue Herausforderungen, die sich in irgendeiner Weise mit Bildschirmkoordinaten befassen. Der Bildschirm enthält jetzt zwei Koordinatensysteme: ein physisches und ein logisches. Die physischen Koordinaten eines Punkts stellen den tatsächlichen Offset in Pixeln vom oberen linken Rand des Ursprungs dar. Die logischen Koordinaten sind die Offsets, die sich ergeben würden, wenn die Pixel selbst skaliert würden.

Angenommen, Sie entwerfen ein Dialogfeld mit einer Schaltfläche an den Koordinaten (100, 48). Wenn dieses Dialogfeld mit dem 96-Standard dpi angezeigt wird, befindet sich die Schaltfläche an den physischen Koordinaten von (100, 48). Bei 120 dpi befindet er sich an physischen Koordinaten von (125, 60). Aber die logischen Koordinaten sind bei jeder dpi-Einstellung identisch: (100, 48).

Logische Koordinaten sind wichtig, da Sie das Verhalten des Betriebssystems und der Anwendungen unabhängig von der dpi-Einstellung konsistent machen. Beispielsweise gibt **System. Windows. Forms. Cursor. Position** normalerweise die logischen Koordinaten zurück. Wenn Sie den Cursor über ein Element in einem Dialogfeld bewegen, werden unabhängig von der dpi-Einstellung dieselben Koordinaten zurückgegeben. Wenn Sie ein Steuerelement bei (100, 100) zeichnen, wird es auf diese logischen Koordinaten gezeichnet und nimmt dieselbe relative Position bei jeder dpi-Einstellung an.

## <a name="scaling-in-active-accessibility-clients"></a>Skalieren in Active Accessibility Clients

Microsoft Active Accessibility verwendet keine logischen Koordinaten. Die folgenden Methoden und Funktionen geben entweder physische Koordinaten zurück oder verwenden Sie als Parameter.

-   [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**IAccessible:: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**Accessibleobjectfrompoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)

Standardmäßig kann eine Microsoft Active Accessibility-Client Anwendung, die in einer nicht-96-dpi-Umgebung ausgeführt wird, keine korrekten Ergebnisse von diesen Aufrufen abrufen. Da die Cursorposition z. b. in logischen Koordinaten angegeben ist, kann der Client diese Koordinaten nicht einfach an [**accessibleobjectfrompoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) übergeben, um das Element zu erhalten, das sich unter dem Cursor befindet.

Außerdem wird eine Anwendung, die ein Fenster außerhalb des Client Bereichs erstellt, z. b. eine Barrierefreiheits Anwendung, die fokussierte Benutzeroberflächen Elemente hervorhebt, das Fenster nicht an der korrekten Bildschirmposition erstellt, da das Fenster an den logischen Koordinaten platziert wird, nicht an den physischen Koordinaten, die von [**IAccessible:: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)zurückgegeben werden.

Die Lösung besteht aus zwei Teilen:

-   Legen Sie die Client Anwendung "dpi-fähig" ab. Um dies zu erreichen, müssen Sie die Funktion [**SetProcessDPIAware**](/windows/win32/api/winuser/nf-winuser-setprocessdpiaware) beim Start aufrufen. Diese Funktion macht den gesamten Prozess dpi-fähig, was bedeutet, dass alle Fenster, die dem Prozess angehören, nicht skaliert werden.
-   Verwenden Sie Funktionen, die dpi-fähig sind. Wenn Sie z. b. Cursor Koordinaten abrufen möchten, müssen Sie die [**GetPhysicalCursorPos**](/windows/win32/api/winuser/nf-winuser-getphysicalcursorpos) -Funktion aufrufen. Verwenden Sie [**GetCursor**](/windows/win32/api/winuser/nf-winuser-getcursorpos)nicht. das Verhalten in dpi-fähigen Anwendungen ist nicht definiert.

Wenn Ihre Anwendung eine direkte prozessübergreifende Kommunikation mit nicht dpi-fähigen Anwendungen ausführt, haben Sie möglicherweise eine Konvertierung zwischen logischen und physischen Koordinaten mithilfe der Funktionen [**PhysicalToLogicalPoint**](/windows/win32/api/winuser/nf-winuser-physicaltologicalpoint) und [**LogicalToPhysicalPoint**](/windows/win32/api/winuser/nf-winuser-logicaltophysicalpoint) durchführen.

 

 