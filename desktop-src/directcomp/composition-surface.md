---
title: Kompositions Oberfläche
description: In diesem Thema werden die Typen von Oberflächen beschrieben, die von Microsoft directcomposition unterstützt werden.
ms.assetid: E19B4F0E-1CFA-4E93-BB6A-BFB701BC72CA
keywords:
- Kompositions Oberfläche
- Logische directcomposition-Oberfläche
- Virtuelle directcomposition-Oberfläche
- Aktualisieren einer logischen Oberfläche
- logische Oberfläche, aktualisieren
- kürzen einer virtuellen Oberfläche
- virtuelle Oberfläche, kürzen
- virtuelle Oberfläche kürzen
- Ändern der Größe einer virtuellen Oberfläche
- virtuelles Surace, Ändern der Größe
- Ändern der Größe der virtuellen Oberfläche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f4bd30bfbd1de91444b7076184db597cd7a8c82
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039167"
---
# <a name="composition-surface"></a>Kompositions Oberfläche

> [!NOTE]
> Für apps unter Windows 10 wird die Verwendung von Windows. UI. Composition-APIs anstelle von directcomposition empfohlen. Weitere Informationen finden Sie unter [modernisieren ihrer Desktop-App mithilfe der visuellen Ebene](/windows/uwp/composition/visual-layer-in-desktop-apps).

In diesem Thema werden die Typen von Oberflächen beschrieben, die von Microsoft directcomposition unterstützt werden.

-   [Logische directcomposition-Oberfläche](#directcomposition-logical-surface)
    -   [Aktualisieren einer logischen Oberfläche](#updating-a-logical-surface)
    -   [Anhalten von Aktualisierungen auf einer logischen Oberfläche](#suspending-updates-to-a-logical-surface)
    -   [Fortsetzen von Aktualisierungen auf einer logischen Oberfläche](#resuming-updates-to-a-logical-surface)
    -   [Beenden der Aktualisierung einer logischen Oberfläche](#suspending-updates-to-a-logical-surface)
    -   [Beispiel für die Verwendung einer logischen Oberfläche](#example-of-using-a-logical-surface)
-   [Virtuelle directcomposition-Oberfläche](#directcomposition-virtual-surface)
    -   [Ändern der Größe einer virtuellen Oberfläche](#resizing-a-virtual-surface)
    -   [Kürzen einer virtuellen Oberfläche](#trimming-a-virtual-surface)
-   [Zugehörige Themen](#related-topics)

## <a name="directcomposition-logical-surface"></a>Logische directcomposition-Oberfläche

Directcomposition macht das [**idcompositionsurface**](/windows/win32/api/dcomp/nn-dcomp-idcompositionsurface) -Objekt verfügbar, das eine logische Kompositions Oberfläche darstellt. Directcomposition stellt APIs zur Verfügung, mit denen Sie diese logischen Oberflächen erstellen, aktualisieren und löschen können. Jede Oberfläche kann einem oder mehreren visuellen Elementen zugeordnet werden. Eine Anwendung ist für die Verwaltung der Lebensdauer logischer Oberflächen verantwortlich.

### <a name="updating-a-logical-surface"></a>Aktualisieren einer logischen Oberfläche

Eine Anwendung kann eine logische Oberfläche durch Aufrufen von [**beginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) aktualisieren und die Größe und den Offset des Rechtecks auf der logischen Oberfläche angeben, die von der APP aktualisiert werden soll. Directcomposition ordnet ein Rechteck der angegebenen Größe zu und gibt dann die Oberfläche und den entsprechenden Offset zurück, den die Anwendung zeichnen oder aktualisieren muss. Die Begrenzungen des Aktualisierungs Rechtecks werden durch die Oberflächen Größe gebunden. So kann z. b. das Aktualisierungs Rechteck für eine 40-bis-100 Pixel-Oberfläche bis zu (0,0, 40100) sein. Außerdem wird der aktualisierbare Bereich durch ein Wächter Rechteck erzwungen. Da nur jeweils ein Schutz Rechteck vorhanden sein darf, kann jeweils nur eine logische Oberfläche aktualisiert werden. **BeginDraw** gibt einen Fehlercode zurück, wenn " [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) " oder " [**suspenddraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) " nach einem vorherigen Aufruf von " **beginDraw**" nicht aufgerufen wurde. Eine Anwendung kann einen commitaufruf von **beginDraw** zu einem Batch hinzufügen, wird jedoch erst wirksam, wenn **EndDraw** aufgerufen und ein Commit ausgeführt wird.

### <a name="suspending-updates-to-a-logical-surface"></a>Anhalten von Aktualisierungen auf einer logischen Oberfläche

Eine Anwendung, die verschiedene Oberflächen aktualisieren muss, kann [**suspenddraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) für das aktuelle Update aufrufen und dann [**beginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) aufrufen, um ein neues Update zu starten. Microsoft directcomposition ermöglicht mehrere Updates, aber es kann jeweils nur eine aktiv sein. Dies bedeutet, dass Sie **suspenddraw** oder [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) auf einer Oberfläche aufrufen müssen, bevor **beginDraw** im nächsten Aufruf aufgerufen wird. Im Gegensatz zu **EndDraw** kann ein zugesichertes Batch eine Oberfläche enthalten, die sich in einem **suspenddraw** -Zustand befindet. solche Aktualisierungen werden jedoch erst dann auf dem Bildschirm angezeigt, wenn **EndDraw** aufgerufen wird.

### <a name="resuming-updates-to-a-logical-surface"></a>Fortsetzen von Aktualisierungen auf einer logischen Oberfläche

Eine Anwendung kann ein Update auf einer Oberfläche fortsetzen, die sich in einem [**suspenddraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) -Zustand befindet, indem [**resumedraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)aufgerufen wird. Diese Methode kann nur auf einer angehaltenen Oberfläche aufgerufen werden.

### <a name="ending-updates-to-a-logical-surface"></a>Beenden der Aktualisierung einer logischen Oberfläche

Das Aufrufen von " [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) " und " [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) " ist die einzige Möglichkeit, Änderungen der bitmapaktualisierung auf dem Bildschirm anzuzeigen. Jeder Aufrufe von **EndDraw** muss über einen entsprechenden Aufrufen von [**beginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) verfügen, um das Wächter Rechteck zu entfernen. Die logische Oberfläche behält alle Updates bei, bis der **Commit** aufgerufen wird. Sie können **EndDraw** auch auf einer Oberfläche aufrufen, die sich im [**suspenddraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) -Zustand befindet, da **EndDraw** ein implizites fortsetzen/Ende ist. Nachdem Sie **EndDraw** aufgerufen haben, wird der aktualisierte Inhalt auf dem Bildschirm angezeigt und verworfen, damit der Arbeitsspeicher für das Update für ein späteres Update wieder verwendet werden kann.

### <a name="example-of-using-a-logical-surface"></a>Beispiel für die Verwendung einer logischen Oberfläche

Im folgenden Beispiel werden die Schritte beschrieben, die eine Anwendung ausführen würde, wenn Sie eine visuelle Struktur erstellt, die aus zwei visuellen Elementen besteht, und dann benötigt wird, um bestimmte Bereiche der beiden logischen Oberflächen zu aktualisieren, die den visuellen Elementen zugeordnet sind:

1.  Erstellen Sie ein directcomposition-Gerät.
2.  Erstellen Sie die visuelle Struktur, die aus einem Stamm Knoten und den visuellen Elementen 1 und 2 besteht.
3.  Erstellen Sie die logischen Oberflächen 1 und 2.
4.  Aufrufen von [**setContent**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setcontent) zum Zuordnen einer logischen Oberfläche zu den visuellen Elementen 1 und 2.
5.  Aufrufen von [**beginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) für ein unter Rechteck der logischen Oberfläche 1.
6.  Aktualisieren Sie die-Oberfläche am Offset, der von directcomposition zurückgegeben wurde.
7.  Optionale Schritte:
    1.  Aufrufen von [**suspenddraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) auf der logischen Oberfläche 1.
    2.  Aufrufen von [**beginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) für das untergeordnete Rect der logischen Oberfläche 2.
    3.  Aktualisieren Sie die-Oberfläche am Offset, der von directcomposition zurückgegeben wurde.
    4.  Aufrufen von [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) auf der logischen Oberfläche 2.
    5.  Aufrufen von [**resumedraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) auf der logischen Oberfläche 1.
8.  Aktualisieren Sie die-Oberfläche am Offset, der von directcomposition zurückgegeben wurde.
9.  Aufrufen von [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) auf der logischen Oberfläche 1.
10. [**Callcommit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit).

## <a name="directcomposition-virtual-surface"></a>Virtuelle directcomposition-Oberfläche

Directcomposition macht die [**idcompositionvirtualsurface**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvirtualsurface) -Schnittstelle zur Darstellung einer virtuellen Oberfläche verfügbar. dabei handelt es sich um eine Auflistung von logischen Oberflächen (Kacheln), die in einem fixierten Raster mit Kacheln mit fester Größe angeordnet sind Die Anwendung gibt die Größe der virtuellen Textur zum Erstellungs Zeitpunkt an. Die Größe legt die Grenzen für die virtuelle Oberfläche fest. Die-Oberfläche kann einem oder mehreren visuellen Elementen zugeordnet werden.

Wenn eine virtuelle Oberfläche initialisiert wird, wird Sie nicht durch tatsächliche Zuweisungen unterstützt. Dies bedeutet, dass keine Bits enthalten sind. Directcomposition ordnet Kacheln (d. h. Kompositions Oberflächen Objekte) zu, nachdem die Anwendung mit dem Aktualisieren der Oberfläche begonnen hat. Die Anwendung aktualisiert die virtuelle Oberfläche durch Aufrufen von [**beginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) und gibt den relevanten Bereich in Bezug auf die Koordinaten der virtuellen Oberfläche an. Anschließend ordnet directcomposition die erforderlichen Kacheln zum Speichern des Updates zu und gibt die zu Aktualisier Endes Kompositions Oberfläche und den Offset zurück.

Wie bei logischen Oberflächen können Sie " [**beginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)", " [**suspenddraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw)", " [**resumedraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) " und " [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) " auf einer virtuellen Oberfläche aufrufen. Außerdem macht directcomposition Methoden verfügbar, mit denen Sie die Größe einer vorhandenen virtuellen Oberfläche ändern und die Größe der vorhandenen virtuellen Oberfläche reduzieren können.

### <a name="resizing-a-virtual-surface"></a>Ändern der Größe einer virtuellen Oberfläche

Die Methode zum [**ändern**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvirtualsurface-resize) der Größe ändert die Grenzen der virtuellen Oberfläche, d. h., dass alle neuen Updates oder Zuordnungen in den von der neuen Größe festgelegten Grenzen liegen müssen. Eine Anwendung verwendet die **Größenänderung** , um directcomposition mitzuteilen, dass ein bestimmter Bereich der virtuellen Oberfläche nicht mehr benötigt wird und freigegeben werden kann. Wenn die **Größenänderung** die virtuelle Oberfläche verkleinert, kann die Anwendung die Bereiche außerhalb der neuen Grenzen nicht mehr aktualisieren.

In der folgenden Abbildung wird die Größe einer virtuellen Oberfläche von 3 bis 3 in 2 bis 2 geändert. Der Rote Bereich stellt Kacheln dar, die im Rahmen der Größenänderung verworfen werden, und der Arbeitsspeicher wird von directcomposition freigegeben. Nach der Größenänderung kann die Anwendung keine Aktualisierungen an der roten Region vornehmen, ohne die Größe der virtuellen Oberfläche wieder zu ändern.

![Ändern der Größe einer virtuellen Oberfläche ](images/resize-virtual-surface.png)

Der Größenänderung wird sofort wirksam. Directcomposition wartet nicht, bis die Anwendung den [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) aufruft, um die Änderungen an der Größenänderung vorzunehmen. Nehmen Sie z. b. an, eine Anwendung führt die folgende Sequenz von Aufrufen aus.


```
pVirtualSurface->Resize(0, 0);
pVirtualSurface->Resize(INT_MAX, INT_MAX);
pDevice->Commit();
```



In diesem Beispiel verliert die Anwendung bei der ersten Größenänderung den gesamten Inhalt. Die zweite Größenänderung hat keine Auswirkung, obwohl Sie vor dem [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit)aufgerufen wurde. In diesem Fall wird auf dem Bildschirm nichts angezeigt.

### <a name="trimming-a-virtual-surface"></a>Kürzen einer virtuellen Oberfläche

Mit der [**Trim**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvirtualsurface-trim) -Methode wird der Bereich der virtuellen Oberfläche identifiziert, der von der Anwendung benötigt wird. Die Größe der Grenzen der virtuellen Oberfläche wird nicht geändert, aber es wird directcomposition mitgeteilt, welche logischen Oberflächen derzeit zugeordnet werden müssen.

In der folgenden Abbildung ist das grüne Quadrat der Viewport der Anwendung. Die Anwendung wird anfänglich auf die ersten sechs Kacheln (blau) der virtuellen Oberfläche (hellgrau) gerendert, die sich im Viewport befinden. Wenn die Seite, die von der virtuellen Oberfläche dargestellt wird, scrollt, muss die Anwendung die letzten sechs Kacheln Rendering. Die Anwendung ruft [**Trim**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvirtualsurface-trim) auf, um anzugeben, dass der Inhalt der von den letzten sechs Kacheln definierten Region ist, und der Rest wird momentan nicht benötigt. Directcomposition kann dann die logischen Oberflächen wieder verwenden, die ursprünglich die ersten sechs Kacheln dargestellt haben (dunkelgrau).

![kürzen einer virtuellen Oberfläche](images/trim-virtual-surface.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Directcomposition-Konzepte](directcomposition-concepts.md)
</dt> </dl>

 

 