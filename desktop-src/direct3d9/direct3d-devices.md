---
description: Ein Direct3D-Gerät ist die Renderingkomponente von Direct3D. Er kapselt und speichert den Renderingzustand. Außerdem führt ein Direct3D-Gerät Transformationen und Beleuchtungs Vorgänge durch und rasteriert ein Bild auf eine Oberfläche.
ms.assetid: b592edb8-351a-4a82-9ff7-8a69d82723bc
title: Direct3D-Geräte (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c07726069b952ba99d608e5f36df8e1fb7745cd7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213895"
---
# <a name="direct3d-devices-direct3d-9"></a>Direct3D-Geräte (Direct3D 9)

Ein Direct3D-Gerät ist die Renderingkomponente von Direct3D. Er kapselt und speichert den Renderingzustand. Außerdem führt ein Direct3D-Gerät Transformationen und Beleuchtungs Vorgänge durch und rasteriert ein Bild auf eine Oberfläche.

-   [XPDM im Vergleich zu WDDM](xpdm-vs-wddm.md)
-   [Gerätetypen (Direct3D 9)](device-types.md)
-   [Erstellen eines Geräts (Direct3D 9)](creating-a-device.md)
-   [Fenster-vs-Full-Screen Modus (Direct3D 9)](windowed-vs-full-screen-mode.md)
-   [Auswählen eines Geräts (Direct3D 9)](selecting-a-device.md)
-   [Verlorene Geräte (Direct3D 9)](lost-devices.md)
-   [Bestimmen der Hardware Unterstützung (Direct3D 9)](determining-hardware-support.md)
-   [Verarbeiten von Scheitelpunkt Daten (Direct3D 9)](processing-vertex-data.md)
-   [Primitive](primitives.md)

In der Architektur enthalten Direct3D-Geräte ein Transformationsmodul, ein Beleuchtungs Modul und ein rasterisierungsmodul, wie im folgenden Diagramm gezeigt.

![Diagramm der Direct3D-Geräte Architektur](images/d3ddev.png)

Direct3D unterstützt derzeit zwei Haupttypen von Direct3D-Geräten:

-   Ein HAL-Gerät mit Hardware beschleunigter rasterisierung und Schattierung mit Hardware-und Software Vertex-Verarbeitung
-   Ein Referenzgerät

Sie können sich diese Geräte als zwei separate Treiber vorstellen. Software-und Referenzgeräte werden von Software Treibern dargestellt, und das HAL-Gerät wird durch einen Hardwaretreiber dargestellt. Die gängigste Methode, diese Geräte zu nutzen, besteht darin, das HAL-Gerät für den Versand von Anwendungen und das Referenzgerät zum Testen von Features zu verwenden. Diese werden von Drittanbietern bereitgestellt, um bestimmte Geräte zu emulieren, z. b. Entwicklungs Hardware, die noch nicht freigegeben wurde.

Das Direct3D-Gerät, das von einer Anwendung erstellt wird, muss den Funktionen der Hardware entsprechen, auf der die Anwendung ausgeführt wird. Direct3D bietet Renderingfunktionen entweder durch den Zugriff auf 3D-Hardware, die auf dem Computer installiert ist, oder durch emulieren der Funktionen von 3D-Hardware in Software. Daher bietet Direct3D Geräte sowohl für den Hardware Zugriff als auch für die Software Emulation.

Hardware beschleunigte Geräte bieten eine viel bessere Leistung als Software Geräte. Der HAL-Gerätetyp ist auf allen von Direct3D unterstützten Grafikadaptern verfügbar. In den meisten Fällen sind Anwendungen auf Computer ausgerichtet, die Hardwarebeschleunigung aufweisen und auf der Software Emulation zur Unterstützung von niedrigeren Computern basieren.

Mit Ausnahme des Referenz Geräts unterstützen Software Geräte nicht immer dieselben Features wie ein Hardware Gerät. Anwendungen sollten immer Gerätefunktionen Abfragen, um zu bestimmen, welche Features unterstützt werden.

Da das Verhalten der Software-und Referenzgeräte, die mit Direct3D 9 bereitgestellt werden, mit der des HAL-Geräts identisch ist, kann der Anwendungscode, der zum Arbeiten mit dem HAL-Gerät erstellt wurde, ohne Änderungen mit der Software oder Referenz Geräten arbeiten. Beachten Sie, dass das bereitgestellte Software-oder Referenzgeräte Verhalten mit dem des HAL-Geräts identisch ist, die Gerätefunktionen jedoch variieren und ein bestimmtes Software Gerät möglicherweise eine viel geringere Anzahl von Funktionen implementiert.

## <a name="behaviors"></a>Verhalten

Mit Direct3D können Sie das Verhalten eines Geräts sowie den Typ des Geräts angeben. Die [**IDirect3D9:: kreatedevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) -Methode ermöglicht eine Kombination aus einem oder mehreren der verhaltenflags, um das globale Verhalten des Direct3D-Geräts zu steuern. Diese Verhaltensweisen geben an, was im Laufzeitbereich von Direct3D ist und nicht verwaltet wird, und die Gerätetypen geben an, welcher Treiber verwendet werden soll. Obwohl einige Kombinationen von Geräte Verhaltensweisen nicht gültig sind, ist es möglich, alle Geräteverhalten mit allen Gerätetypen zu verwenden. Beispielsweise ist es zulässig, D3DDEVTYPE \_ SW auf einem Gerät anzugeben, das mit D3DCREATE \_ puredevice erstellt wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte](getting-started.md)
</dt> </dl>

 

 
