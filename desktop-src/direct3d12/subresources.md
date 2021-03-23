---
title: Unter Berichte (Direct3D 12-Grafiken)
description: Beschreibt, wie eine Ressource in unter Ressourcen aufgeteilt wird und wie auf eine einzelne, mehrere oder ein Slice von unter Ressourcen verwiesen wird.
ms.assetid: C4F92F8A-DBF0-412B-8707-CC4C1BF2D88F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8fa8ea0d48fea7ee8e192d9dcf1fe5e3d22423
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104548696"
---
# <a name="subresources-direct3d-12-graphics"></a>Unter Berichte (Direct3D 12-Grafiken)

Beschreibt, wie eine Ressource in unter Ressourcen aufgeteilt wird und wie auf eine einzelne, mehrere oder ein Slice von unter Ressourcen verwiesen wird.

-   [Beispiel unter Ressourcen](#example-subresources)
    -   [Unter Quell Indizierung](#subresource-indexing)
    -   [MIP-Slice](#mip-slice)
    -   [Array Slice](#array-slice)
    -   [Flachen Slice](#plane-slice)
    -   [Mehrere unter Ressourcen](#multiple-subresources)
-   [Subresource-APIs](#subresource-apis)
-   [Verwandte Themen](#related-topics)

## <a name="example-subresources"></a>Beispiel unter Ressourcen

Wenn eine Ressource einen Puffer enthält, enthält Sie einfach eine untergeordnete Quelle mit dem Index 0. Wenn die Ressource eine Textur (oder ein Textur Array) enthält, ist das verweisen auf die unter Ressourcen komplexer.

Einige APIs greifen auf eine gesamte Ressource zu (z. b. die [**ID3D12GraphicsCommandList:: copyresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource) -Methode), von denen andere auf einen Teil einer Ressource zugreifen (z. b. die [**ID3D12Resource:: Read fromsubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) -Methode). Die Methoden, die auf einen Teil einer Ressource zugreifen, verwenden im Allgemeinen eine Ansichts Beschreibung (z. b. die [**\_ \_ \_ SRV-Struktur D3D12 TEX2D Array**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv) ), um die unter Ressourcen anzugeben, auf die zugegriffen werden soll. Eine komplette Liste finden Sie im Abschnitt " [subresource-APIs](#subresource-apis) ".

### <a name="subresource-indexing"></a>Unter Quell Indizierung

Um eine bestimmte untergeordnete Quelle zu indizieren, werden die MIP-Ebenen zuerst indiziert, wenn jeder Array Eintrag indiziert wird.

![unter Quell Indizierung](images/subresource-index.png)

### <a name="mip-slice"></a>MIP-Slice

Ein MIP-Slice enthält eine MipMap-Ebene für jede Textur in einem Array, wie in der folgenden Abbildung dargestellt.

![unter Quell-MIP-Slices](images/subresource-mip-slice.png)

### <a name="array-slice"></a>Array Slice

Bei einem Array von Texturen enthält jede Textur mit Mipmaps, ein Array Slice, eine Textur und alle zugehörigen MIP-Ebenen, wie in der folgenden Abbildung dargestellt.

![Teil Quell Array Slices](images/subresource-array-slices.png)

### <a name="plane-slice"></a>Flachen Slice

In der Regel werden keine planaren Formate zum Speichern von RGBA-Daten verwendet. in Fällen, in denen es sich handelt (z. b. 24 bpp RGB-Daten), kann eine Ebene das rote Bild, ein grünes Bild und ein blaues Bild darstellen. Eine Ebene ist jedoch nicht notwendigerweise eine Farbe, zwei oder mehr Farben können zu einer Ebene kombiniert werden. In der Regel werden planare Daten für Subsampling von YCbCr-und Depth-Stencil-Daten verwendet. Depth-Stencil ist das einzige Format, das Mipmaps, Arrays und mehrere Ebenen vollständig unterstützt (häufig Ebene 0 für Tiefe und Ebene 1 für Schablone).

Die unter Quell Indizierung für ein Array mit zwei Depth-Stencil Bildern, die jeweils über drei MIP-Ebenen verfügen, ist unten dargestellt.

![tiefen Schablone-Indizierung](images/depth-stencil-indexing.png)

Unterstichprobe: YCbCr unterstützt Arrays und verfügt über Ebenen, unterstützt jedoch keine Mipmaps. YCbCr-Bilder verfügen über zwei Ebenen, eine für die Leuchtkraft (Y), für die das menschliche Auge am empfindlichsten ist, und eine für die Chrominanz (sowohl CB als auch CR, Interleaved), für die das menschliche Auge weniger sensibel ist. Dieses Format ermöglicht die Komprimierung der Chrome-Werte zum Komprimieren eines Bilds, ohne dass sich dies auf die Leuchtkraft auswirkt, und ist aus diesem Grund ein gängiges Video Komprimierungs Format, obwohl es zum Komprimieren von Bildern verwendet wird. Das folgende Bild zeigt das NV12-Format, wobei die Chrominanz in ein Viertel der Auflösung der Leuchtkraft komprimiert wurde, was bedeutet, dass die Breite der einzelnen Ebenen identisch ist, und die Chrominanz-Ebene die Hälfte der Höhe der Leuchtkraft Ebene ist. Die Flächen werden in gleicher Weise wie das oben beschriebene Depth-Stencil Beispiel als unter Ressourcen indiziert.

![Das nv12-Format](images/ycbcr.png)

Planare Formate waren in Direct3D 11 vorhanden, aber einzelne Flächen konnten nicht einzeln adressiert werden, z.. bei Kopier-oder zuordnungsvorgängen. Dies wurde in Direct3D 12 geändert, sodass jede Ebene eine eigene untergeordnete Quell-ID erhalten hat. Vergleichen Sie die beiden folgenden Methoden, um die untergeordnete Quell-ID zu berechnen.

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

Die meisten Hardware geht davon aus, dass der Arbeitsspeicher für die Ebene n nach der Ebene n-1 immer sofort zugewiesen wird.

Eine Alternative zur Verwendung von unter Berichten besteht darin, dass eine APP eine vollständig separate Ressource pro Ebene zuordnen kann. In diesem Fall versteht die Anwendung, dass die Daten planare sind, und verwendet mehrere Ressourcen, um Sie darzustellen.

### <a name="multiple-subresources"></a>Mehrere unter Ressourcen

In einer Shader-Ressourcen Ansicht können beliebige rechteckige Bereiche von unter Berichten ausgewählt werden, wobei eines der oben beschriebenen Slices und die Verwendung von Feldern in den Sicht Strukturen (z. b. [**D3D12 \_ TEX2D \_ array \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)), wie in der Abbildung dargestellt, verwendet wird.

![Auswahl mehrerer unter Quellen](images/subresource-multiple.png)

Eine renderzielansicht kann nur eine einzelne untergeordnete Quelle oder einen MIP-Slice verwenden und darf keine unter Ressourcen aus mehreren MIP-Slice enthalten. Das heißt, jede Textur in einer renderzielansicht muss dieselbe Größe aufweisen. In einer Shader-Ressourcen Ansicht können beliebige rechteckige Bereiche von unter Berichten ausgewählt werden, wie in der Abbildung dargestellt.

## <a name="subresource-apis"></a>Subresource-APIs

Die folgenden APIs verweisen auf und arbeiten mit unter Ressourcen:

Aufzählungen:

-   [**D3D12 \_ Textur \_ \_ kopierungstyp**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_copy_type)

Die folgenden Strukturen enthalten *planeslice* -Indizes, die in den meisten *mipslice* -Indizes enthalten sind.

-   [**D3D12 \_ TEX2D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_rtv)
-   [**D3D12 \_ TEX2D \_ array \_ -RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [**D3D12 \_ TEX2D \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_srv)
-   [**D3D12 \_ TEX2D- \_ Array ( \_ SRV)**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [**D3D12 \_ TEX2D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_uav)
-   [**D3D12 \_ TEX2D \_ array- \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)

Die folgenden Strukturen enthalten *arrayslice* -Indizes, die in den meisten *mipslice* -Indizes enthalten sind.

-   [**D3D12 \_ TEX1D \_ array- \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_dsv)
-   [**D3D12 \_ TEX2D \_ array- \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_dsv)
-   [**D3D12 \_ TEX2DMS \_ array- \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_dsv)
-   [**D3D12 \_ TEX1D \_ array \_ -RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_rtv)
-   [**D3D12 \_ TEX2D \_ array \_ -RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [**D3D12 \_ TEX2DMS \_ array \_ -RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_rtv)
-   [**D3D12 \_ TEX1D- \_ Array ( \_ SRV)**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_srv)
-   [**D3D12 \_ TEX2D- \_ Array ( \_ SRV)**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [**D3D12 \_ TEX2DMS- \_ Array ( \_ SRV)**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_srv)
-   [**D3D12 \_ TEX1D \_ array- \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_uav)
-   [**D3D12 \_ TEX2D \_ array- \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)

Die folgenden Strukturen enthalten *mipslice* -Indizes, aber weder *arrayslice* noch *planeslice* -Indizes.

-   [**D3D12 \_ TEX1D \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_dsv)
-   [**D3D12 \_ TEX2D \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_dsv)
-   [**D3D12 \_ TEX1D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_rtv)
-   [**D3D12 \_ TEX3D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_rtv)
-   [**D3D12 \_ TEX1D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_uav)
-   [**D3D12 \_ TEX3D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_uav)

Die folgenden Strukturen verweisen auch auf unter Ressourcen:

-   [**D3D12 \_ \_Region verwerfen**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region) : eine Struktur, die zur Vorbereitung der verwerfen einer Ressource verwendet wird.
-   [**D3D12 \_ Platzierung \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) der untergeordneten Quelle: Fügt der Grundlagen einen Offset zu einer Ressource hinzu.
-   [**D3D12 \_ Ressourcen \_ Übergangs \_ Barriere**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) : Beschreibt den Übergang von unter Ressourcen zwischen unterschiedlichen Verwendungen (Shader-Ressource, Renderziel usw.).
-   [**D3D12 \_ SUBRESOURCE- \_ Daten**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) : die Daten der untergeordneten Quelle enthalten die Daten selbst und die Zeilen-und Slice-Tonhöhe.
-   [**D3D12 \_ Ressourcen \_ Bedarf**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) in der unter Quelle: ein Ressourcenbedarf umfasst das Format, die Breite, die Höhe, die Tiefe und die Zeilengröße der unter Ressourcen.
-   [**D3D12 \_ Subresource- \_ Informationen**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_info) : enthält den Offset, die Zeilen-und die Tiefe des unter Berichts.
-   [**D3D12 \_ SUBRESOURCE- \_ tiult**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) : Beschreibt ein gespeichertes unter Quell Volume (siehe [Volume-Kachel Ressourcen](volume-tiled-resources.md)).
-   [**D3D12 \_ \_ \_ Speicherort der Textur Kopie**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) : Beschreibt einen Teil einer Textur zum Kopieren.
-   [**D3D12 \_ Gekachelte \_ Ressourcen \_ Koordinate**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : Beschreibt die Koordinaten einer gekachelten Ressource.

Methoden:

-   [**ID3D12Device:: getcopyablefootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints) : Ruft Informationen zu einer Ressource ab, damit eine Kopie erstellt werden kann.
-   [**ID3D12Device:: getresourcetielt**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : Ruft Informationen darüber ab, wie eine gekachelte Ressource in Kacheln aufgeteilt wird.
-   [**ID3D12GraphicsCommandList:: resolvesubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource) : kopiert eine untergeordnete Quelle mit mehreren Stichproben in eine untergeordnete Quelle, die nicht mehrere Stichproben enthält.
-   [**ID3D12Resource:: Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) : gibt einen Zeiger auf die angegebenen Daten in der Ressource zurück und verweigert den GPU-Zugriff auf die untergeordnete Quelle.
-   [**ID3D12Resource:: Read fromsubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) : kopiert Daten aus einer unter Quelle oder einem rechteckigen Bereich einer unter Quelle.
-   [**ID3D12Resource:: unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) : hebt die Zuordnung des angegebenen Speicherbereichs auf und macht den Zeiger auf die Ressource ungültig. Gibt den GPU-Zugriff auf die untergeordnete Quelle wieder.
-   [**ID3D12Resource:: Write-in subresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) : kopiert Daten in eine untergeordnete Quelle oder einen rechteckigen Bereich eines unter Berichts.

Texturen müssen sich im allgemeinen Status des [**D3D12- \_ Ressourcen \_ Zustands \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) befinden, damit der CPU-Zugriff über " [**Write**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) " und "read [**fromsubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) " rechtmäßig ist, aber Puffer nicht. Der CPU-Zugriff auf eine Ressource erfolgt in der Regel über [**map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) / [**unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap).

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Ressourcen Bindung](resource-binding.md)
</dt> </dl>

 

 




