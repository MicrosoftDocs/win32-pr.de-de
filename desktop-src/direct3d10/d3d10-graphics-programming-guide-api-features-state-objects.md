---
description: In Direct3D 10 wird der Gerätestatus in Zustandsobjekte eingekreist, wodurch die Kosten für Zustandsänderungen deutlich reduziert werden.
ms.assetid: b2839da9-60ed-4f6c-9cc7-eac53647cca7
title: Zustandsobjekte (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a51c05e3e220e510c462265941549f91e6368a9
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335424"
---
# <a name="state-objects-direct3d-10"></a>Zustandsobjekte (Direct3D 10)

In Direct3D 10 wird der Gerätestatus in Zustandsobjekte eingekreist, wodurch die Kosten für Zustandsänderungen deutlich reduziert werden. Es gibt mehrere Zustandsobjekte, und jedes ist so konzipiert, dass ein Zustandssatz für eine bestimmte Pipelinephase initialisiert wird. Sie können bis zu 4096 der einzelnen Zustandsobjekttypen erstellen.

-   [Eingabelayoutzustand](#input-layout-state)
-   [Status des Rasterizers](#rasterizer-state)
-   [Tiefen-Schablonenzustand](#depth-stencil-state)
-   [Blend-Zustand](#blend-state)
-   [Samplerzustand](#sampler-state)
-   [Leistungsaspekte](#performance-considerations)
-   [Verwandte Themen](#related-topics)

## <a name="input-layout-state"></a>Input-Layout Status

Diese Zustandsgruppe (siehe [**D3D10 \_ INPUT \_ ELEMENT \_ DESC)**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)bestimmt, wie die [Eingabe-Assembler-Stufe](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) Daten aus den Eingabepuffern liest und für die Verwendung durch den Vertex-Shader zusammenstellen soll. Dies schließt den Zustand ein, z. B. die Anzahl der Elemente im Eingabepuffer und die Signatur der Eingabedaten. Die Eingabe-Assembler-Phase ist eine neue Phase in der Pipeline, deren Aufgabe es ist, Primitive aus dem Arbeitsspeicher in die Pipeline zu streamen.

Informationen zum Erstellen eines Eingabelayout-Zustandsobjekts finden Sie unter [**CreateInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).

## <a name="rasterizer-state"></a>Status des Rasterizers

Diese Zustandsgruppe (siehe [**D3D10 \_ RASTERIZER \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)) initialisiert die [Rasterizerphase](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md). Dieses Objekt umfasst den Zustand, z. B. den Füll- oder CULL-Modus, das Aktivieren eines Scissor-Rechtecks zum Ausschneiden und das Festlegen von Multisampleparametern. Diese Phase rastert Primitive in Pixel und führt Vorgänge wie Clipping und Zuordnen von Primitiven zum Viewport durch.

Informationen zum Erstellen eines rasterizer-state-Objekts finden Sie unter [**CreateRasterizerState.**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createrasterizerstate)

## <a name="depth-stencil-state"></a>Depth-Stencil Status

Diese Statusgruppe (siehe [**D3D10 \_ DEPTH \_ STENCIL \_ DESC)**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)initialisiert den Teil der Tiefenschablone der [Ausgabezusammenführungsphase.](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) Genauer gesagt initialisiert dieses Objekt Tiefen- und Schablonentests.

Informationen zum Erstellen eines Tiefenschablonenzustandsobjekts finden Sie unter [**CreateDepthStencilState.**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createdepthstencilstate)

## <a name="blend-state"></a>Blendzustand

Diese Statusgruppe (siehe [**D3D10 \_ BLEND \_ DESC)**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)initialisiert den Mischungsteil der [Ausgabezusammenführungsphase](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md).

Informationen zum Erstellen eines Blend-State-Objekts finden Sie unter [**CreateBlendState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createblendstate).

## <a name="sampler-state"></a>Samplerstatus

Diese Statusgruppe (siehe [**D3D10 \_ SAMPLER \_ DESC)**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)initialisiert ein Samplerobjekt. Ein Samplerobjekt wird von den Shaderstufen verwendet, um Texturen im Arbeitsspeicher zu filtern.



Unterschiede zwischen Direct3D 9 und Direct3D 10:

- In Direct3D 10 ist das Samplerobjekt nicht mehr an eine bestimmte Textur gebunden. Es wird lediglich beschrieben, wie die Filterung bei einer angefügten Ressource durchgeführt wird.



 

Informationen zum Erstellen eines sampler-state-Objekts finden Sie unter [**CreateSamplerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createsamplerstate).

## <a name="performance-considerations"></a>Überlegungen zur Leistung

Das Entwerfen der API für die Verwendung von Zustandsobjekten bietet mehrere Leistungsvorteile. Dazu gehören das Überprüfen des Zustands zum Zeitpunkt der Objekterstellung, das Aktivieren der Zwischenspeicherung von Zustandsobjekten in der Hardware und die erhebliche Verringerung des Zustands, der während eines ZUSTANDSeinstellungs-API-Aufrufs übergeben wird (durch Übergeben eines Handles an das Zustandsobjekt anstelle des Zustands).

Um diese Leistungsverbesserungen zu erzielen, sollten Sie Ihre Zustandsobjekte erstellen, wenn die Anwendung gestartet wird, und zwar weit vor der Renderschleife. Zustandsobjekte sind unveränderlich, d. h., nachdem sie erstellt wurden, können Sie sie nicht mehr ändern. Stattdessen müssen Sie sie zerstören und neu erstellen. Um diese Einschränkung zu bewältigen, können Sie bis zu 4096 von jedem Typ von Zustandsobjekten erstellen. Beispielsweise können Sie mehrere Samplerobjekte mit verschiedenen Samplerzustandskombinationen erstellen. Das Ändern des Samplerzustands wird dann durch Aufrufen der entsprechenden Set-API erreicht, die ein Handle an das Objekt übergibt (im Gegensatz zum Samplerzustand). Dadurch wird der Mehraufwand während jedes Renderframes zum Ändern des Zustands erheblich reduziert, da die Anzahl der Aufrufe und die Datenmenge erheblich reduziert werden.

Alternativ können Sie das Effektsystem verwenden, das automatisch die effiziente Erstellung und Zerstörung von Zustandsobjekten für Ihre Anwendung verwaltet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[API-Features (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 
