---
title: Übersicht über die Windows-Grafik Architektur
description: Beschreibt die C++/com-Grafik-APIs in Windows.
ms.assetid: 9654b18b-d615-455d-a92a-6fc2ccda469e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f45ba44f54b947d923b888d51080ff0335119a1
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "104132129"
---
# <a name="overview-of-the-windows-graphics-architecture"></a>Übersicht über die Windows-Grafik Architektur

Windows stellt mehrere C++/COM-APIs für Grafiken bereit. Diese APIs sind in der folgenden Abbildung dargestellt.

![ein Diagramm, in dem die Windows-Grafik-APIs angezeigt werden.](images/graphics01.png)

-   Graphics Device Interface (GDI) ist die ursprüngliche Grafikschnittstelle für Windows. GDI wurde zunächst für 16-Bit-Windows geschrieben und anschließend für 32-Bit-und 64-Bit-Windows aktualisiert.
-   GDI+ wurde in Windows XP als Nachfolger für GDI eingeführt. Der Zugriff auf die GDI+-Bibliothek erfolgt über eine Reihe von C++-Klassen, die flatc-Funktionen einschließen. Der .NET Framework stellt außerdem eine verwaltete Version von GDI+ im **System. Drawing** -Namespace bereit.
-   Direct3D unterstützt 3D-Grafiken.
-   Direct2D ist eine moderne API für 2D-Grafiken, die Nachfolger für GDI und GDI+.
-   DirectWrite ist ein Textlayout und eine rasterisierungsengine. Sie können entweder GDI oder Direct2D verwenden, um den rasterierten Text zu zeichnen.
-   Die DirectX-Grafik Infrastruktur (DXGI) führt Aufgaben auf niedriger Ebene aus, z. b. das darstellen von Frames für die Ausgabe. Die meisten Anwendungen verwenden DXGI nicht direkt. Vielmehr fungiert es als Zwischenschicht zwischen dem Grafiktreiber und Direct3D.

Direct2D und DirectWrite wurden in Windows 7 eingeführt. Sie sind auch für Windows Vista und Windows Server 2008 über ein Platt Form Update verfügbar. Weitere Informationen finden Sie unter [Platt Form Update für Windows Vista](../win7ip/platform-update-for-windows-vista-portal.md).

Direct2D ist der Schwerpunkt dieses Moduls. Obwohl sowohl GDI als auch GDI+ weiterhin in Windows unterstützt werden, werden für neue Programme Direct2D und DirectWrite empfohlen. In einigen Fällen kann eine Kombination der Technologien praktischer sein. In diesen Situationen sind Direct2D und DirectWrite für die Interoperabilität mit GDI konzipiert.

In den nächsten Abschnitten werden einige der Vorteile von Direct2D beschrieben.

### <a name="hardware-acceleration"></a>Hardwarebeschleunigung

Der Begriff *Hardwarebeschleunigung* bezieht sich auf Grafik Berechnungen, die von der Grafikverarbeitungseinheit (Graphics Processing Unit, GPU) anstelle der CPU ausgeführt werden. Moderne GPUs sind stark optimiert für die Berechnungs Typen, die beim Rendern von Grafiken verwendet werden. Im Allgemeinen ist der Wert, der von der CPU auf die GPU verschoben wird, besser.

Während GDI die Hardwarebeschleunigung für bestimmte Vorgänge unterstützt, werden viele GDI-Vorgänge an die CPU gebunden. Direct2D ist auf Direct3D aufgeschichtet und nutzt die von der GPU bereitgestellte Hardwarebeschleunigung in vollem Umfang. Wenn die GPU die für Direct2D benötigten Features nicht unterstützt, greift Direct2D auf das Software Rendering zurück. Direct2D outführt in den meisten Fällen GDI und GDI+ aus.

### <a name="transparency-and-anti-aliasing"></a>Transparenz und Antialiasing

Direct2D unterstützt vollständig Hardware beschleunigtes Alpha-Blending (Transparenz).

GDI bietet eingeschränkte Unterstützung für Alpha-Blending. Die meisten GDI-Funktionen unterstützen Alpha Blending nicht, obwohl GDI bei einem BitBLT-Vorgang Alpha Blending unterstützt. GDI+ unterstützt Transparenz, aber die Alpha Mischung wird von der CPU ausgeführt, sodass Sie nicht von der Hardwarebeschleunigung profitiert.

Die Hardware beschleunigte Alpha Mischung ermöglicht außerdem Antialiasing. *Aliasing* ist ein Element, das durch die Stichprobenentnahme einer kontinuierlichen Funktion verursacht wird. Wenn eine gekrümmte Linie z. b. in Pixel konvertiert wird, kann das Aliasing eine verzweigte Darstellung verursachen. \[ 3 \] jede Technik, die die durch Aliasing verursachten Artefakte reduziert, wird als eine Form des Antialiasing angesehen. In Grafiken wird Antialiasing durch das Mischen von Kanten mit dem Hintergrund erreicht. Hier ist z. b. ein Kreis, der von GDI gezeichnet wird, und derselbe Kreis, der von Direct2D gezeichnet wird.

![eine Abbildung der Anti-Aliasing-Techniken in Direct2D.](images/graphics02.png)

Die nächste Abbildung zeigt ein Detail jedes Kreises.

![ein Detail des vorherigen Bilds.](images/graphics03.png)

Der von GDI (links) gezeichnete Kreis besteht aus schwarzen Pixeln, die eine Kurve angleichen. Der von Direct2D (right) gezeichnete Kreis verwendet Blending, um eine glattere Kurve zu erzeugen.

GDI unterstützt das Antialiasing nicht, wenn es Geometrie (Linien und Kurven) zeichnet. GDI kann Text mit Antialiasing mithilfe von ClearType zeichnen. Andernfalls ist der GDI-Text ebenfalls Alias. Aliasing ist für Text besonders bemerkbar, da die verzweigten Linien den Schriftart Entwurf stören, sodass der Text weniger lesbar ist. Obwohl GDI+ Antialiasing unterstützt, wird es von der CPU angewendet, sodass die Leistung nicht so gut ist wie Direct2D.

### <a name="vector-graphics"></a>Vektorgrafiken

Direct2D unterstützt *Vektorgrafiken*. In Vektorgrafiken werden mathematische Formeln verwendet, um Linien und Kurven darzustellen. Diese Formeln sind nicht von der Bildschirmauflösung abhängig und können daher auf beliebige Dimensionen skaliert werden. Vektorgrafiken sind besonders nützlich, wenn ein Bild skaliert werden muss, um unterschiedliche Monitorgrößen oder Bildschirmauflösungen zu unterstützen.

## <a name="next"></a>Nächste

[Der Desktopfenster-Manager](the-desktop-window-manager.md)

 

 
