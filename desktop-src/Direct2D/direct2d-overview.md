---
title: Informationen zu Direct2D
description: Führt Direct2D ein, eine API, die Win32-Entwicklern die Möglichkeit bietet, 2D-Grafik Rendering-Aufgaben mit hoher Leistung und visueller Qualität auszuführen.
ms.assetid: 05cc230e-6fec-4a15-8e28-c68397392fc5
keywords:
- Direct2D, Informationen zu
- Direct2D, Interoperabilität
- Direct2D, Leistung
- Direct2D, Verfügbarkeit
- Direct2D, Anwendungen
- Interoperabilität, Direct2D
- Leistung für Direct2D
- Verfügbarkeit für Direct2D
- Anwendungen für Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 486c83b7a83ef82983e189977f9f99254b0a1977
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948944"
---
# <a name="about-direct2d"></a>Informationen zu Direct2D

In diesem Thema wird Direct2D vorgestellt, eine API, die Win32-Entwicklern die Möglichkeit bietet, 2D-Renderingaufgaben mit hoher Leistung und visueller Qualität auszuführen.

## <a name="what-is-direct2d"></a>Was ist Direct2D?

Bei Direct2D handelt es sich um eine hardwarebeschleunigte 2D-Grafik-API, die eine leistungsstarke und qualitativ hochwertige Darstellung für 2D-Geometrie, Bitmaps und Text bereitstellt. Die Direct2D-API ist für die Interaktion mit vorhandenem Code konzipiert, der GDI, GDI+ oder Direct3D verwendet.

Direct2D wurde hauptsächlich für die Verwendung durch die folgenden Klassen von Entwicklern entwickelt:

-   Entwickler umfangreicher, Unternehmens eigener Anwendungen.
-   Entwickler, die Steuerelement-Toolkits und-Bibliotheken für die Nutzung durch downstreamentwickler erstellen.
-   Entwickler, die ein serverseitiges Rendering von 2D-Grafiken benötigen.
-   Entwickler, die Direct3D-Grafiken verwenden und einfache, hochleistungsfähige 2D-und Text Rendering für Menüs, Elemente der Benutzeroberfläche (UI) und Heads-Up-Anzeige (HUDs) benötigen.

## <a name="why-direct2d"></a>Warum Direct2D?

Die Hauptgründe für das Erstellen einer neuen 2D-Grafik-API in Microsoft Windows sind folgende:

-   Die Geschwindigkeit der zunehmenden visuellen Reichtümer, an die Windows-Benutzer gewöhnt sind.
-   Um Entwicklern das Schreiben von 2D-Renderingcode zu ermöglichen, der direkt mit der Grafik Verarbeitungs Hardware des PCs skaliert, auf dem es ausgeführt wird.
-   Um Entwicklern das Schreiben von Code zum Rendern von 2D-Grafiken zu ermöglichen, die im Kontext eines Dienstanbieter ausgeführt werden können.

In den letzten Jahren haben Endbenutzer damit begonnen, eine höhere visuelle Genauigkeit bei digitalen Erfahrungen zu erwarten. Dieser Trend spiegelt sich in der Unterhaltungselektronik wider. GPS-Geräte, Medienwiedergabe Geräte, Mobiltelefone und digitale Kameras bieten im Jahr nach dem Jahr konsistente Möglichkeiten. Dieser Trend kann auch in der Vielfalt grafischer Inhalte in Filmen, Fernsehsendungen, Videospielen und im Internet angezeigt werden. Um mit diesen Änderungen Schritt zu halten, werden Entwickler ständig aufgefordert, Ihre vorhandenen Windows-Anwendungen auf die nächste Ebene der visuellen Vielfalt zu bringen.

Grafikprozessoren in modernen Windows-PCs wurden auch ständig weiterentwickelt und sind durch Fortschritte in Videospiel Grafiken und Teilen der Windows-Darstellung wie Windows Media Center und Aero gesteuert. Einige Windows-Anwendungen können moderne GPUs mithilfe von Microsoft Direct3D und Windows Presentation Foundation (WPF) nutzen. Obwohl Direct3D High-End-Grafikanwendungen für 3D-Grafiken bietet und WPF den Anforderungen von .NET-Entwicklern gerecht wird, gibt es Lücken für Entwickler, die große vorhandene Codebasen zum Rendern von Code auf Grundlage von GDI und GDI+ haben oder qualitativ hochwertige 2D-Grafiken in Ihre Direct3D-basierten Anwendungen integrieren möchten.

Schließlich ist die Notwendigkeit einer Grafik-API, die in einem Dienst verwendet werden kann, eine neue Anforderung für Entwickler, die in Szenarien für Unternehmen und Webentwicklung arbeiten. Vorhandene Rendering-APIs konzentrieren sich auf Client seitiges Rendering in einer einzelnen Benutzersitzung. Daher können Sie bei Verwendung in einem Dienst Kontext in Bereiche der Stabilität und Skalierbarkeit geraten. Eine neue API ist erforderlich, um dies zu beheben.

## <a name="high-performance-with-maximum-availability"></a>Hohe Leistung mit maximaler Verfügbarkeit

Direct2D ist eine benutzermodusbibliothek, die mit der Direct3D 10,1-API erstellt wird. Dies bedeutet, dass Direct2D-Anwendungen von einem Hardware beschleunigten Rendering auf modernen, Mainstream-GPUs profitieren. Die Hardwarebeschleunigung wird auch auf früheren Direct3D 9-Hardware mithilfe von Direct3D 10-Level-9-Rendering erreicht. Diese Kombination bietet hervorragende Leistung bei Grafikhardware auf vorhandenen Windows-PCs.

> [!Note]  
> Ab Windows 8 wird Direct2D mit der Direct3D 11,1-API erstellt.

 

Das folgende Diagramm zeigt die geschichtete Architektur von Direct2D.

![Diagramm der Direct2D geschichteten Architektur](images/direct2d-architectual-layering.png)

In Szenarien, in denen die Verwendung der Hardwarebeschleunigung nicht möglich ist, enthält Direct2D einen hochleistungsfähigen Software-Rasterizer. Beim Rendern in Software können Anwendungen, die Direct2D verwenden, eine deutlich bessere Renderingleistung als mit GDI+ und mit ähnlicher visueller Qualität erzielen. Der Software Raster ist auch für die Verwendung in einem Dienst Kontext konzipiert.

Inhalte, die mithilfe von Direct2D gerendert werden, können auch Remote mithilfe der Remotedesktopprotokoll-Infrastruktur (RDP) im Windows 7-Betriebssystem angezeigt werden. Entwickler können auswählen, ob das Rendering von der GPU auf dem Anzeige Computer behandelt oder lokal gerendert und als Bitmaps übertragen wird. Diese Auswahl kann basierend auf der erforderlichen Füll Rate und der Anzahl der gerenderten Grafik primitive vorgenommen werden. Wenn auf dem Anzeige Computer ein Betriebssystem vor Windows 7 ausgeführt wird, wird das Rendering der Remote Anzeige durch das Übertragen von Bitmaps über das Netzwerk durchgeführt.

Durch die Bereitstellung einer einzelnen API, die die Leistung von Direct3D und Hochverfügbarkeit durch Bereitstellen von Software Fallback, Remote Desktop und Dienst Rendering kombiniert Direct2D ermöglicht es Entwicklern, eine einzige Implementierung für Hochleistungs Rendering in vielen verschiedenen Szenarien zu haben.

## <a name="visual-quality"></a>Visuelle Qualität

Anwendungen, die Direct2D für Grafiken verwenden, können eine höhere visuelle Qualität bieten, als Sie mit GDI erreichen können. Direct2D verwendet pro primitiver Antialiasing, um optimierte Kurven und Linien im gerenderten Inhalt bereitzustellen. Beim Rendern von 2D-primitiven wird außerdem die vollständige Unterstützung für Transparenz und Alpha Blending unterstützt. In den folgenden Bildern werden Alias Inhalte, die mithilfe von GDI gerendert werden (auf der linken Seite) mit durch Direct2D (rechts) gerenderten Inhalt verglichen.

![Abbildung von Kurven und Linien, die in GDI und in Direct2D gerendert werden](images/rendering-curves-and-lines.png)

Entwickler können das Rendern von Vektorgrafiken mit Aliasnamen angeben. Dies wird in Szenarien verwendet, in denen das Andocken an feste Pixel Grenzen erforderlich ist, wie z. b. Benutzeroberflächen Elemente wie Zeiger oder Lineale, wenn der GDI-Stil der Ausgabe abgeglichen werden muss, oder, wenn das Antialiasing im Renderingprozess über Multisample-Antialiasing oder einen anderen Mechanismus ausgeführt wird.

## <a name="interoperability"></a>Interoperabilität

Die Integration von Direct2D-basiertem Rendering wird Entwicklern Dank der Interoperabilität auf Oberflächenebene mit GDI und Direct3D erleichtert. Anwendungen, die Inhalte hauptsächlich mit GDI, GDI+ oder Direct3D rendern, können mit der Verwendung von Direct2D beginnen, um bestimmte Bereiche der Anwendung zu rendern, und im Laufe der Zeit zu einem Modell, in dem das Rendering primär über Direct2D ausgeführt wird, wobei GDI hauptsächlich für Plug-ins oder die Legacy Erweiterbarkeit verwendet wird.

Direct2D erleichtert auch die Verwendung von [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) für hochwertigen Text und die erweiterten Abbild Erstellungs Funktionen der [Microsoft Windows Imaging Component (WIC)](https://msdn.microsoft.com/library/ms737408.aspx).

Weitere Informationen zur Direct2D-Interoperabilität finden Sie im [Abschnitt Interoperabilität des Direct2D SDK.](interoperability.md)

## <a name="summary"></a>Zusammenfassung

Microsoft Direct2D ermöglicht es Entwicklern, 2D-Grafik Features in Ihren Anwendungen zu erstellen, die eine verbesserte visuelle Qualität gegenüber GDI bieten, und Leistungsmerkmale, die sich mit modernen GPUs skalieren lassen. Das Direct2D-Interoperabilitäts Modell ermöglicht es Entwicklern, Teile Ihrer Anwendung gleichzeitig zusammen mit GDI, GDI+ oder Direct3D-basiertem Rendering zu migrieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct2D Schnellstart für Windows 8](direct2d-quickstart-with-device-context.md)
</dt> <dt>

[Übersicht über die Direct2D-API](the-direct2d-api.md)
</dt> </dl>

 

 