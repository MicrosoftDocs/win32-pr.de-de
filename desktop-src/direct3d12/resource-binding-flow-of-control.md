---
title: Übersicht über Ressourcen Bindungen
description: Der Schlüssel zur Ressourcen Bindung in DirectX 12 besteht aus den Konzepten eines Deskriptors, deskriptortabellen, deskriptorheaps und einer Stamm Signatur.
ms.assetid: 92E100CA-822D-46B1-BD37-FF57C3FB703D
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bc7e78255c123777716eddb43d9443e19113b34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103806"
---
# <a name="resource-binding-overview"></a>Übersicht über Ressourcen Bindungen

Der Schlüssel zur Ressourcen Bindung in DirectX 12 besteht aus den Konzepten eines *Deskriptors*, *deskriptortabellen*, *deskriptorheaps* und einer Stamm *Signatur*.

-   [Ressourcen und die Grafik Pipeline](#resources-and-the-graphics-pipeline)
-   [Ressourcentypen und-Sichten](#resource-types-and-views)
-   [Steuerungs Fluss der Ressourcen Bindung](#resource-binding-overview)
-   [Unter Zuordnung](#suballocation)
-   [Freigeben von Ressourcen](#freeing-resources)
-   [Verwandte Themen](#related-topics)

## <a name="resources-and-the-graphics-pipeline"></a>Ressourcen und die Grafik Pipeline

Shader-Ressourcen (z. b. Texturen, Konstante Tabellen, Bilder, Puffer usw.) sind nicht direkt an die shaderpipeline gebunden. Stattdessen wird auf Sie über einen *Deskriptor* verwiesen. Ein Deskriptor ist ein kleines Objekt, das Informationen zu einer Ressource enthält.

Deskriptoren werden gruppiert, um *deskriptortabellen* zu bilden. Jede Deskriptortabelle speichert Informationen zu einem Bereich von Ressourcentypen. Es gibt viele verschiedene Arten von Ressourcen. Die häufigsten Ressourcen sind:

-   Konstantenpuffersichten (cbvs)
-   Ungeordnete Zugriffs Sichten (UAVs)
-   Shader-Ressourcen Sichten (Srvs)
-   Sampler

SRV-, UAV-und cbvs-Deskriptoren können in derselben Deskriptortabelle kombiniert werden.

Die Grafiken und Compute-Pipelines erhalten Zugriff auf Ressourcen, indem Sie über den Index auf deskriptortabellen verweisen.

Deskriptortabellen werden in einem *deskriptorheap* gespeichert. Deskriptorheaps enthalten im Idealfall alle Deskriptoren (in deskriptortabellen) für einen oder mehrere Frames, die gerendert werden sollen. Alle Ressourcen werden im benutzermodusheaps gespeichert.

Ein anderes Konzept ist die einer Stamm *Signatur*. Bei der Stamm Signatur handelt es sich um eine von der Anwendung definierte Bindungs Konvention, die von Shadern verwendet wird, um die Ressourcen zu finden, auf die Sie Zugriff benötigen. Die Stamm Signatur kann Folgendes speichern:

-   Indizes für deskriptortabellen in einem deskriptorheap, bei dem das Layout der Deskriptortabelle vordefiniert wurde.
-   Konstanten, sodass apps benutzerdefinierte Konstanten (als Stamm *Konstanten* bezeichnet) direkt an Shader binden können, ohne Deskriptoren und deskriptortabellen durchlaufen zu müssen.
-   Eine sehr kleine Anzahl von Deskriptoren, die sich direkt innerhalb der Stamm Signatur befinden, wie z. b. eine Konstante Puffer Ansicht (CBV), die pro zeichnen geändert wird, sodass die Anwendung nicht mehr in den deskriptorheap eingefügt werden muss.

Mit anderen Worten: die Stamm Signatur bietet Leistungsoptimierungen, die für kleine Datenmengen geeignet sind, die pro zeichnen geändert werden.

Der Direct3D 12-Entwurf für die Bindung trennt ihn von anderen Tasks, wie z. b. Speicherverwaltung, Verwaltung von Objekt Lebensdauer, Zustands Verfolgung und Speicher Synchronisierung (siehe [Unterschiede im Bindungs Modell von Direct3D 11](binding-model.md)). Die Direct3D 12-Bindung ist so konzipiert, dass der Aufwand gering ist und für die am häufigsten vorgenommenen API-Aufrufe optimiert wird. Es ist auch für die Skalierung durch Low-End-to-High-End-Hardware und die Skalierbarkeit von älteren (der linearen Direct3D 11-Pipeline) bis hin zu neueren (allgemeineren) Ansätzen der Grafik-Engine-Programmierung.

## <a name="resource-types-and-views"></a>Ressourcentypen und-Sichten

Die Ressourcentypen sind identisch mit Direct3D 11, nämlich:

-   Texture1D und Texture1DArray
-   Texture2D und Texture2DArray, Texture2DMS, Texture2DMSArray
-   Texture3D
-   Puffer (typisiert, strukturiert und unformatiert)

Ressourcen Sichten sind ähnlich, unterscheiden sich jedoch geringfügig von Direct3D 11, Vertex-und Index Puffer Sichten wurden hinzugefügt.

-   Konstantenpufferansicht (CBV)
-   Unsortierter Zugriffs Ansicht (UAV)
-   Shader-Ressourcen Ansicht (SRV)
-   Sampler
-   Renderzielansicht (RTV)
-   Ansicht der tiefen Schablone (DSV)
-   Index Puffer Ansicht (IBV)
-   Vertex-Puffer Ansicht (VBV)
-   Stream-Ausgabe Ansicht (SOV)

Nur die ersten vier dieser Sichten sind für Shader tatsächlich sichtbar. Weitere Informationen finden Sie unter [Shader Visible Descriptor Heaps](shader-visible-descriptor-heaps.md) und [Non Shader Visible Descriptor Heaps](non-shader-visible-descriptor-heaps.md).

## <a name="resource-binding-flow-of-control"></a>Steuerungs Fluss der Ressourcen Bindung

Wenn Sie sich nur auf Stamm Signaturen, Stamm Deskriptoren, Stamm Konstanten, deskriptortabellen und deskriptorheaps konzentrieren, sollte der Ablauf der Renderinglogik für eine app in etwa wie folgt aussehen:

-   Erstellen Sie mindestens ein Stamm Signatur Objekt – eines für jede unterschiedliche Bindungs Konfiguration, die eine Anwendung benötigt.
-   Erstellen Sie Shader und den Pipeline Zustand mit den Stamm Signatur Objekten, mit denen Sie verwendet werden.
-   Erstellen Sie eine (oder ggf. weitere) deskriptorheaps, die alle SRV-, UAV-und CBV-Deskriptoren für jeden Rendering-Frame enthalten.
-   Initialisieren Sie den deskriptorheap (s) mit Deskriptoren, sofern möglich, für Gruppen von Deskriptoren, die in vielen Frames wieder verwendet werden.
-   Für jeden Frame, der gerendert werden soll:
    -   Für jede Befehlsliste:
        -   Legen Sie die aktuelle Stamm Signatur für die Verwendung fest (und ändern Sie Sie bei Bedarf während des Renderings – Dies ist nur selten erforderlich)
        -   Aktualisieren Sie die Konstanten und/oder Stamm Signatur Deskriptoren einiger Stamm Signaturen für die neue Sicht (z. b. Welt-/sichtenprojektionen).
        -   Für jedes zu zeichnende Element:
            -   Definieren Sie alle neuen Deskriptoren in den deskriptorheaps, die für das Objekt übergreifende Rendering benötigt werden. Für Shader-sichtbare deskriptorheaps muss die APP sicherstellen, dass der deskriptorheap-Speicherplatz verwendet wird, auf den nicht bereits durch das Rendering verwiesen wird, das möglicherweise aktiv ist, z. –. das lineare Zuordnen von Speicherplatz über den deskriptorheap beim Rendern.
            -   Aktualisieren Sie die Stamm Signatur mit Zeigern auf die erforderlichen Bereiche der deskriptorheaps. Beispielsweise kann eine Deskriptortabelle auf einige statische (unveränderliche) Deskriptoren verweisen, die zuvor initialisiert wurden, während eine andere Deskriptortabelle auf einige dynamische Deskriptoren verweist, die für das aktuelle Rendering konfiguriert sind.
            -   Aktualisieren Sie die Konstanten und/oder Stamm Signatur Deskriptoren der Stamm Signatur für das Rendering pro Element.
            -   Legt den Pipeline Zustand für das zu zeichnende Element fest (nur, wenn die Änderung erforderlich ist), kompatibel mit der zurzeit gebundenen Stamm Signatur.
            -   Draw
        -   Wiederholen (Nächstes Element)
    -   Wiederholen (nächste Befehlsliste)
    -   Wenn die GPU nicht mehr verwendet werden kann, kann Sie vollständig freigegeben werden. Verweise auf die Deskriptoren müssen nicht gelöscht werden, wenn zusätzliches Rendering, das diese Deskriptoren verwendet, nicht übermittelt wird. Folglich kann das nachfolgende Rendering auf andere Bereiche in deskriptorheaps verweisen, oder veraltete Deskriptoren können mit gültigen Deskriptoren überschrieben werden, um den deskriptorheap-Speicherplatz wiederzuverwenden.
-   Wiederholen (Nächster Frame)

Beachten Sie, dass andere deskriptortypen, renderzielsichten (rtvs), tiefen Schablonen Sichten (DSV), Index Puffer Sichten (ibvs), Vertex-Puffer Sichten (vbvs) und Shader-Objekt Sichten (SOV) anders verwaltet werden. Der Treiber verarbeitet die Versionsverwaltung des Satzes von Deskriptoren, die während der Aufzeichnung der Befehlsliste für jedes zeichnen gebunden sind (ähnlich wie bei der Versionsverwaltung der Stamm Signatur Bindungen durch Hardware/Treiber). Dies unterscheidet sich vom Inhalt von Shader-Visible-deskriptorheaps, die die Anwendung manuell über den Heap zuordnen muss, da Sie auf verschiedene Deskriptoren zwischen den Zeichnungen verweist. Die Versionsverwaltung von Heap Inhalten, die Shader-sichtbar sind, wird der Anwendung überlassen, da Sie Anwendungen die Möglichkeit bietet, Deskriptoren wiederzuverwenden, die nicht geändert werden, oder große statische Sätze von Deskriptoren zu verwenden und die Shader-Indizierung (z. b. nach Material-ID) zu verwenden, um Deskriptoren für verschiedene deskriptorheap auszuwählen. Die Hardware ist nicht zum Verarbeiten dieser Art von Flexibilität für die anderen deskriptortypen (RTV, DSV, IBV, VBV, SOV) gerüstet.

## <a name="suballocation"></a>Unter Zuordnung

In Direct3D 12 verfügt die APP über eine Low-Level-Kontrolle über die Speicherverwaltung. In früheren Versionen von Direct3D, einschließlich Direct3D 11, gibt es eine Zuordnung pro Ressource. In Direct3D 12 kann die APP die API verwenden, um einen großen Speicherblock zuzuordnen, der größer ist als ein beliebiges einzelnes Objekt, das benötigt wird. Nachdem dies geschehen ist, kann die APP Deskriptoren erstellen, um auf Abschnitte dieses großen Speicherblocks zu verweisen. Dieser Prozess der Entscheidung, wo (kleinere Blöcke innerhalb des großen Blocks) eingefügt werden sollen, wird als *unter Zuordnung* bezeichnet. Das Aktivieren der APP zu diesem Zweck kann bei der effizienten Nutzung von Berechnung und Arbeitsspeicher zu Vorteilen führen. Beispielsweise wird das Umbenennen von Ressourcen als veraltet gerendert. Dabei können Apps mithilfe von Zäunen feststellen, wann eine bestimmte Ressource verwendet wird, und wann nicht durch das umzäunen von Befehlslisten Ausführungen, bei denen die Befehlsliste die Verwendung dieser bestimmten Ressource erfordert.

## <a name="freeing-resources"></a>Freigeben von Ressourcen

Bevor der an die Pipeline gebundene Speicher freigegeben werden kann, muss die GPU mit der GPU fertiggestellt werden.

Das warten auf das Frame Rendering ist wahrscheinlich die koarst-Methode, um sicherzustellen, dass die GPU abgeschlossen ist. Mit einer feineren Granularität können Sie wieder Zäune verwenden – wenn ein Befehl in einer Befehlsliste aufgezeichnet wird, für die der Abschluss von nachverfolgt werden soll, fügen Sie direkt darauf einen Fence ein. Anschließend können Sie mit dem Fence verschiedene Synchronisierungs Vorgänge durchführen. Sie übermitteln neue Arbeit (Befehlslisten), die wartet, bis ein angegebener Fence an die GPU übergeben wurde. Dies deutet darauf hin, dass alles vor Abschluss ist, oder Sie können anfordern, dass ein CPU-Ereignis ausgelöst wird, wenn der Fence abgelaufen ist (was die APP auf einen inaktiven Thread warten kann). In Direct3D 11 lautete dies `EnqueueSetEvent` ().

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Ressourcen Bindung](resource-binding.md)
</dt> </dl>

 

 




