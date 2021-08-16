---
title: Vergleich von Direct2D- und GDI-Hardwarebeschleunigung
description: Direct2D und GDI sind beide 2D-Rendering-APIs im Unmittelbarmodus und bieten ein gewisses Maß an Hardwarebeschleunigung.
ms.assetid: 0028a0c3-445d-46b7-b55b-46dff3bce9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: daa5fcb0f186915570d220a2807f816eae7a20fb393fbcd3113f6abf686fcd44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826543"
---
# <a name="comparing-direct2d-and-gdi-hardware-acceleration"></a>Vergleich von Direct2D- und GDI-Hardwarebeschleunigung

[Direct2D](./direct2d-portal.md) und [GDI](/windows/desktop/gdi/windows-gdi) sind beide 2D-Rendering-APIs im Unmittelbarmodus und bieten ein gewisses Maß an Hardwarebeschleunigung. In diesem Thema werden die Unterschiede zwischen Direct2D und GDI untersucht, einschließlich früherer und vorhandener Unterschiede in den Hardwarebeschleunigungsfeatures beider APIs.

Dieses Thema besteht aus den folgenden Teilen:

-   [Unterschiede zwischen Direct2D und GDI](#differences-between-direct2d-and-gdi)
-   [GDI- und Direct2D-Hardwarebeschleunigung](#gdi-and-direct2d-hardware-acceleration)
    -   [Erhöhen der Komplexität und Größe von Anzeigetreibern](#increasing-complexity-and-size-of-display-drivers)
    -   [Schwierigkeiten beim Synchronisieren von Sitzungs- und globalen Kernel-Adressräumen](#difficulty-in-synchronizing-session-and-global-kernel-address-spaces)
    -   [Verwaltung zusammengesetzter Fenster](#composited-window-management)
-   [GDI-Rendering in Windows 7](#gdi-rendering-in-windows-7)
-   [Gegenüber gegenüber der Direct2D- und GDI-Beschleunigung in Windows 7](#contrasting-direct2d-and-gdi-acceleration-in-windows-7)
    -   [Speicherort der Ressourcen](#location-of-resources)
    -   [Renderingmethode](#rendering-method)
    -   [Skalierbarkeit](#scalability)
    -   [Standort](#location-of-resources)
    -   [Verfügbarkeit der Hardwarebeschleunigung](#availability-of-hardware-acceleration)
    -   [Präsentationsmodell](#presentation-model)
-   [Zusammenfassung](#conclusion)

## <a name="differences-between-direct2d-and-gdi"></a>Unterschiede zwischen Direct2D und GDI

[GDI](/windows/desktop/gdi/windows-gdi) rendert nicht transparente Geometrien mit Alias, z. B. Polygone, Ellipsen und Linien. Sie rendert Alias- und ClearType-Text und kann die Transparenzmischung über die AlphaBlend-API unterstützen. Die Handhabung der Transparenz ist jedoch inkonsistent, und die meisten GDI-APIs ignorieren einfach den Alphakanal. Wenige GDI-APIs garantieren, was der Alphakanal nach einem Vorgang enthält. Noch wichtiger ist, dass das GDI-Rendering nicht einfach 3D-Vorgängen zuteil wird, und eine moderne GPU wird auf dem 3D-Teil der Rendering-Engine am effektivsten gerendert. Beispielsweise sind die Aliaslinien von [Direct2D](./direct2d-portal.md)so konzipiert, dass sie einfach als zwei Dreiecke implementiert werden, die auf der GPU gerendert werden, während GDI den Linienzeichnungsalgorithmus von Bresenham verwendet.

[Direct2D](./direct2d-portal.md) rendert undurchsichtige, transparente, Alias- und Antialiasingprimitive. Moderne Beis nutzen häufig Transparenz und Animation. Direct2D erleichtert die Erstellung einer modernen Benutzeroberfläche, da sie strenge Garantien dafür bietet, wie transparente Inhalte akzeptiert und gerendert werden und alle primitiven Elemente mithilfe der Hardwarebeschleunigung gerendert werden. Direct2D ist keine reine Obermenge von [GDI:](/windows/desktop/gdi/windows-gdi)Primitive, die bei der Umsetzung auf einer GPU unverhältnismäßig langsam gewesen wären, sind in Direct2D nicht vorhanden. Da Direct2D mit diesem Schwerpunkt auf der 3D-Beschleunigung erstellt wird, ist es auch einfach mit Direct3D zu verwenden.

Seit Windows NT 4 wird [GDI](/windows/desktop/gdi/windows-gdi) im Kernelmodus ausgeführt. Die Anwendung ruft GDI auf, das dann seine Entsprechung im Kernelmodus aufruft, die die Primitiven an ihr eigenes Treibermodell übergibt. Dieser Treiber sendet die Ergebnisse dann an den globalen Treiber für die Kernelmodusanzeige.

Ab Version Windows 2000 werden [GDI](/windows/desktop/gdi/windows-gdi) und die GDI-Treiber in einem unabhängigen Bereich im Kernel ausgeführt, der als "Sitzungsraum" bezeichnet wird. Für jede Anmeldesitzung wird ein Sitzungsadressenraum erstellt, und jede Instanz von GDI wird unabhängig in diesem eindeutigen Adressraum des Kernelmodus ausgeführt. Direct2D wird jedoch im Benutzermodus ausgeführt und übergibt Zeichnungsbefehle über den Direct3D-Treiber im Benutzermodus an den Kernelmodustreiber.

![Abbildung 1 – direct2d im Vergleich zu gdi](images/direct2d-vs-gdi1.png)

## <a name="gdi-and-direct2d-hardware-acceleration"></a>GDI- und Direct2D-Hardwarebeschleunigung

Der wichtigste Unterschied zwischen [Direct2D und](./direct2d-portal.md) der GDI-Hardwarebeschleunigung ist die zugrunde liegende Technologie, die sie steuert. [](/windows/desktop/gdi/windows-gdi) Direct2D wird über Direct3D auf oberster Ebene gespeichert, und GDI verfügt über ein eigenes Treibermodell, die GDI-Gerätetreiberschnittstelle (Device Driver Interface, DDI), die den GDI-Primitiven entspricht. Das Direct3D-Treibermodell entspricht dem, was die 3D-Renderinghardware in einer GPU rendert. Als die GDI-DDI zum ersten Mal definiert wurde, wurden die meisten Hardwarekomponenten für die Anzeigebeschleunigung auf die GDI-Primitive ausgerichtet. Im Laufe der Zeit lag der Schwerpunkt immer mehr auf der Beschleunigung von 3D-Spielen und weniger auf der Anwendungsbeschleunigung. Dies hat zur Folge, dass die BitBlt-API hardwarebeschleunigt wurde und die meisten anderen GDI-Vorgänge nicht.

Dadurch wird die Phase für eine Sequenz von Änderungen an der Darstellung von [GDI](/windows/desktop/gdi/windows-gdi) auf der Anzeige festgelegt. Die folgende Abbildung zeigt, wie sich das GDI-Anzeigerendering von Windows XP in Windows 7 geändert hat.

![Abbildung 2: Entwicklung des GDI-Anzeigerenderings](images/direct2d-vs-gdi2.png)

Es gab auch eine Reihe zusätzlicher Faktoren, die Änderungen am [GDI-Treibermodell](/windows/desktop/gdi/windows-gdi) verursacht haben, wie unten erläutert.

### <a name="increasing-complexity-and-size-of-display-drivers"></a>Erhöhen der Komplexität und Größe von Anzeigetreibern

3D-Treiber sind im Laufe der Zeit komplexer geworden. Komplexerer Code hat in der Regel mehr Fehler, was es vorteilhaft macht, dass der Treiber im Benutzermodus vorhanden ist, bei dem ein Treiberfehler keinen Systemneustart verursachen kann. Wie in der obigen Abbildung zu sehen ist, ist der Anzeigetreiber in eine komplexe Benutzermoduskomponente und eine einfachere Kernelmoduskomponente unterteilt.

### <a name="difficulty-in-synchronizing-session-and-global-kernel-address-spaces"></a>Schwierigkeiten beim Synchronisieren von Sitzungs- und globalen Kernel-Adressräumen

In Windows XP ist ein Anzeigetreiber in zwei verschiedenen Adressräumen vorhanden: Sitzungs- und Kernelbereich. Teile des Treibers müssen auf Ereignisse wie Energieverwaltungsereignisse reagieren. Dies muss mit dem Treiberzustand im Sitzungsadressenbereich synchronisiert werden. Dies ist eine schwierige Aufgabe und kann zu Fehlern führen, wenn Anzeigetreiber versuchen, diese unterschiedlichen Adressräume zu behandeln.

### <a name="composited-window-management"></a>Verwaltung zusammengesetzter Fenster

Der Desktopfenster-Manager (DWM), der in Windows 7 eingeführte Fenster-Manager für die Zusammenstellung, rendert alle Fenster auf Off-Screen-Oberflächen und erstellt sie dann zusammen, um sie auf dem Bildschirm anzuzeigen. Dies [erfordert, dass GDI](/windows/desktop/gdi/windows-gdi) auf einer Oberfläche gerendert werden kann, die dann von Direct3D zur Anzeige gerendert wird. Dadurch wurde ein Problem im XP-Treibermodell behoben, da GDI und Direct3D parallele Treiberstapel waren.

Daher wurde in Windows Vista der [GDI-DDI-Anzeigetreiber](/windows/desktop/gdi/windows-gdi) als der von Microsoft bereitgestellte Canonical Display Driver (CDD) implementiert, der GDI-Inhalt in einer Bitmap des Systemspeichers renderte, die auf dem Bildschirm zusammengesetzt werden soll.

## <a name="gdi-rendering-in-windows-7"></a>GDI-Rendering in Windows 7

Das in Windows Vista verwendete Treibermodell erforderte, dass jedes [GDI-Fenster](/windows/desktop/gdi/windows-gdi) sowohl von einer Videospeicheroberfläche als auch von einer Systemspeicheroberfläche unterstützt wird. Dies führte dazu, dass der Systemspeicher für jedes GDI-Fenster verwendet wurde.

Aus diesem Grund wurde [GDI](/windows/desktop/gdi/windows-gdi) in Windows 7 erneut geändert. . Anstatt auf eine Systemspeicheroberfläche zu rendern, wurde GDI so geändert, dass es in ein Aperture-Speichersegment gerendert wird. Der Öffnungsspeicher kann von der Videospeicheroberfläche aktualisiert werden, die den Fensterinhalt enthält. GDI kann wieder in den Öffnungsspeicher gerendert werden, und das Ergebnis kann dann zurück an die Fensteroberfläche gesendet werden. Da das Aperture-Speichersegment von der GPU adressiert werden kann, kann die GPU diese Aktualisierungen der Videospeicheroberfläche beschleunigen. Beispielsweise werden Textrendering, BitBlts, AlphaBlend, TransparentBlt und StretchBlt in diesen Fällen beschleunigt.

## <a name="contrasting-direct2d-and-gdi-acceleration-in-windows-7"></a>Gegenüber gegenüber der Direct2D- und GDI-Beschleunigung in Windows 7

[Direct2D](./direct2d-portal.md) und [GDI sind](/windows/desktop/gdi/windows-gdi) beide 2D-Rendering-APIs im unmittelbaren Modus und werden hardwarebeschleunigt. Es gibt jedoch eine Reihe von Unterschieden, die in beiden APIs bestehen bleiben.

### <a name="location-of-resources"></a>Speicherort der Ressourcen

[GDI](/windows/desktop/gdi/windows-gdi) verwaltet seine Ressourcen, insbesondere Bitmaps, standardmäßig im Systemspeicher. [Direct2D](./direct2d-portal.md) verwaltet seine Ressourcen im Videospeicher auf dem Adapter. Wenn GDI den Videospeicher aktualisieren muss, muss dies über den Bus erfolgen, es sei denn, die Ressource befindet sich bereits im Aperture-Speichersegment oder der Vorgang kann direkt ausgedrückt werden. Im Gegensatz dazu kann Direct2D einfach seine Primitive in Direct3D-Primitive übersetzen, da sich die Ressourcen bereits im Videospeicher befinden.

### <a name="rendering-method"></a>Renderingmethode

Um die Kompatibilität zu gewährleisten, führt [GDI](/windows/desktop/gdi/windows-gdi) einen großen Teil seines Renderings aus, um den Arbeitsspeicher mithilfe der CPU zu vergrößern. Im Gegensatz dazu übersetzt [Direct2D](./direct2d-portal.md) seine APIs-Aufrufe in Direct3D-Primitive und Zeichnungsvorgänge. Das Ergebnis wird dann auf der GPU gerendert. Ein Teil des GDI-Renderings wird auf der GPU ausgeführt, wenn der Öffnungsspeicher auf die Videospeicheroberfläche kopiert wird, die das GDI-Fenster darstellt.

### <a name="scalability"></a>Skalierbarkeit

[Die Renderingaufrufe von Direct2D](./direct2d-portal.md)sind alle unabhängige Befehlsstreams an die GPU. Jede Direct2D-Factory stellt ein anderes Direct3D-Gerät dar. [GDI](/windows/desktop/gdi/windows-gdi) verwendet einen Befehlsstream für alle Anwendungen im System. Die GDI-Methode kann zu einem Buildup von GPU- und CPU-Renderingkontextaufwand führen.

### <a name="location"></a>Standort

[Direct2D](./direct2d-portal.md) arbeitet vollständig im Benutzermodus, einschließlich der Direct3D-Laufzeit und des Direct3D-Treibers im Benutzermodus. Dadurch können Systemabstürze verhindert werden, die durch Codefehler im Kernel verursacht werden. [GDI](/windows/desktop/gdi/windows-gdi)verfügt jedoch über einen Großteil seiner Funktionalität im Sitzungsraum im Kernelmodus, dessen API-Oberfläche sich im Benutzermodus befindet.

### <a name="availability-of-hardware-acceleration"></a>Verfügbarkeit der Hardwarebeschleunigung

[GDI](/windows/desktop/gdi/windows-gdi) wird auf Windows XP hardwarebeschleunigt und auf Windows 7 beschleunigt, wenn die Desktopfenster-Manager ausgeführt wird und ein WDDM 1.1-Treiber verwendet wird. [Direct2D wird](./direct2d-portal.md) auf fast jedem WDDM-Treiber hardwarebeschleunigt und gibt an, ob DWM verwendet wird. Unter Vista wird GDI immer auf der CPU gerendert.

### <a name="presentation-model"></a>Präsentationsmodell

Als Windows zum ersten Mal entworfen wurde, war nicht genügend Arbeitsspeicher vorhanden, damit jedes Fenster in einer eigenen Bitmap gespeichert werden konnte. Daher wird [GDI](/windows/desktop/gdi/windows-gdi) immer logisch direkt auf dem Bildschirm gerendert, wobei verschiedene Clippingbereiche angewendet werden, um sicherzustellen, dass eine Anwendung nicht außerhalb ihres Fensters gerendert wurde. Im [Direct2D-Modell](./direct2d-portal.md) wird eine Anwendung in einem Back-Buffer gerendert, und das Ergebnis wird angezeigt, wenn die Anwendung mit dem Zeichnen fertig ist. Dadurch kann Direct2D Animationsszenarien viel flexibler verarbeiten als GDI.

## <a name="conclusion"></a>Zusammenfassung

Der vorhandene [GDI-Code](/windows/desktop/gdi/windows-gdi) funktioniert weiterhin gut unter Windows 7. Beim Schreiben von neuem Grafikrenderingcode sollte [Direct2D](./direct2d-portal.md) jedoch berücksichtigt werden, da moderne GPUs besser genutzt werden.

 

 