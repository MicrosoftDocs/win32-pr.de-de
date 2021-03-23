---
title: Direct3D 12-Interop
description: D3D12 kann zum Schreiben von Anwendungen verwendet werden, die in Komponenten integriert sind.
ms.assetid: 51F7E715-82B6-48D8-A06A-CBBEDF6968F5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b5fcfe2adf756c12f034031675d0c3ac5571b44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548748"
---
# <a name="direct3d-12-interop"></a>Direct3D 12-Interop

D3D12 kann zum Schreiben von Anwendungen verwendet werden, die in Komponenten integriert sind.

-   [Interop-Übersicht](#interop-overview)
-   [Gründe für die Verwendung von Interop](#reasons-for-using-interop)
    -   [Freigeben einer Befehlsliste](#sharing-a-command-list)
    -   [Freigeben einer Befehls Warteschlange](#sharing-a-command-queue)
    -   [Freigabe von Synchronisierungs primitiven](#sharing-sync-primitives)
    -   [Gemeinsame Nutzung von Ressourcen](#sharing-resources)
    -   [Auswählen eines Interop-Modells](#choosing-an-interop-model)
-   [Interop-APIs](#interop-apis)
-   [Verwandte Themen](#related-topics)

## <a name="interop-overview"></a>Interop-Übersicht

D3D12 kann sehr leistungsstark sein und es Anwendungen ermöglichen, Grafik Code mit Konsolen ähnlicher Effizienz zu schreiben, aber nicht jede Anwendung muss das Rad neu erfinden und die gesamte Rendering-Engine von Grund auf neu schreiben. In einigen Fällen ist dies bereits durch eine andere Komponente oder Bibliothek besser, oder in anderen Fällen ist die Leistung eines Teils des Codes nicht so wichtig wie die Richtigkeit und Lesbarkeit.

In diesem Abschnitt werden die folgenden Interop-Techniken behandelt:

-   D3D12 und D3D12 auf demselben Gerät
-   D3D12 und D3D12 auf unterschiedlichen Geräten
-   D3D12 und eine beliebige Kombination aus D3D11, d3d10 oder D2D auf demselben Gerät
-   D3D12 und eine beliebige Kombination aus D3D11, d3d10 oder D2D auf unterschiedlichen Geräten
-   D3D12 und GDI, D3D12 und D3D11 und GDI

## <a name="reasons-for-using-interop"></a>Gründe für die Verwendung von Interop

Es gibt mehrere Gründe, warum eine Anwendung eine D3D12-Interop mit anderen APIs wünschen. Einige Beispiele:

-   Inkrementelles portieren: Es wird eine gesamte Anwendung von d3d10 oder D3D11 auf D3D12 portiert, während Sie in den zwischen Phasen des Portierungs Prozesses funktioniert (um das Testen und Debuggen zu ermöglichen).
-   Black Box-Code: möchten Sie einen bestimmten Teil einer Anwendung unverändert lassen, während Sie den Rest des Codes portieren. Beispielsweise ist es möglicherweise nicht erforderlich, Benutzeroberflächen Elemente eines Spiels zu portieren.
-   Nicht änderbare Komponenten: Sie müssen Komponenten verwenden, die nicht im Besitz der Anwendung sind, die nicht in das Ziel D3D12 geschrieben sind.
-   Eine neue Komponente: Es ist nicht gewünscht, dass Sie die gesamte Anwendung portieren, sondern eine neue Komponente verwenden möchten, die mit D3D12 geschrieben wird.

Es gibt vier Haupttechniken für Interop in D3D12:

-   Eine APP kann eine geöffnete Befehlsliste für eine Komponente bereitstellen, die einige zusätzliche renderingbefehle für ein bereits gebundenes Renderziel aufzeichnet. Dies entspricht dem Bereitstellen eines vorbereiteten Geräte Kontexts für eine andere Komponente in D3D11 und eignet sich hervorragend für Elemente wie das Hinzufügen von Benutzeroberflächen und Text zu einem bereits gebundenen Hintergrund Puffer.
-   Eine APP kann eine Befehls Warteschlange sowie eine gewünschte Ziel Ressource für eine Komponente bereitstellen. Dies entspricht der Verwendung von [**clearstate**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-clearstate) -oder [**devicecontextstate**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate) -APIs in D3D11, um einen sauberen Gerätekontext für eine andere Komponente bereitzustellen. So funktionieren Komponenten wie D2D.
-   Eine Komponente kann sich für ein Modell entscheiden, in dem Sie eine Befehlsliste generiert (möglicherweise parallel), für die die APP zu einem späteren Zeitpunkt für die Übermittlung verantwortlich ist. Mindestens eine Ressource muss über Komponenten Grenzen hinweg bereitgestellt werden. Dieselbe Technik ist in D3D11 mithilfe von verzögerten Kontexten verfügbar, obwohl die Leistung in D3D12 wünschenswert ist.
-   Jede Komponente verfügt über eigene Warteschlangen und/oder Geräte, und die APP und die Komponenten müssen Ressourcen und Synchronisierungs Informationen über Komponenten Grenzen hinweg freigeben. Dies ähnelt der Legacy-Version `ISurfaceQueue` und der moderneren [**idxgikeyedmutex**](/windows/desktop/api/dxgi/nn-dxgi-idxgikeyedmutex).

Die Unterschiede zwischen diesen Szenarien bestehen darin, was genau zwischen den Komponenten Begrenzungen gemeinsam genutzt wird. Es wird davon ausgegangen, dass das Gerät freigegeben ist, aber da es grundsätzlich Zustands loser ist, ist es nicht wirklich relevant. Die Schlüssel Objekte sind die Befehlsliste, die Befehls Warteschlange, die Synchronisierungs Objekte und die Ressourcen. Jeder dieser Komponenten hat bei der Freigabe seine eigenen Komplikationen.

### <a name="sharing-a-command-list"></a>Freigeben einer Befehlsliste

Die einfachste Interop-Methode erfordert die gemeinsame Nutzung einer Befehlsliste mit einem Teil der-Engine. Nachdem die Renderingvorgänge abgeschlossen sind, wird der Besitz der Befehlsliste an den Aufrufer zurückgeleitet. Der Besitz der Befehlsliste kann durch den Stapel verfolgt werden. Da es sich bei den Befehlslisten um Single Thread handelt, gibt es keine Möglichkeit für eine APP, mit dieser Technik etwas eindeutiges oder innovatives zu machen.

### <a name="sharing-a-command-queue"></a>Freigeben einer Befehls Warteschlange

Wahrscheinlich das gängigste Verfahren für mehrere Komponenten, die ein Gerät im selben Prozess gemeinsam nutzen.

Wenn die Befehls Warteschlange die Freigabe Einheit ist, muss die-Komponente aufgerufen werden, um Sie zu informieren, dass alle ausstehenden Befehlslisten sofort an die Befehls Warteschlange gesendet werden müssen (und alle internen Befehls Warteschlangen synchronisiert werden müssen). Dies entspricht der D3D11 [**Flush**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-flush) -API und ist die einzige Möglichkeit, dass die Anwendung ihre eigenen Befehlslisten oder Synchronisierungs primitiven übermitteln kann.

### <a name="sharing-sync-primitives"></a>Freigabe von Synchronisierungs primitiven

Das erwartete Muster für eine Komponente, die auf Ihren eigenen Geräten und/oder Befehls Warteschlangen arbeitet, besteht darin, ein [**ID3D12Fence**](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence) -oder Shared-Handle zu akzeptieren, und UINT64 Pair nach Beginn der Arbeit, auf die gewartet wird, und dann ein zweites ID3D12Fence-oder Shared-handle, und UINT64-Paar, das signalisiert, wenn alle arbeiten vollständig ausgeführt werden. Dieses Muster entspricht der aktuellen Implementierung von [**idxgikeyedmutex**](/windows/desktop/api/dxgi/nn-dxgi-idxgikeyedmutex) und dem Entwurf der DWM/DXGI-Flip-Modell Synchronisierung.

### <a name="sharing-resources"></a>Gemeinsame Nutzung von Ressourcen

Der komplizierteste Teil beim Schreiben einer D3D12-APP, die mehrere Komponenten nutzt, ist die Vorgehensweise beim Umgang mit den Ressourcen, die über Komponenten Grenzen hinweg gemeinsam genutzt werden. Dies ist größtenteils auf das Konzept von Ressourcen Zuständen zurückzuführen. Während einige Aspekte des Ressourcen Status Entwurfs mit der Synchronisierung der internen Befehlsliste zu tun sind, haben andere Auswirkungen auf die Befehlslisten, die sich auf das Ressourcen Layout und entweder auf gültige Vorgänge oder Leistungsmerkmale beim Zugriff auf die Ressourcen Daten auswirken.

Es gibt zwei Muster für den Umgang mit dieser Komplikation, die beide im Grunde einen Vertrag zwischen Komponenten einschließen.

-   Der Vertrag kann vom Komponenten Entwickler definiert und dokumentiert werden. Dies könnte so einfach sein: "die Ressource muss sich im Standardzustand befinden, wenn die Arbeit gestartet wird, und wird in den Standardzustand zurückversetzt, wenn die Arbeit erledigt ist", oder es können kompliziertere Regeln vorhanden sein, die das Freigeben eines tiefen Puffers ermöglichen, ohne dass zwischen Tiefe aufgelöst wird.
-   Der Vertrag kann von der Anwendung zur Laufzeit definiert werden, zu dem Zeitpunkt, zu dem die Ressource über Komponenten Grenzen hinweg freigegeben wird. Sie besteht aus denselben zwei Informationen – dem Zustand, in dem sich die Ressource befindet, wenn Sie von der Komponente verwendet wird, und dem Zustand, in dem die Komponente Sie beim Beenden belassen soll.

### <a name="choosing-an-interop-model"></a>Auswählen eines Interop-Modells

Bei den meisten D3D12-Anwendungen ist die Freigabe einer Befehls Warteschlange wahrscheinlich das ideale Modell. Sie ermöglicht den kompletten Besitz der Erstellung und Übermittlung von Arbeitsaufgaben, ohne dass der zusätzliche Arbeitsspeicher über redundante Warteschlangen liegt, und ohne dass die Auswirkungen des Umgangs mit den GPU-Synchronisierungs primitiven beeinträchtigt werden.

Die Freigabe von Synchronisierungs primitiven ist erforderlich, wenn die Komponenten mit unterschiedlichen Warteschlangen Eigenschaften, z. b. Typ oder Priorität, umgehen müssen, oder wenn die Freigabe die Prozess Grenzen überspannen muss.

Das Freigeben oder Generieren von Befehlslisten wird nicht weitgehend extern von Komponenten von Drittanbietern verwendet, kann jedoch häufig in Komponenten verwendet werden, die für eine Spiel-Engine intern sind.

## <a name="interop-apis"></a>Interop-APIs

Das Thema [Direct3D 11 on 12](./direct3d-11-on-12.md) führt Sie durch die Verwendung eines Großteil der API-Oberfläche, die sich auf die in diesem Thema beschriebenen Arten von Interoperation bezieht.

Weitere Informationen finden Sie auch in der [ID3D12Device:: kreatesharedhandle](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle) -Methode, die Sie zum Freigeben von Oberflächen zwischen Windows-Grafik-APIs verwenden können.

## <a name="related-topics"></a>Verwandte Themen

* [Grundlegendes zu Direct3D 12](directx-12-getting-started.md)
* [Arbeiten mit Direct3D 11, Direct3D 10 und Direct2D](direct3d-12-interop.md)
* [Direct3D 11 on 12](./direct3d-11-on-12.md)