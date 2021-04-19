---
description: In Direct3D 10 wird der Gerätestatus in Zustands Objekte gruppiert, wodurch die Kosten für Zustandsänderungen erheblich reduziert werden.
ms.assetid: b2839da9-60ed-4f6c-9cc7-eac53647cca7
title: Zustands Objekte (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a06e8603361a83049440774cfd2e12b4148b183
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342751"
---
# <a name="state-objects-direct3d-10"></a>Zustands Objekte (Direct3D 10)

In Direct3D 10 wird der Gerätestatus in Zustands Objekte gruppiert, wodurch die Kosten für Zustandsänderungen erheblich reduziert werden. Es gibt mehrere State-Objekte, die jeweils zum Initialisieren eines Zustands Satzes für eine bestimmte Pipeline Phase entwickelt wurden. Sie können bis zu 4096 für jeden Typ von Zustands Objekt erstellen.

-   [Eingabe-Layoutstatus](#input-layout-state)
-   [Status des Rasterizers](#rasterizer-state)
-   [Status der tiefen Schablone](#depth-stencil-state)
-   [Blend-Status](#blend-state)
-   [Samplerstatus](#sampler-state)
-   [Leistungsaspekte](#performance-considerations)
-   [Zugehörige Themen](#related-topics)

## <a name="input-layout-state"></a>Input-Layout Status

Diese Gruppe von Status (siehe [**d3d10 \_ input \_ Element \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)Debug) bestimmt, wie die [Eingabe-Assembler-Phase](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) Daten aus den Eingabe Puffern ausliest und für die Verwendung durch den Vertexshader assembliert. Dies schließt den Zustand ein, z. b. die Anzahl der Elemente im Eingabepuffer und die Signatur der Eingabedaten. Bei der Eingabe-Assembler-Phase handelt es sich um eine neue Phase in der Pipeline, deren Aufgabe das Streamen primitiver Daten aus dem Arbeitsspeicher in die Pipeline ist.

Informationen zum Erstellen eines Input-Layout-State-Objekts finden Sie unter " [**kreateinputlayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout)".

## <a name="rasterizer-state"></a>Status des Rasterizers

Diese Gruppe von Status (siehe [**d3d10 \_ Raster \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)Debug) initialisiert die [Raster-Stufe](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md). Dieses Objekt enthält einen Zustand, wie z. b. Fill-oder auslesen-Modi, das Aktivieren eines Scheren Rechtecks für das Clipping und das Festlegen von Multisampling In dieser Phase werden primitive in Pixel gerengt, die Vorgänge wie das Abschneiden und die Zuordnung von primitiven zum Viewport ausführen.

Informationen zum Erstellen eines Rasterizer-State-Objekts finden Sie unter " [**kreaterasterizerstate**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createrasterizerstate)".

## <a name="depth-stencil-state"></a>Depth-Stencil Status

Diese Gruppe von Status (siehe [**d3d10 \_ tiefen \_ Schablone \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)) initialisiert den tiefen Schablone-Teil der [Ausgabe-Fusion-Phase](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md). Genauer gesagt, initialisiert dieses Objekt Tiefe und Schablonen Tests.

Informationen zum Erstellen eines tiefen Schablone-Status Objekts finden Sie unter " [**kreatedepthstencilstate**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createdepthstencilstate)".

## <a name="blend-state"></a>Blend-Status

Diese Gruppe von Status (siehe [**d3d10 \_ Blend \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)) initialisiert den Mischungs Teil der [Ausgabe-Fusion-Phase](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md).

Informationen zum Erstellen eines Blend-State-Objekts finden Sie unter " [**kreateblendstate**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createblendstate)".

## <a name="sampler-state"></a>Samplerstatus

Diese Gruppe von Status (siehe [**d3d10 \_ Sampler \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)Debug) Initialisiert ein samplerobjekt. Ein samplerobjekt wird von den Shader-Stufen zum Filtern von Texturen im Speicher verwendet.



|                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterschiede zwischen Direct3D 9 und Direct3D 10:<br/> In Direct3D 10 ist das samplerobjekt nicht mehr an eine bestimmte Textur gebunden. es wird lediglich beschrieben, wie das Filtern bei einer beliebigen angefügten Ressource durchzuführen ist. |



 

Informationen zum Erstellen eines samplerstatusobjekts finden Sie unter " [**kreatesamplerstate**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createsamplerstate)".

## <a name="performance-considerations"></a>Überlegungen zur Leistung

Das Entwerfen der API für die Verwendung von Zustands Objekten führt zu mehreren Leistungsvorteilen. Dazu gehört das Überprüfen des Zustands zum Zeitpunkt der Objekt Erstellung, das Aktivieren des zwischen Speicherns von Zustands Objekten in der Hardware und das deutlich reduzieren des Zustands, der während eines Zustands Einstellungs-API-Aufrufes übergeben wird (durch Übergabe eines Handles an das Zustands Objekt anstelle des-Zustands).

Um diese Leistungsverbesserungen zu erzielen, sollten Sie Ihre Zustands Objekte erstellen, wenn Ihre Anwendung gestartet wird, und zwar vor der Renderschleife. Zustands Objekte sind unveränderlich, d. h., nachdem Sie erstellt wurden, können Sie Sie nicht mehr ändern. Stattdessen müssen Sie Sie löschen und neu erstellen. Um diese Einschränkung zu umgehen, können Sie bis zu 4096 für jeden Typ von Zustands Objekten erstellen. Beispielsweise können Sie mehrere samplerobjekte mit unterschiedlichen samplerstatuskombinationen erstellen. Die Änderung des samplerstatus wird dann durch Aufrufen der entsprechenden Set-API durchgeführt, die ein Handle an das Objekt übergibt (im Gegensatz zum samplerzustand). Dadurch wird der Aufwand für jeden Rendering-Frame erheblich reduziert, um den Status zu ändern, da die Anzahl der Aufrufe und die Datenmenge erheblich reduziert wird.

Wahlweise können Sie auch das Effektsystem verwenden, das die effiziente Erstellung und Zerstörung von Zustands Objekten für die Anwendung automatisch verwaltet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[API-Features (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 
