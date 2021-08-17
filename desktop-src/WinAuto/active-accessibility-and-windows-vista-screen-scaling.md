---
title: Active Accessibility und Windows Vista-Bildschirmskalierung
description: Windows Mit Vista können Benutzer die DPI-Einstellung (Dots-per-Inch) ändern, sodass die meisten Benutzeroberflächenelemente auf dem Bildschirm größer erscheinen.
ms.assetid: c781fefd-09f0-4340-b3d3-f4e57308f392
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acf9c1ff6755507541c08b34e183dd751e0941fc646a1f691e4488884e572c79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327060"
---
# <a name="active-accessibility-and-windows-vista-screen-scaling"></a>Active Accessibility und Windows Vista-Bildschirmskalierung

Windows Mit Vista können Benutzer die DPI-Einstellung (Dots-per-Inch) ändern, sodass die meisten Benutzeroberflächenelemente auf dem Bildschirm größer erscheinen. Obwohl dieses Feature seit langem in Microsoft Windows verfügbar war, musste die Skalierung in früheren Versionen von Anwendungen implementiert werden. In Windows Vista führt die Desktopfenster-Manager Standardskalierung für alle Anwendungen aus, die ihre eigene Skalierung nicht verarbeiten. Microsoft Active Accessibility Clientanwendungen müssen dieses Feature berücksichtigen.

## <a name="scaling-in-windows-vista"></a>Skalierung in Windows Vista

Die dpi-Standardeinstellung ist 96, was bedeutet, dass 96 Pixel eine Breite oder Höhe von einem nominalen Zoll belegen. Das genaue Maß für ein „Zoll“ ist abhängig von der Größe und der physischen Auflösung des Monitors. Auf einem Monitor mit einer Breite von 12 Zoll bei einer horizontalen Auflösung von 1280 Pixel erstreckt sich eine horizontale Linie von 96 Pixeln beispielsweise über etwas 9/10 eines Zolls.

Das Ändern der dpi-Einstellung ist nicht mit dem Ändern der Bildschirmauflösung identisch. Bei der DPI-Skalierung bleibt die Anzahl der physischen Pixel auf dem Bildschirm unverändert. Die Skalierung wird jedoch auf die Größe und Position von Benutzeroberflächenelementen angewendet. Diese Skalierung kann vom Desktopfenster-Manager (DWM) für den Desktop und für Anwendungen automatisch durchgeführt werden , die nicht ausdrücklich danach verlangen, nicht skaliert zu werden.

Wenn der Benutzer den Skalierungsfaktor auf 120 dpi fest legt, wird ein vertikaler oder horizontaler Zoll auf dem Bildschirm um 25 Prozent größer. Alle Dimensionen werden entsprechend skaliert. Der Offset eines Fensters vom oberen und linken Rand des Bildschirms erhöht sich um 25 Prozent. Die Größe des Fensters nimmt im gleichen Verhältnis zu, zusammen mit den Offsets und Größen aller elemente der Benutzeroberfläche, die es enthält.

Standardmäßig führt das DWM keine Skalierung für nicht dpi-orientierte Anwendungen durch, wenn der Benutzer den dpi-Wert auf 120 festgelegt hat, führt dies jedoch aus, wenn der dpi-Wert auf einen benutzerdefinierten Wert von 144 oder höher festgelegt ist. Das Standardverhalten kann vom Benutzer jedoch außer Kraft gesetzt werden.

Die Bildschirmskalierung stellt an Anwendungen neue Herausforderungen, die sich in irgendeiner Weise mit Bildschirmkoordinaten befassen. Der Bildschirm enthält jetzt zwei Koordinatensysteme: ein physisches und ein logisches. Die physischen Koordinaten eines Punkts stellen den tatsächlichen Offset in Pixeln vom oberen linken Rand des Ursprungs dar. Die logischen Koordinaten sind die Offsets, die sich ergeben würden, wenn die Pixel selbst skaliert würden.

Angenommen, Sie entwerfen ein Dialogfeld mit einer Schaltfläche an den Koordinaten (100, 48). Wenn dieses Dialogfeld mit dem Standardwert von 96 dpi angezeigt wird, befindet sich die Schaltfläche an physischen Koordinaten von (100, 48). Bei 120 dpi befindet es sich an physischen Koordinaten von (125, 60). Die logischen Koordinaten sind jedoch bei jeder dpi-Einstellung identisch: (100, 48).

Logische Koordinaten sind wichtig, da sie das Verhalten des Betriebssystems und der Anwendungen unabhängig von der dpi-Einstellung konsistent machen. Beispiel: **System.Windows. Forms.Cursor.Position gibt** normalerweise die logischen Koordinaten zurück. Wenn Sie den Cursor über ein Element in einem Dialogfeld bewegen, werden unabhängig von der dpi-Einstellung die gleichen Koordinaten zurückgegeben. Wenn Sie ein Steuerelement bei (100, 100) zeichnen, wird es auf diese logischen Koordinaten gezeichnet und nimmt bei jeder dpi-Einstellung die gleiche relative Position ein.

## <a name="scaling-in-active-accessibility-clients"></a>Skalieren Active Accessibility Clients

Microsoft Active Accessibility verwendet keine logischen Koordinaten. Die folgenden Methoden und Funktionen geben entweder physische Koordinaten zurück oder nehmen sie als Parameter an.

-   [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)

Standardmäßig kann eine Microsoft Active Accessibility, die in einer Nicht-96-dpi-Umgebung ausgeführt wird, keine richtigen Ergebnisse aus diesen Aufrufen abrufen. Da sich die Cursorposition beispielsweise in logischen Koordinaten befindet, kann der Client diese Koordinaten nicht einfach an [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) übergeben, um das Element unter dem Cursor zu erhalten.

Darüber hinaus erstellt eine Anwendung, die ein Fenster außerhalb des Clientbereichs erstellt, z. B. eine Barrierefreiheitsanwendung, die fokussierte Benutzeroberflächenelemente hebt, das Fenster nicht an der richtigen Bildschirmposition, da das Fenster an den logischen Koordinaten platziert wird, nicht an den physischen Koordinaten, die von [**IAccessible::accLocation zurückgegeben**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)werden.

Die Lösung besteht aus zwei Teilen:

-   Machen Sie die Clientanwendung "dpi-aware". Rufen Sie hierzu beim Start die [**Funktion SetProcessDPIAware**](/windows/win32/api/winuser/nf-winuser-setprocessdpiaware) auf. Diese Funktion macht den gesamten Prozess dpi-bewusst, was bedeutet, dass alle Fenster, die zum Prozess gehören, nicht skaliert sind.
-   Verwenden Sie dpi-orientierte Funktionen. Um beispielsweise Cursorkoordinaten zu erhalten, rufen Sie die [**GetPhysicalCursorPos-Funktion**](/windows/win32/api/winuser/nf-winuser-getphysicalcursorpos) auf. Verwenden Sie [**getCursorPos nicht.**](/windows/win32/api/winuser/nf-winuser-getcursorpos) Das Verhalten in dpi-orientierte Anwendungen ist nicht definiert.

Wenn Ihre Anwendung eine direkte prozessübergreifende Kommunikation mit nicht dpi-orientierten Anwendungen ausführt, haben Sie möglicherweise eine Konvertierung zwischen logischen und physischen Koordinaten mithilfe der [**PhysicalToLogicalPoint-**](/windows/win32/api/winuser/nf-winuser-physicaltologicalpoint) und [**LogicalToPhysicalPoint-Funktionen**](/windows/win32/api/winuser/nf-winuser-logicaltophysicalpoint) ausgeführt.

 

 