---
title: Unterressourcen (Direct3D 12-Grafiken)
description: Beschreibt, wie eine Ressource in Unterressourcen unterteilt wird und wie auf eine einzelne, mehrere oder einen Slice von Unterressourcen verwiesen wird.
ms.assetid: C4F92F8A-DBF0-412B-8707-CC4C1BF2D88F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2fc4478e71bbafb8a21897f838ee8091592024a4e3c761280911e395f8ae491
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117911971"
---
# <a name="subresources-direct3d-12-graphics"></a>Unterressourcen (Direct3D 12-Grafiken)

Beschreibt, wie eine Ressource in Unterressourcen unterteilt wird und wie auf eine einzelne, mehrere oder einen Slice von Unterressourcen verwiesen wird.

-   [Beispielunterressourcen](#example-subresources)
    -   [Unterressourcenindizierung](#subresource-indexing)
    -   [MIP-Slice](#mip-slice)
    -   [Arrayslice](#array-slice)
    -   [Ebenenslice](#plane-slice)
    -   [Mehrere Unterressourcen](#multiple-subresources)
-   [Unterressourcen-APIs](#subresource-apis)
-   [Zugehörige Themen](#related-topics)

## <a name="example-subresources"></a>Beispielunterressourcen

Wenn eine Ressource einen Puffer enthält, enthält sie einfach eine Unterressource mit dem Index 0. Wenn die Ressource eine Textur (oder ein Texturarray) enthält, ist das Verweisen auf die Unterressourcen komplexer.

Einige APIs greifen auf eine gesamte Ressource zu (z. B. die [**ID3D12GraphicsCommandList::CopyResource-Methode),**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource) andere greifen auf einen Teil einer Ressource zu (z.B. die [**ID3D12Resource::ReadFromSubresource-Methode).**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) Die Methoden, die auf einen Teil einer Ressource zugreifen, verwenden in der Regel eine Ansichtsbeschreibung (z. B. die [**\_ \_ \_ SRV-Struktur D3D12 TEX2D ARRAY),**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv) um die Zutrittsressourcen anzugeben. Eine vollständige Liste finden Sie im [Abschnitt Unterressourcen-APIs.](#subresource-apis)

### <a name="subresource-indexing"></a>Unterressourcenindizierung

Um eine bestimmte Unterressource zu indizieren, werden die MIP-Ebenen zuerst indiziert, wenn jeder Arrayeintrag indiziert wird.

![Unterressourcenindizierung](images/subresource-index.png)

### <a name="mip-slice"></a>MIP-Slice

Ein MIP-Slice enthält eine Mipmapebene für jede Textur in einem Array, wie in der folgenden Abbildung dargestellt.

![Unterressourcen-MIP-Slices](images/subresource-mip-slice.png)

### <a name="array-slice"></a>Arrayslice

Bei einem Array von Texturen, jeder Textur mit Mipmaps, enthält ein Arrayslice eine Textur und alle seine Mip-Ebenen, wie in der folgenden Abbildung dargestellt.

![Unterressourcenarrayslices](images/subresource-array-slices.png)

### <a name="plane-slice"></a>Ebenenslice

In der Regel werden planare Formate nicht zum Speichern von RGBA-Daten verwendet, aber in fällen, in denen sie sind (vielleicht 24bpp RGB-Daten), könnte eine Ebene das rote Bild darstellen, eine die grüne und eine das blaue Bild. Eine Ebene ist jedoch nicht notwendigerweise eine Farbe, zwei oder mehr Farben können zu einer Ebene kombiniert werden. In der Regel werden planare Daten für untergeordnete YCbCr- und Depth-Stencil verwendet. Depth-Stencil ist das einzige Format, das Mipmaps, Arrays und mehrere Ebenen vollständig unterstützt (häufig Ebene 0 für Tiefe und Ebene 1 für Schablone).

Die Unterressourcenindizierung für ein Array von zwei Depth-Stencil Bildern mit jeweils drei MIP-Ebenen ist unten dargestellt.

![Tiefen-Schablonenindizierung](images/depth-stencil-indexing.png)

YCbCr mit Unterstichproben unterstützt Arrays und verfügt über Ebenen, aber keine Mipmaps. YCbCr-Bilder verfügen über zwei Ebenen: eine für die Leuchtdichte (Y), für die das menschliche Auge am empfindlichsten ist, und eine für die Chrominance (cb und cr, interleaved), für die das menschliche Auge weniger empfindlich ist. Dieses Format ermöglicht die Komprimierung der Chrominancewerte, um ein Bild zu komprimieren, ohne die Leuchtdichte zu beeinträchtigen, und ist aus diesem Grund ein gängiges Videokomprimierungsformat, obwohl es zum Komprimieren von Stillbildern verwendet wird. Die folgende Abbildung zeigt das NV12-Format. Sie sehen, dass die Chrominance auf ein Viertel der Auflösung der Leuchtdichte komprimiert wurde, was bedeutet, dass die Breite jeder Ebene identisch ist und die Chrominanceebene halb so hoch wie die Leuchtdichteebene ist. Die Ebenen würden als Unterressourcen auf die gleiche Weise indiziert wie im obigen Depth-Stencil Beispiel.

![nv12-Format](images/ycbcr.png)

Planare Formate gab es in Direct3D 11, aber einzelne Ebenen konnten nicht einzeln adressiert werden, z. B. für Kopier- oder Zuordnungsvorgänge. Dies wurde in Direct3D 12 geändert, sodass jede Ebene eine eigene Unterressourcen-ID erhält. Vergleichen Sie die folgenden beiden Methoden zum Berechnen der Unterressourcen-ID.

Direct3D 11

``` syntax
inline UINT D3D11CalcSubresource( UINT MipSlice, UINT ArraySlice, UINT MipLevels )
{
    return MipSlice + (ArraySlice * MipLevels); 
}
```

Direct3D 12

``` syntax
inline UINT D3D12CalcSubresource( UINT MipSlice, UINT ArraySlice, UINT PlaneSlice, UINT MipLevels, UINT ArraySize )
{ 
    return MipSlice + (ArraySlice * MipLevels) + (PlaneSlice * MipLevels * ArraySize); 
}
```

Bei der meisten Hardware wird davon ausgegangen, dass der Arbeitsspeicher für die Ebene N immer sofort nach Ebene N-1 zugeordnet wird.

Eine Alternative zur Verwendung von Unterressourcen ist, dass eine App eine vollständig separate Ressource pro Ebene zuordnen kann. In diesem Fall versteht die Anwendung, dass die Daten planar sind, und verwendet mehrere Ressourcen, um sie zu repräsentieren.

### <a name="multiple-subresources"></a>Mehrere Unterressourcen

Eine Shaderressourcenansicht kann einen beliebigen rechteckigen Bereich von Unterressourcen auswählen, indem sie einen der oben beschriebenen Slices verwendet und Felder in den Ansichtsstrukturen (z. B. [**D3D12 \_ TEX2D \_ ARRAY \_ SRV)**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)wie in der Abbildung dargestellt verwendet.

![Auswahl mehrerer Unterressourcen](images/subresource-multiple.png)

Eine Renderzielansicht kann nur eine einzelne Unterressource oder einen einzelnen MIP-Slice verwenden und darf keine Unterressourcen aus mehr als einem MIP-Slice enthalten. Das heißt, jede Textur in einer Renderzielansicht muss die gleiche Größe aufweisen. Eine Shaderressourcenansicht kann einen beliebigen rechteckigen Bereich von Unterressourcen auswählen, wie in der Abbildung dargestellt.

## <a name="subresource-apis"></a>Unterressourcen-APIs

Die folgenden APIs verweisen auf Unterressourcen und arbeiten mit ihnen:

Aufzählungen:

-   [**D3D12 \_ \_ \_ TEXTURKOPIERTYP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_copy_type)

Die folgenden Strukturen enthalten *PlaneSlice-Indizes,* die meisten enthalten *MipSlice-Indizes.*

-   [**D3D12 \_ TEX2D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_rtv)
-   [**D3D12 \_ TEX2D \_ ARRAY \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [**D3D12 \_ TEX2D \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_srv)
-   [**D3D12 \_ TEX2D \_ ARRAY \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [**D3D12 \_ TEX2D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_uav)
-   [**D3D12 \_ TEX2D \_ ARRAY \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)

Die folgenden Strukturen enthalten *ArraySlice-Indizes,* die meisten enthalten *MipSlice-Indizes.*

-   [**D3D12 \_ TEX1D \_ ARRAY \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_dsv)
-   [**D3D12 \_ TEX2D \_ ARRAY \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_dsv)
-   [**D3D12 \_ TEX2DMS \_ ARRAY \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_dsv)
-   [**D3D12 \_ TEX1D \_ ARRAY \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_rtv)
-   [**D3D12 \_ TEX2D \_ ARRAY \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [**D3D12 \_ TEX2DMS \_ ARRAY \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_rtv)
-   [**D3D12 \_ TEX1D \_ ARRAY \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_srv)
-   [**D3D12 \_ TEX2D \_ ARRAY \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [**D3D12 \_ TEX2DMS \_ ARRAY \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_srv)
-   [**D3D12 \_ TEX1D \_ ARRAY \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_uav)
-   [**D3D12 \_ TEX2D \_ ARRAY \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)

Die folgenden Strukturen enthalten *MipSlice-Indizes,* aber weder *ArraySlice-* noch *PlaneSlice-Indizes.*

-   [**D3D12 \_ TEX1D \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_dsv)
-   [**D3D12 \_ TEX2D \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_dsv)
-   [**D3D12 \_ TEX1D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_rtv)
-   [**D3D12 \_ TEX3D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_rtv)
-   [**D3D12 \_ TEX1D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_uav)
-   [**D3D12 \_ TEX3D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_uav)

Die folgenden Strukturen verweisen auch auf Unterressourcen:

-   [**D3D12 \_ DISCARD \_ REGION:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region) Eine Struktur, die als Vorbereitung für das Verwerfen einer Ressource verwendet wird.
-   [**D3D12 \_ PLACED \_ SUBRESOURCE \_ FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) : Fügt einer Ressource einen Offset zum grundlegenden Speicherbedarf hinzu.
-   [**D3D12 \_ RESOURCE \_ TRANSITION \_ BARRIER:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) Beschreibt den Übergang von Unterressourcen zwischen verschiedenen Verwendungen (Shaderressource, Renderziel usw.).
-   [**D3D12 \_ SUBRESOURCE \_ DATA:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) Unterressourcendaten enthalten die Daten selbst sowie die Zeilen- und Slicehöhe.
-   [**D3D12 \_ SUBRESOURCE \_ FOOTPRINT:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) Ein Speicherbedarf umfasst das Format, die Breite, die Höhe, die Tiefe und die Zeilenhöhe der Unterressource.
-   [**D3D12 \_ SUBRESOURCE \_ INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_info) : Enthält den Offset, die Zeilenhöhe und die Tiefenhöhe der Unterressource.
-   [**D3D12 \_ SUBRESOURCE \_ TILING**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) : Beschreibt ein gekacheltes Unterressourcenvolumen (siehe [Volume Tiled Resources](volume-tiled-resources.md)).
-   [**D3D12 \_ TEXTURE \_ COPY \_ LOCATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) : Beschreibt einen Teil einer Textur zum Kopieren.
-   [**D3D12 \_ TILED \_ RESOURCE \_ COORDINATE:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) Beschreibt die Koordinaten einer gekachelten Ressource.

Methoden:

-   [**ID3D12Device::GetCopyableFootprints:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints) Ruft Informationen zu einer Ressource ab, um das Erstellen einer Kopie zu ermöglichen.
-   [**ID3D12Device::GetResourceTiling**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : Ruft Informationen darüber ab, wie eine gekachelte Ressource in Kacheln zerbrochen wird.
-   [**ID3D12GraphicsCommandList::ResolveSubresource:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource) Kopiert eine Unterressource mit mehreren Stichproben in eine Nicht-Mehrfachstichproben-Unterressource.
-   [**ID3D12Resource::Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) : Gibt einen Zeiger auf die angegebenen Daten in der Ressource zurück und verweigert dem GPU-Zugriff auf die Unterressource.
-   [**ID3D12Resource::ReadFromSubresource:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) Kopiert Daten aus einer Unterressource oder einem rechteckigen Bereich einer Unterressource.
-   [**ID3D12Resource::Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) : hebt die Zuordnung des angegebenen Speicherbereichs auf und macht den Zeiger auf die Ressource ungültig. Gibt den GPU-Zugriff auf die Unterressource wieder her.
-   [**ID3D12Resource::WriteToSubresource:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) Kopiert Daten in eine Unterressource oder einen rechteckigen Bereich einer Unterressource.

Texturen müssen sich im Zustand [**D3D12 \_ RESOURCE \_ STATE \_ COMMON**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) befinden, damit der CPU-Zugriff über [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) und [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) zulässig ist. Puffer hingegen nicht. Der CPU-Zugriff auf eine [](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)Ressource erfolgt in der Regel über / [**Zuordnungsentzuordnung.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcenbindung](resource-binding.md)
</dt> </dl>

 

 




