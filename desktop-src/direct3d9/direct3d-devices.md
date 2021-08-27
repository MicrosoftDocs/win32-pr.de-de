---
description: Ein Direct3D-Gerät ist die Renderingkomponente von Direct3D. Er kapselt und speichert den Renderingzustand. Darüber hinaus führt ein Direct3D-Gerät Transformationen und Beleuchtungsvorgänge durch und rastert ein Bild auf einer Oberfläche.
ms.assetid: b592edb8-351a-4a82-9ff7-8a69d82723bc
title: Direct3D-Geräte (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12b36ae856686c0f6a0b821b92a871ed98e016bf1a010200038281f2eb50964e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096054"
---
# <a name="direct3d-devices-direct3d-9"></a>Direct3D-Geräte (Direct3D 9)

Ein Direct3D-Gerät ist die Renderingkomponente von Direct3D. Er kapselt und speichert den Renderingzustand. Darüber hinaus führt ein Direct3D-Gerät Transformationen und Beleuchtungsvorgänge durch und rastert ein Bild auf einer Oberfläche.

-   [XPDM im Vergleich zu WDDM](xpdm-vs-wddm.md)
-   [Gerätetypen (Direct3D 9)](device-types.md)
-   [Erstellen eines Geräts (Direct3D 9)](creating-a-device.md)
-   [Fenstermodus und Full-Screen Modus (Direct3D 9)](windowed-vs-full-screen-mode.md)
-   [Auswählen eines Geräts (Direct3D 9)](selecting-a-device.md)
-   [Verlorene Geräte (Direct3D 9)](lost-devices.md)
-   [Bestimmen der Hardwareunterstützung (Direct3D 9)](determining-hardware-support.md)
-   [Verarbeiten von Scheitelpunktdaten (Direct3D 9)](processing-vertex-data.md)
-   [Primitive](primitives.md)

Architekturgemäß enthalten Direct3D-Geräte ein Transformationsmodul, ein Beleuchtungsmodul und ein Rastermodul, wie im folgenden Diagramm dargestellt.

![Diagramm der Direct3d-Gerätearchitektur](images/d3ddev.png)

Direct3D unterstützt derzeit zwei Haupttypen von Direct3D-Geräten:

-   Ein Speichergerät mit hardwarebeschleuniger Rasterung und Schattierung mit Hardware- und Softwarevertexverarbeitung
-   Ein Referenzgerät

Sie können sich diese Geräte als zwei separate Treiber vorstellen. Software- und Referenzgeräte werden durch Softwaretreiber dargestellt, und das -Gerät wird durch einen Hardwaretreiber dargestellt. Die gängigste Möglichkeit, diese Geräte zu nutzen, besteht darin, das -Gerät für den Versand von Anwendungen und das Referenzgerät für Funktionstests zu verwenden. Diese werden von Drittanbietern bereitgestellt, um bestimmte Geräte zu emulieren, z. B. Entwicklungshardware, die noch nicht veröffentlicht wurde.

Das direct3D-Gerät, das von einer Anwendung erstellt wird, muss den Funktionen der Hardware entsprechen, auf der die Anwendung ausgeführt wird. Direct3D bietet Renderingfunktionen, entweder durch Zugriff auf 3D-Hardware, die auf dem Computer installiert ist, oder durch Emulieren der Funktionen von 3D-Hardware in Software. Daher stellt Direct3D Geräte sowohl für den Hardwarezugriff als auch für die Softwareemulation bereit.

Hardwarebeschleunigte Geräte bieten eine viel bessere Leistung als Softwaregeräte. Der Gerätetyp ist auf allen direct3D-unterstützten Grafikadaptern verfügbar. In den meisten Fällen sind Anwendungen auf Computer ausgerichtet, die über Hardwarebeschleunigung verfügen und auf Softwareemulation angewiesen sind, um Niedrigere-End-Computer zu unterstützen.

Mit Ausnahme des Referenzgeräts unterstützen Softwaregeräte nicht immer die gleichen Features wie ein Hardwaregerät. Anwendungen sollten immer Gerätefunktionen abfragen, um zu bestimmen, welche Features unterstützt werden.

Da das Verhalten der mit Direct3D 9 bereitgestellten Software- und Referenzgeräte mit dem Verhalten des Geräts "halogen" identisch ist, funktioniert der Anwendungscode, der für die Arbeit mit dem Gerät erstellt wurde, ohne Änderungen mit der Software oder referenzierten Geräten. Beachten Sie, dass das bereitgestellte Software- oder Referenzgeräteverhalten zwar mit dem des -Geräts identisch ist, die Gerätefunktionen jedoch variieren, und ein bestimmtes Softwaregerät kann einen viel kleineren Satz von Funktionen implementieren.

## <a name="behaviors"></a>Verhalten

Mit Direct3D können Sie das Verhalten eines Geräts sowie den Typ des Geräts angeben. Die [**IDirect3D9::CreateDevice-Methode**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) ermöglicht eine Kombination aus einem oder mehreren Verhaltensflags, um das globale Verhalten des Direct3D-Geräts zu steuern. Diese Verhalten geben an, was ist und was nicht im Laufzeitteil von Direct3D verwaltet wird, und die Gerätetypen geben an, welcher Treiber verwendet werden soll. Obwohl einige Kombinationen von Geräteverhalten ungültig sind, ist es möglich, alle Geräteverhalten mit allen Gerätetypen zu verwenden. Beispielsweise ist es gültig, D3DDEVTYPE SW auf einem Gerät anzugeben, das \_ mit D3DCREATE \_ PUREDEVICE erstellt wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte](getting-started.md)
</dt> </dl>

 

 
