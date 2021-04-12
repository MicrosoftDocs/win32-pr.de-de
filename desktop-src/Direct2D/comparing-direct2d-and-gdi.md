---
title: Vergleichen von Direct2D-und GDI-Hardware Beschleunigung
description: Direct2D und GDI sind gleichzeitig 2D-renderingapis im unmittelbaren Modus, und beide bieten einen gewissen Grad an Hardwarebeschleunigung.
ms.assetid: 0028a0c3-445d-46b7-b55b-46dff3bce9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f05dce8719f4d07d3160c65b88570391c3eb736
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315260"
---
# <a name="comparing-direct2d-and-gdi-hardware-acceleration"></a>Vergleichen von Direct2D-und GDI-Hardware Beschleunigung

[Direct2D](./direct2d-portal.md) und [GDI](/windows/desktop/gdi/windows-gdi) sind gleichzeitig 2D-renderingapis im unmittelbaren Modus, und beide bieten einen gewissen Grad an Hardwarebeschleunigung. In diesem Thema werden die Unterschiede zwischen Direct2D und GDI erläutert, einschließlich der früheren und aktuellen Unterschiede bei den Hardware Beschleunigungs Features beider APIs.

Dieses Thema enthält die folgenden Teile:

-   [Unterschiede zwischen Direct2D und GDI](#differences-between-direct2d-and-gdi)
-   [GDI-und Direct2D-Hardwarebeschleunigung](#gdi-and-direct2d-hardware-acceleration)
    -   [Erhöhen der Komplexität und der Größe von Anzeige Treibern](#increasing-complexity-and-size-of-display-drivers)
    -   [Schwierigkeiten beim Synchronisieren der Sitzungs-und globalen Kernel Adressräume](#difficulty-in-synchronizing-session-and-global-kernel-address-spaces)
    -   [Zusammengesetzte Fensterverwaltung](#composited-window-management)
-   [GDI-Rendering in Windows 7](#gdi-rendering-in-windows-7)
-   [Gegenüberstellung von Direct2D-und GDI-Beschleunigung in Windows 7](#contrasting-direct2d-and-gdi-acceleration-in-windows-7)
    -   [Speicherort der Ressourcen](#location-of-resources)
    -   [Rendering-Methode](#rendering-method)
    -   [Skalierbarkeit](#scalability)
    -   [Location](#location-of-resources)
    -   [Verfügbarkeit der Hardware Beschleunigung](#availability-of-hardware-acceleration)
    -   [Präsentationsmodell](#presentation-model)
-   [Zusammenfassung](#conclusion)

## <a name="differences-between-direct2d-and-gdi"></a>Unterschiede zwischen Direct2D und GDI

[GDI](/windows/desktop/gdi/windows-gdi) rendert nicht transparente, Alias förmige Geometrien wie Polygone, Ellipsen und Linien. Es rendert Alias-und Klartext-Text und kann Transparenz durch die AlphaBlend-API unterstützen. Die Handhabung der Transparenz ist jedoch inkonsistent, und die meisten GDI-APIs ignorieren einfach den Alphakanal. Einige GDI-APIs garantieren, was der Alphakanal nach einem Vorgang enthält. Noch wichtiger ist, dass das Rendering von GDI nicht einfach zu 3D-Vorgängen führt und eine moderne GPU am effizientesten auf dem 3D-Teil der Rendering-Engine gerendert wird. Beispielsweise sind die Zeilen mit dem Namen " [Direct2D](./direct2d-portal.md)" so konzipiert, dass Sie einfach als zwei Dreiecke auf der GPU gerendert werden, während GDI den Zeilen Zeichnungs Algorithmus Bresenham verwendet.

[Direct2D](./direct2d-portal.md) rendert nicht transparente, transparente, Alias-und Antialiasing-primitive. Moderne Benutzeroberflächen nutzen häufig Transparenz und Animation. Direct2D vereinfacht die Erstellung einer modernen Benutzeroberfläche, da Sie strikte Garantien hinsichtlich der Annahme und Rendern transparenter Inhalte bietet und alle primitiven mithilfe der Hardwarebeschleunigung gerendert werden. Direct2D ist keine reine supermenge von [GDI](/windows/desktop/gdi/windows-gdi): Primitive, die bei der Implementierung auf einer GPU nicht in Direct2D vorhanden wären. Da Direct2D mit diesem Schwerpunkt auf 3D-Beschleunigung erstellt wird, ist es auch einfach mit Direct3D zu verwenden.

Seit Windows NT 4 wurde [GDI](/windows/desktop/gdi/windows-gdi) im Kernel Modus ausgeführt. Die Anwendung ruft GDI auf, die anschließend den kernelmodusgegenpart aufruft, der die primitiven an das eigene Treibermodell übergibt. Anschließend sendet der Treiber die Ergebnisse an den globalen Kernel Modus-Anzeigetreiber.

Ab Windows 2000 wurden [GDI](/windows/desktop/gdi/windows-gdi) -und GDI-Treiber in einem unabhängigen Bereich im Kernel mit dem Namen "Sitzungsraum" ausgeführt. Für jede Anmelde Sitzung wird ein Sitzungs Adressraum erstellt, und jede Instanz von GDI wird unabhängig in diesem eindeutigen kernelmodusbereich ausgeführt. Direct2D wird jedoch im Benutzermodus ausgeführt und übergibt Zeichnungs Befehle über den Benutzermodus Direct3D-Treiber an den Kernelmodustreiber.

![Abbildung 1 Direct2D Vergleich mit GDI](images/direct2d-vs-gdi1.png)

## <a name="gdi-and-direct2d-hardware-acceleration"></a>GDI-und Direct2D-Hardwarebeschleunigung

Der wichtigste Unterschied zwischen der [Direct2D](./direct2d-portal.md) -und der [GDI](/windows/desktop/gdi/windows-gdi) -Hardwarebeschleunigung ist die zugrunde liegende Technologie, die Sie antreibt. Direct2D wird auf oberster Ebene Direct3D und GDI verfügt über ein eigenes Treibermodell, d. h. die GDI-Gerätetreiber Schnittstelle (DDI), die den GDI-primitiven entspricht. Das Direct3D-Treibermodell entspricht dem, was die 3D-renderinghardware in einer GPU rendert. Bei der ersten Definition des GDI-DDI zielten die meisten Hardware zur Anzeige Beschleunigung auf die GDI-primitive. Im Laufe der Zeit wurden mehr und mehr Akzente bei der Beschleunigung von 3D-Spielen und weniger bei der Anwendungsbeschleunigung platziert. Folglich war die BitBlt-API Hardware beschleunigt, und die meisten anderen GDI-Vorgänge waren nicht.

Dadurch wird die Phase für eine Sequenz von Änderungen an der Darstellung von [GDI](/windows/desktop/gdi/windows-gdi) in der Anzeige festgelegt. Die folgende Abbildung zeigt, wie sich das Rendering der GDI-Anzeige von Windows XP zu Windows 7 geändert hat.

![Abbildung 2: Entwicklung von GDI-Anzeige Rendering](images/direct2d-vs-gdi2.png)

Es gab auch eine Reihe zusätzlicher Faktoren, die Änderungen am [GDI](/windows/desktop/gdi/windows-gdi) -Treibermodell, wie unten erläutert, verursacht haben.

### <a name="increasing-complexity-and-size-of-display-drivers"></a>Erhöhen der Komplexität und der Größe von Anzeige Treibern

3D-Treiber sind im Laufe der Zeit komplexer geworden. Komplexere Codes haben tendenziell mehr Fehler, sodass der Treiber im Benutzermodus vorhanden ist, in dem ein Treiber Fehler keinen Systemneustart verursachen kann. Wie in der obigen Abbildung zu sehen ist, ist der Anzeigetreiber in eine komplexe Benutzermoduskomponente und eine einfachere Kernelmoduskomponente unterteilt.

### <a name="difficulty-in-synchronizing-session-and-global-kernel-address-spaces"></a>Schwierigkeiten beim Synchronisieren der Sitzungs-und globalen Kernel Adressräume

In Windows XP ist ein Anzeigetreiber in zwei unterschiedlichen Adressräumen vorhanden: Sitzungs Bereich und Kernel-Speicherplatz. Teile des Treibers müssen auf Ereignisse wie z. b. Energie Verwaltungs Ereignisse reagieren. Dies muss mit dem Treiber Status im Sitzungs Adressbereich synchronisiert werden. Dies ist eine schwierige Aufgabe und kann zu Fehlern führen, wenn Anzeigetreiber versuchen, diese unterschiedlichen Adressräume zu behandeln.

### <a name="composited-window-management"></a>Zusammengesetzte Fensterverwaltung

Der Desktopfenster-Manager (DWM), der in Windows 7 eingeführte zusammengesetzte Fenster-Manager, rendert alle Fenster auf Off-Screen-Oberflächen und fasst diese dann zusammen, damit Sie auf dem Bildschirm angezeigt werden. Dies erfordert, dass [GDI](/windows/desktop/gdi/windows-gdi) in eine Oberfläche gerendert werden kann, die dann von Direct3D zur Anzeige gerendert wird. Dies stellte ein Problem im XP-Treibermodell dar, da GDI und Direct3D parallele Treiber Stapel waren.

Daher wurde in Windows Vista der [GDI](/windows/desktop/gdi/windows-gdi) -DDI-Anzeigetreiber als der von Microsoft bereitgestellte kanonische Anzeigetreiber (CDD) implementiert, der GDI-Inhalt zu einer auf dem Bildschirm zusammen zufügenden systemspeicherbitmap gerendert hat.

## <a name="gdi-rendering-in-windows-7"></a>GDI-Rendering in Windows 7

Das in Windows Vista verwendete Treibermodell erforderte, dass jedes [GDI](/windows/desktop/gdi/windows-gdi) -Fenster sowohl durch eine Grafikspeicher Oberfläche als auch durch eine Systemspeicher Oberfläche gesichert werden muss. Dies führte dazu, dass für jedes GDI-Fenster der System Arbeitsspeicher verwendet wird.

Aus diesem Grund wurde [GDI](/windows/desktop/gdi/windows-gdi) in Windows 7 erneut geändert. . Anstatt auf eine Systemspeicher Oberfläche zu rendern, wurde GDI so geändert, dass es in ein Aperture-Speichersegment gerendert wird. Der Arbeitsspeicher für die Arbeitsauslastung kann von der Videospeicher Oberfläche mit den Fenster Inhalten aktualisiert werden. GDI kann wieder in den Aperture-Arbeitsspeicher gerenbt werden, und das Ergebnis kann dann zurück an die Fenster Oberfläche gesendet werden. Da das Aperture-Speichersegment durch die GPU adressierbar ist, kann die GPU diese Aktualisierungen auf die Videospeicher Oberfläche beschleunigen. Beispielsweise werden Text Rendering, bitblts, AlphaBlend, TransparentBlt und StretchBlt in diesen Fällen beschleunigt.

## <a name="contrasting-direct2d-and-gdi-acceleration-in-windows-7"></a>Gegenüberstellung von Direct2D-und GDI-Beschleunigung in Windows 7

[Direct2D](./direct2d-portal.md) und [GDI](/windows/desktop/gdi/windows-gdi) sind beide 2D-Rendering-APIs im unmittelbaren Modus und sind Hardware beschleunigt. Allerdings gibt es eine Reihe von unterschieden, die in beiden APIs verbleiben.

### <a name="location-of-resources"></a>Speicherort der Ressourcen

[GDI](/windows/desktop/gdi/windows-gdi) behält seine Ressourcen (in bestimmten Bitmaps) standardmäßig im Systemspeicher. [Direct2D](./direct2d-portal.md) verwaltet seine Ressourcen im Videospeicher auf dem Anzeige Adapter. Wenn GDI den Videospeicher aktualisieren muss, muss dies über den Bus erfolgen, es sei denn, die Ressource befindet sich bereits im Aperture-Speichersegment oder, wenn der Vorgang direkt ausgedrückt werden kann. Im Gegensatz dazu kann Direct2D einfach seine primitiven in Direct3D primitive übersetzen, da sich die Ressourcen bereits im Videospeicher befinden.

### <a name="rendering-method"></a>Rendering-Methode

Um die Kompatibilität zu gewährleisten, führt [GDI](/windows/desktop/gdi/windows-gdi) einen großen Teil des Renderings aus, um den Arbeitsspeicher mithilfe der CPU zu blenden. Im Gegensatz dazu übersetzt [Direct2D](./direct2d-portal.md) seine API-Aufrufe in Direct3D Primitives und Zeichnungsvorgänge. Das Ergebnis wird dann auf der GPU gerendert. Einige der GDI? s-Rendering werden auf der GPU ausgeführt, wenn der Aperture-Arbeitsspeicher auf die Grafikspeicher Oberfläche kopiert wird, die das GDI-Fenster darstellt.

### <a name="scalability"></a>Skalierbarkeit

Die renderingaufrufe von [Direct2D](./direct2d-portal.md)sind alle unabhängigen Befehlsdaten Ströme zur GPU. Jede Direct2D Factory stellt ein anderes Direct3D-Gerät dar. [GDI](/windows/desktop/gdi/windows-gdi) verwendet einen Befehlsdaten Strom für alle Anwendungen auf dem System. Die GDI-Methode kann dazu führen, dass der GPU-und CPU-Rendering-Kontext mehr Aufwand entsteht.

### <a name="location"></a>Standort

[Direct2D](./direct2d-portal.md) arbeitet vollständig im Benutzermodus, einschließlich der Direct3D-Laufzeit und des Direct3D-Treibers für den Benutzermodus. Dadurch wird verhindert, dass Systemabstürze durch Code Fehler im Kernel verursacht werden. [GDI](/windows/desktop/gdi/windows-gdi)hat jedoch den größten Teil seiner Funktionalität im Kernel Modus mit der API-Oberfläche im Benutzermodus.

### <a name="availability-of-hardware-acceleration"></a>Verfügbarkeit der Hardware Beschleunigung

[GDI](/windows/desktop/gdi/windows-gdi) ist Hardwarebeschleunigung unter Windows XP und wird unter Windows 7 beschleunigt, wenn die Desktopfenster-Manager ausgeführt wird und ein WDDM 1,1-Treiber verwendet wird. [Direct2D](./direct2d-portal.md) wird auf nahezu jedem WDDM-Treiber Hardware beschleunigt, und zwar unabhängig davon, ob DWM verwendet wird. Bei Vista wird GDI immer auf der CPU-Auslastung angezeigt.

### <a name="presentation-model"></a>Präsentationsmodell

Wenn Windows zum ersten Mal entworfen wurde, gab es nicht genügend Arbeitsspeicher, um zuzulassen, dass jedes Fenster in einer eigenen Bitmap gespeichert wird. Folglich wird [GDI](/windows/desktop/gdi/windows-gdi) immer logisch direkt auf dem Bildschirm gerendert, wobei verschiedene Clippingbereiche angewendet werden, um sicherzustellen, dass eine Anwendung nicht außerhalb des Fensters gerendert wurde. Im [Direct2D](./direct2d-portal.md) -Modell wird eine Anwendung in einen BackBuffer gerendert, und das Ergebnis wird angezeigt, wenn die Anwendung die Zeichnung abgeschlossen hat. Dies ermöglicht es Direct2D, Animations Szenarios weitaus flüssiger als GDI zu verarbeiten.

## <a name="conclusion"></a>Zusammenfassung

Vorhandener [GDI](/windows/desktop/gdi/windows-gdi) -Code funktioniert unter Windows 7 weiterhin gut. Wenn Sie jedoch neuen Grafik Renderingcode schreiben, sollte [Direct2D](./direct2d-portal.md) berücksichtigt werden, da die modernen GPUs besser genutzt werden.

 

 