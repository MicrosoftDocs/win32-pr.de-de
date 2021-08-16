---
title: Informationen zu Direct2D
description: Führt Direct2D ein, eine API, die Win32-Entwicklern die Möglichkeit bietet, 2D-Grafikrenderingaufgaben mit einer höheren Leistung und visueller Qualität auszuführen.
ms.assetid: 05cc230e-6fec-4a15-8e28-c68397392fc5
keywords:
- Direct2D,about
- Direct2D, Interoperabilität
- Direct2D, Leistung
- Direct2D, Verfügbarkeit
- Direct2D, Anwendungen
- Interoperabilität,Direct2D
- Leistung für Direct2D
- Verfügbarkeit für Direct2D
- Anwendungen für Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbe011b2d61fbb116efa4818f0db988d24e39fcb707e3ae42ddc0fb91f065652
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117825581"
---
# <a name="about-direct2d"></a>Informationen zu Direct2D

In diesem Thema wird Direct2D, eine API, die Win32-Entwicklern die Möglichkeit bietet, 2D-Grafikrenderingaufgaben mit überlegener Leistung und visueller Qualität auszuführen.

## <a name="what-is-direct2d"></a>Was ist Direct2D?

Direct2D ist eine hardwarebeschleunigte 2D-Grafik-API im Unmittelbarmodus, die leistungsstarkes und hochwertiges Rendering für 2D-Geometrie, Bitmaps und Text bietet. Die Direct2D-API ist für die Zusammenarbeit mit vorhandenem Code konzipiert, der GDI, GDI+ oder Direct3D verwendet.

Direct2D ist in erster Linie für die Verwendung durch die folgenden Entwicklerklassen konzipiert:

-   Entwickler großer nativer Anwendungen auf Unternehmens-Ebene.
-   Entwickler, die Steuerungstoolkits und Bibliotheken erstellen, die von Downstreamentwicklern verwendet werden können.
-   Entwickler, die serverseitiges Rendering von 2D-Grafiken benötigen.
-   Entwickler, die Direct3D-Grafiken verwenden und einfaches, leistungsstarkes 2D- und Textrendering für Menüs, Benutzeroberflächenelemente (UI) und Kopf-auf-Bildschirme (HUDs) benötigen.

## <a name="why-direct2d"></a>Gründe für Direct2D

Die wichtigsten Beweggründe für das Erstellen einer neuen 2D-Grafik-API in Microsoft Windows folgende:

-   Um mit dem zunehmenden visuellen Wandel Schritt zu halten, an Windows Benutzer gewohnt sind.
-   Damit Entwickler 2D-Renderingcode schreiben können, der direkt mit der Grafikverarbeitungshardware des PCs skaliert wird, auf dem er ausgeführt wird.
-   Damit Entwickler Code für das Rendern von 2D-Grafiken schreiben können, die im Kontext eines Diensts ausgeführt werden können.

In den letzten Jahren haben Endbenutzer begonnen, mehr visuelle Genauigkeit bei digitalen Erfahrungen zu erwarten. Dieser Trend spiegelt sich in der Unterhaltungsindustrie wider. GPS-Geräte, Medienwiedergabegeräte, Mobiltelefone und Digitalkameras bieten Jahr für Jahr konsistent vielfältigere Erfahrungen. Dieser Trend lässt sich auch in der Vielfalt grafischer Inhalte in Film, Fernsehsendungen, Spielen und im Web erkennen. Um mit diesen Änderungen Schritt zu halten, werden Entwickler ständig aufgefordert, ihre vorhandenen Windows-Anwendungen auf die nächste Ebene der visuellen Vielfalt zu bringen.

Grafikprozessoren auf modernen Windows-PCs wurden ebenfalls ständig weiterentwickelt. Dies wird durch Fortschritte bei der Grafik von Grafikkarten und Teilen der Windows-Erfahrung wie Windows Media Center und Beinen unterstützt. Einige Windows können moderne GPUs nutzen, indem Sie Microsoft Direct3D und Windows Presentation Foundation (WPF) verwenden. Während Direct3D High-End-3D-Grafikanwendungen und WPF die Anforderungen von .NET-Entwicklern erfüllt, gibt es Lücken für Entwickler, die über große Codebasis für das Rendern von Code basierend auf GDI und GDI+ verfügen oder hochwertige 2D-Grafiken in ihre Direct3D-basierten Anwendungen integrieren möchten.

Schließlich ist die Notwendigkeit einer Grafik-API, die in einem Dienst verwendet werden kann, zu einer neuen Anforderung für Entwickler geworden, die in Unternehmens- und Webentwicklungsszenarien arbeiten. Vorhandene Rendering-APIs konzentrieren sich auf clientseitiges Rendering in einer einzelnen Benutzersitzung. Daher können sie bei der Verwendung in einem Dienstkontext in Bereichen der Stabilität und Skalierbarkeit nicht zu kurz kommen. Dafür ist eine neue API erforderlich.

## <a name="high-performance-with-maximum-availability"></a>Hohe Leistung mit maximaler Verfügbarkeit

Direct2D ist eine Benutzermodusbibliothek, die mit der Direct3D 10.1-API erstellt wird. Dies bedeutet, dass Direct2D-Anwendungen vom hardwarebeschleunigten Rendering auf modernen Mainstream-GPUs profitieren. Die Hardwarebeschleunigung wird auch auf früherer Direct3D 9-Hardware mithilfe des Direct3D 10-Level-9-Renderings erreicht. Diese Kombination bietet eine hervorragende Leistung auf Grafikhardware auf vorhandenen Windows PCs.

> [!Note]  
> Ab Windows 8 wird Direct2D mithilfe der Direct3D 11.1-API erstellt.

 

Das folgende Diagramm zeigt die mehrschichtige Architektur von Direct2D.

![Diagramm der direct2d-mehrschichtigen Architektur](images/direct2d-architectual-layering.png)

In Szenarien, in denen die Verwendung der Hardwarebeschleunigung nicht möglich ist, enthält Direct2D einen hochleistungsbasierten Softwareraster. Beim Rendern in Software erzielen Anwendungen, die Direct2D verwenden, eine wesentlich bessere Renderingleistung als mit GDI+ und mit ähnlicher visueller Qualität. Der Softwareraster ist auch für die Verwendung in einem Dienstkontext konzipiert.

Inhalte, die mit Direct2D gerendert werden, können auch remote mithilfe der Remotedesktopprotokoll-Infrastruktur (RDP) im Windows 7-Betriebssystem angezeigt werden. Entwickler können auswählen, ob das Rendering von der GPU auf dem Anzeigecomputer verarbeitet oder lokal gerendert und als Bitmaps übertragen wird. Diese Auswahl kann basierend auf der erforderlichen Füllrate und der Menge der gerenderten Grafikprimitiven getroffen werden. Wenn auf dem Anzeigecomputer ein Betriebssystem ausgeführt wird, das vor Windows 7 liegt, erfolgt das Rendering der Remoteanzeige, indem Bitmaps über das Netzwerk übertragen werden.

Durch die Bereitstellung einer einzelnen API, die die Leistung von Direct3D und Hochverfügbarkeit kombiniert, indem Softwarefallback, Remotedesktop und Dienstrendering bereitgestellt werden, ermöglicht Direct2D Entwicklern eine einzelne Implementierung für hochleistungsbasiertes Rendering in vielen verschiedenen Szenarien.

## <a name="visual-quality"></a>Visuelle Qualität

Anwendungen, die Direct2D für Grafiken verwenden, können eine höhere visuelle Qualität bieten, als mit GDI erreicht werden kann. Direct2D verwendet antialiasing pro Primitive, um geglättetere Kurven und Linien in gerenderten Inhalten zu liefern. Es gibt auch vollständige Unterstützung für Transparenz und Alphablending beim Rendern von 2D-Primitiven. Die folgenden Bilder vergleichen aliased content rendered by using GDI (auf der linken Seite) mit antialiased content rendered by Direct2D (auf der rechten Seite).

![Abbildung von Kurven und Linien, die in gdi und direct2d gerendert werden](images/rendering-curves-and-lines.png)

Entwickler können das Aliasrendering von Vektorgrafiken angeben. Dies wird in Szenarien verwendet, in denen das Ausrichten an Hartpixelgrenzen erforderlich ist, z. B. Benutzeroberflächenelemente wie Zeiger oder Lineals, wenn der GDI-Ausgabestil übereinstimmen muss, oder wenn Antialiasing im Renderingprozess über Multisample Antialiasing oder einen anderen Mechanismus nachgeschaltet wird.

## <a name="interoperability"></a>Interoperabilität

Die Integration des Direct2D-basierten Renderings wird Entwicklern durch die Interoperabilität auf Oberflächenebene mit GDI und Direct3D erleichtert. Anwendungen, die Inhalte hauptsächlich mit GDI, GDI+ oder Direct3D rendern, können mit Direct2D beginnen, um bestimmte Bereiche ihrer Anwendung zu rendern, und im Laufe der Zeit zu einem Modell wechseln, bei dem das Rendering hauptsächlich über Direct2D erfolgt, wobei GDI hauptsächlich für Plug-Ins oder Legacy-Erweiterbarkeit verwendet wird.

Direct2D erleichtert auch die Verwendung von [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) für hochwertigen Text und die erweiterten Bildverarbeitungsfunktionen der [Microsoft Windows Imaging Component (WIC).](https://msdn.microsoft.com/library/ms737408.aspx)

Weitere Informationen zur Direct2D-Interoperabilität finden Sie im Abschnitt [Interoperabilität des Direct2D SDK.](interoperability.md)

## <a name="summary"></a>Zusammenfassung

Microsoft Direct2D ermöglicht Entwicklern das Erstellen von 2D-Grafikfeatures in ihren Anwendungen, die eine bessere visuelle Qualität als GDI bieten, und Leistungsmerkmale, die mit modernen GPUs skaliert werden. Das Direct2D-Interoperabilitätsmodell ermöglicht Es Entwicklern, Teile ihrer Anwendung parallel zum GDI-, GDI+- oder Direct3D-basierten Rendering selektiv zu migrieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct2D-Schnellstart für Windows 8](direct2d-quickstart-with-device-context.md)
</dt> <dt>

[Übersicht über die Direct2D-API](the-direct2d-api.md)
</dt> </dl>

 

 